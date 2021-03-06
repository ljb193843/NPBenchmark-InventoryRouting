# 问题描述

## 概述

在若干个周期中为客户送货，要求在每个客户每个周期都不断供的情况下，使得库存维护开销和路由开销的总和最小.


## 已知

- 车辆
  - 容量
- 仓库
  - 库存维护的单位开销
  - 初始库存
  - 每周期补充库存
- 客户
  - 库存维护的单位开销
  - 容量
  - 初始库存
  - 每周期消耗库存
- 路径
  - 路程开销


## 约束

- 每个周期同一客户最多访问一次
- 车辆每一轮送货是从仓库出发，最后回到仓库
- 每个周期同一辆车最多从仓库出发一次
- 送货量不超过客户的容量
- 在仓库的装货量不超过车辆容量，且装货量为同一周期所有客户送货量之和
- 客户每周期剩余库存不超过客户容量，不低于最低库存量
- 仓库每周期剩余库存不为负


## 目标

库存维护开销和路由开销之和.


## 决策

每个周期每辆车去哪些客户送多少货以及客户的访问顺序.



# 数据接口

## 输入数据格式

### 基本情况

见 `Protocol/InventoryRouting.proto`.

### 数据约定

- 车辆数为 1
- 周期数为 3 或 6


## 输出数据格式

### 基本情况

见 `Protocol/InventoryRouting.proto`.
