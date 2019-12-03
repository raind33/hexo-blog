---
title: hexo与github page搭建博客
tags: 
  - hexo
  - github page
categories:
  - 其他
---
#### 安装
``` bash
npm i hexo-cli -g
hexo init blog
cd blog
npm install
hexo server
```
#### 发布hexo到github page
```
npm i hexo-deployer-git -S

然后在_config.yml文件最下面找到有deploy的地方，粘贴如下：
deploy:
  type: git
  repo: git@github.com:raind33/raind33.github.io.git
  branch: master
  name: raind33
  email: 2331336537@qq.com

hexo g     // 产生静态文件

hexo d  // 把我们的hexo部署到远程的github上去, 运行完成后就可以在github中的仓库raind33.github.io看到了

现在就可以访问https://raind33.github.io/  看到我们的blog了
```
#### 将自己的域名关联到github page上
- lz的域名是bianluoyu.xyz, 自己定义一个三级域名rain.bianluoyu.xyz, 然后github page的域名又是rand33.github.io，到自己域名提供商的控制台进行解析。添加一条主机记录为自己想要的CNAME解析，记录值为raind33.github.io
![](https://img2018.cnblogs.com/blog/1347866/201912/1347866-20191201155130700-2020091416.png)

- 然后更改github page 中的custom domain
![](https://img2018.cnblogs.com/blog/1347866/201912/1347866-20191201160623379-1621689499.png)



[更详细](https://blog.csdn.net/grave2015/article/details/79961843)