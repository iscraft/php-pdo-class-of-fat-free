//init   
```
require("s/pdo.php");   
//$db = new DB(ROOT_PATH.'/sqlite/blog.php');   
//Flight::register('db', 'SQL', array(ROOT_PATH.'/sqlite/blog.php'));   
//$db = Flight::db();   
$db = new SQL('pgsql:host=localhost;port=5432;dbname=postgres','Administrator','123456');   
```
//use   
```
$db->row("select * from test where id='1'");   
print_r ($db);   
$db->exec("select * from test where id='1'");   
print_r ($db);  
echo $db->count();   
echo $db->lastInsertId();   
```
//base info   
```
echo $db->driver();   
echo $db->version();   
echo $db->name();   
print_r ($db->schema("test"));   
```
//log time   
```
$stamp=TRUE   
```
//detail   
https://fatfreeframework.com/3.6/sql   
