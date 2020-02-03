# 部署

详解讲解如何部署渲染好的Blog至Github或码云。

## 创建一个新的Github仓库

登录[Github](https://github.com)然后创建一个新的仓库。同时请将名字设置为`username.github.io`。如图，如果你的git用户名为`wyyy`，则将仓库名称设置为`wyyy.github.io`。其余选项视情况编写，一般不写，点击创建。
![1.png](https://i.loli.net/2020/02/03/H2YDVCUWTia1nEK.png)

## 编辑deployUrl

创建成功后，你会看到以下界面。将仓库地址复制下来（点击圆圈的复制按钮即可）。
![2.png](https://i.loli.net/2020/02/03/LKFpiXxtQwgmHoz.png)
随后打开`/config/base.json`。将`deployUrl`填写为刚才复制的地址，编辑完成后保存。

```json
{
    "system": {
        "title": "WyY's Blog",
        "subtitle": "记录生活的美好",
        "descriptio": "",
        "keywords": "",
        "author": "Kingsr",
        "language": "zh-CN",
        "theme": "default",
        "url": "",
        "deployUrl": "https://github.com/wyml/wyyy.github.io.git" // 将地址复制到此
    }
}
```

## 推送

打开WyYBE，点击`站点管理>渲染`随后等待提示渲染并推送成功即可。

## 绑定自定义域名

返回仓库，点击右上方的`setting`进入仓库编辑。下滑找到`Github Pages`，在`Custom domain`编辑框中填写你要绑定的域名，点击`save`保存。
![3.png](https://i.loli.net/2020/02/03/38rSic7AzDV5LIW.png)
打开域名解析管理，新建一个CNAME解析，解析目标为`username.github.io`即你的仓库名称即可！

## 码云

推送至码云同理，但由于国内情况，码云Pages服务无法自动部署且免费版本无法绑定自定义域名，因此推荐Github。
