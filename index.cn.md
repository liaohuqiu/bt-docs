---
layout: default
title: Bt-docs
description:        "bootstrap 模板"
keywords:           "bootstrap 模板"
lead:               "轻松写出简洁好看的文档"
---

#主要功能
---
#### 仿[Bootstrap模板](http://getbootstrap.com/getting-started/)的一个网站框架，用来快速写一个UI好看的文档。

* 使用[Jekyll][], 支持`markdown`
* 使用简单
* 基于Bootstrap
* 支持多语言

#示例网站
---

####[http://cube-sdk.liaohuqiu.net/](http://cube-sdk.liaohuqiu.net/)
####[http://jekyll-langs.liaohuqiu.net/](http://jekyll-langs.liaohuqiu.net/)

#Jekyll

网站内容使用[Jekyll][] 生成，所以你需要先安装好[Jekyll][].

####一篇关于安装[Jekyll][]的文章: [Install jekyll on CentOS](http://www.liaohuqiu.net/cn/posts/install-jekyll/)
---

#如何使用
---
<p class='lead'>你可以在Github上fork这个项目，或者直接下载源码包。</p>

<div class="row">
    <div class="col-sm-6">
        <h3>Github</h3>
        <p>Fork 这个项目，然后加入到你的项目中。</p>
{% highlight bash %}
git checkout -b docs
git merge {{ site.download.rep }}
git submodule upate
git commit
git push origin docs
{% endhighlight %}
        <a href="{{ site.download.rep }}" class="btn btn-lg btn-outline" role="button" >Github</a>
    </div>
    <div class="col-sm-6">
        <h3 id="download-zip">直接复制文件</h3>
        <p>不使用Git的话，直接下载源码包，解压后放到项目中。</p>
        <a href="{{ site.download.dist }}" class="btn btn-lg btn-outline" role="button" >下载源码包</a>
    </div>
</div>

---

###目录结构
```bash
bt-docs/
 ├── assets         # js / css / image
 ├── _config.yml    # Jekyll 的配置文件
 ├── dist           # js / css of bootstrap
 ├── _includes      # templete parts
 ├── _layouts
 ├── _plugins
 ├── README.md
 └── _site          # 若非指定，生成的内容默认在这个目录
```

###配置

*   `_config.yml`

```yaml

# 网站信息
info:
  site_name:        Bt-docs

meta:
  description:      "默认的description"
  keywords:         "默认keywords"
  author:           "作者信息"

# 多语言支持
language_default:   'en'

languages:          ["en", "cn"]

# 左侧导航
left_nav:
  en:
    title:          The title
    path:           /
    items:
      - path:       /page1
        title:      "Another page"
      - path:       /page2
        title:      "Yet another page"
  cn:
    title:          "网站标题"
    path:           /cn
    items:
      - path:       /cn/page1
        title:      "页面1"
      - path:       /cn/page2
        title:      "页面2"

# 右侧导航
right_nav:
  - title:          English Version
    url:            /
  - title:          中文版文档
    url:            /cn
  - title:          Fork on Github
    url:            https://github.com/liaohuqiu/bt-docs

# Google analytics的统计信息，请修改账号，不用请删除
# 其他统计器请自行修改 _includes/header.html
analytics:
  google:
    account:         UA-43024238-5

```

###网站生成和部署

---

如果你使用git的话，生成之前切记 `git submodule update`。

如果没有在`_config.yml`中配置，网站内容默认生成到: `_site`。

你可以使用jekyll在本地调试: `jekyll server -w`。


###Github Pages需要注意的问题

---

多语言支持是用Jekyll的一个多语言插件实现的: **[Jekyll Multiple Languages Plugin][Jekyll Multiple Languages Plugin]**，但是Github Pages 目前不允许插件运行。

如果你网站要放到Github上，这里有一个解决方案：: **[托管在Github上的网站如何使用插件](http://www.liaohuqiu.net/cn/posts/jekyll-plugins-on-github-pages/)**

[Jekyll]:   http://jekyllrb.com/    "Jekyll"
[Jekyll Multiple Languages Plugin]: http://jekyll-langs.liaohuqiu.net/ "Jekyll Multiple Languages Plugin"
