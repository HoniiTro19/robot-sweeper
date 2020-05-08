# README
规划并模拟扫地机器人的清扫路径，并与随机游走的清扫方式做对比

## Requirements

test on

- MATLAB R2018a

## Idea

- 规定扫地机器人的尺寸为1×1的网格，地图尺寸为20×15（参数可修改），在利用矩阵Tag储存障碍物信息（障碍物标1，非障碍物标0），barrier_generate函数随即生成障碍物
- 路径规划考虑采用深度优先搜索算法，根据标记矩阵Tag的信息，找到网格之间可达性关系，建立图的邻接压缩表，深度优先搜索求出路径（深度优先所搜算法是在别人的代码上进行修改）
[深度优先搜索源码地址](https://www.cnblogs.com/tiandsp/archive/2013/07/05/3174262.html)
- 可视化过程中首先建立起地图网格，利用网格着色体现扫地机器人的运动过程，白色表示未清扫过，黑色表示障碍物，蓝色表示清扫过一次，红色表示反复清扫过。
- 随机游走采用向上下左右四个方向等可能地游走，可视化过程和路径规划的一样
- 主函数返回的是路径规划和随机游走所花的总步数

## Usage

run robot_sweeper.m

## Tips

“项目4：扫地机器人的路径规划策略.pdf”为项目说明

“扫地机器人路径规划.pdf”为实验报告，其中有对代码的说明

