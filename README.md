# mysqldump2json
mysqldump file to json

```
mysqldump database_name_here -u root -p > dump.sql
```
Once you have the dump.sql file, run this command to generate output.json:
```
node converter.js dump.sql
```


You can now import the json file to mongo via this command:
```
mongoimport --type json --jsonArray --db db_name_here --collection collection_name_here --file file_name_here.json
```
