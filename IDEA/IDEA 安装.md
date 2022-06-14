# IDEA 安装

## 插件

![图 1](.IDEA%20%E5%AE%89%E8%A3%85/20220614100730165.png)  

.ignore (4.3.0)

Convert YAML and Properties File (1.0.5)

GenerateAllSetter (2.8)

Git Commit Template (1.2.0)

GsonFormatPlus (1.6.1)

IDE Eval Reset (2.3.5)

Maven Helper (4.19.212.000.1)

MyBatisX (1.5.4)

POJO to JSON (1.2.2)

String Manipulation (9.5.0)

Swagger Tools (1.1.1)

Translation (3.3.2-203u212)

Settings Repository

## 配置

如果之前有配置过配置同步，可跳转到[配置同步](#配置同步)

![图 10](.IDEA%20%E5%AE%89%E8%A3%85/20220614102359284.png)  

### 文件编码

Editor>File Encodings

![图 11](.IDEA%20%E5%AE%89%E8%A3%85/20220614102429115.png)  

![图 12](.IDEA%20%E5%AE%89%E8%A3%85/20220614102438372.png)  

### 多行标签栏

Editor>General>Editor Tabs

![图 13](.IDEA%20%E5%AE%89%E8%A3%85/20220614102508475.png)  

### 设置标签数量

Editor>General>Editor Tabs

![图 14](.IDEA%20%E5%AE%89%E8%A3%85/20220614102527604.png)  

### 智能提示忽略大小写

Editor>General>Code Completion

![图 15](.IDEA%20%E5%AE%89%E8%A3%85/20220614102547583.png)  

### 自动导包

Editor>General>Auto Import

![图 16](.IDEA%20%E5%AE%89%E8%A3%85/20220614102602617.png)  

### Maven配置 

Build,Execution,Deployment>Build Tools>Maven

![图 17](.IDEA%20%E5%AE%89%E8%A3%85/20220614102621605.png)  

![图 18](.IDEA%20%E5%AE%89%E8%A3%85/20220614102627806.png)  

### 配色方案

Editor>Color Scheme

![图 19](.IDEA%20%E5%AE%89%E8%A3%85/20220614102643527.png)  

### 模板-头部注释

Editor>File and Code Templates>includes>File Header

```java
/**
 *
 * @author ${USER}
 * @date ${DATE} ${TIME}
 */
 ```

 ![图 20](.IDEA%20%E5%AE%89%E8%A3%85/20220614102721925.png)  

### 关闭默认打开文件

Appearance&Behavior>System Settings

![图 21](.IDEA%20%E5%AE%89%E8%A3%85/20220614102744758.png)  

### Git 提交侧栏

Version Control>Commit

![图 22](.IDEA%20%E5%AE%89%E8%A3%85/20220614102802716.png)  

### 工具栏

View>Appearance>Toolbar

![图 23](.IDEA%20%E5%AE%89%E8%A3%85/20220614102821031.png)  

### IDE Eval Reset自动重置

Help>Eval Reset

![图 24](.IDEA%20%E5%AE%89%E8%A3%85/20220614102904457.png)  

![图 25](.IDEA%20%E5%AE%89%E8%A3%85/20220614102913183.png)  

![图 26](.IDEA%20%E5%AE%89%E8%A3%85/20220614102921688.png)  


## 配置同步

IntelliJ IDEA 提供了配置同步功能，可以将自己的配置同步到云端。这里的云端总共有两种形式，第一种是归属于 JetBrains 账号下，通过账号进行同步。第二种是可以利用 Github 项目进行同步。

### Settings Repository

*通过 Github 的方式同步配置*

因为是通过 Github 的方式同步配置，所以需要在 Github 创建一个新的项目。

项目类型私有和公有都行

![图 2](.IDEA%20%E5%AE%89%E8%A3%85/20220614101405444.jpg)  

![图 3](.IDEA%20%E5%AE%89%E8%A3%85/20220614101405456.jpg)  

创建完成后，先选择左侧的 HTTPS 选项，然后点击右侧 Copy 按钮, 然后你会获得一个这样的 https://github.com/xiaoxiunique/intellij-idea-setting-repository.git 地址

然后在菜单栏中选择 File - Manage IDE Settings - Settings Repository 设置我们对应的 Git 地址。

![图 4](.IDEA%20%E5%AE%89%E8%A3%85/20220614101525967.jpg)  

![图 5](.IDEA%20%E5%AE%89%E8%A3%85/20220614101525978.jpg)  

然后点击 OverWrite Remote，因为我们这是第一次配置设置地址，所以直接选择覆盖远程即可。不出意外的话，编辑器应该会弹出一个 请输入 access token 的一个提示框。

![图 6](.IDEA%20%E5%AE%89%E8%A3%85/20220614101608098.jpg)  

我们需要在 Github 针对这个项目创建一个 access token。

登录Github>头像>Settings>Developer settings>Personal access tokens

![图 7](.IDEA%20%E5%AE%89%E8%A3%85/20220614101919737.png)  

等 token 创建完成之后直接输入地址，然后提交就可以直接覆盖远程配置了。

![图 8](.IDEA%20%E5%AE%89%E8%A3%85/20220614102112173.png)  

上面就是我上传了配置后 项目的样子。

完成上面的设置之后，我们现在就能够自动的同步配置了, 这样只需要在另外一台电脑上配置好 Github 地址之后就可以保持两边设置同步了。

上面我们是完成了我们自己的两台电脑间的配置同步，但是这个 Setting Repository 还可以设置 Readonly Source 就是只读配置

![图 9](.IDEA%20%E5%AE%89%E8%A3%85/20220614102221089.jpg)  

上图所示，在 Read-only sources 中点击添加，然后设置一个公开的配置地址，比如我的地址https://github.com/xiaoxiunique/intellij-idea-setting-repository.git 因为我的地址是公开的，所以可以直接拉取，这样就能直接获取得到我的「IntelliJ IDEA」的配置了。
