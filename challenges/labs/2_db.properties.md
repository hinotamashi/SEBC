root@instance-2 hinotamashi94]# head -1  /var/log/cloudera-scm-server/cloudera-scm-server.log 
2016-12-09 02:57:52,803 INFO main:com.cloudera.server.cmf.Main: Starting SCM Server. JVM Args: [-Dlog4j.configuration=file:/etc/cloudera-scm-server/log4j.properties, -Dfi
le.encoding=UTF-8, -Dcmf.root.logger=INFO,LOGFILE, -Dcmf.log.dir=/var/log/cloudera-scm-server, -Dcmf.log.file=cloudera-scm-server.log, -Dcmf.jetty.threshhold=WARN, -Dcmf.
schema.dir=/usr/share/cmf/schema, -Djava.awt.headless=true, -Djava.net.preferIPv4Stack=true, -Dpython.home=/usr/share/cmf/python, -XX:+UseConcMarkSweepGC, -XX:+UseParNewG
C, -XX:+HeapDumpOnOutOfMemoryError, -Xmx2G, -XX:MaxPermSize=256m, -XX:+HeapDumpOnOutOfMemoryError, -XX:HeapDumpPath=/tmp, -XX:OnOutOfMemoryError=kill -9 %p], Args: [], Ve
rsion: 5.9.0 (#249 built by jenkins on 20161006-1801 git: 898a5e032c080e18833dfc58180761f6ef2ea351)
[root@instance-2 hinotamashi94]# 

[root@instance-2 hinotamashi94]# cat /var/log/cloudera-scm-server/cloudera-scm-server.log |grep "Started Jetty server"
2016-12-09 03:04:09,081 INFO WebServerImpl:com.cloudera.server.cmf.WebServerImpl: Started Jetty server.
[root@instance-2 hinotamashi94]# 

[root@instance-2 hinotamashi94]# cat /etc/cloudera-scm-server/db.properties
# Auto-generated by scm_prepare_database.sh on Fri Dec  9 03:00:43 UTC 2016
#
# For information describing how to configure the Cloudera Manager Server
# to connect to databases, see the "Cloudera Manager Installation Guide."
#
com.cloudera.cmf.db.type=mysql
com.cloudera.cmf.db.host=10.128.0.2
com.cloudera.cmf.db.name=scm
com.cloudera.cmf.db.user=scm
com.cloudera.cmf.db.password=scm_password
com.cloudera.cmf.db.setupType=EXTERNAL
[root@instance-2 hinotamashi94]# 
