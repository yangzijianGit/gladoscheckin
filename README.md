# Glados自动签到

## 食用方式：

邀请的方式：

1. 直接注册GLaDOS(注册地址在 https://github.com/glados-network/GLaDOS 实时更新)

成功后输入邀请码:M8WGU-E9AK5-ZSIL4-IN9J8 激活

2. 通过 https://glados.space/landing/M8WGU-E9AK5-ZSIL4-IN9J8 注册, 自动填写激活

3. 通过 https://m8wgu-e9ak5-zsil4-in9j8.glados.space , 自动填写激活

### **Fork**本仓库

![图片加载失败](imgs/1.png)

### 添加**secret**

1. 跳转至自己的仓库的`Settings`->`Secrets and variables`->`Action`

2. 添加1个`repository secret`，命名为`COOKIES`，其值对应GLaDOS账号的cookie值中的有效部分（获取方式如下）

- 在GLaDOS的签到页面按`F12`

- 切换到`Network`页面下，刷新

![图片加载失败](imgs/2.png)

- 点击第一个选项卡后在`Request Headers`下找到`Cookie`，右键复制cookie的值即可

  > 参考格式：koa:sess=eyJ1c2xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxAwMH0=; koa:sess.sig=xJkOxxxxxxxxxxxxxxxtnM;

![图片加载失败](imgs/3.png)

- 多账号请在 `COOKIES` 中 添加多个 `cookies` 中间使用 `&`连接即可。（例如： `c1&c3&c3...`）

3. plus 微信推送（非必须）

- 添加1个`repository secret`，命名为`PUSHPLUS`，其值对应pushplus秘钥: [获取地址](http://www.pushplus.plus)。

### **star**自己的仓库

![图片加载失败](imgs/4.png)

## 文件结构

```shell
│  checkin.py	# 签到脚本
│
├─.github
│  └─workflows
│          gladosCheck.yml	# Actions 配置文件
```

## 声明

本项目不保证稳定运行与更新, 因GitHub相关规定可能会删库, 请注意备份
