# scoop-package

## 添加 Bucket

```powershell
scoop bucket add songloft-org https://github.com/songloft-org/scoop-package
```

## 安装应用

```powershell
scoop install songloft-org/songloft-player
```

## 更新应用

```powershell
scoop update songloft-player
```

## 卸载应用

```powershell
scoop uninstall songloft-player
```

如需同时删除持久化数据（配置文件等），使用 `--purge` 参数：

```powershell
scoop uninstall songloft-player --purge
```
