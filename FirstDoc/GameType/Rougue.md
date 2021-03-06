地牢类游戏
---------------------------------
### 简述 & 历史
Roguelike是电子角色扮演游戏（RPG游戏）的一个子类。1980年开发的Rogue被认为是Roguelike的先驱与该类型名称的来源。上个世纪在大学生及程序员中十分流行，并衍生出了诸多变体,上古时代的Rouguelike游戏里最著名的有Tome，angband，nethack，adom，dungeon crawl。<br>
Rouguelike游戏有三大主要标志性特征：**地图随机性**、**系统深度性**、以及**永久死亡机制**。
* **地图随机性**<br>
早期的电子游戏受限于储存设备的容量，没办法像现代游戏制作时一样进行精致到可怕的关卡设计。一旦采用人为的关卡设计模式，意味着更多的图片资源使用，和在当时看来十分可怕的关卡信息的存储。这既是技术难题，也会提高游戏容器的成本。在这样的困境面前，关卡生成的技术自然而然的出现了。程序员先存储几种组成地形的基础砖块，然后编写能够组成连通区域的算法，用算法随着游戏进行不断生成新区域，再设置敌人和物品以一定难度系数随机的出现在这些迷宫里。以随机性换取了游戏程序的小容量，而随机性本身也让游戏充满了挑战和惊喜。随机性就这样成为了Rouguelike游戏的标配。
* **系统深度性**<br>
很多人都玩过像贪食蛇，扫雷这样以随机性来驱动的游戏，它们往往也是写游戏程序路上的必修课。这类游戏往往都在游戏性上不够让人满意。固定的玩法，随机常常只意味着位置的变化，仅仅依靠随机性来生成游戏内容的游戏，很容易就会让人感到厌倦。可能有人会说棋类游戏不也是这样吗？但棋类游戏有人作为对战对象，相当于有一个高智商的AI（也不一定~），自然会在简单的玩法里产生无穷的游戏性。<br>
这个时候，系统的深度成为了Rouguelike游戏的又一法宝。<br>
电子游戏诞生之初有一股潮流，当时的所有游戏都致力于还原DND（龙与地下城）桌游带来的游戏体验，早期的Rouguelike也是如此。如果你是一名桌游玩家，那你一定明白我的意思。在像龙与地下城，克苏鲁的召唤这样的复杂桌游中，玩法手册定义了大量千奇百怪的道具和魔法，在按照脚本进行冒险故事的时候，玩家可以根据物品描述，以自己想象得到的所有方式搭配，使用道具，大量的道具和魔法提供了丰富的组合，你有几乎无数种方法来对付敌人，进行战斗，这种每场冒险都使用不同道具，属性不同的人物所带来的丰富体验，使得每一场冒险都那么的独一无二，这也就是我们所说的游戏性。
>>> 笔者查阅资料的时候，发现回合制也被定义为Roguelike的一大要素，在某种程度上的确如此。然而，经过深思熟虑，我还是认为无论是元素的经典性还是对Rouguelike游戏体验的重要性上，富有深度的系统设计都更为重要，所以将其当做一个重点来讨论。
* **永久死亡机制**<br>
在电子游戏刚刚出现的那个时代，严厉的死亡惩罚在很大程度上提升了游戏的难度。每次死亡都会失去一切，只能重头再来，失去一切，表面上看是这样。但实际上，玩家的记忆和手感是存在，对抗不同类型的敌人该使用的策略和战术也留在了玩家心里。玩家毫无疑问成长了，在下一次游戏中将变得更加成熟，有实力走的更远。<br>
永久死亡机制在提升了游戏难度的同时，使玩家积累成长，采取更谨慎，聪明的方式进行游戏。当然，也有很多轻度玩家会因为没办法突破死亡的沮丧感接触到新内容而放弃Rouguelike游戏，这的确是一个大问题，也是为什么现在有越来越多的Rouguelite游戏更受欢迎，这点我们将在稍后做更多讨论。

