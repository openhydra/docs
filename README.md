# OpenHydra产品文档

OpenHydra项目是由全国师范生人工智能教育共同体、九州未来亓绚科技联合发起，华东师范大学、华南师范大学、中国儿童中心儿童人工智能教育研究院、中国电子学会现代教育技术分会、上海开源信息技术协会、上海白玉兰开源开放研究院、温州大学元宇宙与人工智能研究院、NOAI组委会、虚谷计划组委会等共同参与的面向人工智能教育的开放学习与实践平台。OpenHydra开源社区构建方面，在以下几个方面进行布局：
- 面向开源众筹模式的人工智能开源课程、数据集等知识分享社区构建；
- 面向学校提供开源人工智能实验室解决方案，赋能AI教育；
- 研发软硬一体的大模型一体机，实现标准化大模型私域交付。

## 产品概述及特点

针对AI教育平台，我们以致力于快速构建校级AI实训实验室为目标，打造了AI教育软件（或一体机单机&集群），为AI教育实训提供如下价值：
1. 最小单元GPU算力切分，最佳算力资源复用
     - 允许算力服务器被动态地切割和分配给不同的实训终端，实现最大化算力资源复用。
     - 单服务器（8卡GPU）最多支持64个独立GPU实训终端。
2. 内置多个深度学习框架，在线IDE灵活使用
     - **多个深度学习框架**：内置不同的深度学习框架，如：Paddlepaddle、Keras和XEdu，便于用户选择合适的深度学习框架，提高教学与实训效率。
     - **在线IDE集成**：可集成不同IDE环境，如Vscode、Jupyterlab等，不仅提供丰富的功能和工具，还与GPU算力切分功能完美配合，为用户提供了灵活多样的训练环境。
3. 教学资源与教学秩序透明化管理，便捷的在线支持
     - **算力资源统一调度**：账户统一管理，算力资源统一调度。为用户提供统一资源分配调度的功能，轻松地管理不同账户并分配资源，灵活调度算力，从而确保每位用户都能够获得足够的资源支持。
     - **教学透明化**：教师可以通过资源环境管理功能跟进学生的学习进度和实操情况。支持远程排查学生碰到的疑难问题，可以直接进入实验环境，远程实操，与学生进行即时沟通和协作，解决学生在学习过程中遇到的问题。
4. 自动分发、更新课程课件，保持课堂及时同步
     - **课程课件版本管理**：课程课件的版本管理，为老师提供了便捷的课程课件版本管理功能，无需耗费大量时间来手动分发和更新课程资料。
     - **自动分发**：系统实时将更新的课程资源分发到不同账户的容器中，保障所有终端及时获取到最新的教学内容。避免了教学资源版本混乱和使用错误。
6. 虚拟助教在线辅教，让每个学生都有私教体验
     - **虚拟助教自助问答**：支持大模型召回的方式提供教辅材料自助问答查询，允许用户上传文件，利用RAG技术进行知识库问答，更加针对性、准确性的解决老师的问题。
     - **教学样例代码**：以课纲课件等约束条件为上下文，通过大模型自动生成相匹配的教学样例代码，标准化教学质量。
     - **支持多种大语言模型切换**：包括Qwen-7B等，这意味着用户可以根据自己的需求选择合适的模型，从而更加精准地获取答案。
7. 开箱即用的AI教学实训环境，云原生的部署
     - **极速初始化**：无需费时费力地进行繁琐的环境配置和环境搭建，只需插入U盘，一建实现环境初始化。
     - **算力自动配置**：基础GPU算力并自动部署操作系统，从而克服了用户购置和配置硬件设备上的困难。
     - **云生态虚拟化**：与OpenStack及K8S云生态无缝对接，提供更高层次的虚拟化支持，确保用户独享独立的实验环境。

## 产品使用场景

### 场景一：开源协作模式：快速构建中小学人工智能实验室基础设施

在教育领域，人工智能（AI）的普及和应用已成为培养未来科技人才的关键。为了帮助中小学快速搭建人工智能实验室基础设施，我们倡导并实践开源协作模式，通过以下步骤实现高效、低成本的实验室建设：

