# 案件看板更新发布仓库

本仓库只保存案件看板的签名更新包、公开更新清单 `latest.json` 和版本说明，不包含私有源码、用户数据或签名私钥。

支持的平台：

- Windows 10/11 x64（NSIS）
- macOS Apple 芯片（arm64）
- macOS Intel（x86_64）

客户端按以下顺序检查更新：GitHub Raw → jsDelivr 备用 → GitHub Release 备用。Raw 清单放在第一位，避免 CDN 旧缓存返回 HTTP 200 后阻断后续地址。

更新包必须通过案件看板独立 Minisign 公钥验证后才会安装。首个包含更新器的版本仍需用户手动安装一次，此后的版本可以在应用内更新。
