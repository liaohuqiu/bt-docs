---
layout: default
title: Bt-docs
lead: "Write beautiful and concise document in a easy way."
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


#How to use

###First you need [Jekyll][]

####A post about: [Install jekyll on CentOS](http://www.liaohuqiu.net/posts/install-jekyll/)
---

<h3 id="download">Download</h3>
<p class='lead'>You can fork the github repository, or download zip package.</p>

<div class="row">
    <div class="col-sm-6">
        <h3>Github</h3>
        <p>Fork it in Github, use the souce code in your project.</p>
        <pre><code>git clone {{ site.download.rep }}</code></pre>
        <a href="{{ site.download.rep }}" class="btn btn-lg btn-outline" role="button" >View on Github</a>
    </div>
    <div class="col-sm-6">
        <h3 id="download-zip">Zip</h3>
        <p>If you dont use git, you can download the zip package.</p>
        <a href="{{ site.download.dist }}" class="btn btn-lg btn-outline" role="button" >Download zip</a>
    </div>
</div>
###dirctory structure
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

##Configure
```yaml

```

#Multiple Languages

###Multiple Languages

**Try to use Jekyll plugins on Github Pages is a little complicated.**

###[How to use Jekyll plugins on Github Pages](http://www.liaohuqiu.net/posts/jekyll-plugins-on-github-pages/)


[Jekyll]:   http://jekyllrb.com/    "Jekyll"
