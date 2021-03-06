# Landscape plus

针对中国大陆的hexo用户，优化hexo官方主题landscape。支持hexo 3.x 和 hexo 2.x. 欢迎大家参与进来. [演示](https://levy9527.github.io)

## 主题特色

+ **移除外国类库**，确保所有资源不用翻墙每次能加载成功
+ **新增swiftype搜索模块**，需要配置自己的swiftype_key,[参考教程](http://theme-next.iissnan.com/third-party-services.html#swfitype)。
+ **新增百度统计模块**，需要配置自己的baidu_analytics,[参考教程](http://theme-next.iissnan.com/third-party-services.html#analytics-baidu)。
+ **主题配置项优化**，你可以将主题配置项放在站点的`_config.yml`中，避免主题更新造成的冲突。
+ **新增多说评论模块**，开启方法看下面的[常见问题](#常见问题)。
+ **新增百度分享模块**，已默认开启。
+ **新增友情链接模块**，已默认开启，修改方法看下面的[常见问题](#常见问题)。
+ **新增mathjax模块**，即latex数学公式的支持，默认关闭。（感谢 @Svtter 的[pull request](https://github.com/xiangming/landscape-plus/pull/35)）
+ **新增多语言支持**，支持英文、中文简体和中文繁体。
+ **新增IE8支持**。
+ **外观美化**，美化了部分外观样式。
+ **使用Monokai代码高亮配色**，最流行、最优雅的代码高亮配色方案。

主题还在扩展中，欢迎各种**Pull Request**。

## TODO 
- 取消图片border
- 归案的样式想变成时间线(timeline)
- 换一个搜索方式, swiftype免费试用结束后, 就不能搜索到新文章了


## 文档目录

+ [安装](#install)
+ [启用](#enable)
+ [配置](#config)
+ [更新](#update)
+ [常见问题](#troubleshoots)
+ [更新日志](#logs)
+ [网站列表](#sites)
+ [贡献者们](#contribute)

## <a name='install'>安装</a>

```bash
git clone https://github.com/levy9527/landscape-plus.git
```

## <a name='enable'>启用</a>

修改hexo的配置文件`_config.yml`，把`theme`的值设置为`landscape-plus`

```yml
# Extensions
## Plugins: http://hexo.io/plugins/
## Themes: http://hexo.io/themes/
theme: landscape-plus
```

## <a name='config'>配置</a>

主题的默认配置文件说明`landscape-plus\_config.yml`：
+ `mathjax` - 是否开启latex数学公式
+ `links` - 友情链接
+ `duoshuo_shortname` - 多说评论id
+ `baidushare` - 是否开启百度分享

**建议！** `mathjax`、`links`、`duoshuo_shortname`、`baidushare`配置项也支持放在站点的`_config.yml`中，并且我们建议你这样做。

> 在归档页面显示所有文章, 需要修改主配置文件:

```yml
archive_generator:
  per_page: 0
	yearly: false
	monthly: false
	daily: false
```
如果不生效, 可能Hexo版本没有自带`hexo-generator-archive`插件, 则自己手动安装一下即可:

```sh
npm i hexo-generator-archive
```

## <a name='update'>更新</a>

```bash
cd themes/landscape-plus
git pull
```

**提示** 如果更新发生错误，你可以删除整个主题文件夹，然后重新执行[安装](#install)操作。

## <a name='troubleshoots'>常见问题</a>

**问**：**怎么使用landscape plus主题？**
> 按照上方的步骤进行`安装`、`启用`。

**问**：如何开启多说评论模块？
> 在站点的`_config.yml`中，增加`duoshuo_shortname: xxx`配置项，xxx是你的多说id。

**问**：如何关闭百度分享模块？
> 删掉`themes/landscape-plus\_config.yml`中的`baidushare`配置项。

**问**：如何使用RSS分享功能？
> 请参考这条[issue](https://github.com/xiangming/landscape-plus/issues/31)进行配置。

**问**：怎么切换语言版本？
> 在站点的配置文件`_config.yml`，修改`language:`配置项，zh-CN为中文简体，zh-TW为中文繁体，default为英文。

**问**：怎么提建议？
> 主题还在扩展中, 本人在写博客的过程中, 发现主题可优化的地方还有很多, 因此本项目会持续更新, 欢迎大家Pull Request, 我都会响应的(至少2016年是这样).

## <a name='logs'>更新日志</a>

## levy fork 的版本
> [版本号的定义](http://taobaofed.org/blog/2016/08/04/instructions-of-semver/)

### v1.4.0
- 取消右上角的搜索icon
- 可配置fork-me-on-github, 在右上角显示
- 参考别人的博客, 修改文章hover样式, 文章字体
- 更新友情链接

### v1.3.4
- 取消最近文章, 更新友情链接
- fontawesome字体从本地获取, 不再担心有时加载不出来了
- 去掉一些不必要的链接
- fix moble-nav 未多语言化的bug

### v1.3.3
- 字体默认颜色#333
- 上一页/下一页去掉数字, 只显示翻页按钮
- 超链接的风格统一为蓝色, 页面整体更和谐了

### v1.3.2
- 恢复阅读全文的显示
- 全面支持多语言切换(之前有些地方不能切换)

### v1.3.1
- fix https协议下获取不了fontawesome.font的bug

### v1.3.0
- 修改布局上的感觉"反人类的设计", 包括"下一篇"与"上一篇"的位置, 归档文章的排列顺序
- 修改链接的样式, 参考github
- 修改字体样式, 参考github
- 使用bootcdn获取jquery


### v1.2.0
+ 修改#logo的文字，通过主题配置文件banner字段配置
+ 添加百度统计

### v1.1.0
+ 恢复原主题的大图(`themes/landscape-plus/source/css/_partial/header.styl`)
+ 取消logo的鲜红色背景(同上)
+ 使用站点的favicon.ico,即项目根目录source/favicon.ico文件(`themes/landscape-plus/layout/_partial/head.ejs`)
+ 增加swiftype搜索(`themes/landscape-plus/layout/_partial/after-footer.ejs`)

## 原版本
### v1.0.5
+ 主题配置项优化, refs #17
+ 百度分享样式调整，refs #45, refs #61
+ 更新主题说明README.md

### v1.0.4
+ 增加返回顶部功能
+ 修改渲染方式，现在默认page布局下仅渲染 .md 文件格式，其他格式一律只做复制。（方便添加静态页面，原本需要在每个文件开头添加 **layout: false**）
+ 添加**mathjax**的模块开关,不需要的可以自己关闭。

特别感谢来自 @myqianlan 的[pull request](https://github.com/xiangming/landscape-plus/pull/39) 和 @bearpaw 的[pull request](https://github.com/xiangming/landscape-plus/pull/53)。

### v1.0.3
+ 增加对 **IE8** 的支持
+ 集成 **mathjax** ，即latex数学公式的支持。（感谢 @Svtter 的[pull request](https://github.com/xiangming/landscape-plus/pull/35)）

### v1.0.2
+ 修改: 优化Generate速度，refs #13

### v1.0.1
+ 新增: 百度分享模块

### v1.0.0
+ 修改：根据国情，去掉Google的库，改用cloudflare的cdn
+ 新增：语言包
+ 修改：代码高亮配色修改为`Monokai`
+ 新增：友情链接
+ 修改：隐藏顶部大图
+ 修改：主题配色和部分markdown样式
+ 新增：多说评论模块

## <a name='contribute'>贡献者们</a>

+ [xiangming](https://github.com/xiangming)
+ [myqianlan](https://github.com/myqianlan)
+ [HADB](https://github.com/HADB)
+ [Svtter](https://github.com/Svtter)
+ [bearpaw](https://github.com/bearpaw)

## <a name='sites'>网站列表</a>

如果你的网站正在使用**landscape-plus**主题，你可以将网址添加到[wiki的网站列表](https://github.com/xiangming/landscape-plus/wiki)。
