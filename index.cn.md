---
layout: default
title: Bt-docs
description:        "bootstrap 模板"
keywords:           "bootstrap 模板"
lead:               "轻松写出简洁好看的文档"
---

#What is it?
---
#### Using [Bootstrap document Template](http://getbootstrap.com/getting-started/) to write document for your project.

* Based on [Jekyll][]
* Bootstrap document style
* Very easy to use
* Write in `markdown`
* Bootstrap
* Multiple languages

#Examples
---

####[http://cube-sdk.liaohuqiu.net/](http://cube-sdk.liaohuqiu.net/)
####[http://jekyll-langs.liaohuqiu.net/](http://jekyll-langs.liaohuqiu.net/)

#Jekyll

First we need use [Jekyll][] to build the content.

####A post about: [Install jekyll on CentOS](http://www.liaohuqiu.net/posts/install-jekyll/)
---

#How to use
---
<p class='lead'>You can fork the github repository, or download zip package.</p>

<div class="row">
    <div class="col-sm-6">
        <h3>Github</h3>
        <p>Fork it in Github, use the souce code in your project.</p>
{% highlight bash %}
git checkout -b docs
git merge {{ site.download.rep }}
git submodule upate
git commit
git push origin docs
{% endhighlight %}
        <a href="{{ site.download.rep }}" class="btn btn-lg btn-outline" role="button" >View on Github</a>
    </div>
    <div class="col-sm-6">
        <h3 id="download-zip">Copy file</h3>
        <p>If you dont use git, you can download the zip package.</p>
        <p>The copy the files into your document directory.</p>
        <a href="{{ site.download.dist }}" class="btn btn-lg btn-outline" role="button" >Download zip</a>
    </div>
</div>

---

###Directory structure
```bash
bt-docs/
 ├── assets         # js / css / image
 ├── _config.yml    # configure for jekyll
 ├── dist           # js / css of bootstrap
 ├── _includes      # templete parts
 ├── _layouts
 ├── _plugins
 ├── README.md
 └── _site          # the site content will be build to 
```

###Configure

*   `_config.yml`

```yaml

# site information
info:
  site_name:        Bt-docs

meta:
  description:      "The default description for this site"
  keywords:         "Default keywords for this site"
  author:           "Author information"

# multiple language
language_default:   'en'

languages:          ["en", "cn"]

# left navigation
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

# right navigation
right_nav:
  - title:          English Version
    url:            /
  - title:          中文版文档
    url:            /cn
  - title:          Fork on Github
    url:            https://github.com/liaohuqiu/bt-docs

# analytics account information, remember to change this.
analytics:
  google:
    account:         UA-43024238-3

```

###Build & Deploy

If you are using git, please remember `git submodule update` before build.

The site content will be generated into the destination directory, for example: `_site`

You can publish the content.

###Github Pages Issue

**Multiple Languages is sported by [Jekyll Multiple Languages Plugin][Jekyll Multiple Languages Plugin]**, and Github page runs in a `safe mode` in which most of the plugins can not run.

Here is a solution: **[How to use Jekyll plugins on Github Pages](http://www.liaohuqiu.net/posts/jekyll-plugins-on-github-pages/)**

[Jekyll]:   http://jekyllrb.com/    "Jekyll"
[Jekyll Multiple Languages Plugin]: http://jekyll-langs.liaohuqiu.net/ "Jekyll Multiple Languages Plugin"
