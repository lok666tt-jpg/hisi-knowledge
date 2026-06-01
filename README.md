# 民航机场软件知识库 App

## 打开方式

直接用浏览器打开 `index.html`。


## 已包含功能

- 知识卡片新增、编辑、保存草稿、发布保存
- 默认只查询已发布内容，可切换草稿或全部
- 关键词搜索标题、答案、场景、注意事项、标签、附件解析文字
- 标签和业务分类筛选
- 详情页一键复制标准答案
- 附件选择与解析状态展示，TXT/CSV 可读取文本，PDF/Word/Excel 预留后端异步解析状态
- 手机、平板、电脑响应式布局
- 浏览器本地保存演示数据，可重置示例

## 后续接入后端

当前版本是前端可交互原型，数据存储在浏览器本地。接入正式服务时，建议把 `cards` 的本地读写替换成 REST API：

- `POST /auth/login`
- `GET /cards?query=&status=&category=&tags=`
- `POST /cards`
- `PATCH /cards/:id`
- `POST /cards/:id/attachments`
- `GET /attachments/:id`

数据库、附件目录、文档解析、HTTPS 和备份任务可按方案部署到 Docker Compose。
