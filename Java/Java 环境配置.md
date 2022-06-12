# Java 环境配置

安装完成 JDK 后，右击"我的电脑"，点击"属性"，选择"高级系统设置"，选择"高级"选项卡，点击"环境变量"。

在 "系统变量" 中设置 3 项属性，JAVA_HOME、PATH、CLASSPATH(大小写无所谓),若已存在则点击"编辑"，不存在则点击"新建"。

> 如果使用 1.5 以上版本的 JDK，不用设置 CLASSPATH 环境变量，也可以正常编译和运行 Java 程序

变量设置参数如下：

- 变量名：JAVA_HOME
- 变量值：C:\Program Files (x86)\Java\jdk1.8.0_91        // 要根据自己的实际路径配置
- 变量名：CLASSPATH
- 变量值：.;%JAVA_HOME%\lib\dt.jar;%JAVA_HOME%\lib\tools.jar;         //记得前面有个"."
- 变量名：Path
- 变量值：%JAVA_HOME%\bin;%JAVA_HOME%\jre\bin;

## 无法通过环境变量切换 JDK 版本

这是因为在安装高版本的 JDK 的时候，安装程序会自动在 PATH 变量上配置变量（在不手动配置环境变量的情况下，可以通过该变量直接使用 Java 命令）指定到最高版本的 JDK

```txt
C:\Program Files\Common Files\Oracle\Java\javapath
C:\Program Files (x86)\Common Files\Oracle\Java\javapath
```

只需要将手动配置的 PATH 变量移动到这两条变量之前即可