## pig 整合前后端分离项目登录


![](https://minio.pigx.vip/alei/2023/01/5331045f8c867c6ae6c4e62aa6434850.png)

```sql
INSERT INTO `pig`.`sys_oauth_client_details`(`client_id`, `resource_ids`, `client_secret`, `scope`, `authorized_grant_types`, `web_server_redirect_uri`, `authorities`, `access_token_validity`, `refresh_token_validity`, `additional_information`, `autoapprove`, `create_time`, `update_time`, `create_by`, `update_by`) VALUES ('jeecg-boot', '', 'jeecg-boot', 'server', 'authorization_code', 'http://127.0.0.1:3100/sso', '', 168000000, 168000000, '', 'false', '2023-01-17 08:31:46', '2023-01-17 09:32:06', 'admin', 'admin');
```

## 后端配置

> 配置  jeecg-boot 前端地址 默认 3100 端口  
> 配置  PIG 网关地址

- 增加sso的配置
  ![](https://minio.pigx.vip/alei/2023/01/eb241f5b203e21d5cb762f8886359f21.png)

- 增加一个登录
  ![](https://minio.pigx.vip/alei/2023/01/d479312b9c2ab8569b19fd8f84d7d6fa.png)


## 前端配置
前端地址 https://github.com/pig-mesh/jeecgboot-vue3
- 登录页面配置
 ![](https://minio.pigx.vip/alei/2023/01/7c61cb04d291a39c026205bafc25e3c5.png)

- 增加sso 页面，回调使用，用于code 处理
  ![](https://minio.pigx.vip/alei/2023/01/d6eb64a260f87cae36740c7e7cf7abf4.png)

- 退出系统
  ![](https://minio.pigx.vip/alei/2023/01/ecd7091d1ebf3cba98baa8db3ba48aad.png)