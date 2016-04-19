
```
Usage:
     check_maatkit -K <check_name> [options]

     Options:
       -a, --args=<key=value>    Optional arguments.
       -K, --check=<check_name>  The check to run
       -c, --critical=<limit>    The level at which a critical alarm is raised.
       -d, --database=<dbname>   The database to use
       -h, --help                Display this message and exit
       -H, --host=<hostname>     The target MySQL server host
       -p, --password=<password> The password of the MySQL user
       --port=<portnum>          The port MySQL is listening on
       -s, --socket=<sockfile>   Use the specified mysql unix socket to connect
       -t, --timeout=<timeout>   Seconds before connection/query attempts timeout
       -u, --username=<username> The MySQL user used to connect
       -v, --verbose             Increase verbosity level
       -V, --version             Display version information and exit
       -w, --warning             The level at which a warning is raised.

     Defaults are:

     ATTRIBUTE                  VALUE
     -------------------------- ------------------
     args                       No default value
     check                      No default value
     critical                   Check-specific
     database                   No default value
     help                       FALSE
     host                       localhost
     password                   No default value
     port                       3306
     socket                     No default value
     timeout                    10 seconds
     username                   No default value
     verbose                    1 (out of 3)
     version                    FALSE
     warning                    Check-specific

     The following checks are supported:

     mk-deadlock-logger
```