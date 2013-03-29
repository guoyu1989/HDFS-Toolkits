## Reference

https://github.com/tub78/HDFS-Tools/blob/master/README.md

## Installation & Setup

*HDFS-Tools* are available on [GitHub](https://github.com/tub78).

Note: This version can support Hadoop 1.12

### Bare Minimum

 1. Install these scripts somewhere on your path
 1. `HDFS_PREFIX` - Select the _local_ directory where you wish to mirror *HDFS*
 1. `HADOOP_CONF_DIR` - Select the directory containing the active configuration, in order to lookup information on *HDFS*
 1. Add the following line to your `.bash_profile`
      ``` source <HDFS-TOOLS>/henv 
          if ! type hdfs &> /dev/null; then
              export HDFS_COMM="hadoop"
          fi```
      

### For Remote Connections

 1. `HDFS_USER` - Set the user name used to connect to the remote hadoop filesystem
  1. `HDFS_HOST` - Set the host
   1. `HDFS_PORT` - Set the port

   `hconnect` opens an ssh tunnel to the remote host using `ssh -ND $HDFS_PORT $HDFS_USER@$HDFS_HOST`
