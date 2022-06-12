# Java JRE生成

打开（管理员权限） CMD 或 Windows powerShell

执行

```shell
# cd <JDK 安装目录>
cd "C:\Program Files\Java\jdk-11.0.1"
# 生成 JRE
bin\jlink.exe --module-path jmods --add-modules java.desktop --output jre
```

执行命令后将在 JDK 安装目录下生成 jre 文件夹