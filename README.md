# AliDrive-Go  

This project was largely inspired by [Hsury/BiliDrive](https://github.com/Hsury/BiliDrive)  


## 特色

- 用了都说好 （X
- 不需要登录

## 使用指南

### 准备

下载[源代码](https://github.com/Si-Huan/AcDrive/archive/master.zip)后自行编译使用，咱也不知道需要什么版本的go才行

### 上传

```
./alidrive upload [-h] [-t THREAD] -f *file*

file: 待上传的文件路径
THREAD: 上传线程数, 默认值为4, 过大的话你的 ip 可能被 ban 掉
```

上传完毕后，终端会打印一串META URL（通常以`alidrive://`开头）用于下载或分享，请务必妥善保管！  

### 下载

```
./alidrive download [-h] [-t THREAD] -m *meta*

meta: META URL(通常以 alidrive://开头)
THREAD: 下载线程数, 默认值为4
```

下载完毕后会自动进行文件完整性校验（会有提示），对于大文件该过程可能需要较长时间，若不愿等待可直接退出

### 查看文件元数据

```
./alidrive info [-h] -m *meta*

meta: META URL(通常以 alidrive://开头)
```


## 技术实现

将任意文件分块编码为图片后上传至阿里图片CDN，对该操作逆序即可下载并还原文件


## 免责声明

请自行对重要文件做好本地备份

请勿使用本项目上传不符合社会主义核心价值观的文件

请合理使用本项目，避免对 AliYun 的存储与带宽资源造成无意义的浪费

该项目仅用于学习和技术交流，开发者不承担任何由使用者的行为带来的法律责任

## 许可证

AliDrive-Go is under MIT License

本项目基于MIT协议发布