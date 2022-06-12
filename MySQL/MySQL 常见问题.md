# MySQL 常见问题

## Public Key Retrieval is not allowed

连接mysql时报错

```txt
Public Key Retrieval is not allowed（不允许公钥检索）
```

### 解决方法

设置驱动属性 allowPublicKeyRetrieval=false （这里的运输公钥检索是默认关闭的，需要把它开启），改为allowPublicKeyRetrieval=true 即可。