- **开源软件与工具的选择**：OpenHydra精选了一系列经过验证的开源软件和工具，如Jupyter Notebook、XEdu、PaddlePaddle等，这些工具不仅功能强大，而且社区支持广泛，能够满足不同层次的教学需求。
- **社区协作与资源共享**：通过参与OpenHydra开源社区，学校和学校可以获取丰富的教学资源和案例，包括课程设计、实验指导和项目模板。同时，教师和学生也可以贡献自己的创新成果，形成良性循环，不断丰富和优化教学内容。
- **模块化硬件解决方案**：提供模块化的硬件解决方案，如树莓派（Raspberry Pi）和NVIDIA Jetson Nano等，这些设备成本低廉且易于扩展，能够满足基础的AI实验需求。学校可以根据实际需求选择合适的硬件配置，灵活搭建实验室环境。
- **在线协作平台**：利用GitHub、Gitee等在线协作平台，教师和学生可以共同开发和维护实验项目，实现代码共享、版本控制和团队协作。这不仅提高了教学效率，还培养了学生的团队合作和项目管理能力。
- **持续的技术支持和培训**：提供定期的技术支持和培训，帮助教师掌握最新的AI技术和教学方法。通过线上线下的培训课程和研讨会，教师可以不断提升自己的专业能力，更好地指导学生进行AI实验和项目开发。

通过OpenHydra开源协作模式，中小学可以快速构建起功能完善、资源丰富的人工智能实验室基础设施，为学生提供一个实践和探索AI教育平台，助力在未来的科技人才培养领域中脱颖而出。

### 场景二：在线 “虚拟大模型助教”，支持问答式“一对一”学生指导

提供“虚拟助教”，凭借其内置的大模型知识库功能，为教学注入了新的活力。

作为老师，可以进行如下应用：
- 教学内容自动生成：大模型可以学习大量的教学资源和教学经验，自动生成符合要求的教学内容。例如，可以根据教学大纲和教学目标，自动生成教案、课件和教学报告等，从而减轻教师的教学负担，提高教学效率。
- 教师培训与发展：大模型还可以用于教师培训和发展。大模型可以模拟教学场景，为教师提供教学案例和教学策略等，帮助教师提升专业素养和教学能力。同时，大模型还可以对教师的教学过程进行数据分析和反馈，帮助教师发现自身的不足，并进行针对性的改进。

从学生的角度来说，可以帮助他们：
- 课件文档知识点提取与学习：大模型知识库可以处理和分析课件文档，通过自然语言处理（NLP）技术提取其中的关键知识点。学生可以利用这些知识点进行有针对性的学习，快速掌握课程的核心内容。
- 智能辅导与答疑：大模型可以为学生提供智能的作业辅导服务。通过对课程材料的学习，大模型可以对学生提出的问题进行实时解答，并提供针对性的学习建议。

通过大模型赋能教育，中小学实现了个性化的学习体验，大模型辅助教学精准匹配学生需求，提升学习效果；互动式学习环境激发学生兴趣，培养创新思维。大模型技术为教育带来革命性变化，助力学校快速搭建智能教育平台，全面提升教学效率。

## 产品快速入门

通过几个简单的课程案例，即可快速体验AI教育平台。目前OpenHydra(水螅)社区开源的AI课程可以无缝的切入本产品本地使用。

### 案例1：OpenHydra使用入门

本课程主要针对OpenHydra的新手，介绍OpenHydra的基本概念，并介绍如何使用OpenHydra进行基础的应用实践。

#### 课程目标

- 让新手快速入门OpenHydra
- 可以体验人工智能的课程
- 可以使用OpenHydra开一门课
- 可以寻找到自己感兴趣的课程
- 可以开始贡献（想法、BUG、课程、改进意见等），也可以**贡献代码**

#### 课程目录

- 红烧鱼变清蒸鱼

