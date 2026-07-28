# 26思政科研项目：生物启发的无人机具身智能控制与自主导航
## 项目概述

本课题面向具身智能与仿生机器人研究，学生将结合仿真平台与真实无人机系统，探索具身智能、强化学习、自主导航与脑机接口等前沿方向。

目标是基于Crazyflie平台，拆分避障、导航、归巢、编队、任务执行等能力，构建实时低资源智能系统。

## 主要方向

1. 生物启发感知与自主导航
2. 智能控制与群体协同
3. 脑机接口与数字孪生

## 方向一：生物启发感知与自主导航
围绕昆虫、鸟类等生物的感知与导航机制，研究无人机在复杂环境中的自主飞行能力，包括：

- 生物启发避障导航（Optic Flow、Looming、LGMD等）

- 视觉语言导航（Vision-Language Navigation）

## 方向二：智能控制与群体协同

围绕学习驱动的控制与多机协同决策，研究无人机自主学习与群体智能，包括：

- 强化学习自主飞行与穿门竞速

- 多无人机群体智能与协同控制

## 方向三：脑机接口与数字孪生

围绕人机协同与智能体训练，研究脑信号控制和虚实融合系统，包括：

- 脑机接口（BCI）控制无人机

- Crazyflie数字孪生与Sim2Real迁移

## 需要学习的基础知识

- 仿真：Mujoco平台
- 真机：Crazyflie
- 嵌入式：控制器、通信、烧录、底层接口等
- 运控算法：闭环调节、强化学习

## 学习资料

### 相关论文（不分先后，凭兴趣阅读）

#### 一、LGMD 的生物学基础与经典计算模型

这一类论文主要解释 LGMD 神经元如何编码目标接近、角尺寸和角速度，以及早期计算模型如何形成兴奋—抑制—汇聚框架。

> Hatsopoulos, N., Gabbiani, F., & Laurent, G. (1995). Elementary computation of object approach by a wide-field visual neuron. *Science, 270*(5238), 1000–1003. doi: 10.1126/science.270.5238.1000.

> Gabbiani, F., Krapp, H. G., & Laurent, G. (1999). Computation of object approach by a wide-field, motion-sensitive neuron. *Journal of Neuroscience, 19*(3), 1122–1141. doi: 10.1523/JNEUROSCI.19-03-01122.1999.

> Blanchard, M., Rind, F. C., & Verschure, P. F. M. J. (2000). Collision avoidance using a model of the locust LGMD neuron. *Robotics and Autonomous Systems, 30*(1–2), 17–38. doi: 10.1016/S0921-8890(99)00063-9.

> Bermúdez i Badia, S., Bernardet, U., & Verschure, P. F. M. J. (2010). Non-linear neuronal responses as an emergent property of afferent networks: A case study of the locust LGMD. *PLOS Computational Biology, 6*(3), e1000701. doi: 10.1371/journal.pcbi.1000701.

#### 二、LGMD 模型改进与机器人、无人机避障

这一类包括 ON/OFF 通路、LGMD2、脉冲适应、分区竞争、神经形态视觉以及与无人机控制和规划器的结合。

##### 2.1 ON/OFF 通路与碰撞选择性

> Fu, Q., Yue, S., & Hu, C. (2016). Bio-inspired collision detector with enhanced selectivity for ground robotic vision system. In *Proceedings of the British Machine Vision Conference (BMVC)* (Paper 6, pp. 1–13).

> Fu, Q., Hu, C., Peng, J., & Yue, S. (2018). Shaping the collision selectivity in a looming-sensitive neuron model with parallel ON and OFF pathways and spike-frequency adaptation. *Neural Networks, 106*, 127–143. doi: 10.1016/j.neunet.2018.04.001.

> Fu, Q., Hu, C., & Yue, S. (2019). Collision selective visual neural network inspired by LGMD2 neurons in juvenile locusts. *IEEE Transactions on Neural Networks and Learning Systems, 31*(10), 4303–4317. doi: 10.1109/TNNLS.2019.2950674.

##### 2.2 神经形态视觉与事件相机

> Salt, L., Indiveri, G., & Sandamirskaya, Y. (2017). Obstacle avoidance with LGMD neuron: Towards a neuromorphic UAV implementation. In *2017 IEEE International Symposium on Circuits and Systems (ISCAS)* (pp. 1–4). doi: 10.1109/ISCAS.2017.8050976.

> Salt, L., Howard, D., Indiveri, G., & Sandamirskaya, Y. (2020). Parameter optimization and learning in a spiking neural network for UAV obstacle avoidance targeting neuromorphic processors. *IEEE Transactions on Neural Networks and Learning Systems, 31*(2), 464–477. doi: 10.1109/TNNLS.2019.2941506.

