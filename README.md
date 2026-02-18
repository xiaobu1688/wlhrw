
# 外卖配送员交流论坛

一个专为外卖配送员设计的现代化交流论坛平台。

## 功能特点

### 🌟 核心功能
- **用户认证**：注册、登录、密码重置
- **发布帖子**：支持文字、图片、视频内容
- **分类管理**：8个预置分类，支持自定义分类
- **评论系统**：多级评论、点赞功能
- **个人主页**：用户资料、发帖记录、收藏管理
- **积分系统**：基于活跃度的等级制度
- **搜索功能**：支持全文搜索和标签搜索

### 📱 设计特点
- **响应式设计**：适配PC端和移动端
- **现代化界面**：使用Ant Design组件库
- **实时通知**：消息提醒和通知
- **快速导航**：侧边栏菜单和顶部导航

### 🎯 用户群体
- 外卖配送员（美团、饿了么、闪送等）
- 同城配送员
- 兼职配送员
- 配送行业从业者

## 技术架构

### 前端技术栈
- **框架**：React 18
- **UI库**：Ant Design 5
- **构建工具**：Vite
- **路由**：React Router 6
- **富文本编辑**：React Quill
- **HTTP请求**：Axios
- **状态管理**：React Context + useReducer
- **日期处理**：Day.js

### 后端技术栈
- **框架**：Node.js + Express
- **数据库**：MongoDB
- **ORM**：Mongoose
- **身份认证**：JWT + bcrypt
- **文件上传**：Multer
- **跨域处理**：CORS
- **环境变量**：Dotenv

### 部署方式
- **Docker容器化**：支持Docker Compose
- **Nginx反向代理**：静态文件服务
- **PM2进程管理**：Node.js进程管理

## 快速开始

### 1. 环境准备
- Node.js >= 16.x
- MongoDB >= 4.4
- npm或yarn

### 2. 安装依赖

```bash
# 安装后端依赖
cd forum
npm install

# 安装前端依赖
cd forum/client
npm install
```

### 3. 配置环境变量
创建 `.env` 文件在 `forum` 目录下：

```env
PORT=3001
MONGODB_URI=mongodb://localhost:27017/delivery-forum
JWT_SECRET=your-secret-key-here
NODE_ENV=development
```

### 4. 启动项目

```bash
# 启动后端服务器
cd forum
npm run dev

# 启动前端开发服务器（另一个终端）
cd forum/client
npm run dev
```

### 5. 访问应用
- 前端应用：http://localhost:3000
- 后端API：http://localhost:3001/api
- 健康检查：http://localhost:3001/api/health

## 项目结构

```
forum/
├── server.js                 # 后端入口文件
├── package.json              # 后端依赖配置
├── .env                      # 环境变量配置
├── models/                   # 数据模型
│   ├── User.js              # 用户模型
│   ├── Post.js              # 帖子模型
│   ├── Comment.js           # 评论模型
│   └── Category.js          # 分类模型
├── routes/                   # API路由
│   ├── users.js             # 用户相关路由
│   ├── posts.js             # 帖子相关路由
│   ├── comments.js          # 评论相关路由
│   └── categories.js        # 分类相关路由
├── middleware/              # 中间件
├── config/                  # 配置文件
├── client/                  # 前端项目
│   ├── src/
│   │   ├── components/      # 通用组件
│   │   ├── pages/          # 页面组件
│   │   ├── layouts/        # 布局组件
│   │   ├── services/       # API接口
│   │   ├── hooks/          # 自定义Hooks
│   │   └── utils/          # 工具函数
│   ├── public/             # 静态资源
│   └── index.html          # HTML模板
└── README.md                # 项目说明
```

## 分类说明

### 1. 配送技巧
- 路线规划经验
- 取餐送件技巧
- 恶劣天气应对
- 超时处理方法

### 2. 路线规划
- 最佳路线推荐
- 交通状况分析
- 避堵攻略
- 导航软件使用

### 3. 平台规则
- 平台规则解读
- 投诉处理流程
- 扣款申诉
- 新手入门指南

### 4. 安全注意
- 交通安全知识
- 物品保管方法
- 人身安全防范
- 事故处理流程

### 5. 生活分享
- 骑手生活记录
- 配送故事分享
- 兼职经验
- 行业感悟

### 6. 装备推荐
- 配送装备选购
- 电动车改装
- 防雨防晒装备
- 实用工具推荐

### 7. 平台对比
- 平台政策对比
- 收入计算方法
- 兼职选择建议
- 平台选择指南

### 8. 其他
- 行业动态
- 建议反馈
- 招募信息
- 自由交流

## 数据管理

### 初始化数据
首次运行时，系统会自动创建8个预置分类。

### 数据导入
可以通过MongoDB导入工具导入示例数据。

### 备份策略
建议定期备份MongoDB数据。

## 安全配置

### 生产环境建议
- 使用HTTPS协议
- 配置防火墙
- 设置强密码策略
- 定期更新依赖

### 数据安全
- 密码加密存储
- 文件上传限制
- XSS防护
- SQL注入防护

## 贡献指南

欢迎大家贡献代码和建议！

### 开发流程
1. Fork项目
2. 创建功能分支
3. 提交代码
4. 创建Pull Request

### 代码规范
- 使用ESLint和Prettier
- 遵循React最佳实践
- 保持代码简洁易懂
- 新增功能需要测试

## 许可证

MIT License

## 联系方式

如有问题或建议，请通过以下方式联系：

- 邮箱：contact@example.com
- 微信：delivery-forum
- QQ群：123456789

## 更新日志

### v1.0.0 (2024-01-15)
- 项目初始化
- 基础功能实现
- 发布第一个版本
