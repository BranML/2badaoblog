# 开启独立AMD显卡

## 背景

作为一个计算机相关专业的学生，在我的笔记本电脑已经使用近5年后才我才学会利用独立显卡来提升电脑性能

笔记本电脑可能有两个显卡，我的电脑是一颗Intel的核显，一颗是AMD的独显

接下来演示如何在玩游戏时开启笔记本电脑的AMD独立显卡

## 查看显卡信息

方法一

Windows10打开任务管理器查看

点击切换下方的详细信息与简略信息，选择上方的性能选项卡，分别点击GPU 0和GPU 1来查看显卡信息

![任务管理器查看显卡信息](https://github.com/tothepythonmoon/2badaoblog/blob/master/blog/No_0023_%E5%BC%80%E5%90%AF%E7%8B%AC%E7%AB%8BAMD%E6%98%BE%E5%8D%A1/rw-1024x576.jpg?raw=true)

方法二：利用GPU-Z来查看GPU信息

点击下方红框位置切换，显示不同显卡的信息

![GPU-Z查看显卡信息](https://github.com/tothepythonmoon/2badaoblog/blob/master/blog/No_0023_%E5%BC%80%E5%90%AF%E7%8B%AC%E7%AB%8BAMD%E6%98%BE%E5%8D%A1/GPUZ.gif?raw=true)

## 设置使用独立显卡的程序

第一步：右键选择Radeon设置

![右键radeon](https://github.com/tothepythonmoon/2badaoblog/blob/master/blog/No_0023_%E5%BC%80%E5%90%AF%E7%8B%AC%E7%AB%8BAMD%E6%98%BE%E5%8D%A1/youjian-1024x576.jpeg?raw=true)

如果右键没有Radeon设置，可以点击开始菜单，寻找AMD settings，或者你需要安装AMD的显卡驱动程序，[点击跳转学安装AMD显卡驱动YouTube](https://www.youtube.com/watch?v=QBYCSwnSSCs)

![开始菜单AMDsetting](https://github.com/tothepythonmoon/2badaoblog/blob/master/blog/No_0023_%E5%BC%80%E5%90%AF%E7%8B%AC%E7%AB%8BAMD%E6%98%BE%E5%8D%A1/output-1024x576.jpeg?raw=true)

打开后选择系统

![AMD系统](https://github.com/tothepythonmoon/2badaoblog/blob/master/blog/No_0023_%E5%BC%80%E5%90%AF%E7%8B%AC%E7%AB%8BAMD%E6%98%BE%E5%8D%A1/AMD%E7%B3%BB%E7%BB%9F.jpeg?raw=true)

依次点击 可交换显卡 运行中的应用程序 已安装的配置好的应用程序

![AMD可交换显卡](https://github.com/tothepythonmoon/2badaoblog/blob/master/blog/No_0023_%E5%BC%80%E5%90%AF%E7%8B%AC%E7%AB%8BAMD%E6%98%BE%E5%8D%A1/AMD%E5%8F%AF%E4%BA%A4%E6%8D%A2%E6%98%BE%E5%8D%A1jpeg.jpeg?raw=true)

点击浏览选项

![AMD浏览选项](https://github.com/tothepythonmoon/2badaoblog/blob/master/blog/No_0023_%E5%BC%80%E5%90%AF%E7%8B%AC%E7%AB%8BAMD%E6%98%BE%E5%8D%A1/AMD%E6%B5%8F%E8%A7%88%E9%80%89%E9%A1%B9.jpeg?raw=true)

在弹出的窗口中选择你要使用独立显卡运行的程序（这里以英雄联盟为例）

![AMD选择程序](https://github.com/tothepythonmoon/2badaoblog/blob/master/blog/No_0023_%E5%BC%80%E5%90%AF%E7%8B%AC%E7%AB%8BAMD%E6%98%BE%E5%8D%A1/AMD%E9%80%89%E6%8B%A9%E7%A8%8B%E5%BA%8F.jpeg?raw=true)

程序位置可以通过右键属性查看

英雄联盟的启动程序在"E:\Program Files\腾讯游戏\英雄联盟\TCLS\Client.exe"(不是桌面快捷方式的路径)

炉石传说启动程序在"E:\exeinstall\Hearthstone\Hearthstone Beta Launcher.exe"（ 不是桌面快捷方式的路径 ）

![程序路径](https://github.com/tothepythonmoon/2badaoblog/blob/master/blog/No_0023_%E5%BC%80%E5%90%AF%E7%8B%AC%E7%AB%8BAMD%E6%98%BE%E5%8D%A1/%E7%A8%8B%E5%BA%8F%E8%B7%AF%E5%BE%84.jpeg?raw=true)

按照启动程序的所在路径，在刚刚设置程序使用独立显卡的弹窗里选择好程序

![选定程序](https://github.com/tothepythonmoon/2badaoblog/blob/master/blog/No_0023_%E5%BC%80%E5%90%AF%E7%8B%AC%E7%AB%8BAMD%E6%98%BE%E5%8D%A1/%E9%80%89%E5%AE%9A%E7%A8%8B%E5%BA%8F.jpeg?raw=true)

最后选择程序双击即可

你所添加的这个程序就会使用AMD独立显卡运行
