# NodePanel Android

[NodePanel](https://github.com/fgozxy) 多服务器管理面板的安卓客户端安装包发布仓库。本仓库只发布 APK，不包含源码。

## 安装

1. 在 [Releases](https://github.com/fgozxy/nodepanel-android/releases/latest) 下载 `NodePanel-vX.Y.Z.apk`
2. 安装时如提示「未知来源」，在系统设置里允许浏览器（或文件管理器）安装应用
3. 打开 App，填写你部署的面板域名、用户名和密码登录

已安装的 App 会每天检查一次新版本，也可以在「设置 → App」或右上角菜单里手动「检查更新」，下载完成并校验通过后直接调起系统安装，登录状态保留。

## 校验

每个版本都附带 `SHA256SUMS.txt`：

```bash
sha256sum -c SHA256SUMS.txt
```

所有版本使用同一个签名证书，SHA-256 指纹：

```
DE:21:C2:3C:12:7F:E2:02:26:E1:D8:1B:0B:46:4A:59:AF:CE:FD:B2:AF:D7:81:55:D0:75:A4:FC:76:33:C2:6F
```

可用 `apksigner verify --print-certs NodePanel-vX.Y.Z.apk` 核对。App 内更新会自动检查 SHA-256、包名、版本号和签名证书，任何一项不一致都不会安装。
