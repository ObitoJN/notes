# introduction
记录一下安装使用omnisafe遇到的坑

# installation
## 方法一
先从github上下载，再安装。缺点是pycharm不能进入源码查看，不推荐。而且会遇到依赖冲突问题

## 方法二
用pip更方便
```
$ conda create -n omnisafe python=3.8
$ conda activate omnisafe
$ pip install omnisafe
```

# cuda使用注意点
从清华源下载的pytorch版本默认是cpu版，推荐从官网下
```
$ pip uninstall torch
$ conda install pytorch torchvision torchaudio pytorch-cuda=11.8 -c pytorch -c nvidia
```
安装后发现还是报错，缺少依赖chardet，那么再安装一下：
```
$ conda install chardet
```

然后就可以用gpu来训练啦！