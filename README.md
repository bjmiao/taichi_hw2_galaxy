# 太极图形课S1-Galaxy
根据课上作业做了Galaxy的作业

## 背景简介
- 重构了Celestial结构，把ComputeForce当中的两部分（类内部成员计算/不同类之间相互计算）拆开，然后把clearForce写作了一个kernel，这样可以最大程度复用代码。

- 为了动态设置Mass，把mass成员设置为了一个Field成员，并且设置了Getter，Setter的Kernel。（为了方便观察，还额外考虑了planet对star的引力）

- 增加了一个简单地SuperStar.没有速度，不考虑planet和star对其的引力。

## 成功效果展示
![demo](./data/animation.gif)

## 整体结构（Optional）

## 运行方式
例如:  `python3 galaxy.py`

按B可以添加SuperStar（是的，质量就这么凭空产生了），按上或者下可以给Planet增加质量或减少质量（质量还凭空消失了）