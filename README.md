# ADF-Hive-Bash-Shell
How to call a *.sh file in HDI from ADF with Hive activie? With Microsoft Support team, we figured out...


1.	With ADLS as the storage for HDI , blob storage needs to be added as additional storage to use the HDI related activities in ADF.
2.	The required hive scripts are to be placed in Blob Storage 
3.	With the above set up, the ADF successfully triggers the shell script on the HDI, but it tries to execute the shell script on the worker node instead of the head node.
4.	Hence to make shell script call from Hive activity, the shell scripts need to be placed in the worker nodes. (In fact all the worker nodes, since it might connect to any worker nodes)
