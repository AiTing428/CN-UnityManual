# 下载并安装Unity

从Unity下载页面下载并安装Unity编辑器。安装程序使用下载助手，并有详细的说明。如果您想使用Torrent下载Unity编辑器或者立即安装多个版本的Unity，请参见下面的Torrent下载。

## Unity下载助手

Unity下载助手是一个小的可执行程序（大小约1 MB），可以让您选择要下载和安装的Unity编辑器的哪些组件。

如果您不确定要安装哪些组件，请保留默认选择，单机**继续**，然后按照安装程序的说明进行操作。

![](https://docs.unity3d.com/uploads/Main/UnityDownloadAssistant_v52_75.png)

> Unity下载助手（如果您不确定选择哪个，请保留默认选项）

*请注意，在PC上有Microsoft Visual Studio Community 2015.*

## 没有下载助手的情况下安装Unity

如果您愿意，可以单独下载和安装所有组件，而无需使用“下载助手”。这些组件是正常的安装可执行程序和软件包，因为您可能会发现它更简单，特别是如果您是新的Unity用户，则可以使用“下载助手”。一些用户（如那些希望在组织中自动部署Unity的用户）可能更喜欢从命令行进行安装。

## 从命令行在Windows上安装Unity

在Windows上从命令行安装Unity编辑器和其他组件时，可以使用以下选项。请注意，安装程序命令行参数区分大小写。

### Unity Editor安装

|||
|---|---|
|/S|执行安装|  
|/d=PATH|设置默认安装目录。与无提示安装选项结合使用时很有用。默认文件夹是**C:\Proggram Files（X86）\Unity（32位）或C:\Proggram Files\Unity（64位）**|

例：

	UnitySetup64.exe /S /D=E:\Development\Unity

将Unity静默安装到E:\Development\Unity文件夹，这将成为Unity安装的根目录。在这种情况下，Unity编辑器可执行文件将安装在E:\Develoment\Unity\Editon\Unity.exe中。即使路径包含空格，“/D”参数必须是最后一个，不包括引号。

### Unity Editor卸载

要执行无提示卸载，请运行`Uninstall.exe /S`(例如，从命令行或脚本)

要注意，尽管该过程将立即结束，但在文件实际删除之前需要几秒钟的时间。这样做的原因是卸载程序被复制到一个临时的位置，以便能够删除它自己。此外，请确保工作目录不在Unity安装目录，因为如果是这种情况，它将无法删除文件夹。

### 标准资源安装

静默安装标准资源。如果指定文件夹，请使用Unity“root”文件夹（即，包含Editor文件夹的文件夹，而不是Unity.exe的安装位置）。

	UnityStandardAssetsSetup.exe /S /D=E:\Development\Unity

### 示例项目安装

静默安装示例项目。默认文件夹是**C：\ Users \ Public \ Documentation \ Unity Projects \ Standard Assets示例项目。**

	UnityExampleProjectSetup.exe /S /D=E:\Development\Unity

## 在命令行上在OS X上安装Unity

单独的Unity安装程序以.pkg文件形式提供，可以按照`installer`下面的说明进行安装。

### Unity Editor安装

安装到`/Applications/Unity`指定目标卷上的文件夹中：

	sudo installer [-dumplog] -package Unity.pkg -target /

### 标准资源安装

安装到`/Applications/Unity/Standard Assets`指定卷上的文件夹中：

	sudo installer [-dumplog] -package StandardAssets.pkg -target /

### 示例项目安装

安装到`/Users/Shared/Unity/Standard-Assets`指定卷上的文件夹中：

	sudo installer [-dumplog] -package Examples.pkg -target /

## Torrent下载

如果您希望通过BitTorrent客户端下载Unity，则可以从[Unity下载归档页面](http://unity3d.com/get-unity/download/archive?_ga=2.141275122.1387186018.1512480322-217021860.1511878465)下载获取Torrent链接。并非所有版本都有一个torrent下载。如果某个版本可以下载为torrent，则该选项在“ **下载**”下拉菜单中显示为**Torrent下载（Win + Mac）**。

![](https://docs.unity3d.com/uploads/Main/InstallingUnityTorrentDownload.png)

> 通过Torrent下载Unity

## 一次安装多个版本

你可以在同一台计算机上安装尽可能多的Unity版本。

Mac上的安装程序将创建一个名为**Unity**的文件夹，并使用该名称覆盖任何现有文件夹 - 但是，如果在安装其他版本之前将文件夹重命名为其他文件夹，则两个版本都可以在同一台计算机上存在，而不会出现任何问题。

在PC上，安装文件夹始终命名为**Unity XYZ [fp] W**，其中'f'用于正式版本，'p'用于标记修补程序版本。

我们强烈建议，如果您重命名Unity文件夹，则可以从逻辑上选择新的文件夹名称（例如，将版本号添加到名称末尾）。请注意，任何现有的快捷方式，别名和链接到离线文档可能不再指向旧版本的Unity。这对于离线文档可能会特别混乱; 如果突然发现离线文档的浏览器书签不再有效，请检查URL中是否有正确的文件夹名称。
