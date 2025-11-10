# course-design
Leehaoxuan's course design with unitree go2edu dog and piper, specifically, is supervised by Prof Hu Zhongxu
## **Reference Materials**

1. **[User Manual](https://marketing.unitree.com/article/zh/Go2/User_Manual.html):**  Includes frequently asked questions, indicator light meanings, and mobile app usage instructions
2. **[技术文档](https://support.unitree.com/home/zh/developer/Architecture%20Description):** 主要参考资料
## paper
1. [Deep Whole-Body Control: Learning a Unified Policy for Manipulation and Locomotion](https://arxiv.org/abs/2210.10044):CoRL bestpaper,比较早的经典论文，提出来Advantage Mixing、Regularized Online Adaptation两个trick来训练出来wholebody的locomo和manip，但是没啥感知闭环的任务，实际上是在做轨迹跟踪。使用PPO
2. [UMI on Legs: Making Manipulation Policies Mobile with Manipulation-Centric Whole-body Controllers](https://arxiv.org/abs/2407.10353) ：CoRL spotlight，分离了操作的policy（使用了dp）和loco，使用操作预测末端位置并且使用whole body跟踪轨迹，其中操作策略是在4090上面跑的，我觉得可以尝试替换为rdt2，wbc控制器大概率要重新训练
3. [RDT2](https://rdt-robotics.github.io/rdt2/#)对夹爪和相机有要求，但是支持zeroshot的部署，RDT2VQ支持RL后训练
4. [Visual Whole-Body Control for Legged Loco-Manipulation](https://arxiv.org/abs/2403.16967):CoRL Oral
5. [Learning coordinated badminton skills forlegged manipulators](https://www.science.org/doi/epdf/10.1126/scirobotics.adu3922):science robotics
  
