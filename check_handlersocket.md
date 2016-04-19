
```
Usage:
     check_handlersocket -K <check_name> [options]

     Options:
       -K, --check=<check_name>  The check to run
       --columns=<columns>       Comma-separated list of column names
       -c, --critical=<limit>    The level at which a critical alarm is raised.
       -d, --database=<dbname>   The database to use
       -h, --help                Display this message and exit
       -H, --host=<hostname>     The target server host
       --index                   The name of the index to open
       --index-value             The key to find
       --limit                   The maximum number of records to retrieve
       --offset                  The number of records skipped before retrieving records
       --port=<portnum>          The port HandlerSocket is listening on
       --table                   The table to use
       -t, --timeout=<timeout>   Seconds before connection/query attempts timeout
       -v, --verbose             Increase verbosity level
       -V, --version             Display version information and exit
       -w, --warning             The level at which a warning is raised.

     Defaults are:

     ATTRIBUTE                  VALUE
     -------------------------- -------------------------------
     check                      No default value
     columns                    No default value 
     critical                   Check-specific
     database                   No default value
     help                       FALSE
     host                       localhost
     index                      No default value
     index-value                No default value
     limit                      1
     offset                     0
     port                       9998 for reads, 9999 for writes
     socket                     No default value
     table                      No default value
     timeout                    10 seconds
     verbose                    1 (out of 3)
     version                    FALSE
     warning                    Check-specific

     The following checks are supported:

     read_connect write_connect read_exec delete_exec

```