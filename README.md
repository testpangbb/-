# 苹果马甲包上架过审4.3原理分析 

**从17年开始接触传奇游戏马甲，慢慢摸索，从半年过不了一个包，到如今社交马甲、游戏马甲、原生马甲,从最开始到github上面找混淆工具，到自己编写混淆工具，一份代码用了4、5年，照样能混淆上架，对苹果的审核不敢说百分百能了解他的规则，但是至少也是有个七八成了。**

### 苹果的审核原理
##### 1.机器预审核
<p style="font-size:20px;">最开始对苹果审核不太了解，后面通过和广州游戏同行的交流，了解到苹果原来是有预审核的，当你在苹果后台，点击提交审核，苹果通常会用机器静态扫描你的代码，如果静态扫描你的代码都能关联到其他App，不管是线上或已经下架的，关联程度过高，可能都不会进行下一步审核。
  一般情况下大部分App这一步都不会出现问题，接着一般会有苹果的审核设备打开你的App进行机器模拟用户点击，你在后台也能看到苹果的爱尔兰、美国加州、新加坡等等IP访问记录，通常我认为这一步苹果会对你代码关联到的App做一定的界面相似度比较。
</p>

##### 2.人工审核
<p style="font-size:20px;">
  我们在脑海中可以设想一副这样的场景，工作人员坐着办公桌前面，面前摆着iPhone和一些iPad设备，电脑上是一个苹果的审核软件，每个工作人员每天需要完成一定的审核任务，具体审核哪个App，则是由苹果后台的软件进行分发，每当工作人员在电脑上点击开始审核后，你苹果后台的状态变成了“正在审核”。
  
  这个时候，苹果的审核机器开始重点对你的代码进行分析排查，找出你代码能够关联到的一些App，因为机器进行代码关联分析需要一定的时间，所以一个工作人员，同一时间肯定不会干等这你一个App的机器出结果，而是会点击多个App进行审核。等哪一个App的机器审核结果完成以后，就进入接下来他的重点工作了。
  这个时候审核界面会弹出一个审核结果的界面，能够出现你代码的查重率，比如你的关联程度是40%，关联点是某某界面，某某文件，或者某某字符串等等，和以下这些App相似度过高，这个时候工作人员会打开你的App和关联到的App进行人工审查比对，这个时候是有主观因素的影响的。当然如果你关联程度过高，比如关联程度达到了90%，那他甚至都不会打开你的App和对方的App进行比对，直接在审核结果上面打上一个4.3

  如果关联程度过低，则他可能就直接去审查你的App功能和界面了。这则是正常审核，通常我们认为一个审核人员真正把玩你App的时间大概就在1-5分钟左右。甚至更短。大部分审核工作和任务其实都是交给苹果的审核机器和AI了。
</p>


##### 3.审核人员
<p style="font-size:20px;">
其实如果能够了解审核人员的工作内容和日常，大概也就能对审核有一个清晰的了解了，你只要知道，你被拒绝的大部分原因其实是机器，甚至你刚刚提的包4.3被拒，下一秒你混淆或UI处理到位，他机器之前找出的关联点全都消失了，那就能过审，因为机器找不到你的漏洞了，审核人员不认识你，也不会管你上个版本为什么4.3，他只认当前的机器审核结果，就自热而然的让你通过了。

审核人员的自由度也没那么大，你也不需要去巴结他，觉得马屁拍到位了就能过审，甚至威胁审核人员，这些都没有意义，重点是他的审核机器找不到你问题了，你就能过审。

充其量他就是一个NPC而已，他有每天的工作任务，每天审核上百个App，你头大不大，他也有绩效，如果他手里审核的App最后判断为马甲包，如果数量过多，他们每周甚至每天的周会日会就会挨屌。
</p>


有时间再写后续..
