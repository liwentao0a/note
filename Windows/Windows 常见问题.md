# Windows 常见问题

## 缺少VCRUNTIME140_1.DLL

启动应用弹出缺少DLL

### 解决方案

1. 方案1
    
    下载[微软常用运行库](https://docs.microsoft.com/zh-CN/cpp/windows/latest-supported-vc-redist?view=msvc-170)并安装即可解决该问题

2. 方案2

    直接下载VCRUNTIME140_1.DLL，并将其复制在C:\Windows\System32