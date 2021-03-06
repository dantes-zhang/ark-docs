# 项目成员管理

易观方舟支持一个项目多个成员共享，方便企业内部共同参与到数据分析和决策的过程中来。项目创建人或管理员可以邀请多个成员，并对不同成员分配不同角色来实现应用的授权。

## 1. 角色-权限

系统预置了常用的角色，不同角色对应不同的权限，管理员授权时对不同的成员选择不同的角色即可。

| 角色 | 角色描述 | 看板 | 分析 | 分群 | 运营 | 管理 |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| 管理员 | 通常赋予项目的leader | √ | √ | √ | √ | √ |
| 产品人员 | 通常赋予产品经理或产品运营该角色 | √ | √ | √ | √ | 使用相关功能 |
| 数据分析师 | 赋予数据分析师该角色 | √ | √ | √ | 仅查看运营列表 | 使用相关功能 |
| 工程师 | 赋予内部协助埋点的工程师 | 仅查看 | 仅查看图表列表和已有图表详情页 | 仅查看分群列表 | 仅查看运营列表 | 集成相关功能 |
| 普通成员 | 赋予普通查看者角色 | 仅查看 | 仅查看图表列表和已有图表详情页 | 仅查看分群列 | 仅查看运营列表 |  |

更多权限明细详见《易观方舟角色-权限对应表》 [https://shimo.im/sheets/6hGxwHhHXXRktTcY/Icvbp](https://shimo.im/sheets/6hGxwHhHXXRktTcY/Icvbp)

## 2. 邀请成员

项目管理员有权限邀请企业成员到本项目中。点击 **成员管理** 进入项目成员列表。

点击右上角 **添加成员** ，选择要邀请的 **企业内成员**，直接添加到 **已选择成员**，点击 **确定** 即可。

![ ](https://imguserradar.analysys.cn/fangzhou/img/2018/12/201812191130157614.gif)

添加成功后，被邀请成员就可以使用 **邮箱/手机号/用户名** 和 **初始密码** 登录到项目中。

## 3. 修改成员

在成员列表页可以查看当前项目中，成员的信息以及对应的权限，管理员有权移除某个成员。

> 注：管理员之间没有权限移除或者修改对方权限

![ ](https://imguserradar.analysys.cn/fangzhou/img/2018/12/201812191136255193.png)

**A. 移除成员**

当添加的成员已离职，或者不再授权时，点击移除成员，移除后将无法访问该项目的数据。

![ ](https://imguserradar.analysys.cn/fangzhou/img/2018/12/201812191140131115.png)

**B. 修改权限**

当成员权限错误时，可以点击角色下拉框，快速修改角色

![ ](https://imguserradar.analysys.cn/fangzhou/img/2018/12/201812191141170214.png)

## 4. 成员数据权限

#### 基于用户数据

可以针对每一个独立的成员设置数据访问权限，目前仅支持基于用户属性的数据权限设置。

例如：设置的权限为张三仅能访问城市=北京的用户数据，那么张三在登录系统后，除分群之外的全部分析功能，都只可访问北京用户的行为数据，无法查看和分析其他城市用户的数据。

![](../../.gitbook/assets/image%20%2881%29.png)

#### 基于行为数据

开发中……

## 常见问题

### 1 是否支持自定义角色？

目前还不支持，如果您有需要，请联系我们反馈  [4006 - 010 - 231](tel:4006-010-231) 

### 2 为什么平台管理员添加了 A 用户，在项目中仍然不可见？

方舟支持一个平台中添加多个项目，每个项目中添加不同的成员，同一成员在不同项目中的角色可不相同，所以在平台中添加成员时，赋予的是用户在平台上的角色，可以是一个项目的管理员，此时可以进入对应的项目，也可以是一个普通的成员，但此时需要项目管理员将其添加到项目中，再赋予其对应的角色。



