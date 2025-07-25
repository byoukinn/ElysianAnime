# 变更日志


## v2.4.0
- 优化 兼容http链接
- 新增 导入/导出RSS配置
- 优化 推荐作品随机查询条目
- 优化 推荐作品检索页面
- 优化 推荐作品查询性能
- 作品 内容获取方式改成bangumi-api


## v2.3.2
- 优化 菜单自适应展开/收起
- 优化 分享链接基础地址可配置


## v2.3.1
- 变更 sqltoy --> 5.6.46
- 变更 fastjson --> fastjson2
- 变更 hutool --> 5.8.38
- 变更 sa-token --> 1.43.0
- 变更 smart-doc --> 3.1.0
- 优化 readme页面使用AI自动构建内容


## v2.3.0
- 新增 增加对当前已观看集数、更新时间、等功能 by @[byoukinn](https://github.com/byoukinn) in [#31](https://github.com/CoCoTeaNet/ElysianAnime/issues/31)
- 调整 lombok --> 1.18.38


## v2.2.7
- 修复 添加通知消息时未处理事务导致调度异常问题


## v2.2.6
- 优化 请求时出现的StatusException统一处理
- 修复 解析部分番剧无法正常删除文件夹和重命名 by @[byoukinn](https://github.com/byoukinn) in [#27](https://github.com/CoCoTeaNet/ElysianAnime/issues/27)


## v2.2.5
- 优化 系统通知日志信息打印
- 优化 添加配置项控制邮件通知
- 优化 预览区无法实时显示 by @[byoukinn](https://github.com/byoukinn) in [#25](https://github.com/CoCoTeaNet/ElysianAnime/issues/25)
- 修复 当查不到中文名称时就用原名称代替 by @[byoukinn](https://github.com/byoukinn) in [#26](https://github.com/CoCoTeaNet/ElysianAnime/issues/26)


## v2.2.4

- 新增 在主页显示看到第几集，更新到N集和全N集
- 优化 使用qb的api对资源重命名
- 优化 首页的番剧卡片自适应
- 优化 番剧观看页面增加关闭订阅按钮
- 修复 未追番时没能正常自动播放资源


## v2.2.3

- 新增 启动banner展示效果
- 新增 RSS资源解析后的匹配结果预览
- 新增 RSS订阅资源重刷功能
- 优化 RSS可配置默认排除方案
- 优化 index.html添加meta用来禁止搜索引擎爬虫
- 优化 封面接口新增参数用来控制图片缩放大小
- 优化 RSS资源规则配置弹窗UI组件尺寸
- 修复 番剧管理页面分页栏没有固定问题
- 修复 字典页面启用状态显示异常问题
- 变更 smart-doc升级到3.0.9

## v2.2.2

- 优化 番剧作品管理列表作品名称查询条件改成模糊查询
- 优化 URL添加番剧提示语
- 优化 兼容非整形集数的媒体文件，如OVA、05.5
- 修复 取消追番操作异常问题
- 修复 500 状态码时默认响应 “ERROR” 消息提示问题
- 变更 字段ani_user_opus.reading_num整形改成字符串

## v2.2.1

- 修复：登录日志没法展示登录人名称问题
- 修复：番剧管理页面不展示创建人信息和更新人信息
- 修复：404页面没有显示背景图片问题
- 修复：后台用户头像显示异常问题
- 修复：默认头像失效问题
- 修复：番剧作品管理列表排序失效问题
- 优化：后台表格分页保持在底部展示
- 优化：后台左侧导航栏组件阴影移除
- 调整：番剧首页移到原后台分栏展示

## v2.2.0

- 新增：资源媒体播放页面添加番剧链接展示
- 修复：rss订阅完成后系统通知失效问题
- 修复：系统通知消息时间未格式化问题
- 优化：在重命名时发现qb下载记录中路径不存在则删除下载记录
- 优化：增加初始化数据SQL执行脚本
- 优化：日志文件名称小调整
- 优化：RSS执行情况UI调整
- 优化：RSS执行完毕Email通知的账号配置从properties集成到Solon
- 优化：RSS资源解析高亮颜色改成“#f38181”
- 重构：前端项目webpack迁移到vite
- 变更：包名及相关配置项从janime改成elysiananime
- 变更：版本包控制最终使用x.y.z
- 变更：接口system/dashboard/getRssWorkStatus => anime/rss/getRssWorkStatus
- 升级：Solon框架升级到2.9.1
- 升级：mysql-connector升级到8.3.0

## v2.1_202408

- 变更：核心框架从springboot2框架替换为solon2.x
- 变更：接口名(system/file/getBackground)变成(anime/opus/getBackground)
- 变更：logo更换
- 变更：项目名最终命名为“ElysianAnime”
- 变更：主题颜色同步ElysianAnime-Viewer
- 变更：默认宽屏展示
- 变更：devDependencies依赖升级[readme.md](readme.md)
- 修复：番剧管理中心删除番剧失效问题
- 优化：兼容nodejs 20+

## v2.0_202407

- 新增：系统日志添加‘接口路径’字段保存和展示
- 新增：系统日志添加@LogPersistence注解拦截存储
- 修复：当进入播放页面时立即切换其它页面会偶现播放器继续播放的问题
- 修复：远程主机强迫关闭了一个现有的连接引发的ClientAbortException
- 优化：页面路由切换动画
- 优化：后台表头新增Tab按钮动画
- 优化：系统日志查询列表默认根据id倒叙
- 优化：媒体资源接口判断逻辑
- 优化：创建Logger实例增加static关键词
- 变更：系统日志列表接口lambda多表查询模式改成xml sql模式

## v2.0_202406

1. 点开视频自动播放
2. 优化视频界面封面加载
3. 优化：验证码缓存键从ip改成用UUID标识
4. 优化：登陆成功删除验证码缓存
5. 变更：验证码接口方法post改成get
6. 新增：密码参数使用sm2加密传输
7. 优化：解决侧边栏折叠卡顿的问题
8. 修复：当token失效时未能跳转登录界面（token失效后再次登录之后token失效会触发）

## v2.0_20240615

1. 首屏数据响应速度优化
2. 删除废弃功能：schedule、cms
3. 移除echarts依赖，表格显示CPU使用情况
4. 修复跳转BGM链接多了斜杠问题

## v2.0_20240605

1. 根据观看时长自动更新观看状态
2. 异步保存封面文件

## v2.0_20240509

1. 异步保存封面文件
2. 使用Forest替换hutool-http获取番剧信息

## v2.0.0

- [X]  蜜柑RSS订阅自动下载内容
- [X]  在线番剧检索和播放
- [X]  番剧信息管理
- [X]  追番进度管理
- [X]  番剧推荐栏目