##### 2.3 小型四旋翼闭环避障与方向控制

> Zhao, J., Hu, C., Zhang, C., Wang, Z., & Yue, S. (2018). A bio-inspired collision detector for small quadcopter. In *2018 International Joint Conference on Neural Networks (IJCNN)* (pp. 1–7). doi: 10.1109/IJCNN.2018.8489142.

> Zhao, J., Ma, D., Fu, Q., Hu, C., & Yue, S. (2019). An LGMD-based competitive collision avoidance strategy for UAV. *arXiv preprint*, arXiv:1904.07206. doi: 10.48550/arXiv.1904.07206.

> He, L., Aouf, N., Whidborne, J. F., & Song, B. (2020). Integrated moment-based LGMD and deep reinforcement learning for UAV obstacle avoidance. In *2020 IEEE International Conference on Robotics and Automation (ICRA)* (pp. 7491–7497). doi: 10.1109/ICRA40945.2020.9197152.

> Zhao, J., Wang, H., Bellotto, N., et al. (2023). Enhancing LGMD’s looming selectivity for UAV with spatial-temporal distributed presynaptic connections. *IEEE Transactions on Neural Networks and Learning Systems, 34*(5), 2539–2553. doi: 10.1109/TNNLS.2021.3106946.

#### 三、LPLC2 生物机制与径向运动检测模型

这一类从果蝇 LPLC2 神经元的径向运动对抗机制出发，逐步发展到计算模型、LGMD–LPLC2 混合模型、多目标 attention field 和复杂动态场景检测。

##### 3.1 LPLC2 神经生理基础

> Klapoetke, N. C., Nern, A., Peek, M. Y., et al. (2017). Ultra-selective looming detection from radial motion opponency. *Nature, 551*(7679), 237–241. doi: 10.1038/nature24626.

> Ache, J. M., Polsky, J., Alghailani, S., et al. (2019). Neural basis for looming size and velocity encoding in the Drosophila giant fiber escape pathway. *Current Biology, 29*(6), 1073–1081.e4. doi: 10.1016/j.cub.2019.01.079.

##### 3.2 LPLC2 计算模型与 LGMD–LPLC2 扩展

> Zhao, Z., Xi, W., Li, N., et al. (2023). A fly-inspired solution to looming detection for collision avoidance. *iScience, 26*(4), 106337. doi: 10.1016/j.isci.2023.106337.

> Shuang, F., Zhu, Y., Xie, Y., et al. (2023). OppLoD: The opponency-based looming detector, model extension of looming sensitivity from LGMD to LPLC2. *arXiv preprint*, arXiv:2302.10284. doi: 10.48550/arXiv.2302.10284.

> Gu, B., Feng, J., & Song, S. (2024). Looming detection in complex dynamic visual scenes by interneuronal coordination of motion and feature pathways. *Advanced Intelligent Systems, 6*(9), 2400198. doi: 10.1002/aisy.202400198.

##### 3.3 mLPLC2 与 Attention Field 多目标定位

> Liu, R., & Fu, Q. (2025). Attention-driven LPLC2 neural ensemble model for multi-target looming detection and localization. In *2025 International Joint Conference on Neural Networks (IJCNN)* (pp. 1–8). doi: 10.1109/IJCNN64981.2025.11227781.

#### 四、微型无人机视觉感知与低算力运动估计

这一类不直接采用 LGMD 或 LPLC2，但为避障系统提供光流、目标跟踪、深度估计、三维重建和事件视觉等底层感知信息。

##### 4.1 光流与极简视觉导航

> Bouwmeester, R. J., Paredes-Vallés, F., & de Croon, G. C. H. E. (2023). NanoFlowNet: Real-time dense optical flow on a nano quadcopter. In *2023 IEEE International Conference on Robotics and Automation (ICRA)* (pp. 1996–2003). doi: 10.1109/ICRA48891.2023.10161258.

> Patil, A., Singh, M., Maradana, U. G., & Sanket, N. J. (2026). MinNav: Minimalist navigation using optical flow for active tiny aerial robots. *arXiv preprint*, arXiv:2606.07813. doi: 10.48550/arXiv.2606.07813.

##### 4.2 单目深度估计与环境重建

> Simon, N., & Majumdar, A. (2023). MonoNav: MAV navigation via monocular depth estimation and reconstruction. *arXiv preprint*, arXiv:2311.14100. doi: 10.48550/arXiv.2311.14100.

##### 4.3 UAV 目标跟踪与遮挡建模

> Zhang, J., Yu, X., & Lin, Y. (2026). Rethinking occlusion modeling for UAV tracking. In *Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR)* (pp. 13563–13573).

