---
layout:     post
title:      "兴趣并不是最好的老师，责任才是，不甘、屈辱是导员和班主任"
subtitle:   "MediaStudio项目总结"
date:       2017-09-24 12:00:00
author:     "Wjl"
header-img: "img/post_msfr.png"
catalog: true
tags:
    - 项目总结
---

windows平台有非编客户端，加上当时有用户提过想要简单编辑录像，和环出需求，于是大佬们研究决定立项。  
在得知是QtCreator项目的二次开发，加上某些模块还有MFC的具体实现，上下一片乐观。  
在没分配到具体任务时先看QtCreator源码，弄清core/iplugin的模式。  
框架搭好后clone下来从解析配置文件开始，一个模块一个模块干。  
详细工作过程
![pic1](https://github.com/halukasama/imghosting/blob/master/post/1609/mediastudio1.png?raw=true)
![pic2](https://github.com/halukasama/imghosting/blob/master/post/1609/mediastudio2.png?raw=true)

不知不觉3个月之中，大佬在帮我Review源接入模块时，因为着急出长差，
直接干掉了我所有CV源接入部分，加了一周班指导我重写了一个，
并嘱咐Local,KV源也得是这个思路。  
MVC阿，算是初窥了。
后来又经历了项目组两个同事离职代码交接之后。  
这项目就基本我一个人在搞了。  
写到后面，问题渐渐暴露出来  
1. `不沟通，就是原罪。` 
2. 过于乐观，加上没有经验，很多问题没想太远，导致后期频繁修改。
3. 兴趣驱动不可取，责任感才是持续的长久的。(看看那些半死不活的开源项目)

> 所谓的各个插件不相影响，但是公共插件互相影响阿，基础工具，抽象类，共享数据对象不实用。 
> 打个比方：就元数据这块fastPreview时我要实现drop功能，改一次MetaData,那么重度依赖元数据的Node要改，Seg要改，又对源接入和录像部分有影响。如果运气好，上述两个Plugin不用动。 
> Profile肯定要改，改了之后，又要把工程管理的解析部分对应节点改一下。  
> 加上没经验，想的不够全面，频繁改，后来每动一次，恨不得三思^2，(这里感谢一波git checkout,  stash, reset)最后写东西的乐趣变成折磨。  
> 当初要是大家想的多一些，全一些，一些想法尽早互通一下，达成相关的约定，也不会出现这种情况。  
> 最关键的是，和预期的目标差了太多，核心模块(编辑)别说编码，连想都没想过呢。  
> 热情没有了，心态消极，就渐渐把工作重心放在其他工作上了。  
> `这是我个人暴露出来的最大的问题，什么都是兴趣驱动，作事靠热情，特别幼稚。`  
> 好在当时已经认识到症结所在，在全民ZLC时我顶住压力，没被抽调过去。  
> 完成了ONVIF。也算是对MS有个交代。  

半年之后，在回忆这件事，又有新的认识，假如我当初咬牙把这个比较困难的节点攻下来，
那么大佬回来，看到哪怕一点点成绩，会不会出现另一个结局？
大佬出差回来，连句重话都没说。
这锅我甩不出去。。。。。。

`其实语法糖，设计模式，编程思想，奇技淫巧，编码命名规范等这些都是建立在问题被解决之后的锦上添花。  
只有能解决问题的代码才是炉子里的碳。除了继续学习实践，积累经验，提升编码能力没有别的办法。`

>”To me，being perfect is not about that scoreboard out there. It's not about winning. It's about you and your relationship to yourself and your family and your friends. Bein' perfect is about being able to look your friends in the eye and know that you didn't let them down. Because you told 'em the truth. And that truth is, is that you did everything that you could. There wasn't one more thing that you could've done. Can you live in that moment as best you can with clear eyes and love in your heart? With joy in your heart? If you can do that, gentlemen, then you're perfect.”——————<<Friend Night Light>>

对我来说，追求完美与获取高分无关，与胜负无关。而在于你，在于你跟你自己、家人和朋友的关系。追求完美就是你能够双眼直视你的朋友，知道自己没有让他们失望。因为你始终可以坦诚地告诉他们，你已经尽你所能、不遗余力。在那一刻，你能否以清澈的眼睛和满腔的热忱去面对他们？并且在深心里感到欢愉？先生们，如果你们能够做到这一点，那你们就是完美的。

我知道在今后的工作当中，我还是会失败，但那一定是竭尽全力后的我坦然面对的失败。  
一定不会向这一次一样，充满遗憾。

抱歉峰神。😶  
------ 