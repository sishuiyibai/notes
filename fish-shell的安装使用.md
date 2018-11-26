## fish shell 的安装配置及基本使用
### 1.  添加软件源并手动安装
> *对于Centos7, 请以根用户root运行下面命令:*

>     cd /etc/yum.repos.d/
>     wget https://download.opensuse.org/repositories/shells:fish:release:2/CentOS_7/shells:fish:release:2.repo
>     yum install fish
### 2. 启动,退出与帮助
> * 启动Fish:

>     $fish

> 由于 Fish 的语法与 Bash 有很大差异，Bash 脚本一般不兼容。因此，我建议不要将 Fish 设为默认 Shell，而是每次手动启动它。使用过程中，如果需要帮助，可以输入help命令。浏览器就会自动打开，显示在线文档。

>     $help

>* 退出Fish:

>     >exit
### 3. 自动建议
> Fish 自动会在光标后面给出建议,表示可能的选项,颜色为灰色,如果接受建议,可按下→或者Control + F,如只接受部分建议,按下Alt + → 。

### 4. 语法,函数和提示符
> Fish的配置文件是~/.config/fish/config.fish,每次Fish启动，就会自动加载这个文件，我们可以在这个文件里面写入各种自定义函数，它们会被自动加载。Fish 还提供 Web 界面配置该文件。

>     $fish_config

