# restore_mysql

[pt-br]
Você possui um backup de banco de dados muito grande e só precisa de uma tabela específica?

Essa pode ser sua solução:

sed -n -e '/DROP TABLE.*`mytable`/,/UNLOCK TABLES/p' mydump.sql > tabledump.sql

Esse comando abre e lê o arquivo mydump.sql e gera um novo arquivo (tabledump.sql) de backup apenas com a tabela informada (mytable).

[en]
Do you have a very large database backup and only need a specific table?

This may be your solution:

sed -n -e '/ DROP TABLE. * `mytable` /, / UNLOCK TABLES / p' mydump.sql> tabledump.sql

This command opens and reads the mydump.sql file and generates a new backup file (tabledump.sql) only with the reported table (mytable).
