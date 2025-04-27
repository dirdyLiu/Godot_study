出于对游戏的兴趣我开始学习Godot。

昨天在某学习网站看了速通教程后，今天准备上手实战下。

## 工欲善其事必先利其器——下载Godot引擎

这里我下载的是 v4.4.1 windows 版

![image-20250427231021220](C:\Users\23570\AppData\Roaming\Typora\typora-user-images\image-20250427231021220.png)

Godot支持C#以及Godot自带的GD Script进行开发，由于速通教程中使用的是GD Script，所以我的第一次试手也将使用GD Script进行。

Start！

![image-20250427231259270](C:\Users\23570\AppData\Roaming\Typora\typora-user-images\image-20250427231259270.png)

**第一个阶段**

![image-20250427231406532](C:\Users\23570\AppData\Roaming\Typora\typora-user-images\image-20250427231406532.png)

游戏场景，创建Node2D根节点，使用教程所附素材包中的背景来熟悉游戏场景创建方式，学到了一些快捷键技巧以及Godot开发规则。

创建游戏场景更改渲染中心后开始创建玩家。使用Animatedsprite2D节点创建玩家，创建玩家时使用了另一个独立场景（玩家场景）来进行封装，方便日后参数调整。

**第二阶段**

![image-20250427232816871](C:\Users\23570\AppData\Roaming\Typora\typora-user-images\image-20250427232816871.png)

作者讲的很细，算是面向0编程经验观众做的教程。

这一阶段主要学习了使用键盘监控来控制玩家行为（主要实现移动），以及复习编程知识。

**第三阶段**

![image-20250427233050435](C:\Users\23570\AppData\Roaming\Typora\typora-user-images\image-20250427233050435.png)

由限制玩家节点在屏幕内的移动引出玩家体积碰撞知识。StaticBody2D来创建空气墙以保证玩家在预期范围内移动，CollisionShape2D节点给予玩家碰撞体积，来保证与空气墙的互动存在。

**第四阶段**

![image-20250427233401263](C:\Users\23570\AppData\Roaming\Typora\typora-user-images\image-20250427233401263.png)

创建敌人单位，使用Area2D节点创建敌方单位，设计玩家与敌方单位碰撞事件，以及游戏结束事件。

今天进度先到这里了，后续每天补充进度！