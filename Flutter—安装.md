#### 1、Flutter SDK下载

（beta、dev、master、stable）

终端执行：`git clone -b dev https://github.com/flutter/flutter.git `

载完成后默认路径是：`Users/xxxxx/flutter、($HOME/flutter)`

#### 2、Flutter 环境变量配置

进入：`cd $HOME 或者 cd ~`

执行： `vim ~/.bash_profile`

```
此为临时镜像(该网址https://flutter.dev/community/china，以获得有关镜像服务器的最新动态)
export PUB_HOSTED_URL=https://pub.flutter-io.cn 
export FLUTTER_STORAGE_BASE_URL=https://storage.flutter-io.cn
export PATH=$PATH:$HOME/flutter/bin	
```

执行：`source ~/.bash_profile`

验证目录是否在已经在PATH中：`echo $PATH`

检测 flutter执行： `flutter doctor`

(禁用发送报告：请执行`flutter config --no-analytics`并显示当前设置，然后执行`flutter config`)

#### 3、升级 Flutter

要查看您当前使用的分支，请运行`flutter channel`查看。

要切换分支，请使用`flutter channel beta` 或 `flutter channel master`，然后执行` flutter upgrade`

```
注意：
1、要同时更新Flutter SDK和你的依赖包，在你的应用程序根目录（包含`pubspec.yaml`文件的目录）中运行`flutter upgrade` 命令
2、升级你的依赖包：
如果您修改了pubspec.yaml文件，或者只想更新应用依赖的包(不包括Flutter SDK)，请使用以下命令：
flutter packages get获取pubspec.yaml文件中列出的所有依赖包
flutter packages upgrade 获取pubspec.yaml文件中列出的所有依赖包的最新版本
```

#### 4、创建 Flutter 应用

```
执行：(注意：项目名称不能大写)
flutter create my_app
cd my_app
flutter run
```

#### 5、问题

`https://www.jianshu.com/p/5eb49e7f67e8`