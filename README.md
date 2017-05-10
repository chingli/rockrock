# RockRock

**RockRock** is a minimalist [Hugo](https://gohugo.io/) theme used by [Chingli's personal blog](http://www.chingli.com/). It's mainly suitable for Chinese users.

**RockRock** 是一个极简的 [Hugo](https://gohugo.io/) 主题, 它最初用于[青砾的个人博客](http://www.chingli.com/). 该主题主要适用于中文用户.

## 安装

将其拷贝到Hugo的`themes`目录下:

```
$ cd themes
$ git clone https://github.com/chingli/rockrock
```

## 配置

`config.toml` 文件的配置如下:

```
baseurl = "http://www.example.com/"
languageCode = "zh-CN"
hasCJKLanguage=true
title = "Example"
theme = "rockrock"

[Params]
	subTitle = "你网站的描述"
	beian = "天ICP备88888888号"
	copyright = "2017 by You"
```

## 自定义样式

本主题的样式表是根据 [Bootstrap](https://getbootstrap.com/) v4.0.0-alpha.6 的 [SASS](http://sass-lang.com/) 文件修改而来, 为了使所生成的 .css 文件最小, 舍弃了许多未用到的内容. 你可能需要根据自己的需求, 重新对样式文件进行修改:

1. 进入 `rockrock/static/css` 目录, 新建 `bootstrap` 目录.
2. 从 [Bootstrap](https://getbootstrap.com/) 网站下载v4版本的 Bootstrap 源文件, 解压之, 将其中 `scss` 目录下的所有内容复制到前面的 `bootstrap` 目录中.
3. 在 `css` 目录下, 编辑 `_bootstrap.scss` 文件以增减 Bootstrap 的文档部件. 例如, 加入你的网站需要使用网格系统, 则删除 `//@import "bootstrap/grid";` 行前面的注释符号.
4. 若要更改 Bootstrap 中的相关变量, 请复制 `bootstrap/_variables.scss` 中相应的行, 加入 `css` 目录下的 `_custom.scss` 中进行更改.
5. 其他样式的修改请在 `style.scss` 文件中进行.
6. 修改完成后, 在 `css` 目录下运行以下命令重新生成 `style.css` 文件(需要已经安装好 [SASS](http://sass-lang.com/)):

```
sass style.scss > style.css --style compressed
```

## 其他

因为多说即将关闭, 本主题将不再集成多说. 我个人的博客将在从多说迁移到其他评论系统导入数据时总遇到一些问题, 因此目前本主题暂时没有集成评论系统. 将来我考虑把评论系统改为 [Commento](https://github.com/adtac/commento), 等我把自己的评论数据导入到 Commento, 并修改其评论主题后, 会将 Commento 集成到此主题中.

如果你想在博客中集成其他评论系统, 其仿照 `layouts/partials/duoshuo.html`文件和`layouts/_default/single.html` 文件的注释部分进行修改添加.

我自己的博客中 `content/mining` 目录下的文章是支持 [MathJax](https://www.mathjax.org/) 数学公式的, 而其他目录下的文章不支持. 因此我专门建立了`layouts/mining/single.html` 文件以适应这种需求. 如果你不需要 MathJax 支持, 就不必理会该文件. 如果你的所有文章都需要 MathJax 支持, 则请用 `layouts/mining/single.html` 替换 `layouts/_default/single.html`文件.

## License

Open sourced under the [MIT license](https://github.com/chingli/rockrock/blob/master/LICENSE.md).
