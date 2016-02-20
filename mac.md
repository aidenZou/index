# mac

## shell(iTerm2 + zsh + oh-my-zsh) autojump

```shell
# 看下系统内置了几种shell
~  cat /etc/shells
# List of acceptable shells for chpass(1).
# Ftpd will not allow users to connect who are not using
# one of these shells.

/bin/bash
/bin/csh
/bin/ksh
/bin/sh
/bin/tcsh
/bin/zsh

# wget 自动安装
~  wget https://github.com/robbyrussell/oh-my-zsh/raw/master/tools/install.sh -O - | sh

# 切换到 zsh 模式
~  chsh -s /usr/local/bin/zsh
```

oh-my-zsh 安装后,它的配置在用户目录下的 .oh-my-zsh 目录下 `/Users/aidenZou/.oh-my-zsh`

zsh 的配置文件也在用户目录下 .zshrc 隐藏文件

`~  vim ~/.zshrc`

1. z
2. d
	> 按一下 d 再回车你会看到最近的历史记录，然后你就可以通过数字比如 1, 2 之类的返回到某个历史记录中了。
3. zsh_stats 可以看到你的使用频率前 20 的命令是什么！

```shell
~  brew install autojump
# 查看 Autojump 的版本
~  j -v
autojump v22.2.4

# 跳到先前到过的目录 www
~  j www
/Users/aidenZou/www

# 跳到子目录
~  jc www

# 打开目录
~  jo www

# 查看每个文件夹的权重和全部文件夹计算得出的总权重的统计数据
# 文件夹的权重代表在这个文件夹中所花的总时间。 文件夹权重是该列表中目录的数字。
~  j --stat
~  j --help
```

> j 是 autojump 的一个封装，你可以使用 j 来代替 autojump

- [oh-my-zsh Wiki](https://github.com/robbyrussell/oh-my-zsh/wiki/Plugins-Overview)

