# cnblogs-theme-next
next-theme博客园主题,使用论文格式设计，专注阅读体验

## 特性
- 高度还原[next-theme](https://theme-next.js.org/)
- 响应式设计
- 支持目录
- 论文规范排版
- 与博客园既有特性融合

## 预览
### 截图
![](https://static01.imgkr.com/temp/8afda14ed79b4a6393fd07026520c96e.gif)
![](https://static01.imgkr.com/temp/4e9579bc084e4740873687ef112722f5.gif)

### 样例
[我的博客](https://www.cnblogs.com/makergyt)

## 使用
打开[后台](https://i.cnblogs.com/settings)
1. 选择博客皮肤为custom,勾选禁用模板css
2. 将三个文件内容分别复制入相应区域(页首、页尾、定制css)
3. 在[选项中](https://i.cnblogs.com/preference)勾选**首页仅列出标题与摘要**,控件显示勾选**公告**
4. 通过[随笔](https://i.cnblogs.com/posts)写文章，填写摘要和标签后发布。
5. (可选),由于无法在首页获取头像，如需正常显示，手动在`foot.html`头部配置`avatar`;其他可配置部分如下
  - github:右上角跳转github用户名,默认为本仓库链接
  - author:作者，默认取后台设置
  - siteTitle:网站标题默认取后台设置标题

## 开发
原则
- 能通过脚本获取的信息，如用户已经在管理后台设置的信息，就无需再次配置
- 不应该完全自定义而脱离博客园设置，比如个人信息应该以默认设置为主,尽可能作为补充而不冲突
- 专注于阅读体验而非花里胡哨
- 不必苛求完全与next原主题一致，毕竟该主题也一般需要改动，适合、可用即可。