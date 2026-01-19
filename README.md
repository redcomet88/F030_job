# F030 vue+flask求职薪资预测职位推荐知识图谱机器学习系统neo4j数据库

> 完整项目收费，可联系QQ: 81040295 微信: mmdsj186011 注明从git来的，谢谢！
也可以关注我的B站： 麦麦大数据 https://space.bilibili.com/1583208775
> 

关注B站，有好处！
编号:  F030 pro
## 视频

[video(video-gdphNf0e-1757034640297)(type-bilibili)(url-https://player.bilibili.com/player.html?aid=113773465572781)(image-https://i-blog.csdnimg.cn/img_convert/4c2f49ffd49721b81c068a3300ee543d.jpeg)(title-AI知识图谱机器学习薪资预测系统+求职就业推荐工资预测可视化大数据vue+flask)]
## 1 系统简介
系统简介：本求职系统（F030 Vue+Flask 薪资与职位推荐知识图谱可视化系统）旨在为用户提供一站式的求职体验，集成了职位推荐、数据分析、薪资预测及个人设置等多元功能。系统核心功能包括：精准职位推荐，通过Usercf和Itemcf等多种推荐算法，根据用户偏好和行为，智能匹配最合适的职位，并在主页展示，同时辅以数据分析和类型分析，帮助用户洞察职位市场。详尽职位库，允许用户通过查询功能，结合地图分析直观了解职位分布。深度数据分析，通过数据可视化和词云分析，直观呈现行业趋势与热点，同时融入求职问答功能，利用流式问答模式辅助知识图谱查询，解决用户求职困惑。智能薪资预测，引入决策树和随机森林等预测模型，为用户提供薪资参考，助力求职决策。此外，系统还具备完善的登录&注册系统及个人设置模块，包括实名认证、修改信息、头像和密码管理，确保用户数据安全与个性化体验。整个系统以知识图谱为基础，旨在通过可视化方式，让求职信息更加直观、易懂，助力用户高效找到心仪工作。
## 2 功能设计
本求职系统采用模块化、前后端分离的架构设计，以提升系统的可扩展性、可维护性和用户体验。前端部分基于Vue.js框架开发，利用HTML、CSS、JS构建用户界面，结合Vuex进行状态管理，vue-router实现路由跳转，并集成echarts等图表组件，为用户提供直观的数据可视化展示和流畅的交互体验。用户通过浏览器即可轻松访问系统。后端则采用Flask框架（Python）实现，负责处理前端请求、业务逻辑、数据存储与检索。数据存储层面，系统采用双数据库策略：MySQL用于存储如用户信息、职位信息等结构化数据，通过Sqlalchemy等ORM工具与Flask后端交互；Neo4j则作为图数据库，用于构建和存储知识图谱，通过py2neo等库与Flask后端连接，实现知识图谱的查询与推理。系统还包含爬虫模块，负责从外部数据源抓取职位、薪资等数据并存入MySQL。抓取到的数据经过图谱生成程序处理，利用py2neo等工具将节点和关系抽取出来，并生成到Neo4j中，从而构建出丰富的知识图谱，为推荐和问答服务提供强大的知识支撑。整体架构清晰，各模块职责明确，保证了系统的高效稳定运行。
**在问答方面，采用了Flask后端结合流式处理提供大模型问答服务，前端也配合流式处理的模式实现聊天界面。**
**图谱使用neo4j数据库作为存储，实现对求职知识图谱的存储、查询等操作。**
### 2.1系统架构图
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/8ca2a3040e67422fbe76af116621aa6d.png)
### 2.2 功能模块图
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/f728b08d1e384430aeac344ad8cc391a.png)
## 3 功能展示
### 3.1 登录 & 注册
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/2941e1227ca44c1a9d08625bcfe39e9e.png)
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/9191eae2314242cf94a232278f461395.png)
### 3.2 主页 & 推荐算法
主页左边是菜单栏，右边是操作面板，提供UserCF+ItemCF两种协同过滤推荐算法推荐职位：
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/0921ca7b1c414adea4e590b77768ee2a.png)
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/13aca57f6593498b96af3ac8cd5deb05.png)
### 3.3 数据分析
在这个界面可以分析职位、城市职位分析、学历与城市薪酬的关系、高薪工资、底薪公司的分析。
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/e15849babe814effb98042702026b2b8.png)
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/fa57ee04941b488191364433d4146968.png)

### 3.4 地图分析
利用中国地图分析我们系统爬取到的职位。
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/0f61ce0c770148099f13e2bd5cc71b87.png)
### 3.5 类型分析
利用散点图进行职位和薪酬的分析。
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/4a46e6df50e247af89a72f34b7778f61.png)
### 3.6 词云分析
还支持利用jieba分词进行的关键词词云分析：
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/7e649de315c64e88ac54d3f3e8a03658.png)
### 3.7 图谱可视化
知识图谱可视化：
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/678d8255b26b4788ad90ab7020206f09.png)
利用关键词进行知识图谱的查询：
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/532ef6993dca4e71b5359ac3671e9b68.png)
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/c1eebed93f164687bfbf9e93ad5335d9.png)
### 3.8 薪资预测
利用机器学习训练的**决策树模型**预测薪资：
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/7538e2a77c3942ae967582bef0ee13c6.png)
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/44f531d01d034a6bb20da93742756408.png)
利用机器学习训练的**随机森林模型**预测薪资：
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/773b156e475d442fa3a5f5db6108c9d7.png)
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/04afff14a72e4887b95b755f05e738f2.png)
### 3.9 求职助手（AI问答）
后端利用Flask 搭建流式回答，并通过服务器发送事件（SSE）逐块返回内容；整个过程确保了用户能够实时获取问题的回答，并且在流结束后得到确认。
前端将Markdown格式进行渲染，支持对Markdown常见格式包含表格的渲染：
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/721ac1d6e0f04fa4a94f1eb540067350.png)
**Markdown格式渲染：**
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/518e555fcd094c18b32619a78345fe01.png)
**支持表格的渲染：**
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/37d3db19b6414c2e95f7bf456317e7f1.png)
### 3.10 个人设置
修改个人信息、头像、修改密码、实名认证功能都集成在这个页面上。
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/c361fe3d407944f99275350f7c37de03.png)
### 3.11 实名认证
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/cf3cfc514ea644e4b22d96dc1bd40b49.png)
### 3.12 修改密码
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/f862614d89b34917b279bf5946e288eb.png)
## 4程序代码
### 4.1 代码说明
代码介绍：使用scikit-learn库来创建和训练一个决策树回归模型。数据集将使用pandas读取，并进行预处理。模型训练后，我们将使用测试集进行预测，最后计算预测的准确性。代码中包含了数据加载、特征选择、模型训练、预测和评估的步骤。
### 4.2 流程图
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/87465665b21b460f8549087dea5a8b8f.png)
### 4.3 代码实例
```python
import pandas as pd
from sklearn.model_selection import train_test_split
from sklearn.tree import DecisionTreeRegressor
from sklearn.metrics import mean_squared_error

# 加载数据
data = pd.read_csv('salaries.csv')

# 特征选择
X = data[['experience', 'education_level']]
y = data['salary']

# 数据集分割
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)

# 创建决策树回归模型
model = DecisionTreeRegressor(random_state=42)

# 训练模型
model.fit(X_train, y_train)

# 进行预测
y_pred = model.predict(X_test)

# 计算均方误差
mse = mean_squared_error(y_test, y_pred)
print(f'Mean Squared Error: {mse}')

```
