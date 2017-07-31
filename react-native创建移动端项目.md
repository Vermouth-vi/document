# 创建项目

react-native init helloworld  
cd helloworld  
react-native run-android  
运行安卓项目  
react-native run-ios  
运行IOS项目

# 安卓模拟器相关配置

IOS项目在MAC安装Xcode的情况下运行正常，会自动打开IOS模拟器  
而Android项目直接运行存在很多问题  

### genymotion的安装

官网下载客户端，需要注册账号  

下载完毕后运行客户端，创建新的虚拟机，选择自己需要的版本，等待下载  

虚拟机下载完毕后，点击扳手按钮进行虚拟机设置，如图所示，网络模式一定要选Bridge  

选择Settings->ADB，选择Use custom Android SDK tools 将SDK目录更改为本地目录（Android studio的SDK目录）

### ADB的安装

什么是 ADB?  

Android调试桥（ adb ）是一个开发工具，帮助安卓设备和个人计算机之间的通信。 这种通信大多是在USB电缆下进行，但是也支持Wi-Fi连接。 adb 还可被用来与电脑上运行的安卓模拟器交流通信。 adb 对于安卓开发来说就像一把“瑞士军刀”。  

brew cask install android-platform-tools  

adb devices 如果安装成功，此时会显示连接的模拟器的相关信息  

### 相关错误解决方法

1.如图所示  
  
  
SDK路径找不到  
  
在项目根目录中的android文件夹下，新建文件local.properties  
编辑该文件，写入sdk.dir = /Users/vi/Desktop/sdk  
此路径为前面设置过的本地SDK目录路径，保存，问题解决  
  
2.如图所示  
  
提示模拟器无法连接  
要保证模拟器处于