详细参考：[OpenHydra使用入门](https://gitee.com/openhydra/open-hydra-course/blob/main/courses/demo-course)

使用步骤如下：

1. 从github或者gitee上克隆课程仓库

```
git clone https://gitee.com/openhydra/open-hydra-course.git
cd open-hydra-course/courses
tar cvzf demo-course.tar.gz demo-course
```

2. 使用课程

- 方式1：在OpenHydra上`demo-course.tar.gz`传课程并启动课程
- 方式2：直接在启动的`JupterLab`上传`demo-course`课程到自己的工作空间


### 案例2：n个经典机器学习

机器学习n个经典实验聚焦于机器学习对应的相关课程实验。本课程基于BaseML设计，选择机器学习中最为经典的算法和数据集，以实验的方式呈现。课程涉及了线性回归（LinearRegression）、多项式回归（Polynomial）、随机森林（RandomForest）、支持向量机（SVM）、决策树（CART）、朴素贝叶斯（NaiveBayes）、K最近邻（KNN）、多层感知机（MLP）、Kmeans和Birch等。 实验涉及到的数据集，除来自经典数据集（如汽车燃油、波士顿房价、鸢尾花等）外，大部分属于自行制作。实验涉及的代码可以通过浦育平台（OpenInnoLab）、Mo平台访问和运行。 本课程由AI课程众筹计划团队开发，涉及的文档、代码、演示文稿、数据集等全部采用CC-BY协议开源。AI课程众筹计划全称为中小学开源AI课程众筹计划，由谢作如名师工作室和温州科技高级中学发起的公益活动。活动关注以机器学习、深度学习为核心的新一代AI技术，以“开源”的方式分享各种面向真实问题解决的项目式学习课程，期望能形成一系列具备复制价值的中小学AI课程库。

#### 课程目录

- 回归任务
     - 线性回归和温度转换探究
     - 多项式回归和汽车燃油效率预测
     - 随机森林和波士顿房价
     - 支持向量机和鲍鱼年龄预测
- 分类任务
     - 决策树和出行预测
     - 朴素贝叶斯和天气预报
     - K最近邻和果物分类
     - 支持向量机和手势分类
     - 多层感知机和鸢尾花分类
- 聚类任务
     - Kmeans聚类和场馆分布
     - Birch算法和操场人群分布实验

详细参考：[机器学习n个经典实验](https://gitee.com/openhydra/open-hydra-course/tree/main/courses/n-ml-lab)，使用方式参考案例1的使用方式。

## 产品核心功能

1. **高效灵活且可扩展的AI教学与实训解决方案**
   1. **多样化部署方案，一键部署&开箱即用**
        - 软件+一体机开箱即用
        - 一个U盘，即插即用
        - 开源赋能，软件需求灵活定制
        - 国产信创融合
        - 跨云无界，k8s赋能
   2. **GPU算力切分**
        - GPU算力最小切分：单服务器（8卡GPU）最多支持64个独立GPU实训终端
2. **AI教学一步到位，课程、环境及虚拟助教三位一体**
   1. **海量AI课程，携手Openhydra社区共建公开课程仓库**
        - 共创共享AI教育生态
        - 开放课程仓，集思广益
   2. **内置多个深度学习框架和多个IDE集成环境**
        - 集成多个深度学习框架和不同IDE环境
        - 实现了教学透明化
        - 支持远程排查学生碰到的疑难问题
        - 支持Xedu库为用户提供更简单便捷操作的训练方式
   3. **虚拟助教赋能多功能对话体验，支持大模型召回的知识库问答**
        - 多功能对话体验
        - 支持大模型召回的方式提供教辅材料自助问答查询
3. **标准化课程、高效资源管理与全面管理体系**
   1. **规范课程创建并标准化，即时资源分发与同步更新**
        - 全流程课程管理
        - 即时资源分发与同步更新
   2. **算力资源统一调度并可视化，平台参数灵活配置**
        - 算力资源即时透视窗
        - 平台配置灵活友好
        - 设备容器算力资源统一调度
   3. **全面的学生与教师管理体系，账号、角色和班级共同协作**
        - 统一账号管理与身份认证
        - 灵活的角色权限分配
        - 班级协作与资源共享

## 使用手册
**一、主页**

[1.1 学习中心](01homepage/01-01center.md)

[1.2 资源总览](01homepage/01-02view.md)

**二、学习工具**

[2.1 课程](02tools/02-01course.md)

[2.2 实验环境](02tools/02-02environment.md)

[2.3 虚拟助教](02tools/02-03assistant.md)

**三、教学管理**

[3.1 数据集](03manage/03-01dataset.md)

**四、用户管理**

[4.1 账号管理](04user/04-01account.md)

[4.2 角色管理](04user/04-02role.md)

[4.3 班级管理](04user/04-03class.md)

**五、设备资源管理**

[5.1 设备管理](05resources/05-01device.md)

[5.2 平台配置](05resources/05-02configuration.md)

## AI教育解决方案


## 版本信息
