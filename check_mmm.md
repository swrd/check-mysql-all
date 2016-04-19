
```
Usage:
     check_mmm [--cluster C#]

     Options:
       --cluster=<cluster_id>       The MMM Cluster to check
       -c, --critical=<limit>       The level at which a critical alarm is raised.
       -h, --help                   Display this message and exit
       --mmm-base=<base-dir>        Base directory where MMM is installed
       -v, --verbose                Increase verbosity level
       -V, --version                Display version information and exit
       -w, --warning                The level at which a warning is raised.
       --nsca-host=<remote host>    Address of the remote nsca host
       --nsca-this=<hostname>               Hostname to report for nagios
       --nsca-conf=<path-to-conf>   Path to nsca config file

     Defaults are:

     ATTRIBUTE                  VALUE
     -------------------------- ------------------
     cluster                    No default value
     critical                   HARD_OFFLINE,REPLICATION_FAIL
     help                       FALSE
     mmm-base                   No default value
     verbose                    1 (out of 3)
     version                    FALSE
     warning                    ADMIN_OFFLINE,AWAITING_RECOVERY,REPLICATION_DELAY
     nsca-host                                      FALSE
     nsca-this                                      Default is the local hostname
     nsca-conf                                      No default value

```