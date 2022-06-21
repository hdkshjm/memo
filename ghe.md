# GitHub Enterprise 

## git daemonのbabeldのログ
babeldが3.0からcontainer化されたため、babeldのログはsyslog(`/var/log/syslog`)に格納されている。
syslogからbabeldログを抜き出す方法は以下。
```
awk '$5 ~ /babeld/' /var/log/syslog > babeld.log
```

