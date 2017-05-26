# fastlaneDemo
用来测试fastlane自动化脚本

从git获取最新代码（git pull --rebase），恢复暂存区，提升版本号，根据当前版本号打tag并push，编译，暂存代码，通知开发者

注意：
increment_build_number方法会默认读取和fastlane同级目录的项目文件，如果项目目录不是如此设定，将会报错：

[11:37:49]: ▸ There are no Xcode project files in this directory.  agvtool needs a project to operate.
[11:37:49]: Before being able to increment and read the version number from your Xcode project, you first need to setup your project properly. Please follow the guide at https://developer.apple.com/library/content/qa/qa1827/_index.html

此外increment_build_number还需要开启xcode响应的功能，详情请见：https://developer.apple.com/library/content/qa/qa1827/_index.html

最后还是决定读取info.plist文件了。。。
