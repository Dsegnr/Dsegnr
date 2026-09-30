<div align="center">
  <img src="https://cdn.jsdelivr.net/gh/Dsegnr/Dsegnr@7a965291932930c5fec492fee7267b1c2e7867ec/assets/header.svg" width="100%" alt="王佳豪 · Dsegnr">
</div>

<h3 align="center">跨被试脑电情感识别　·　多模态视觉感知　·　灾害预警</h3>

<p align="center">
  <a href="mailto:3660157476@qq.com"><img src="https://cdn.jsdelivr.net/gh/Dsegnr/Dsegnr@main/assets/badges/email.svg" alt="Email"></a>
  <a href="https://dsegnr.github.io"><img src="https://cdn.jsdelivr.net/gh/Dsegnr/Dsegnr@main/assets/badges/homepage.svg" alt="Homepage"></a>
  <a href="https://github.com/Dsegnr"><img src="https://cdn.jsdelivr.net/gh/Dsegnr/Dsegnr@main/assets/badges/github.svg" alt="GitHub"></a>
</p>

<br>

河南工业大学　计算机科学与技术　2025 级本科生，**复杂性科学研究院「飞鸟创新实验班」2025 级（首届）成员**，现在大二上。

<div align="center">
  <img src="https://cdn.jsdelivr.net/gh/Dsegnr/Dsegnr@7a965291932930c5fec492fee7267b1c2e7867ec/assets/timeline.svg" width="100%" alt="2025.09 – 2026.09 里程碑">
</div>

## 能力概览

### 研究方向

**基于情绪先验与认知预算的可学习 Mamba 脑区扫描策略。**

Mamba 的因果扫描要求人为指定遍历顺序，而脑区之间并没有天然的一维序——我关心的是这个顺序能否被学出来，以及学到的东西能否跨被试泛化。在 DEAP（32 折）与 SEED（15 折）上，全部实验走严格 LOSO 协议。

### 这件事难在哪

**效应量比噪声小。** 论文级的增益在 +1pp 量级，而折间波动 SD 有 4–5pp，32 折的 SE ≈ 0.9pp。也就是说，一个"看起来有效"的机制很可能只是噪声。这决定了我做研究的方式：

- **多臂对照矩阵** —— 把机制拆成可隔离的开关，做全组合 + 打乱对照 + 第二种子，单轮 17 臂
- **预注册判据** —— 达标线提前写死（Δ ≥ +0.8pp、|Δ|/SE ≥ 2、两种子同向、弱组止跌），不做事后找补
- **机制级诊断** —— 不只盯准确率：用真实训练步反查梯度，抓到过"路由上下文编码器全程 `grad=None`"这类只看指标永远发现不了的实现漏洞
- **弱 / 强被试分解** —— 定位到核心机制的收益几乎全部来自弱被试（+1.94pp 对比 −0.18pp），此后每个新机制都必验"弱组是否止跌"

### 能力

- **实验设计与统计推断** —— 小效应量下的多臂对照、同折配对检验、机制对照（shuffle）与预注册判据
- **深度学习** —— CNN / Transformer / 图网络 / 状态空间模型（SSM · Mamba）；多尺度融合、梯度反转、对比学习、EMA
- **机器学习与优化** —— 随机森林 / XGBoost / SHAP、ARIMAX 时序建模、强化学习（Q-Learning / PPO）、组合优化（SABRE）
- **工程交付** —— 全栈开发（TypeScript / React / FastAPI / MySQL / Neo4j / Docker）；传感器接入协议设计；版式与 UI 由代码生成
- **写作与表达** —— 32 页竞赛论文、22 页项目计划书、21 页作品说明文档、5 页 A3 设计交付

3 项软件著作权（均为第一著作权人）｜蓝桥杯省一等奖 + 全国总决赛三等奖｜APMCM 本科组二等奖｜"华数杯"本科生组三等奖

## 教育

