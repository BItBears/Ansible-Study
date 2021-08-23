---------------------------------------------------BitBears---------------------------------------------------

1.适用范围：
    部署剧本适用于基于systemd管理的Redhat、Debian两大家族Linux
2.部署前提条件
    手工安装如下包：gcc、gcc-c++、cmake、curl-devel、libtirpc-devel、bison、pkg-config
    剧本自动安装依赖包：ncurses、openssl、rpcsvc-proto-1.4.2
3.执行剧本之前请手工修改相关变量：
    --config.yaml
        app_user--mysql安装后运行的用户
        app_group--mysql安装后运行的用户组
        app_gid--mysql安装后运行的用户组ID
        app_uid--mysql安装后运行的用户ID
        app_root_dir--mysql安装的上级目录
    --vars/mysql.yaml
        mysql_version--mysql版本号，pkg目录中的mysql源码包命名格式“mysql-版本号.tar.gz”
        mysql_gversion--mysql主要版本号
        mysql_port--mysql实例端口，多实例时只需修改端口再次运行剧本
        mysql_root_password--mysql数据库root账户密码
        mysql_data_root--mysql数据库数据上级目录
        mysql_base_dir--mysql安装目录
        mysql_data_dir--该mysql实例的数据目录
        mysql_tmp_dir--该mysql实例的数据临时目录
        mysql_logs_dir--mysql数据库的日志目录，统一存放该位置
        mysql_pid_dir--mysql数据库的PID目录，统一存放该位置
        mysql_socket_dir--mysql数据库的SOCK目录，统一存放该位置
        mysql_cnf_file--my.cnf存放位置，一般无需修改

4.若实例已经被安装，再次执行剧本操作时不会覆盖之前操作
5.执行剧本前，请配置好相关hosts，并修改“install_app_mysql.yaml”文件中的hosts值
6.多实例时请不要修改mysql安装目录、版本等

---------------------------------------------------BitBears---------------------------------------------------
