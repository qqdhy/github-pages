## MacOS Shell
### Mac通过.zshrc自动加载.bash_profile文件
Mac Shell 的用户级配置启动文件是 `.zshrc` 
```shell
cd
sudu vim ~/.zshrc
```

在`.zshrc`文件中加入 `.bash_profile` 的启动配置
```shell
source ~/.bash_profile
```

