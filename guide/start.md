# 开始

## 环境要求

- system：Windows7及以上
- 安装Windows Git

## 安装

你可以从一下几个地方获取到最新的WyYBE编辑器：

- [自用网盘](https://pan.kingsr.cc/s/9jsmd70c)
- [蓝奏云](https://www.lanzous.com/b00z7ehfe)
  
>新版本（20200202）已经内置了更新通知。当有新版本时，将会弹窗通知。

下载完成后，解压至你的应用目录即可。目录结构应与下面类似：

```dos
WyYBlogEditor
 ├── _posts
 ├── public
 ├── assets
 │   ├── css
 │   ├── images
 │   ├── js
 │   ├── layer
 │   └── layui
 ├── config
 │   ├── .example.base.json
 │   ├── .example.conf.ini
 │   ├── conf.ini
 │   └── Engine.json
 ├── editor
 │   └── editor.md
 ├── template
 │   ├── editor.html
 │   ├── index copy.html
 │   ├── index.html
 │   └── test.html
 ├── themes
 │   └── default
 ├── node.dll
 ├── README.md
 └── WyYBlogEditor.exe
```

此时复制`.example.base.json`并从命名为`base.json`，其内部结构大致如下：

```json
{
    "system": {
        "title": "WyY's Blog", //博客名称
        "subtitle": "记录生活的美好", //博客副标题
        "descriptio": "", //博客简介
        "keywords": "", //博客关键字
        "author": "Kingsr", //博客作者
        "language": "zh-CN", //博客语言
        "theme": "default", //博客主题
        "url": "",//博客地址
        "deployUrl": ""//博客部署地址及Git地址
    }
}
```

将后方的注释删除，并按照自己的实际情况填写好内容。

随后打开`WyYBlogEditor.exe`即可开始你的写作！
默认的编辑器使用`Editor.md`，这是一款Markdown编辑器，使用Markdown语法。*如果你不了解什么是Markdown语法，请点击这里学习!👉[Markdown](http://www.markdown.cn/)👈*

编写完成后请按`Ctrl+S`保存，编辑器会打开保存窗口。请将文章保存至`/_posts`目录下，同时**文件名即为文章标题**

## 管理文章

### 编辑文章

在主界面上方选择`文章管理`，此时将弹出文章目录浏览，将你需要编辑的文章拖入主界面即可进行编辑。注意编辑完成后按`Ctrl+S`保存哦~

### 删除文章

在主界面上方选择`文章管理`，此时将弹出文章目录浏览，将你需要删除的文章*彻底删除* 或*移入回收站* 即可完成删除。

## 渲染即推送

编写完成并**保存**后，关闭文章编写窗口，返回主界面。此时你可以看到*站点管理* 下方的三个按钮，他们分别是`渲染并推送`、`仅渲染`、`仅推送`。

- 渲染并推送：将文章以及主题下自定义的Pages渲染至发布目录（/public），同时依据`base.json.system.deployUrl`推送至Git托管
- 仅渲染：将文章即主题下自定义的Pages渲染至发布目录（/public）
- 仅推送：将发布目录下的文章推送至Git托管

当编写完成后，根据需要点击上方的按钮即可完成渲染、推送。
>需要注意的是，请确保/config目录下的配置文件已经填写完整。否则将会出错。

## conf.ini

`conf.ini`是软件的运行配置文件，目前拥有以下配置：

```ini
[base]
ShowDOS=1
AbsoluteUrl=1
Mini=1 // 2020.02.03更新
```

- ShowDos：该选项为`1`时将显示Git运行时的DOS窗口，你可以用它查看DOS运行信息以及得到报错
- AbsoluteUrl：该选项为`1`时将会渲染主题中`{$assetsPath}`为`base.json.system.url`即转为绝对地址
- Mini：该选项将在打开时提供置托盘选项，置托盘后快捷键`Alt+B`将快速呼出界面

你可以视情况而定，打开(=1)或关闭(=Anything)上方选项。
