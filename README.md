# RockRock

**RockRock** is a minimalist [Hugo](https://gohugo.io/) theme used by [Chingli's personal blog](http://www.chingli.com/). It's mainly suitable for Chinese users.

**RockRock**是一个极简的[Hugo](https://gohugo.io/)主题, 它最初用于[青砾的个人博客](http://www.chingli.com/). 该主题主要适用于中文用户.

## 安装

将其拷贝到Hugo的`themes`目录下:

```
$ cd themes
$ git clone https://github.com/chingli/rockrock
```

## 配置

`config.toml`文件的配置如下:

```
baseurl = "http://www.example.com/"
languageCode = "zh-CN"
hasCJKLanguage=true
title = "Example"
theme = "rockrock"

[Params]
	duoshuoShortname = "your-duoshuo-user-name"
	subTitle = "你网站的描述"
	beian = "天ICP备88888888号"
	copyright = "2017 by You"
```

## 自定义样式

本主题的样式表是根据[Bootstrap](https://getbootstrap.com/) v4.0.0-alpha.6的[SASS](http://sass-lang.com/)文件修改而来, 为了使所生成的 .css 文件最小, 舍弃了许多未用到的内容. 你可能需要根据自己的需求, 重新对样式文件进行修改:

1. 进入`rockrock/static/css`目录, 新建`bootstrap`目录.
2. 从[Bootstrap](https://getbootstrap.com/)网站下载v4版本的Bootstrap源文件, 解压之, 将其中`scss`目录下的所有内容复制到前面的`bootstrap`目录中.
3. 在`css`目录下, 编辑`_bootstrap.scss`文件以增减Bootstrap的文档部件. 例如, 加入你的网站需要使用网格系统, 则删除`//@import "bootstrap/grid";`行前面的注释符号.
4. 若要更改Bootstrap中的相关变量, 请复制`bootstrap/_variables.scss`中相应的行, 加入`css`目录下的`_custom.scss`中进行更改.
5. 其他样式的修改请在`style.scss`文件中进行.
6. 修改完成后, 在`css`目录下运行以下命令重新生成`style.css`文件(需要已经安装好[SASS](http://sass-lang.com/)):

```
sass style.scss > style.css --style compressed
```

## License

Open sourced under the [MIT license](https://github.com/chingli/rockrock/blob/master/LICENSE.md).
