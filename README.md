# 公主连结实用/娱乐插件 for HoshinoBot on Mirai

A repository for [HoshinoBot](https://github.com/Ice-Cirno/HoshinoBot) based [PCR](http://priconne-redive.jp/) plugins made by myself.


## 简介

一些基于 [HoshinoBot](https://github.com/Ice-Cirno/HoshinoBot) 开发的公主连结实用插件或有趣的娱乐插件，开发环境为Mirai。

其他还有一些之前在酷Q Pro环境下开发的HoshinoBot插件，我没迁移到此仓库中，不过它们基本都可以直接装在Mirai的HoshinoBot上，它们是：

- **[轴管理插件](https://github.com/GWYOG/HoshinoBotTimelinePlugin)**：加入了向机器人录入图片或者文字轴的指令，之后可以方便地查询数据库中存放的轴。此插件可使公会在会战中更方便的查询、交流、优化轴，也可以让几个公会之间共享轴。

- **[box统计插件](https://github.com/GWYOG/HoshinoBotBoxCollectionPlugin)**：加入指令，在管理员设定好需要统计的角色星级后，机器人会自动私聊指定人员询问并统计汇总他们的角色星级。统计完毕后，在群内可以使用指令方便的查看分类汇总的统计结果；也可以自动生成统计结果的csv文件，或者把统计结果的表格以图片形式发送到群中(这个功能很实用!)。

- **[猜语音小游戏插件](https://github.com/GWYOG/HoshinoBotVoiceGuessPlugin)**：机器人会自动从干炸里脊资源站下载所有角色的打开游戏时说的的那句"cygames"语音。之后机器人会随机发送一句语音到群里，让群友猜猜是哪位角色说的，并在一定时间后公布正确答案和猜对的人。由于只有较高版本的cqhttp-mirai支持发送语音，这个插件装在HoshinoBot-mirai上时需要适当注意。

- **[会战名次查询插件](https://github.com/GWYOG/HoshinoBotClanRankSearchPlugin)**：使用查询指令后，机器人会从镜华会战名次查询网获取数据，把需要查询的公会的会战当前名次或历史名次发送到群里。这个插件功能刚写到一半就开巨蟹座会战了，所以功能比较简陋。打完会战发现github上有不少同类型的功能更完善的插件，所以就弃坑了(笑)。
 
## 此仓库插件介绍(基于Mirai开发)
 #### 猜角色小游戏插件pcrdescguess
|指令|说明|
|-----|-----|
|猜角色|机器人会随机给出角色的一些描述，群友需要根据这些描述猜出是哪个角色|
|猜角色排行榜|显示猜角色小游戏猜对次数的群排行榜|

 #### 猜头像小游戏插件pcravatarguess
|指令|说明|
|-----|-----|
|猜头像|机器人会发送某个角色头像随机截取的一小部分，群友需要猜出它来自哪个角色头像|
|猜头像排行榜|显示猜头像小游戏猜对次数的群排行榜|


## 安装方式

1. clone或者下载此仓库的代码

2. 将需要安装的插件文件夹放在`hoshino/modules/`文件夹中。比如如果想安装pcrdescguess插件，那么就把`pcrdescguess`文件夹放入。
  
3. 打开`hoshino/config/`文件夹中的`__bot__.py`文件，在`MODULES_ON`中加入插件的名称。比如如果想安装pcrdescguess插件，那么就加入一行`'pcrdescguess',`


## 注意事项
 最好事先下载全角色头像放在HoshinoBot的资源文件夹中。虽然机器人在发现需要发送的角色头像缺失时也会自动从干炸里脊资源站下载，不过这样机器人会变卡。
