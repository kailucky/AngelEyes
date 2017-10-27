hbase操作
sqoop import --connect jdbc:mysql://localhost:3306/movielens \
--username root --password root \
--table user \
--hbase-table user \
--column-family info 

sqoop import --connect jdbc:mysql://localhost:3306/movielens \
--username root --password root \
--table movie \
--hbase-table movie \
--column-family media 

sqoop import --connect jdbc:mysql://localhost:3306/movielens \
--username root --password root \
--table movierating \
--hbase-table movierating \
--column-family ratings


put 'user','10000','info:age',30
put 'user','10000','info:gender','F'
put 'user','10000','info:occupationname','Shanghai'
put 'user','10000','info:zip',90210

put 'user','10000','info:age',31
put 'user','10000','info:age',32

get 'user','10000',{COLUMN => "info:age", VERSIONS => 2}
