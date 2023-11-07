# EZAppDeploy
Application wrapper for use with multiple installation packages and pre-requisites stored in one IntuneWin file. Use it in conjunction with IntuneWinAppUtil.exe
EZAppDeploy.exe creates a folder on the c: drive called AppDeploymentLogs. This is hardcoded into the application.
Define your executable command lines in the command.xml file.

<commands>
<command>
<executable>.\Package1Setup.exe</executable>
<arguments>/exenoui /exelog C:\AppDeploymentLogs\CWRDSS.log</arguments>
<delayInSeconds>5</delayInSeconds>
<!--  Specify the delay (duration in seconds) before executing the next command  -->
</command>
<command>
<executable>msiexec.exe</executable>
<arguments>/i package2.msi /log C:\AppDeploymentLogs\package2.log</arguments>
<delayInSeconds>0</delayInSeconds>
</command>
</commands>