##### 4.4 事件视觉、运动去模糊与辐射场重建

> Zou, R., Cannici, M., & Scaramuzza, D. (2026). Event-aided sharp radiance field reconstruction for fast-flying drones. *IEEE Transactions on Robotics, 42*, 1591–1606. doi: 10.1109/TRO.2026.3672537.

#### 五、无人机局部规划、MPC 与无地图避障

这一类主要解决从感知结果到安全轨迹或控制量的生成，与 LGMD/LPLC2 的反应式碰撞检测属于互补关系。

> Zhang, L., Hu, Y., Deng, Y., et al. (2025). Mapless collision-free flight via MPC using dual KD-trees in cluttered environments. *arXiv preprint*, arXiv:2503.10141. doi: 10.48550/arXiv.2503.10141.

> Zheng, H., Chen, Z., Fu, Y., et al. (2026). SCAN-Planner: Spatial collision-aware local planning for route-guided long-range quadruped navigation. *arXiv preprint*, arXiv:2606.19555. doi: 10.48550/arXiv.2606.19555.

注：SCAN-Planner 的实验对象是四足机器人而非无人机，但其空间碰撞感知、局部轨迹生成和长距离路线引导思路，可作为 UAV 局部规划器的跨平台参考。

#### 六、纳米四旋翼数据集、系统辨识与状态估计

这一类论文主要用于模型训练、飞行动力学辨识、控制器评估和状态估计基准，不属于单独的避障方法。

> Ullah, S. I., & Baca, J. (2026). NanoBench: A multi-task benchmark dataset for nano-quadrotor system identification, control, and state estimation. *arXiv preprint*, arXiv:2603.09908. doi: 10.48550/arXiv.2603.09908.

#### 七、果蝇视觉系统、连接组与具身神经模型

这一类研究不直接输出 UAV 避障控制信号，但为构建具有生物结构约束的视觉网络、运动神经回路和具身智能模型提供基础。

##### 7.1 果蝇视觉连接组与神经活动预测

> Lappalainen, J. K., Tschopp, F. D., Prakhya, S., et al. (2024). Connectome-constrained networks predict neural activity across the fly visual system. *Nature, 634*(8036), 1132–1140. doi: 10.1038/s41586-024-07939-3.

##### 7.2 果蝇全身物理仿真与具身控制

> Vaxenburg, R., Siwanowicz, I., Finkelstein, A., et al. (2025). Whole-body physics simulation of fruit fly locomotion. *Nature, 643*(8074), 1312–1320. doi: 10.1038/s41586-025-09029-4.

##### 7.3 气味羽流跟踪与人工智能体神经动力学

> Singh, S. H., van Breugel, F., Rao, R. P. N., & Brunton, B. W. (2023). Emergent behaviour and neural dynamics in artificial agents tracking odour plumes. *Nature Machine Intelligence, 5*, 58–70. doi: 10.1038/s42256-022-00599-w.

#### 八、仿生导航与动物空间表征

这一类研究从蜜蜂学习飞行和蝙蝠方向细胞中提取导航机制，重点是归航、方向估计和低资源长距离导航，而不是近距离 looming 避障。

##### 8.1 蜜蜂启发的低资源无人机归航

> Ou, D., Hagenaars, J. J., Jankowski, M. R., et al. (2026). Efficient robot navigation inspired by honeybee learning flights. *Nature, 653*(8116), 1039–1046. doi: 10.1038/s41586-026-10461-3.

##### 8.2 蝙蝠头方向细胞与自然环境导航

> Palgi, S., Geva-Sagiv, M., Las, L., et al. (2025). Head-direction cells as a neural compass in bats navigating outdoors on a remote oceanic island. *Science, 390*(6770), eadw6202. doi: 10.1126/science.adw6202.

### 仿真软件学习

- 可参考B站视频，例如：<https://www.bilibili.com/video/BV1YnLP6uEeZ/>

### 强化学习运动控制算法学习

- <https://github.com/google-deepmind/mujoco_playground>
- <https://www.bilibili.com/video/BV1znLy6hEGR/>

### Crazyflie官方文档

- <https://www.bitcraze.io/>

### 嵌入式硬件

- 参考`./hardware`，自行结合视频、实物学习

## 仓库文件

- `./bitcraze_crazyflie_2`：Crazyflie仿真模型与场景，可导入Mujoco运行
- `./hardware`：硬件学习资料，包括焊接、PCB、stm32、无人机等

## 学习情况记录表

【腾讯文档】仿生无人机项目学习进度表
- https://docs.qq.com/sheet/DZHdnaVhaVFVCcXNs
