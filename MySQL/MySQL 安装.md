# MySQL 安装

## Window 环境下 ZIP 安装包安装

1. 前往[MySQL官网](https://dev.mysql.com/downloads/mysql/)，下载 ZIP 安装包并解压

2. 在安装目录下创建 my.ini 文件

    ```ini
    [client]
    # 设置mysql客户端默认字符集
    default-character-set=utf8
    [mysqld]
    # 设置3306端口
    port = 3306
    # 设置mysql的安装目录
    basedir=C:/_app/mysql-8.0.28-winx64
    # 设置 mysql数据库的数据的存放目录，MySQL 8+ 不需要以下配置，系统自己生成即可，否则有可能报错
    # datadir=C:/_app/mysql-8.0.28-winx64/data
    # 允许最大连接数
    max_connections=20
    # 服务端使用的字符集默认为8比特编码的latin1字符集
    character-set-server=utf8
    # 创建新表时将使用的默认存储引擎
    default-storage-engine=INNODB
    ```

3. 接下来安装并启动 MySQL 服务

    打开 **（管理员权限）** CMD ,切换目录到安装目录

    ```shell
    cd C:\_app\mysql-8.0.28-winx64\bin
    ```

    初始化数据库

    ```shell
    mysqld --initialize --console
    ...
    2022-06-12T11:59:42.945792Z 6 [Note] [MY-010454] [Server] A temporary password is generated for root@localhost: w+pPRSHpj8I?
    ```

    执行完成后，会输出 root 用户的初始默认密码

    w+pPRSHpj8I? 就是初始化密码，后续修改密码需要用到

    安装

    ```shell
    mysqld install
    ```

    启动 MySQL 服务

    ```shell
    net start mysql
    ```

    > 注意: 在 5.7 需要初始化 data 目录：
    >
    > ```shell
    > cd C:\_app\mysql-8.0.28-winx64\bin
    > mysqld --initialize-insecure 
    > ```
    >
    > 初始化后再运行 net start mysql 即可启动 mysql。

4. 修改密码

    执行后输入旧密码即可

    ```shell
    mysqladmin -u <用户名> -p password <新密码>
    Enter password: ************
    ```