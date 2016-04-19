# Examples #

These are only examples. Please read the documentation for more detail:

```
perldoc check_mysql_all
```

## Check DB Connection ##

```
# Simply connect to the database with the provided credentials
check_mysql_all connect --host=localhost --username=root --password=pass
```

## Check Query Execution ##

```
# Executes an arbitrary query, only tests for successful query execution
check_mysql_all mysql_query --host=localhost --username=root --password=pass \
    --args='query=SELECT NOW()'
```

## Check Query Execution Time ##

```
# Executes the target query, raising a critical alarm if it takes > 1 second to execute
check_mysql_all mysql_query --host=localhost --username=root --password=pass \
    --args='query=SELECT COUNT(*) FROM test.t1' \
    --args='query_timeout=1'
```

## Check Replication ##

```
# Check for IO thread
check_mysql_all repl_io --host=slavehost --username=root --password=pass
```

```
# Check for SQL thread
check_mysql_all repl_sql --host=slavehost --username=root --password=pass
```

```
# Check how many seconds behind master a slave is
# warning if 60 seconds behind, critical if 5 minutes behind
check_mysql_all repl_sbm --host=slavehost --username=root --password=pass \
    --warning=60s \
    --critical=600s
```

```
# Check for all of the above
check_mysql_all repl_all --host=slavehost --username=root --password=pass \
    --warning=60s \
    --critical=600s
```

## Check Connection Usage ##

```
# Compare the current number of processes to the max allowed connections
# warning if > 75% of the connections are used, critical if > 85% are used
check_mysql_all connections --host=localhost --username=root --password=pass \
    --warning=75% \
    --critical=85%
```

## Check Table Status ##

```
# Check if any tables in the 'foobar' database are damaged
check_mysql_all table_status --host=localhost --username=root --password=pass \
    --database=foobar
```

```
# Check if any tables in any database are damaged
check_mysql_all table_status --host=localhost --username=root --password=pass
```