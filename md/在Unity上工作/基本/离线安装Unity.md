# 离线部署Unity

Unity Download Assistant支持离线部署。这允许您下载安装Unity所需的所有文件，并生成一个脚本，用于在没有网络连接的其他计算机上重复进行相同的安装。

## 制作

运行下载助手，并在一台计算机上正常安装Unity。这台计算机必须有足够的可用磁盘空间来下载所有文件。点击下拉菜单并选择**自定义**，然后选择您想要下载文件的位置。

![](https://docs.unity3d.com/uploads/Main/DeployingUnityOffline-DownloadAssistant.png)

## 检查你拥有的文件

打开您的PC的文件管理器，导航到您之前指定的自定义位置文件夹，然后在该文件夹内查找`.sh`或`.bat`文件。检查这个文件的内容。它应该看起来类似于下面的例子：

![](https://docs.unity3d.com/uploads/Main/DeployingUnityOffline-installsh.png)

## 将Unity安装到其他计算机上

### Windows

1. 将整个文件夹复制到目标Windows PC，然后运行提供的`.bat`文件。
2. 要避免Windows UAC提示，请`install.bat`从Administrator shell 运行。在“ **开始**”菜单中，搜索`cmd.exe`，右键单击并选择**以管理员身份运行**。
3. 使用脚本导航到文件夹。这通常会在您的下载文件夹（`cd C:\Users\[YourName]\Download\UnityPackages`）中。

### Mac

1. 将整个文件夹复制到目标Mac OS X机器，然后运行提供的`.sh`文件。运行`sudo install.sh`。
2. 使用脚本导航到文件夹。这通常会在您的下载文件夹（`cd ~/Downloads/UnityPackages`）中。
3. 您可以为需要安装Unity的每台计算机多次重复这些说明。