# 简介

一个尚未完成的war3自定义地图，使用[Wurst](https://wurstlang.org/)制作。

完成进度似乎还不到一半的样子。

# 下载

[内置JAPI版](https://github.com/colorful300/platform-escape-without-delay/raw/master/output.w3x)

[YDWElua引擎版](https://github.com/colorful300/platform-escape-without-delay/raw/use_lua_engine/output.w3x)

# 逃脱大师

这个图看起来像是逃脱大师系列的样子，请参考[逃脱大师的百度百科](https://baike.baidu.com/item/逃脱大师/20175006)。

这个图的按键操作没有延时，玩家本地的操作由玩家本地完成(当然也是可以多人同时游戏的)，所以就无需使用反延时工具了，可以在对战平台上愉快地玩耍。

加入了一个按↓加速下降的设定，仅仅是增加最大下降速度而不会改变重力加速度，给懒得等待小球慢吞吞下降的dalao们。

加入了一个当重力反转时镜头翻转的设定，这样重力反转之后看起来更和谐了，但是看起来难度增大了的样子。

# 基本操作

参考[基本操作](https://baike.baidu.com/item/逃脱大师/20175006#1)

使用键盘←↑→↓操作(游戏内可以按ESC自行设定)

↑ - 跳跃

← - 向左移动

→ - 向右移动

↓ - 加速下降

# 加速

参考[进阶加速操作](https://baike.baidu.com/item/逃脱大师/20175006#2)

举个栗子: 如果当前小球**向左加了N速**，那么

    A. 不作任何操作时，小球以N倍移动速度向左移动
    B. 按←时，小球以(N+1)倍移动速度向左移动
    C. 按→时，小球以(N-1)倍移动速度向左移动

如果需要**向左加N速**，则需

    1. 按下←键不放
    2. 按N下→键

# 编辑

## 修改地形

    1. 直接打开map.w3x修改保存，然后使用wurst来构建一下就OK了

## 添加地形类型

    1. 修改wurst/Base/GameSystem/TerrainType.wurst，根据注释和例子增加地形类型

## 添加特殊地形/机关

    1. 参考wurst/Base/GameSystem/Traps里的几个机关(没有做同步，所以暂时消失类的机关只会在本地玩家的机器上消失)

## 其他

    1. 自己看着修改吧。。。不过早期代码没写好，有点乱，一堆东西全都堆到了Character.wurst里面了。。。只要摸清楚同步方法了就可以随意修改了
