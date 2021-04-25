### 准备工作

> 安装git

....

> 安装nodejs

官网很慢，推荐下载地址：**http://nodejs.cn/download/**

> 新建工作目录

进入工作目录，安装hexo

![image-20210321100433664](.assets/image-20210321100433664.png)

初始化hexo模板

使用powershell报错

![image-20210321101202522](.assets/image-20210321101202522.png)

由于powershell默认不允许执行脚本，需要在设置中开启，在开发者选项中应用执行powershell脚本

![image-20210321101347025](.assets/image-20210321101347025.png)

再次执行hexo init

![image-20210321101122886](.assets/image-20210321101122886.png)

看到工作目录下已经生成了文件

![image-20210321101809299](.assets/image-20210321101809299.png)

### hexo主题

> 运行hexo

```shell
hexo clean # 清空已有hexo网站文件
hexo generate(or g) # 依据网页文本与新的CSS样式生成新网站文件
hexo server(or s) # 启动本地服务器，可以在localhost:4000查看网站修改效果
```

下载主题，使用next主题，在github上下载太慢，在gitee上找到有人fork的next仓库，从gitee上下载https://gitee.com/Lee-Li/hexo-theme-next

下载后，将压缩包解压到themes目录下，重命名为next

在工作目录下找到配置文件`_config.yml`，将主题更改为next

![image-20210321104242983](.assets/image-20210321104242983.png)



> 重新运行

```shell
hexo clean
hexo g
hexo s
```

> 显示效果

![image-20210321104807588](.assets/image-20210321104807588.png)

细节修改

pass



### Gitee配置

> 新建仓库

![image-20210321105524738](.assets/image-20210321105524738.png)

> 获取仓库地址

https://gitee.com/xiaopgone/xiao-pgone.git

> 修改配置文件中部署地址

修改`_config.yml`

![image-20210321105834521](.assets/image-20210321105834521.png)

> 部署博客

```shell
npm install hexo-deployer-git --save
hexo g --d  #一键部署
```
 
> 开启Page模式

![image-20210321110357493](.assets/image-20210321110357493.png)

