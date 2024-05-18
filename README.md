# 邮件API配置发送邮件接口调用测试_在线调试

#### 介绍
通过使用AokSend邮件API接口进行调用发送邮件测试，在线调试配置邮件接口实现发送邮件。只需要简单的配置即可快速测试邮件api的可用性和使用效果。更简单更高效的使用接口发送邮件。
![AokSend邮件API接口](https://gitee.com/aoksend/emailsend/raw/master/aaa.png)
#### 在线调试演示界面
![邮件API接口调用测试_在线调试配置发送邮件](https://gitee.com/aoksend/emailsend/raw/master/pic/Pic_20240518_182740.jpg)
在线调试链接：[使用Apifox在线调试AokSend](https://apifox.com/apidoc/shared-c8d42c32-1e1b-43c8-8d18-716b822bfb20)

## 手动调用调试AokSend邮件接口

#### 请求URL
```json
https://www.aoksend.com/index/api/send_email
```
#### 请求方式
```json
POST
```
#### 参数

| 参数名 | 必选 | 类型 | 说明 |  
| :--: | :--: | :--: | :--: |  
| app_key | 是 | 字符串 | API密钥 |  
| template_id | 是 | 字符串 | 模板ID |  
| to | 是 | 字符串 | 收件人地址 |  
| reply_to | 否 | 字符串 | 默认回复地址 |  
| alias | 否 | 字符串 | 发件人名称 |  
| data | 否 | JSON | 模板变量 |

#### data参数示例

```json  
{  
    "name": "张三",  
    "address": "深圳市"  
}
```

#### 返回参数

| 参数名 | 必选 | 类型 | 说明 |  
| :--: | :--: | :--: | :--: |  
| code | 是 | 数值 | 返回状态码 |  
| message | 是 | 字符串 | 返回结果说明 |

#### 返回示例

```json  
{  
    "code": "200",  
    "message": "请求成功"  
}
```

#### code返回值对照

| 值 | 文本 | 说明 |  
| :---: | :---: | :---: |  
| 200 | 请求成功 |  |  
| 40001 | API密钥不能为空 |  |  
| 40002 | 认证失败 | API密钥错误 |  
| 40003 | 模板ID错误 |  |  
| 40004 | 收件人地址to不能为空 |  |  
| 40005 | 收件人地址to格式不正确 |  |  
| 40006 | 默认回复地址reply_to格式不正确 |  |  
| 40007 | 余额不足 |  |  
| 40008 | data格式错误 | . |

## AokSend的api_key的获取方式
![AokSend的api_key的获取方式](https://gitee.com/aoksend/emailsend/raw/master/pic/%E5%BC%80%E5%8F%91%E6%B5%81%E7%A8%8B%E5%9B%BE2.jpg)

#### 链接

1.  AokSend官网 [www.aoksend.com](https://www.aoksend.com)
2.  在线调试AokSend的API接口 [https://apifox.com/aoksend](https://apifox.com/apidoc/shared-c8d42c32-1e1b-43c8-8d18-716b822bfb20) 

