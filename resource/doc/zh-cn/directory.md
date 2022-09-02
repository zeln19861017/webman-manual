# 目录结构
```
.
├── app                           应用目录
│   ├── controller                控制器目录
│   ├── model                     模型目录
│   ├── view                      视图目录
│   └── middleware                中间件目录
│   |   └── StaticFile.php        自带静态文件中间件
|   |—— functions.php             自定义函数
|
├── config                        配置目录
│   ├── app.php                   应用配置
│   ├── autoload.php              这里配置的文件会被自动加载
│   ├── bootstrap.php             进程启动时onWorkerStart时运行的回调配置
│   ├── container.php             容器配置
│   ├── dependence.php            容器依赖配置
│   ├── database.php              数据库配置
│   ├── exception.php             异常配置
│   ├── log.php                   日志配置
│   ├── middleware.php            中间件配置
│   ├── process.php               自定义进程配置
│   ├── redis.php                 redis配置
│   ├── route.php                 路由配置
│   ├── server.php                端口、进程数等服务器配置
│   ├── view.php                  视图配置
│   ├── static.php                静态文件开关及静态文件中间件配置
│   ├── translation.php           多语言配置
│   └── session.php               session配置
├── public                        静态资源目录
├── process                       自定义进程目录
├── runtime                       应用的运行时目录，需要可写权限
├── start.php                     服务启动文件
├── vendor                        composer安装的第三方类库目录
└── support                       类库适配(包括第三方类库)
    ├── Request.php               请求类
    ├── Response.php              响应类
    ├── Plugin.php                插件安装卸载脚本
    ├── helpers.php               助手函数
    └── bootstrap.php             进程启动后初始化脚本
```
>> webma 启动后第一个请求会扫描整个app目录找到请求对应控制器，所以前端静态文件放到/public目录下，避免因文件过多扫描时间过长导致重启变慢。
