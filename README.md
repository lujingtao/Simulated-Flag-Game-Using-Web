# 前言
本人从小受到“火焰纹章”、“机器人大战”等熏陶，比较喜欢策略型游戏，但有时候玩人家的游戏总有点不尽人意，于是尝试模拟这类型游戏。

本次尝试用web技术实现战旗游戏中战场的游戏逻辑，抛砖引玉。

先放成果：[**在线地址**](https://lujingtao.github.io/Simulated-Flag-Game-Using-Web/)

# 游戏逻辑
战旗游戏逻辑比较简单：

## 一、总方向
单位：我方 vs 敌方

操作：移动+行动

结束条件：一方团灭

## 二、实现细节
地图：底图 + 操作层 + 单位层

单位放置：随机地图 + 随机单位属性 + 指定范围随机放置单位

AI逻辑：判断攻击范围有无敌人，有则攻击(优先血量少)，无则移动(移动到最近对方单位)，再判断攻击范围内有无敌人。

伤害公式：.......不详细写了，会有一些特殊情况出现，闪避、格挡之类。

## 待优化地方：
- 目前为了操作方便而使用div+canvas模式，可以改成全部canvas，提高性能
- 随机地图生成时可能把单位围住，算法待完善
- 移动范围生成时没有处理障碍物阻挡造成移动范围减少情况，算法待完善
- 目前寻路算法比较简单，可以改成使用A*寻路算法
