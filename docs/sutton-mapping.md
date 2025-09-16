# 按 Sutton《强化学习导论（第二版）》章节 → 代码索引

说明：以下按书籍章节列出本仓库中对应的目录、Notebook 与脚本，便于学习者对照练习与阅读。路径均为相对仓库根目录的相对路径。

- 第1章 强化学习问题
  - Introduction/
    - Introduction/README.md（RL 简介、Gym 入门）

- 第2章 多臂老虎机（Bandits）
  - 暂无专门实现或笔记本（建议后续补充简单 ε-贪心/乐观初值/UCΒ 案例）

- 第3章 有限马尔可夫决策过程（MDP、Bellman 方程）
  - MDP/
    - MDP/README.md（概念与公式总览）
  - 相关工具
    - lib/envs/discrete.py（离散环境基类：nS/nA/P/isd）

- 第4章 动态规划（DP：策略评估、策略迭代、价值迭代、Gambler）
  - DP/
    - DP/Policy Evaluation.ipynb
    - DP/Policy Evaluation Solution.ipynb
    - DP/Policy Iteration.ipynb
    - DP/Policy Iteration Solution.ipynb
    - DP/Value Iteration.ipynb
    - DP/Value Iteration Solution.ipynb
    - DP/Gamblers Problem.ipynb
    - DP/Gamblers Problem Solution.ipynb
  - 教学环境
    - lib/envs/gridworld.py（注释标明来源于 Sutton 第4章 Gridworld）

- 第5章 蒙特卡洛方法（MC：预测、控制、重要性采样、Blackjack）
  - MC/
    - MC/MC Prediction.ipynb
    - MC/MC Prediction Solution.ipynb
    - MC/MC Control with Epsilon-Greedy Policies.ipynb
    - MC/MC Control with Epsilon-Greedy Policies Solution.ipynb
    - MC/Off-Policy MC Control with Weighted Importance Sampling.ipynb
    - MC/Off-Policy MC Control with Weighted Importance Sampling Solution.ipynb
    - MC/Blackjack Playground.ipynb
  - 教学环境
    - lib/envs/blackjack.py（注释对应书中 Example 5.1）

- 第6章 时序差分（TD：TD(0)、SARSA、Q-Learning）
  - TD/
    - TD/SARSA.ipynb
    - TD/SARSA Solution.ipynb
    - TD/Q-Learning.ipynb
    - TD/Q-Learning Solution.ipynb
    - TD/Windy Gridworld Playground.ipynb
    - TD/Cliff Environment Playground.ipynb
  - 教学环境
    - lib/envs/windy_gridworld.py
    - lib/envs/cliff_walking.py

- 第7章 多步自举（n-step 方法）
  - TD/README.md（概念性总结）
  - 暂未提供独立 n-step 实现的 Notebook

- 第8章 基于模型与规划（Dyna、规划-学习结合）
  - 根 README 提及 “Learning and Planning (WIP)”
  - 暂未提供实现

- 第9章 近似下的在策略预测（函数逼近）
  - FA/
    - FA/MountainCar Playground.ipynb
    - FA/README.md（函数逼近动机、半梯度方法、经验回放与固定目标技巧等）

- 第10章 近似下的在策略控制
  - FA/
    - FA/Q-Learning with Value Function Approximation.ipynb
    - FA/Q-Learning with Value Function Approximation Solution.ipynb

- 第11章 近似下的离策略方法
  - 暂未有专章 Notebook；相关思想在 DQN 等实践中体现

- 第12章 资格迹（Eligibility Traces）
  - TD/README.md（包含 TD(λ) 概念与前向/后向视角）
  - 暂未提供 λ-Return 或 True Online 等具体实现的 Notebook

- 第13章 策略梯度（REINFORCE、优势函数、Actor-Critic）
  - PolicyGradient/
    - PolicyGradient/CliffWalk REINFORCE with Baseline Solution.ipynb
    - PolicyGradient/CliffWalk Actor Critic Solution.ipynb
    - PolicyGradient/Continuous MountainCar Actor Critic Solution.ipynb
    - PolicyGradient/README.md（策略梯度方法综述）
  - A3C（扩展）
    - PolicyGradient/a3c/README.md（运行方法与 TensorBoard 监控）
    - PolicyGradient/a3c/train.py
    - PolicyGradient/a3c/estimators.py
    - PolicyGradient/a3c/worker.py
    - PolicyGradient/a3c/policy_monitor.py
    - PolicyGradient/a3c/*_test.py

- 深度 Q 学习（DQN，书外扩展/与第二版选读相关）
  - DQN/
    - DQN/Deep Q Learning.ipynb
    - DQN/Deep Q Learning Solution.ipynb
    - DQN/Double DQN Solution.ipynb
    - DQN/Breakout Playground.ipynb
    - DQN/dqn.py（Atari 端到端训练脚本）
  - Atari 预处理与辅助
    - lib/atari/state_processor.py（TF1：RGB→灰度→裁剪→84×84）
    - lib/atari/helpers.py（若存在）

- 通用可视化与实验工具
  - lib/plotting.py（学习曲线、价值函数曲面等）
  - 在多章节 Notebook 中可复用

注意
- 依赖版本：仓库历史提示对 gym==0.26 做过兼容，深度部分多用 TensorFlow v1 API（tf.placeholder / tf.Session）。
- 现代环境建议：Gymnasium + PyTorch/stable-baselines3/CleanRL 等（与本仓库教学定位无冲突，可作为扩展练习）。
