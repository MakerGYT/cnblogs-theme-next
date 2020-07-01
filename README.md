# <div align="center"><a title="cnblogs-theme-next" href="https://github.com/MakerGYT/cnblogs-theme-next"><img align="center" width="56" height="56" src="https://static01.imgkr.com/temp/d342ea371a6041b3bf57d1da8a79d9cc.svg"></a> e x T</div>

# [cnblogs-theme-next](https://github.com/MakerGYT/cnblogs-theme-next)
将hexo 经典的next-theme主题迁移至博客园,使用论文格式设计，专注阅读体验,极简主义设计

## 特性
- 高度还原[next-theme](https://theme-next.js.org/)
- 响应式设计
- 支持目录、阅读进度
- 论文规范排版、衬线字体
- 与博客园既有特性融合
- 代码高亮选用github风格
- 优化评论区、上下文切换

## 预览
### 截图
![](https://imgkr.cn-bj.ufileos.com/a3af8dc0-31a0-4cfb-a726-004d6fd13332.gif)
![](https://static01.imgkr.com/temp/4e9579bc084e4740873687ef112722f5.gif)

### 样例
[博客园](https://www.cnblogs.com/makergyt/p/13220468.html) <=> [hexo](https://blog.makergyt.com/)

## 选型
### 为什么选择博客园
- 经常使用搜索引擎查找某些问题会发现博客园有着良好的SEO,相比自主建站或者其他静态站点方式，省去了SEO优化和推送，便于更好的呈现和分享。
- 博客园用户大多是早期开发者，内容可信度高。由于没有其他平台类似的激励计划(比如X币)，写文章出发点很纯粹，也就不会存在用一两句话凑一篇文章、凑一篇原创（比如CSDN）,即便存在也往往就是标准答案。
- 搜索结果比较真实，不像CSDN，通过**在大量相干不相干的广告和文章链接中夹带着文章**，导致可能搜索概要中含关键词但是打开文章却毫无干系，迫使在其环境下跳来跳去增加点击率和广告曝光率，却永远找不到答案。 
- 免备案,免服务器,https,自动二级域名(xxx.cnblogs.com)
- 支持标准markdown，渲染准确，可完美迁移。图片不会像其他平台一样强制转内链，但还往往转不成功需要找原图再上传。
- **重要**:支持高度自定义，jquery于网页的意义就好比ssh的22端口于服务器的意义。不像~~CSDN~~，只能换头图和底图，还得开会员.

### 为什么选择next-theme(Pisces)
- 真正大道至简。很多主题标榜极简、专注阅读，但往往花样繁多。
- 可配置、可自定义、可扩展。

## 使用
打开[后台](https://i.cnblogs.com/settings)
1. 选择博客皮肤为custom,勾选禁用模板css,申请js权限
2. 将[三个文件](https://github.com/MakerGYT/cnblogs-theme-next/find/master)内容分别复制入相应区域(页首、页尾、定制css)
3. 在[选项中](https://i.cnblogs.com/preference)勾选**首页仅列出标题与摘要**,控件显示勾选**公告**
4. 通过[随笔](https://i.cnblogs.com/posts)写文章，填写**摘要**和**标签**后发布。
5. (可选),由于无法在首页获取头像，如需正常显示，手动在`foot.html`头部配置`avatar`(可在[头像设置](https://account.cnblogs.com/settings/account/avatar)上传后右键头像获取链接)
其他可配置部分如下
  - github:右上角跳转github用户名,默认为本仓库链接
  - author:作者，默认取后台设置
  - siteTitle:网站标题默认取后台设置
  - gallery: 要展示的相册ID(新建相册后在url中获取ID，如`1796566`)

### 配置主题色
```css
/*custom.css*/
:root {
  --primary-color:#027AFF;/* 全局主色*/
  --body-bg-color: #f5f7f9; /*页面背景色*/
	--content-bg-color: #fff; /*页面内容背景色*/
	--heading-color: rgba(0, 0, 0, 0.85); /* 标题色 */
	--text-color: #353535; /*主文本色*/
	--text-color-secondary:rgba(0, 0, 0, 0.45);/*次文本色*/
	--text-color-grey:rgba(0, 0, 0, 0.25); /*失效色，无需关注色*/
  --link-color: #555; /*链接色*/
  --code-bg-color:#f0f0f0; /*代码块背景色*/
}
```
可通过devtools调试来选择
![通过devtools调试来选择](https://static01.imgkr.com/temp/70ca34797054440395ffa98e2db628b7.gif)
## 开发
### 原则
- 能通过脚本获取的信息，如用户已经在管理后台设置的信息，就无需再次配置
- 不应该完全自定义而脱离博客园设置，比如个人信息应该以默认设置为主,尽可能作为补充而不冲突
- 专注于阅读体验而非花里胡哨
- 不必苛求完全与next原主题一致，毕竟该主题也一般需要改动，适合、可用即可。

### Todo
- 优化配置方式
- 显示代码行和复制
- 修复可能存在的时序问题
- 修复订阅(非导航区id="blog_nav_rss"无法绑定事件)