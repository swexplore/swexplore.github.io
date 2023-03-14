---
title: "Hugo_basic_usage"
date: 2022-11-24 11:46:36
draft: True
---

# Hugo 小白使用手册

---

## Install hugo

- windows
  1. download the hugo package
  [hugo_sites](https://github.com/gohugoio/hugo/releases)
  2. Decompress and compile the env
  3. check `hugo version`

---

## 创建个人blog

1. windows 打开 powershell
2. 定位到 ./hugo/Sites
3. 创建blog

```
    hugo new site myblog
    cd myblog
    pwd
```

4. 下载主题

- [hugo_themes](https://themes.gohugo.io)

```
    git clone https://github.com/vaga/hugo-theme-m10c.git themes/m10c
    ls -l
    cd themes
    cd ..
    pwd
```

5. 启动命令
`hugo server -l m10c --buildDrafts`

6. 访问blog地址

7. 新建一个文章

```
hugo new post/blog.md
ls -l
cd content/post
ls
```

8. 写文章

- use vscode
- markdown style

9. 预览blog

- 进入myblog根目录
- 输入命令
  `hugo server -t m10c --buildDrafts`
- 查看本地blog

10. 部署到远端

- 需要安装GIT
- GitHub --create new repo[xxx(yourname).github.io]

```
hugo --theme=m10c --baseUrl="https://xxx.github.io/" --buildDrafts
pwd   #生成public文件夹
cd public
ls -l
cd posts
ls   #发现它会自动生成html格式
cd blog
cd ../..
ls
```

- 上传blog

```
cd public
ls -l
git init
git add .
git commit -m "create blog for you name"
pwd
git remote add origin git@github.com:xxx/xxx.github.io.git   ##添加远程地址 xxx -your name
git push -u origin master
# 输入你的用户名和密码
```

---

## ***Finished all congrates!!***
