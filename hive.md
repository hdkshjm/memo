## SQuirreLSQL
JDBC Driverいれてみたが、失敗。もうすこし調査が必要。

## pyhive
以下でアクセス可能
```
#!/usr/bin/python

from pyhive import hive
conn = hive.Connection(host="<hive-server>", port=<port>, username="<username>", auth="CUSTOM", password="<password>")

cursor = conn.cursor()

query = "select count(*) from table where id='{}'"
for i in range(1, 30):
  id=str(i).zfill(2)
  cursor.execute(query.format(id))
  for result in cursor.fetchall():
    print(result)
```