**河南工业大学**　计算机科学与技术（本科）｜2025.09 – 2029.06（预计）

**[复杂性科学研究院](https://cs.haut.edu.cn/) · 飞鸟创新实验班 2025 级**（首届成员）
2025.10 经个人报名、资格审核与面试考核入选（[选拔公示](https://cs.haut.edu.cn/info/1421/8304.htm)）。创新实验班实行全程导师制，导师 刘广恩，研究方向为跨被试脑电情绪识别。

**学生工作**　信息学院第二十三届学生会 · 学习部成员；明德书院校运会铅球队队长

**社会实践**　暑期"三下乡"社会实践；寒假返乡宣传（学校组织）

## 项目

**[星图 · 岗位能力图谱动态演化与分析系统](https://github.com/Talent-Star-Map/XINGTU)**　`挑战杯"揭榜挂帅"专项赛 · 参赛中`　多源异构岗位数据 + 知识图谱 + 大模型的人岗匹配平台，团队项目。本人负责求职端"我的"模块与企业端企业信息模块，并参与模型幻觉防控。

**边坡哨兵 · 边坡形变监测与分级预警系统**　`学科竞赛 · 参赛中`　多传感器融合的双时间尺度边坡分级预警，负责数据对齐、预警算法与可视化。

**跨被试脑电情感识别**　`科研 · 长期进行中`　在 DEAP 与 SEED 上执行严格 LOSO 协议，复现并改进基于 Mamba / SSM 的架构。

**[噪声自适应量子编译器](https://github.com/Dsegnr/ccf-quantum-compiler)**　`2026 CCF 量子计算编程挑战赛（量旋杯）· 算法赛道 · 已提交`　基于 SABRE 映射算法的面向 NISQ 硬件的量子编译器，针对含噪中间规模量子设备做布局与路由的噪声自适应优化。

**[心聆 · 青少年心理健康多模态智能筛查平台](https://github.com/Dsegnr/xinling-mental-health)**　`中国国际大学生创新大赛 · 进行中`　以脑电为主、量表为辅的青少年心理健康客观筛查与分级预警平台。

**城市场景多模态目标检测**　`全球校园人工智能算法精英大赛 · 进行中`　可见光、红外与深度三种模态的数据对齐与融合。

**[畅途灵控 · 实时转向车道级交通管控 AI 交警](https://github.com/Dsegnr/iflytek-cup-ai-city)**　`第二届"讯飞杯"AI+ 创新应用大赛 · 2025.11`　多源数据感知 + 随机森林预测 + Q-Learning 多路口协同的信号配时优化，控制粒度下沉到转向车道。

## 竞赛与荣誉

- **蓝桥杯全国软件和信息技术专业人才大赛**（C/C++ 程序设计大学 B 组）：河南赛区一等奖、全国总决赛三等奖｜2026
- **中国高校计算机大赛 · 团体程序设计天梯赛**：参赛｜2026
- **APMCM 亚太地区大学生数学建模竞赛**：本科组二等奖｜2026　（[论文与代码](https://github.com/Dsegnr/math-modeling/tree/main/apmcm-2026)）
- **"华数杯"全国大学生数学建模竞赛**：本科生组三等奖｜2026　（[论文与代码](https://github.com/Dsegnr/math-modeling/tree/main/huashubei-2026)）
- **全国大学生数学建模竞赛（高教社杯）**：参赛｜2026
- **第十八届蓝桥杯大赛「主视觉与赛事 IP 文创设计」专项赛**（赛事 IP 文创设计赛道）：参赛中｜2026
- **中国（国际）传感器创新创业大赛**：参赛中｜2026
- **中国国际大学生创新大赛**：进行中｜2026
- **"挑战杯"**：院赛二等奖；揭榜挂帅专项赛进行中｜2026
- **全球校园人工智能算法精英大赛**：进行中｜2026
- **河南工业大学 2025 年度"三好学生"**（2026.05）
- **IITC 工业互联网平台开发工程师（中级）**（2026.07）
- **全国大学英语四级 497**（2026.06）

## 软件著作权

申请中，均为**第一著作权人**：

- 边坡哨兵滑坡灾害协同感知与预警系统 V1.0
- 滑坡多传感器融合与涌浪风险估算软件 V1.0
- 星图智能简历解析与简历管理软件 V1.0

## 技术栈

<p>
  <img src="https://cdn.jsdelivr.net/gh/Dsegnr/Dsegnr@main/assets/badges/python.svg" alt="Python">
  <img src="https://cdn.jsdelivr.net/gh/Dsegnr/Dsegnr@main/assets/badges/cpp.svg" alt="C/C++">
  <img src="https://cdn.jsdelivr.net/gh/Dsegnr/Dsegnr@main/assets/badges/pytorch.svg" alt="PyTorch">
  <img src="https://cdn.jsdelivr.net/gh/Dsegnr/Dsegnr@main/assets/badges/opencv.svg" alt="OpenCV">
  <img src="https://cdn.jsdelivr.net/gh/Dsegnr/Dsegnr@main/assets/badges/matlab.svg" alt="MATLAB">
  <img src="https://cdn.jsdelivr.net/gh/Dsegnr/Dsegnr@main/assets/badges/fastapi.svg" alt="FastAPI">
  <img src="https://cdn.jsdelivr.net/gh/Dsegnr/Dsegnr@main/assets/badges/typescript.svg" alt="TypeScript">
  <img src="https://cdn.jsdelivr.net/gh/Dsegnr/Dsegnr@main/assets/badges/react.svg" alt="React">
  <img src="https://cdn.jsdelivr.net/gh/Dsegnr/Dsegnr@main/assets/badges/mysql.svg" alt="MySQL">
  <img src="https://cdn.jsdelivr.net/gh/Dsegnr/Dsegnr@main/assets/badges/neo4j.svg" alt="Neo4j">
  <img src="https://cdn.jsdelivr.net/gh/Dsegnr/Dsegnr@main/assets/badges/docker.svg" alt="Docker">
  <img src="https://cdn.jsdelivr.net/gh/Dsegnr/Dsegnr@main/assets/badges/latex.svg" alt="LaTeX">
</p>

## 开源仓库

- [**Talent-Star-Map/XINGTU**](https://github.com/Talent-Star-Map/XINGTU)　星图 · 岗位能力图谱动态演化与分析系统（团队仓库，本人为开发者之一）
- [**math-modeling**](https://github.com/Dsegnr/math-modeling)　数学建模竞赛作品存档：APMCM 2026 与华数杯 2026 的论文、代码、数据与结果表
- [**iflytek-cup-ai-city**](https://github.com/Dsegnr/iflytek-cup-ai-city)　畅途灵控 · 实时转向车道级交通管控 AI 交警（讯飞杯参赛作品，含策划书、源代码与演示材料）
- [**ccf-quantum-compiler**](https://github.com/Dsegnr/ccf-quantum-compiler)　噪声自适应量子编译器（2026 CCF 量旋杯 · 算法赛道，含 21 页作品说明文档）
- [**xinling-mental-health**](https://github.com/Dsegnr/xinling-mental-health)　心聆 · 青少年心理健康多模态智能筛查平台（项目计划书、LaTeX 源码与配图）
- [**Dsegnr.github.io**](https://github.com/Dsegnr/Dsegnr.github.io)　本主页与简历的源码

## 数据

<div align="center">
  <img src="https://cdn.jsdelivr.net/gh/Dsegnr/Dsegnr@main/github-metrics.svg" alt="GitHub Metrics">
</div>

---

<p align="center">
  <sub>河南工业大学　计算机科学与技术　2025 级　|　<a href="https://dsegnr.github.io">个人主页与简历</a></sub>
</p>
