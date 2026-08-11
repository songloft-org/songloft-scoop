# scoop-package

## 添加 Bucket

```powershell
scoop bucket add songloft-org https://github.com/songloft-org/scoop-package
```

## 应用说明

本 Bucket 提供以下三个应用，请根据需要选择安装：

| 应用 | 说明 |
| --- | --- |
| `songloft-server` | Songloft 自托管音乐服务端（CLI，仅命令行程序，不含图形界面） |
| `songloft-player` | Songloft Player，跨平台音乐播放器（GUI 客户端，仅播放器，不含服务端） |
| `songloft-bundled` | Songloft 服务端与 Flutter 前端（GUI）打包在一起的一体化版本，安装后同时包含服务端与播放器界面 |

### 冲突说明

由于 `songloft-bundled` 已经内置了服务端和播放器功能，与单独安装的 `songloft-server`、`songloft-player` 存在功能重复和文件冲突（如可执行文件、快捷方式等），因此三者之间设置了互斥关系（`conflicts`），**不能同时安装**：

- `songloft-server` 与 `songloft-bundled` 互斥
- `songloft-player` 与 `songloft-bundled` 互斥
- `songloft-server` 与 `songloft-player` 可以同时安装（两者不冲突，分别提供服务端和播放器）

若需要从 `songloft-server` / `songloft-player` 切换到 `songloft-bundled`（或反之），请先卸载已安装的冲突应用，再安装目标应用：

```powershell
scoop uninstall songloft-server songloft-player
scoop install songloft-org/songloft-bundled
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
