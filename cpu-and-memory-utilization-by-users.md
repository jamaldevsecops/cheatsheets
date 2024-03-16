1. CPU and Memory Utilization by Apache
```
ps aux | awk '$1 == "apache" || $1 == "www-data" || $1 == "httpd" { cpu += $3 } END { print "Apache CPU Usage:", cpu "%"}'
```
```
ps aux | awk '$1 == "apache" || $1 == "www-data" || $1 == "httpd" { mem += $4 } END { print "Apache Memory Usage:", mem "%"}'
```


2. CPU and Memory Utilization by MySQL
```
ps aux | awk '$1 == "mysql" { cpu += $3 } END { print "MySQL CPU Usage:", cpu "%"}'
```
```
ps aux | awk '$1 == "mysql" { mem += $4 } END { print "MySQL Memory Usage:", mem "%"}'
```


3. CPU and Memory Utilizaiton of All Users
```
ps aux | awk 'NR > 1 { cpu[$1] += $3 } END { for (user in cpu) print user, ":", cpu[user] "% CPU"}'
```
```
ps aux | awk 'NR > 1 { mem[$1] += $4 } END { for (user in mem) print user, ":", mem[user] "% Memory"}'
```
