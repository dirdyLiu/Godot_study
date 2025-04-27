昨天在某学习网站看了速通教程后，今天准备上手实战下。

## 工欲善其事必先利其器——下载Godot引擎

这里我下载的是 v4.4.1 windows 版

![image](https://github.com/user-attachments/assets/ab4bdce8-e339-4517-8217-f9e12fece13f)

Godot支持C#以及Godot自带的GD Script进行开发，由于速通教程中使用的是GD Script，所以我的第一次试手也将使用GD Script进行。

Start！

![image](https://github.com/user-attachments/assets/93682c66-213b-4877-be3d-11d01f976f87)

**第一个阶段**

![image](https://github.com/user-attachments/assets/6dc46b76-6e70-4efa-84d1-ceae176ca993)

游戏场景，创建Node2D根节点，使用教程所附素材包中的背景来熟悉游戏场景创建方式，学到了一些快捷键技巧以及Godot开发规则。

创建游戏场景更改渲染中心后开始创建玩家。使用Animatedsprite2D节点创建玩家，创建玩家时使用了另一个独立场景（玩家场景）来进行封装，方便日后参数调整。

**第二阶段**

![image](https://github.com/user-attachments/assets/94f96dec-a12b-4854-ad8f-f0f650ea3e10)

作者讲的很细，算是面向0编程经验观众做的教程。

这一阶段主要学习了使用键盘监控来控制玩家行为（主要实现移动），以及复习编程知识。

**第三阶段**

![image](https://github.com/user-attachments/assets/15cd1fd7-fb98-4f3b-be38-8fc0445a4409)

由限制玩家节点在屏幕内的移动引出玩家体积碰撞知识。StaticBody2D来创建空气墙以保证玩家在预期范围内移动，CollisionShape2D节点给予玩家碰撞体积，来保证与空气墙的互动存在。

**第四阶段**

![image](https://github.com/user-attachments/assets/4d76cb87-af83-4bbc-83be-0b4ad09b6def)

创建敌人单位，使用Area2D节点创建敌方单位，设计玩家与敌方单位碰撞事件，以及游戏结束事件。

今天进度先到这里了，后续每天补充进度！
