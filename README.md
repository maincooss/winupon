**应用与大数据的单点登录配置**

# **一、oa7数字校园模块对接到大数据**

## **1.1、在大数据开发者平台添加数字校园应用**

以oa7地址【http://192.168.0.1:8081/desktop/index/page】为例

| Web校验地址 | http://192.168.0.1:8081/homepage/openapi/uc/verifyUcLogin  |
| ----------- | ---------------------------------------------------------- |
| Web首页地址 | http://192.168.0.1:8081/desktop/index/page                 |
| Web退出地址 | http://192.168.0.1:8081/homepage/openapi/uc/verifyUcLogout |

## **1.2、数字校园模块参数**

sso.uc.client.id #应用ID,在开发者平台里面查看

sso.uc.secret #KEY, 在开发者平台里面查看

sso.uc.homepage #大数据桌面页地址（即大数据my平台地址）

sso.uc.page.of.logout #大数据桌面的退出接口，按F12键可以查询

## **1.3、修改配置**

```bash
Apache
sso.uc=true  #开启与大用户中心的对接
sso.uc.client.id=8a809ea07b0b10a9017b2a092dd6002f
sso.uc.secret=1993637415933180681161992647748907643884440751757076680801510659
sso.uc.homepage=http://192.168.0.1:9093/
sso.uc.page.of.logout=http://192.168.0.1:9093/api/idaas/logout/
```

## **1.4、更新配置**

请上述配置格式，更新数字校园7.0包下的conf.properties配置文件

# **二、人人通模块对接到大数据**

## **2.1、在大数据开发者平台添加人人通应用**

以人人通地址【[http://192.168.0.1:8081](http://192.168.0.1:8081/)/spaceIndex.htm】为例

| Web校验地址 | [http://192.168.0.1:8081](http://192.168.0.1:8081/)/passport/ucVerifyLogin.htm |
| ----------- | ------------------------------------------------------------ |
| Web首页地址 | [http://192.168.0.1:8081](http://192.168.0.1:8081/)/spaceIndex.htm |
| Web退出地址 | [http://192.168.0.1:8081](http://192.168.0.1:8081/)/passport/ucLogout.htm |

## **2.2人人通cms后台配置参数:****cms.****&****url**

# ![](https://raw.githubusercontent.com/maincooss/boomb/main/Clip_20220613_193809.png)

# **三、资源库对接到大数据******

## **3.1、在大数据开发者平台添加资源库应用**

以资源库地址【[http://192.168.01:8081/countyIndex.htm](http://192.168.0.1:8081/countyIndex.htm)】为例

| Web校验地址 | http://192.168.0.1:8081/opVerify.htm                         |
| ----------- | ------------------------------------------------------------ |
| Web首页地址 | [http://192.168.01:8081/countyIndex.htm](http://192.168.0.1:8081/countyIndex.htm) |
| Web退出地址 | http://192.168.0.1:8081/oplogout.htm                         |

## **3.2、资源库support后台配置参数：****url****&****/support/**

资源库后台修改共七处

| system.res.login.url.2.opcenter | 1表示开启用户中心登录               |
| ------------------------------- | ----------------------------------- |
| jwt.parse.url                   | 大数据开放平台地址 （open地址）     |
| system.res.opverify             | 资源库地址                          |
| op.login.url                    | 大数据桌面地址（my地址）            |
| op.login.appid                  | 资源库应用ID                        |
| service.opcenter.verifykey      | 大数据开放平台个人中心中的SecretKey |
| ticket.key                      | 大数据开放平台个人中心中的ticketKey |

# <img src="https://raw.githubusercontent.com/maincooss/boomb/main/Clip_20220613_194502.png" style="zoom: 80%;" />

# **四、评审评定对接到大数据**

## **4.1、在大数据开发者平台添加评审评定应用**

以评审评定地址【[http://192.168.01:8081/index.htm](http://192.168.0.1:8081/index.htm)】为例

| Web校验地址 | [http://192.168.0.1:8081](http://192.168.0.1:8081/)/opVerify.htm |
| ----------- | ------------------------------------------------------------ |
| Web首页地址 | http://192.168.0.1:8081/index.htm                            |
| Web退出地址 | [http://192.168.0.1:8081](http://192.168.0.1:8081/)/oplogout.htm |

## **4.2、改配置****url****&****/support/**

和资源库中修改的七处的定义一样

# ![](https://raw.githubusercontent.com/maincooss/boomb/main/Clip_20220613_194602.png)

# **五、在线学习平台对接到大数据**

## **5.1、在大数据开发者平台添加在线学习平台应用**

以在线学习平台地址【http://192.168.0.1:8081/estudy/estudyIndex.action】为例

| Web校验地址 | http://192.168.0.1:8081/estudy/passport/opVerify.action |
| ----------- | ------------------------------------------------------- |
| Web首页地址 | http://192.168.0.1:8081/estudy/estudyIndex.action       |
| Web退出地址 | http://192.168.0.1:8081/estudy/oplogout.action          |

## **5.2、在线学习平台后台参数设置**

# ![](https://raw.githubusercontent.com/maincooss/boomb/main/Clip_20220613_194633.png)

# **六、直播平台对接到大数据**

## **6.1、在大数据开发者平台添加直播平台应用**

以直播平台地址【http://192.168.0.1:8081/home/index.action】为例

| Web校验地址 | [https://192.168.0.1:8081](https://192.168.0.1:8081/)/open/service/verifyLogin.action |
| ----------- | ------------------------------------------------------------ |
| Web首页地址 | https://192.168.0.1:8081/home/index.action                   |
| Web退出地址 | [https://192.168.0.1:8081](https://192.168.0.1:8081/)/open/service/loginout.action |

## **6.2、后台参数设置**

# ![](https://raw.githubusercontent.com/maincooss/boomb/main/Clip_20220613_194714.png)
