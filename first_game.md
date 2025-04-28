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

***

**第五阶段**

![image](https://github.com/user-attachments/assets/b3a70cd6-f46b-4360-b9c4-5729a9fb50ec)

创建子弹节点实现玩家攻击行为，内容涵盖子弹生成位置，子弹循环生成方式，子弹生成时机，以及子弹销毁时机以防止内存占用问题的出现。

**第六阶段**

![image](https://github.com/user-attachments/assets/d7205bed-a1ce-4ae0-85ba-d86c985aac8f)

上一阶段创建子弹节点后自然要进行子弹与怪物的交互，这一阶段中，将子弹节点设置一个独立的分组，然后用条件语句判断怪物的碰撞区域内是否有area进入（将子弹分组的目的在这里提现：由于怪物同样使用Area2D创建，分组后防止了怪物之间的触碰亦会导致条件生效-即触发怪物死亡事件的情况。）

设置完子弹与怪物的交互后，下一步实现怪物自动生成。这里在主场景下挂在了GameManager脚本来控制怪物的自动生成，包括怪物生成的位置范围，以及随着时间推移，敌人生成的频率逐渐加快。

按照上面子弹与怪物的交互设计，子弹碰撞怪物后销毁自身，怪物播放死亡动画，之后怪物依旧会移动且具有碰撞体积。按教程来的话，是通过一个bool变量来控制，若怪物已死，则停止移动，且在播放完死亡动画后释放掉自身。但这样处理还是会有问题，一是博主使用了固定的时间间隔（0.6s）来代表动画已播放完毕，二是怪物死亡后播放死亡动画期间若触碰玩家，依旧会触发玩家死亡（即游戏结束）事件。将Ai与博主的方案结合后的处理方式为：

![image](https://github.com/user-attachments/assets/beb35ce6-44ac-4461-b9d3-c28e592f05a0)
这里的判断逻辑应该还有问题并非最优解，后续学习以及创作过程中若意识到此处问题会返回修改

**第七阶段**

![image](https://github.com/user-attachments/assets/8b7f1a66-589a-41ff-8e64-6778af0a6685)

此阶段主要添加UI内容，包括分数显示，以及游戏结束的GameOver显示。

**第八阶段**

![image](https://github.com/user-attachments/assets/5da65aa8-7d6e-40ee-9456-50748a125fc3)

此阶段使用AudioStreamPlayer节点来为游戏添加音效，包括射击音效，脚步声，怪物受击音效，游戏BGM，游戏结束音效等。

**第九阶段**

最后是导出游戏，Godot的导出模板需要额外下载（Steam版听说自带有）。下载安装完成后将游戏导出为Windows版可执行文件。

![image](https://github.com/user-attachments/assets/e36c35f2-033a-4f4c-82d3-b227bc995227)

作者最后还给了导出为Web的教程，但是我下载的Godot版本并不支持，有点可惜。初步尝试到此完结，撒花❀！！

![image](https://github.com/user-attachments/assets/6ac35d57-8e1b-4da9-96b6-c83fd346fcb1)

本次尝试参考的教程几乎手把手教，作者讲的很详细，给了我很大信心，后续我的学习可能要进入更理论一些的过程中了，如果有再次尝试，会继续在本文更新。最后对本次教程的作者表示感谢~

参考教程：BV1fuCrYFEoG
