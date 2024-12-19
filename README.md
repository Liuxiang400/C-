# 这是sjtu2024级程序设计大作业
## 我们组的扫雷程序分工可以参考成功案例https://github.com/xiaoxi666/mines_sweeper,大体由如下部分组成
### cellitem.h 和 cellitem.cpp 类文件：每个格子元素item，包含状态等

### configdialog.h 和 configdialog.cpp 类文件：游戏配置操作
### fielddata.h 和 fielddata.cpp 类文件：底层数据 // 以上三部分是逻辑部分
### main.cpp 程序入口  //
### mainwindow.h 和 mainwindow.cpp 类文件：主窗口操作（统一调用及设置数据，维护视图，设置场景等）
### mainwindow.ui 图形文件：主窗口图元描述
### minesweepscene.h 和 minesweepscene.cpp 类文件：场景布置 // 这些是ui界面
### res.qrc 资源文件：描述加载的文件（本项目是一些图片）
### sweep_minesV1.pro qt项目文件，包含一些项目相关设置
### sweep_minesV1.pro.user 用户设置，这个文件可以删掉，再次编译时会自动生成
### imgs.pptx 游戏中用到的图片原件，去除透明背景k可以利用ps处理
### 我们组怎么分工？


### 就状态而言，扫雷总共就两种格子，一种是blank,一种是explode,而在玩家游玩过程中，实则就只有一种，未知
### 那么玩家本身就可以进行插旗flag，判定是炸弹，或者question,表示不确定
### 而在玩家进行了点按操作后，第一会有不规则个数的格子状态已知，并且呈现数字 Digit
### 我们应该在在对所有格子进行初始化 INItial 布置时，现确定炸弹数和空格子，并且随机布设炸弹
### 这个时候，我们就已经知道每个格子上的数字应该是多少
### 问题是接下来玩家每揭开一个格子，我们应该展示多少其他格子
### 然后游戏应该就在玩家插旗判断所有炸弹结束
### 因此在技术细节上，我们应该实现一确定格子状态，二初始化 ，三点击后的反应，四结束反馈
### 在优化方面，我们可以添加一个计时器，可以让玩家自行调整大小和炸弹数，以及可以制作连锁爆炸动画

### ***此外，作为大作业，我们还有统一变量名***

### 暂时分工如下，刘翔负责cellitem和fielddata,周江涛负责mainwindow
