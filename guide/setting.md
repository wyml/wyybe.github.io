# 内置主题的修改

## 主题目录结构

内置主题目录结构如下：

```tree
default
 ├── assets
 │   ├── css
 │   ├── fonts
 │   ├── icons
 │   ├── images
 │   └── js
 ├── layout
 │   └── public.mtpl
 ├── pages
 │   ├── about.mtpl
 │   └── links.mtpl
 ├── index.mtpl
 ├── post.mtpl
 ├── timeline.mtpl
 └── _conf.json
 ```

- assets：静态资源目录，存放各种静态资源
- layout：布局文件目录，因为布局简单，仅使用一个`public.mtpl`就完成了所有页面的布局
- pages：自定义页面目录，目前有links友链、about关于两个页面文件
- index.mtpl：首页模板文件，将渲染为博客首页
- post.mtpl：文章模板文件，编写的文章将依据此文件渲染为文章页面
- timeline.mtpl：时间线模板文件，目前未完善
- _conf.json：主题配置文件，不同主题的配置以及作者信息将在此显示

## _conf.json

大部分的主题配置都在这里完成。_conf.json文件内容如下：

```json
{
    "conf": {
        "author": "Kingsr",
        "name": "MlT"
    },
    "name": "藍某人",
    "title": "WyY's Blog",
    "subtitle": "记录生活的美好,一起发现创造",
    "avatar": "https://q1.qlogo.cn/g?b=qq&nk=1143524493&s=5",
    "mail": "i@kingsr.cc",
    "icp": "桂ICP备16007573号-1",
    "gov": "桂公网安备45012602000065号",
    "govUrl": "http://www.beian.gov.cn/portal/registerSystemInfo?recordcode=45012602000065",
    "pages": [{
        "tpl": "pages/links",
        "target": "pages/links"
    }, {
        "tpl": "pages/about",
        "target": "pages/about"
    }],
    "links": [{
        "title": "freejishu的美丽世界",
        "url": "https://www.freejishu.com",
        "description": "A New World",
        "avatar": "https://cn-south-227-storage-freejishu-21499426.oss.dogecdn.com/g.jpg"
    }],
    "siderbar":[
        {
            "title":"Links",
            "icon":"link",
            "url":"/pages/links.html"
        },{
            "title":"About",
            "icon":"info",
            "url":"/pages/about.html"
        }
    ]
}
```

### conf

该项下，为主题的作者信息以及主题名称，此项为了作者的权益，请不要随意修改！

### name、title、subtitle、avatar、mail、icp、gov、govUrl

- name：侧边栏及文章等处的名称
- title：博客首页标题
- subtitile：博客首页副标题
- avatar：侧边栏、文章头像地址
- mail：侧边栏邮箱地址
- icp：工信部备案号
- gov：公安网备案号
- govUrl：公安网备案号地址

### pages

该选择为页面渲染选项。软件将根据该项渲染page文件及地址。
其中：

- tpl：模板地址，根目录为主题根目录
- target：渲染路径，根目录为/pulic/

系统将根据两个选项渲染。

### siderbar

该选项为侧边栏渲染，将依据该选项渲染侧边栏，可以根据添加，其中：

- title：侧边栏标题
- icon：侧边栏图标，图标列表👉[material_icon](https://www.mdui.org/docs/material_icon)👈
- url：链接地址，注意加上`.html`

>注意，目前不支持嵌套列表渲染。
