# service-gin

## 项目目录结构
```
project/
├── cmd/                    # 项目入口
│   └── main.go            # 主程序入口
├── config/                # 配置管理
│   ├── config.go         # 配置加载和解析逻辑
│   └── config.yaml       # 配置文件（支持 YAML/JSON 等格式）
├── internal/              # 私有基础设施实现（仅项目内部使用）
│   ├── database/         # 数据库相关
│   │   ├── mysql.go     # MySQL 实现
│   │   └── postgres.go  # PostgreSQL 实现
│   ├── cache/           # 缓存相关
│   │   ├── redis.go    # Redis 实现
│   │   └── memcached.go # Memcached 实现
│   ├── logger/          # 日志相关
│   │   ├── zap.go      # Zap 日志库实现
│   │   └── logrus.go   # Logrus 日志库实现
│   ├── auth/           # 身份验证
│   │   └── jwt.go     # JWT 认证实现
│   └── middleware/     # HTTP 中间件
│       ├── auth.go    # 认证中间件
│       └── logger.go  # 日志中间件
├── pkg/                  # 可复用的公共代码（可被外部使用）
│   ├── database/        # 数据库接口
│   │   └── interface.go # 定义 Database 接口
│   ├── cache/          # 缓存接口
│   │   └── interface.go # 定义 Cache 接口
│   ├── logger/         # 日志接口
│   │   └── interface.go # 定义 Logger 接口
│   ├── utils/          # 通用工具函数
│   │   ├── string.go  # 字符串处理工具
│   │   └── date.go    # 日期处理工具
│   └── types/          # 通用类型定义
│       └── user.go    # 用户类型定义
├── services/             # 业务逻辑
│   ├── user/            # 用户管理模块
│   │   └── user.go     # 用户注册、登录等逻辑
│   ├── order/          # 订单处理模块
│   │   └── order.go   # 订单创建、查询等逻辑
│   └── product/        # 产品展示模块
│       └── product.go # 产品列表、详情等逻辑
├── handlers/             # HTTP 请求处理（控制器）
│   ├── user.go          # 用户相关请求处理
│   ├── order.go        # 订单相关请求处理
│   └── product.go     # 产品相关请求处理
├── routes/               # 路由定义
│   └── routes.go        # 定义所有路由
├── migrations/           # 数据库迁移脚本
│   └── 001_create_users_table.sql # 创建用户表的迁移脚本
├── tests/                # 测试代码
│   ├── handlers/        # 处理函数测试
│   │   └── user_test.go # 用户处理函数测试
│   ├── services/       # 业务逻辑测试
│   │   └── user_test.go # 用户服务测试
│   └── internal/       # 基础设施测试
│       └── database_test.go # 数据库测试
├── docs/                 # 项目文档
│   ├── api.md           # API 接口文档
│   └── architecture.md  # 项目架构文档
├── scripts/              # 构建和部署脚本
│   ├── build.sh        # 构建脚本
│   └── deploy.sh       # 部署脚本
├── wire/                 # 依赖注入相关
│   ├── wire.go         # 定义 ProviderSet 和 InitializeApp
│   └── wire_gen.go     # Wire 生成的依赖注入代码
├── static/ (可选)        # 静态资源文件
│   ├── css/            # CSS 文件
│   ├── js/            # JavaScript 文件
│   └── images/        # 图片文件
├── templates/ (可选)     # HTML 模板文件（服务器端渲染）
│   ├── layout.html     # 通用布局模板
│   └── index.html      # 首页模板
├── logs/                 # 日志文件
│   └── app.log         # 应用日志文件
├── go.mod                # Go 模块定义
├── go.sum                # 依赖校验信息
├── README.md             # 项目说明文档
└── LICENSE (可选)        # 项目许可证
```

