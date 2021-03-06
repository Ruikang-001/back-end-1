# 链小信——区块链可信农业融资与经营交易平台

## 项目简介
本项目产品演示：
[产品演示视频](https://clipchamp.com/watch/qfUBvSJJ4Vv)
<br/>
本项目产品介绍：
[产品介绍视频](https://clipchamp.com/watch/ht3rtAdtpcn)
<br/>
链小信是一个基于可信区块链的农业融资与经营交易平台，平台由信用评估系统与电子商务平台组成。
<br/>
[![qfLRzQ.png](https://s1.ax1x.com/2022/04/01/qfLRzQ.png)](https://lianxiaoxin.com/)
<br/>
信用评估系统为平台的核心，主要用于收集信用数据，形成初步的贷前评估并将所有材料交由投资方进行复审，与此同时在农业生产过程中不断收集信用数据，用于向投资方反馈投资对象的生产经营情况以及为日后可能的新融资积累信用数据；电子商务平台在整个平台中起到了协助农民售卖农副产品，为农民提供农用物资供应的辅助作用，同时依靠生产过程中的信用数据收集，向消费者出具农副产品质量溯源报告。
<br/>
本平台主要解决的痛点是农村贷款放贷难的问题，因而平台设计了两种贷款形式，分别为助农贷和振兴贷。
<br/>
助农贷主要用于扶农助农，提供小额贷款帮助小型农户缓解家庭困难；振兴贷主要用于支持农村土地使用权流转，扶持农业经理人或乡镇企业，促进乡村振兴。
<br/>
本平台在进行产品设计时参考了当前增强农村信贷支持的各种举措，如土地承包经营权质押贷款、房屋所有权质押贷款、预期收益权质押贷款等各种举措，参考《民法典》及相关法律解释与法律规定，在确保合规合法的条件下形成两种主要产品，两种产品的具体贷款形式可根据银行等投资方自身的产品设计进行调整。
<br/>
本平台的实际作用在于收集信用数据，在为农业贷款提供各种信贷支持的同时，降低投资方贷款的信用风险，从而打破“资方不愿贷，农户不能贷”的局面。
<br/>

## 仓库说明
本仓库库所有代码均为项目的PC端后端代码，且未完成开发。
<br/>
<br/>
项目还有以下仓库地址：
<br/>
[PC前端代码仓库](https://github.com/Feudalman/XDU)
<br/>
[小程序代码仓库](https://github.com/HongMingfeng/LianXiaoxin-Xiaochengxu)
<br/>

## 技术栈
前端：Vue+Element-ui
<br/> 
Java后端：SpringBoot + Thymeleaf + WebSocket + Spring Security + SpringData-Jpa + MySql
<br/> 

## API示例
接口基准地址：http://localhost:8888/api/private/v1/
<br/> 
服务端已开启 CORS 跨域支持
<br/> 
API V1 认证统一使用 Token 认证
<br/> 
需要授权的 API ，必须在请求头中使用 Authorization 字段提供 token 令牌
<br/> 
使用 HTTP Status Code 标识状态
<br/> 
数据返回格式统一使用 JSON
<br/> 

### 支持的请求方法
GET（SELECT）：从服务器取出资源（一项或多项）。
<br/> 
POST（CREATE）：在服务器新建一个资源。
<br/> 
PUT（UPDATE）：在服务器更新资源（客户端提供改变后的完整资源）。
<br/> 
PATCH（UPDATE）：在服务器更新资源（客户端提供改变的属性）。
<br/> 
DELETE（DELETE）：从服务器删除资源。
<br/> 
HEAD：获取资源的元数据。
<br/> 
OPTIONS：获取信息，关于资源的哪些属性是客户端可以改变的。
<br/> 

***API接口说明待完善***

## 常见问题
0、maven下载jar包长时间无反应？
```text
原因：网络原因连不上maven仓库或其他未知原因导致IDE间接性抽风，导致无法下载联网下载jar包

解决：网络原因自行解决，如果网络没问题就不要一直傻傻的等了，重启IDE，让它重新联网下载
```
1、IDE编译报错，识别不到实体类的set、get方法？
```text
原因：项目使用lombok开发，lombok会在生成class字节码文件帮我们生成set、get等方法，java文件没有set、get等方法，IDE索引不到set、get方法所以编译报错

解决：IDE安装lombok插件即可能识别到对应set、get方法，重启生效
``` 
2、数据库文件在哪？
```text
原因：没有好好看文档，建议先好好看下博客介绍，博客文末“代码开源”处已经早有说明

解决：base_admin.sql文件在resources/static/sql下面
```
3、如何启动程序？
```text
原因：对springboot项目不熟，建议先去了解一下springboot，感兴趣的可以去看我的springBoot开源项目

解决：等待IDE识别成springboot项目后，在BaseAdminApplication.java中运行main函数启动程序
```
4、测试账号/密码是多少？    PS：dev分支环境，默认关闭验证码校验
```text
账号/密码

sa/123456
```
5、如何逆向工程生成后端代码？我封装有一个工具类AutoGenerator.java用于生成单表全套后端代码
```text
首先建好数据表，在该类中配置好数据源以及项目所在路径，在main函数的tables数组指定要生成代码表，运行main函数即可生成全套后端增删改查、分页代码

一套通用common代码，每个单表去继承从而实现这套基础代码，使用AutoGenerator.java代码自动生成一套单表的基础增、删、改、查接口，大大提高开发效率，
详情见博客介绍：https://www.cnblogs.com/huanzi-qch/p/10281773.html

2021-06-24更新：我优化了AutoGenerator.java的代码，并升级了V2.0版本的代码生成器，支持使用模板文件生成代码：AutoGeneratorPlus.java
```
6、如何跳过登录，直接测试接口？
```text
场景：有的同学发现在“无需权限访问”那里配置了测试接口，但还是跳转到了登录页面，例如：/sys/sysUser/getUserById

原因：这是因为跟“权限管理”那里配置的url接口冲突了（例如：/sys/**），权限管理那里的配置优先级更高，因此还是会跳去登录页面

解决：暂时删除所有跟测试接口冲突的“权限管理”配置的url接口（例如：/sys/**，/sys/sysUser/*等）

2021-01-25更新：还是有人搞不定无需登录接口，我在项目中新增了一个OpenApi模块，以供大家参考！启动项目后，访问OpenApi测试接口：http://localhost:8888/openApi/test，即可看到效果
```
7、ORM框架不想用JPA，如何快速转MyBatis-Plus？
```text
JPA、MyBatis-Plus我都有进行封装，编码风格高度统一，都是单表继承基础通用的代码，有代码自动生成工具，本项目用的就是JPA的封装，快速切换可看之前的博客

MP：SpringBoot系列——MyBatis-Plus整合封装（https://www.cnblogs.com/huanzi-qch/p/13561164.html）
JPA：SpringBoot系列——Spring-Data-JPA（究极进化版） 自动生成单表基础增、删、改、查接口（https://www.cnblogs.com/huanzi-qch/p/10281773.html）
```
8、我想升级成前后端分离项目，麻烦吗？应当如何下手？
```text
难度肯定还是有的，如何你对这个项目比较熟悉，相信你已早有思路，如果没有可以参考下面的博客文章

springboot+spring security +oauth2.0 demo搭建（password模式）（认证授权端与资源服务端分离的形式）（https://www.cnblogs.com/hetutu-5238/p/10022963.html）
GitHub地址（https://github.com/hetutu5238/zmc_security_oauth2）

另外，我封装开源了一套极简的前后端分离项目脚手架：Fast Scaffold，包含一个portal前端、一个admin后端，可用于快速的搭建前后端分离项目进行二次开发
详情请看博客：https://www.cnblogs.com/huanzi-qch/p/13933461.html
GitHub地址：https://github.com/huanzi-qch/fast-scaffold

```
9、运行jar包，启动失败？
```text
十有八九是打的jar包有问题，参考博客重新打包，SpringBoot系列——jar包与war包的部署：https://www.cnblogs.com/huanzi-qch/p/9948060.html

发现还是有很多同学打的包不对，我已经修改了pom.xml的打包配置，直接指定了打包生成路径：package，
直接运行maven打包命令：package，就会在pom.xml的同级目录下生成package文件夹，打的jar包就在文件夹里面
另外说一下：
../package pom.xml文件的上一层目录下面的package
/package C盘下面的package文件夹
package pom.xml文件的同级目录下面的package

```
<br/>

## 作者列表
蔡子瑞@Feudalman
<br/>
刘睿康@Ruikang-001
<br/>
洪铭锋@HongMingfeng
<br/>
与作者交流请加项目负责人QQ：
<br/>

## 开源协议
<a rel="license" href="http://creativecommons.org/licenses/by-nc-nd/4.0/"><img alt="知识共享许可协议" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-nd/4.0/88x31.png" /></a><br />本作品采用<a rel="license" href="http://creativecommons.org/licenses/by-nc-nd/4.0/">知识共享署名-非商业性使用-禁止演绎 4.0 国际许可协议</a>进行许可。
