### 项目说明 ###
* 利用github action实现定时自动运行api调用，保持E5开发活跃。 
* 免费，不需要额外设备/服务器，部署完不用管啦。 

### 特别说明/Thanks ###
* 原教程博主-黑幕（酷安id-Paran）：https://blog.432100.xyz/index.php/archives/50/ 已失效
* 原项目地址：https://github.com/wangziyingwen/Autoapi-test 已失效，本项目系从https://github.com/1634222787/Autoapi-test 复制而来，感谢各位。本文部分配图就是从前面各位项目中复制而来，读者自行把里面的用户名换成我的或者你的就可以正常阅读了
* 本项目地址：https://github.com/shencore/Autoapi-test

--------------------------------------------------------------

### 步骤 ###
* 登录/注册一个github账号，新建一个repository/项目 权限选择Public（我实测发现Private库会在后面运行时报错，如果有读者发现设置Private不会报错的办法，请给我提issue）
  ![image](https://github.com/shencore/Autoapi-test/blob/master/images/新建仓库.png)
  
* 注册E5账号，这部分教程很多，不再赘述。
* 后续请参考https://www.daniao.org/9652.html github actions自动调用api – 实现Microsoft 365 E5玄学订阅 ，目前链接可用，我存了一个备份，如果链接失效时请给我提issue，我会在这里公开密码。
* 点击右上角fork本项目的代码到到你自己的仓库（相当于新建repository并复制本项目代码）

  ![image](https://github.com/shencore/Autoapi-test/blob/master/images/fork.png)
  
  然后修改文件 .github\workflows\autoapi.yml 中的代码地址为你自己的地址
  
  ![image](https://github.com/shencore/Autoapi-test/blob/master/images/修改地方.png)
  
* 搞定，接下来就不用管了。我设定的每12小时自动运行一次，每次调用3轮（点击右上角星星/star也可以立马调用一次），你们自行斟酌修改（我也不知道活跃要调用多少、多久）：

   · 定时自动启动修改地方：（在autoapi.yml里，自行百度cron定时任务格式）
   
   ![image](https://github.com/shencore/Autoapi-test/blob/master/images/定时.png)
   
   · 每次轮数修改地方：（在1.py最后面）
   
   ![image](https://github.com/shencore/Autoapi-test/blob/master/images/次数.png)
   
   · 点击上面的Action就能看到每次的运行日志（都看下，api有没有调用到位，我就少了一个3，不管了）
   
   ![image](https://github.com/shencore/Autoapi-test/blob/master/images/日志.png)

------------------------------------------------------------

### GithubAction介绍 ###
提供的虚拟环境：

· 2-core CPU
· 7 GB RAM 内存
· 14 GB SSD 硬盘空间

使用限制：
* 每个仓库只能同时支持20个 workflow 并行。
* 每小时可以调用1000次 GitHub API 。
* 每个 job 最多可以执行6个小时。
* 免费版的用户最大支持20个 job 并发执行，macOS 最大只支持5个。
* 私有仓库每月累计使用时间为2000分钟，超过后$ 0.008/分钟，公共仓库则无限制。

（我们这里用的公共仓库，按理，你们可以设定无限循环调用，然后6小时启动一次，保证24小时全天候调用）

### 最后 ### 本段来自原作者
  教程很直白了，应该都会弄吧。有空更新一下怎样网页获取refresh_token（不再需要rclone？）！所以不用电脑应该可以都搞定！

  我是代码小白，我实在不会把两个项目合并啊，只能分开弄两个项目，一个原代码，一个action流程，请各位多多包涵。有没有大佬能修改一下代码呀，十分欢迎！
  
  这个项目都是我根据以往看过的代码整合的，ORZ。
  
  有修改建议可以发邮件给我:
  wz.lxh@outlook.com
  
  基安id-卷腿毛菌
