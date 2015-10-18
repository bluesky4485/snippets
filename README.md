## 补充
如果要自己搭建这个应用，并且也想贡献代码给作者的话，建议clone下来后先新建一个分支**git chechout -b pull**，然后在snippets文件夹中增加自己的内容。然后提交代码到这个分支中。然后再切换回gh-pages，进行自行搭建的配置相关的修改。

> 自己搭建的话，其实就修改3个地方就可以了，
>
* CNAME文件修改，将域名修改为自己的二级域名。
* 修改_config.yml，将github相关地址都变成自己的github地址，其他的还是保留原作者的链接，修改github地址主要是为了让自己能直接在snippet上面点编辑后直接跳转到github的repo进行编辑。
* 修改main.js文件，其中有百度统计和多说的帐号需要修改下，百度统计不改也罢，多说可以考虑自己修改下。然后评论就比较自由了，与原作者的不相关了，当然也可以不改。

前面2项改了就算是自己搭建完成了。

在切换到gh-pages分支后再**git merge pull**操作两个分支的合并去更新主分支的内容。

想要贡献代码的话也可以将pull分支中的代码提pull request到fork的上级（或原作者）的gh-pages分支，这样贡献代码的话就不会影响到自己搭建。

## Snippets

很多语言、很多配置、很多语法，太多太多东西，不能单靠大脑来记忆。[本应用](http://snippets.barretlee.com) 收集了一些平时常用以及网上寻觅的代码片段，并且在页面中提供了搜索功能，可以快速找到我们平时记下的代码，这里保存的部分片段还是十分有价值的。

本应用对应的网址为: <http://snippets.barretlee.com>

![snippet](http://www.barretlee.com/blogimgs/2015/09/20150902_2774c376.jpg)

### 贡献代码

如果你希望帮助丰富代码片段库，可以操作如下流程：

- fork [barretlee/snippets](https://github.com/barretlee/snippets.git) 仓库
- 然后执行如下命令
```
git clone https://github.com/{YOUR_GITHUB_NAME}/snippets.git
cd snippets
git chechout -b gh-pages
cd snippets
# 选择你想提交的文件类型，比如 html
cd html
touch {YOUR_CONTRIBUTE_FILE_NAME}.snippet
```
其中，`{YOUR_CONTRIBUTE_FILE_NAME}.snippet` 的格式为：
```
---
title: {NAME}
---

{CONTENT}
```
可以使用 markdown 语法。
- 提交代码
```
git add --all
git commit -m "add file html/{YOUR_CONTRIBUTE_FILE_NAME}.snippet"
git push origin gh-pages
```
- 然后在你的 [PR](https://github.com/{YOUR_GITHUB_NAME}/snippets/pulls) 页面提交一个 PR 到 `barretlee/snippets` 的仓库

### 关于

![小胡子哥](http://www.barretlee.com/avatar150.png)

[小胡子哥的联系方式](http://www.barretlee.com/about/)

### LISCENSE

MIT LISCENSE.

自由分享使用，注意保留署名。