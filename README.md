# Amazing Racer

## 项目简介
本项目是基于 Unity 引擎开发的第一个简单 3D 游戏——**Amazing Racer**。
游戏的核心理念是让玩家在一个充满挑战的地形中，从起点尽快行进到终点。

## 核心玩法 (Gameplay)
- **目标**：从复活点（Spawn Point）出发，穿越地形，到达完成区域（Finish Zone）。
- **挑战**：
  - 复杂的地形（山丘、树木、障碍物）。
  - 水障（Water Hazard）：掉入水中会被送回起点。
- **胜利条件**：到达终点即视为完成。虽然没有内置计时器，但鼓励玩家尝试以最短时间完成。

## 项目结构与需求
### 场景组件
- **地形 (Terrain)**：使用高度图雕刻的 200x100 矩形区域。
- **环境 (Environment)**：
  - 天空盒 (Skybox)
  - 水域 (Water)
  - 树木与纹理
- **交互对象**：
  - `SpawnPoint`：空物体，定义玩家复活位置。
  - `WaterHazardDetector`：带有触发器（Trigger）的平面，检测玩家落水。
  - `Finish`：带有光源和胶囊碰撞器（Capsule Collider）的完成区域。

### 脚本说明 (Scripts)
- `RespawnScript.cs`：挂载在 `WaterHazardDetector` 上，负责将落水的玩家移回 `SpawnPoint`。
- `FinishScript.cs`：挂载在 `Finish` 对象上，检测玩家是否到达终点。
- `GameControlScript.cs`：挂载在 `GameControl` 对象上，管理游戏的整体逻辑和 UI 显示。

## 如何运行
双击re1.exe以运行游戏。
