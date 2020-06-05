# local_planner

机器人局部路径规划算法

## 问题描述

* 基本避障功能，静态和动态，尤其动态障碍物的追身问题
* 路径，速度连续平滑
* 平均速度0.5m/s
* 狭窄通道的通过性， 尤其目标点在正后方时
* 全局路径存在解的情况下，仍然有失败的现象

## 方案介绍

* pure pursuit 纯跟踪算法
    * 在全局路径上选取预瞄距离，几何跟踪的比例控制器
    * 容易实现，计算效率高，全局路径贴合程度高
    * 速度过快，转弯曲率过大，预瞄点选取不合理时容易超调，无人车应用

* dwa 动态窗口法

    * 在满足加速度约束的条件下，采样多组线速度，角速度，并依次检查评估，选取代价最低的轨迹
    * 采样时间内加速度恒定。
    * 前向仿真，容易实现，计算效率高
    * 适合差速底盘

* mpc 模型预测控制

    * 建立系统，问题模型，预测未来时刻系统状态，求解代价函数的最优控制量
    * 最优控制问题，计算量大，实时性问题
    * 无人车应用广泛，适用于差速底盘的开源代码可能还不太完善

* teb_local_planner 
    * 基于时间的最优控制问题，计算量很大，实时性问题
    * 适用于各种类型底盘
    * 目前开源代码相对成熟稳定

* minimum jerk, minimum snap 
    * 无人机相关

## 参考资料

* PythonRobotics
    * [https://atsushisakai.github.io/PythonRobotics/]()

* pure_pursuit
    * [https://github.com/larics/pure_pursuit]()
* dwa
    * [http://wiki.ros.org/dwa_local_planner?distro=melodic]()
* mpc
    * [https://github.com/rst-tu-dortmund/mpc_local_planner]()
    * [https://github.com/Geonhee-LEE/mpc_ros]()           
* teb
    * [https://github.com/rst-tu-dortmund/teb_local_planner]()    