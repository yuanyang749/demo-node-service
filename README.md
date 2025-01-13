# Demo Node Service

一个基于Node.js的多功能服务项目，为多个客户端页面提供数据接口服务。目前包含生日惊喜、微信通知等功能模块。

## 功能模块

### 1. 生日惊喜页面 (`/client/birthday-suprise/`)
一个浪漫的生日祝福互动页面，主要功能：
- 🎂 生日倒计时展示
- 💝 动态生日祝福页面
- 🎮 互动答题游戏
- 🎵 背景音乐播放
- 📱 移动端自适应
- 💌 微信消息通知
- 🧧 红包打赏功能

### 2. 其他功能模块
*(可以根据后续开发的其他功能进行补充)*

## 技术栈

### 前端技术
- jQuery：DOM操作和事件处理
- Lottie：轻量级动画播放
- Swiper：页面滑动切换
- rem布局：移动端适配

### 后端技术
- Express：Web应用框架
- EJS：模板引擎
- MySQL：数据存储
- wechat-api：微信模板消息
- JWT：用户认证
- Multer：文件上传
- Socket.io：实时通信
- Nodemon：开发热更新
- Axios：HTTP请求
- Cheerio：网页解析
- Lodash：工具函数库

## 项目结构
```bash
.
├── client/                 # 客户端代码
│   ├── birthday-suprise/   # 生日惊喜项目
│   │   ├── css/           # 样式文件
│   │   ├── js/            # JavaScript文件
│   │   ├── assets/        # 静态资源
│   │   └── index.html     # 入口页面
│   └── index.html         # 主页
├── server/                 # 服务端代码
│   ├── config/            # 配置文件
│   ├── utils/             # 工具函数
│   └── server.js          # 服务入口
└── package.json           # 项目依赖
```

## 开发环境要求
- Node.js >= 14.0.0
- MySQL >= 5.7
- 微信公众号测试号
- 域名（需要备案）
- 服务器（支持Node.js环境）

## 快速开始

1. 克隆项目
```bash
git clone https://github.com/yuanyang749/demo-node-service.git
cd demo-node-service
```

2. 安装依赖
```bash
npm install
```

3. 启动服务
```bash
# 开发环境
npm run start

# 生产环境
npm run pm2
```

## 配置说明

### 微信配置
在 `server/config/wechat.js` 中配置：
```javascript
module.exports = {
    appId: 'your_app_id',
    appSecret: 'your_app_secret',
    templateId: 'your_template_id'
};
```

### 数据库配置
在 `server/config/database.js` 中配置：
```javascript
module.exports = {
    host: 'localhost',
    user: 'your_username',
    password: 'your_password',
    database: 'your_database'
};
```

## API文档

### 微信通知接口
```
POST /api/send-redpacket-notification
Content-Type: application/json

{
    "price": "520"
}
```

## 部署说明

1. 服务器环境配置
2. 域名配置和SSL证书
3. Nginx反向代理配置
4. PM2进程管理

## 开发计划
- [ ] 支持更多互动游戏
- [ ] 添加用户管理系统
- [ ] 优化页面加载性能
- [ ] 增加数据统计功能

## 贡献指南
欢迎提交Issue和Pull Request，一起完善项目。

## 许可证
MIT License