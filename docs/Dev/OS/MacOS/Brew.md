## Brew Usage
## Homebrew

https://brew.sh/

https://brew.sh/zh-cn/

https://github.com/Homebrew/brew

https://docs.brew.sh/Manpage

### Install Homebrew

```shell
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

#### 中科大镜像

```shell
cd "$(brew --repo)"
git remote set-url origin git://mirrors.ustc.edu.cn/brew.git
cd "$(brew --repo)/Library/Taps/homebrew/homebrew-core"
git remote set-url origin git://mirrors.ustc.edu.cn/homebrew-core.git
```

#### 清华镜像

```shell
git -C "$(brew --repo)" remote set-url origin https://mirrors.tuna.tsinghua.edu.cn/git/homebrew/brew.git

git -C "$(brew --repo homebrew/core)" remote set-url origin https://mirrors.tuna.tsinghua.edu.cn/git/homebrew/homebrew-core.git
```



### 安装软件

- `brew install app123` 默认安装最新版
- `brew install app123@14.16.8` 安装指定版本
- `brew switch app123 16.0.0` 切换版本

### 更新软件
- `brew upgrade name` 更新安装过的软件(如果不加软件名，就更新所有可以更新的软件)
-  `brew outdated` 查看所有有更新版本的软件

### 卸载软件
- `brew uninstall app123` 卸载应用

### 其它常用命令
- `brew search app123` 搜索可用node相关软件
- `brew info app123` 查看node安装信息
- `brew config` 查看brew配置
- `brew list` 查看已安装软件
- `brew list --versions` 查看已安装软件版本号
- `brew update` brew自身更新
- `brew cleanup` 清除下载的缓存
- `brew doctor` 诊断brew，并给出修复命

## QnA
### Q1
```shell
panda@bogon ~ % brew install tree

Running `brew update --auto-update`...

Warning: No available formula with the name "tree".
```

Run `brew doctor` to fix brew config issues. 

Example:

```text
Warning: Suspicious https://github.com/Homebrew/brew git origin remote found.

The current git origin is:

  https://github.com/Homebrew/homebrew-cask.git

  

With a non-standard origin, Homebrew won't update properly.

You can solve this by setting the origin remote:

  git -C "/usr/local/Homebrew" remote set-url origin https://github.com/Homebrew/brew

  

Warning: Homebrew/homebrew-cask was not tapped properly! Run:

  rm -rf "/usr/local/Homebrew/Library/Taps/homebrew/homebrew-cask"

  brew tap homebrew/cask
```



### Q2: mac 终端 command not found解决方法

MacOS的环境变量

1. /etc/profile
2. /etc/paths
3. ~/.bash_profile
4. ~/.bash_login
5. ~/.profile
6. ~/.bashrc

1~2 是系统级，系统启动就会加载。其余是用户级别。

添加环境变量

1. `sudo vim ~/.bash_profile`
2. 在文件末尾增加一行 `export PATH="/opt/homebrew/bin:$PATH"`
3. 保存退出vim `:wq`
4. 激活文件配置 `source ~/.bash_profile`



### Q3: Cannot install in Homebrew on ARM processor in Intel default prefix (/usr/local)!

当你用homebrew在配置Apple M1芯片的MacOS里安装应用时，可能会遇到以上问题。解决方案如下：

1. 打开Finder应用
1. 在Applications/Utilities文件夹中找到Terminal.app  
1. 右键菜单选择Get Info
1. 在General中勾选Open using Rosetta
1. 重启Terminal.app之后再运行homebrew