以上是我个人的意见，除此之外，你可能还会考虑一下“柏林准则”，这是在一次国际会议上，一些开发者对Rouguelike游戏类型的描述，它很全面的描述了Rouguelike游戏**可以**包含的要素。注意我的措辞是 可以。在制作一款游戏时通常不需要包含所有的这些特性，但你也许会觉得它有参考价值：
> 柏林准则:<br>
>>1、生成随机性。每一次新开局游戏都会随机生成游戏场景，敌人，宝物等不同事物。玩家的每一次冒险历程也都将是独一无二，不可复制的。只要玩家愿意的话，可以让玩家连扮演的角色都设置成随机生成的。
例如敌人，武器，甚至只是一个角色的皮肤或者场景中的河流等。<br>
2、进程单向性。当你在玩一款Roguelike游戏时，存档功能的唯一作用就是记录你当前的游戏进度，每当存档被读取时，对应的进度就会被清空，
直到你进行下一次存档。这种存档机制确保玩家无法利用"S/L大法"来降低游戏难度。甚至在Roguelike玩家圈中，手动备份存档会被当做一种作弊行为受到鄙视。<br>
3、不可挽回性。在大多数Roguelike游戏中，每一个角色只有一次生命，一个角色的死亡意味着玩家将永远失去该角色。
无论你是主角，敌人，物品或者场景。甚至在很多Roguelike玩家眼中，Roguelike的最大魅力之一就在于体验每一次不同的死亡与失败，
并最大努力的做好当下的自己。<br>
4、游戏非线性。严谨而不失灵活性的游戏规则，使Roguelike具备了极高的自由度，在游戏中，玩家可以发挥想象力，
利用各种手段去达成任何他们想做的事情，或合乎常理，或匪夷所思，目的只在于解决他们在游戏中遇到的问题。<br>
5、画面朴素性。其实Roguelike类游戏的鼻祖Rogue被普遍认为是最先有图形界面的冒险游戏之一，虽然这种“图形界面”抽象的过分。
但是很多Roguelike类游戏出于对Rogue的致敬，会直接使用ASCII字符来表示游戏画面。而到了近代，虽然电脑的性能有了质的提高，即便是小团队的开发者也能够开发出绚丽的3D画面，但Rouguelike游戏却依旧高举着复古的大旗，在当下这个时代，像素风成为了Rouguelike游戏的主流。<br>
6、系统复杂性。Rogue本身的复杂程度就远远超过同时期的任何一款作品。
而Roguelike类游戏可能会在一款游戏中包括多到无法估量的元素，例如地质、气候和生物分布，以及精细到皮肤、肌肉、血液、骨骼
和脂肪的战斗系统，甚至战损痊愈后会留下伤疤以及后遗症。在有些游戏里则可能包括数百种的死亡原因，数千种的生物，数万种的物品。
可以说除了Roguelike类游戏，再也没有任何传统游戏能够不计成本的拥有如此多的元素了。<br>

  柏林准则可以说在很大程度上影响了地牢类游戏的发展趋势，但它更像是一种预言，开发者们并不会遵照柏林准则去制作自己的游戏，但他们往往在迭代的
过程中，一步一步符合了柏林准则中提到的这些特性。可以认为，柏林准则的确抓住了Rouguelike的精髓。
  不过，作为一个开发者，你也许还听说过Rouguelite。Rouguelite其实主要是对上述准则中的不可挽回性做出了妥协，换取了成长性要素，给游戏的体验
带来了巨变。这个问题很有趣，我们将在后面做更多的讨论。
### 要素
#### 关卡生成系统
  毫无疑问，关卡生成系统是地牢类游戏的核心机制。事实上，如果你想提高自己的游戏编程能力，尝试去做一款Rouguelike游戏应该是你的首选。可以断言，每一款成功的Rouguelike游戏背后都有一个巧妙而充满生机的房间生成系统。<br>
  <div align=center><img width="300" height="300" src="https://github.com/IndieGuide/ImagesRepo/blob/master/Images/Fromnet/Graphic%20Method/Dungeon/dungeonMap.png"/></div>
  让我们来考虑一个传统地牢形态地图的实现，它应该包含以下要点：
  
  * 一组相互连通的房间、门和通道
  * 一个地牢入口
  * 一个地牢出口
  * 所有的空间相互连通
  
作为Rouguelike游戏的开发者，首先应该掌握的算法，就是如何生成游戏的房间，这并不是什么难事，考虑以下步骤：<br>

第一步，使用随机数控制生成一组形状不等的矩形，确保它们在游戏场景里不会相互重叠，最后生成走廊将其一一连接起来。

第二步，在这些房间中生成两块用来代表入口和出口的地砖，通常需要通过限制条件使它们所在的房间不会相隔太近。这里可能会出现对房间进行遍历的操作，所以，如果你使用的是面向对象语言，在生成房间的阶段应该考虑以节点的方式让房间之间互相记录相互连通的房间id，有一个节点式的房间结构会对后续的一些机制设计有很大的帮助。比如控制宝箱和boss房间的位置。

第三步，房间里


### 作品展示
#### The Binding of Isaac
<div align=center><img width="640" height="360" src="https://github.com/IndieGuide/ImagesRepo/blob/master/Images/Fromnet/Works%20Show/Isaac/1.jpg"/></div>

#### Don't Starve
<div align=center><img width="540" height="360" src="https://github.com/IndieGuide/ImagesRepo/blob/master/Images/Fromnet/Works%20Show/Dont%20starve/1.png"/></div>

#### Dead Cell
<div align=center><img width="640" height="360" src="https://github.com/IndieGuide/ImagesRepo/blob/master/Images/Fromnet/Works%20Show/Dead%20cells/1.jpg"/></div>

#### Enter the gungeon
<div align=center><img width="640" height="360" src="https://github.com/IndieGuide/ImagesRepo/blob/master/Images/Fromnet/Works%20Show/Enter%20the%20gungeon/1.jpg"/></div>

#### Faster Than Light
<div align=center><img width="640" height="360" src="https://github.com/IndieGuide/ImagesRepo/blob/master/Images/Fromnet/Works%20Show/Ftl/1.jpg"/></div>

### 发展趋势
* Rouguelite成为主流
* 与Metroidvania的融合
* 更好地画面表达
* 提早上架，持续更新
