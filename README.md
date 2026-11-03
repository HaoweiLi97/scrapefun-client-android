<div align="center">
  <img src="./docs/images/client-icon.png" alt="ScrapeFun Client" width="80" />
  <h1>ScrapeFun Client for Android</h1>
  <p><strong>简体中文</strong> · <a href="./README.en.md">English</a></p>
  <p><a href="https://scrapefun.com/">官网</a> · <a href="https://github.com/HaoweiLi97/scrapefun-client-android/releases/latest">下载安装</a> · <a href="https://github.com/HaoweiLi97/scrapefun-client-android/releases">全部发行</a> · <a href="https://scrapefun.com/#/docs">使用文档</a></p>
</div>

> 文档更新：2026-11-03。下列版本和资产为核对当日的稳定版；后续以对应 Release 为准。

Android 客户端，连接已有 ScrapeFun Server，在移动设备上浏览和播放媒体。服务器可部署于 Docker、macOS 或 Windows；媒体库与用户由 Server 管理。

**升级说明：**0.5.1 沿用 0.5.0 的正式签名，可直接覆盖升级并保留数据。0.5.0 以前使用旧签名的客户端无法直接覆盖升级；如系统提示签名不一致，请勿卸载原应用来绕过检查。

0.5.1 改善远程连接在长时间播放和空闲后的稳定性，应用运行期间维护连接，并在连接失去响应后自动尝试重连。

## 下载与设备架构

| 项目 | 当前稳定版 |
| --- | --- |
| 版本 | [0.5.1](https://github.com/HaoweiLi97/scrapefun-client-android/releases/tag/v0.5.1) |
| 64 位 ARM | `scrapefun-android-0.5.1-stable-arm64-v8a.apk` |
| 32 位 ARM | `scrapefun-android-0.5.1-stable-armeabi-v7a.apk` |
| 校验与更新信息 | `.sha256`、`SHA256SUMS`、发行 manifest |

从[稳定版下载页](https://github.com/HaoweiLi97/scrapefun-client-android/releases/latest)获取匹配设备 ABI 的 APK。当前 Release 未提供 x86 / x86_64 包；Android 版本要求以系统安装器检查和该版说明为准。

## 安装与连接

1. 下载官方 APK，按 Android 系统提示允许当前下载来源安装应用。
2. 完成安装后打开 ScrapeFun，填写 Server 地址，例如 `http://192.168.1.10:8096`。
3. 使用 Server 的账号登录。

手机中的 `localhost` 指手机本身。局域网访问请使用 Server 的实际 IP、端口，并确认双方网络可达。

## 更新与数据

应用可检查 Release 并核对发布的校验信息，再调用 Android 系统安装器；也可手动下载同签名、同应用 ID 的新版 APK 覆盖安装。

系统提示签名不一致时，不要直接卸载以绕过问题：先核对包来源，保存本地配置，再联系支持。卸载可能清除客户端本地设置；Server 的业务数据应在 Server 侧独立备份。

## 文件校验

使用 Linux 下载时，可在 APK 与 `SHA256SUMS` 所在目录运行：

```bash
sha256sum --check --ignore-missing SHA256SUMS
```

macOS 可用 `shasum -a 256 文件.apk` 计算摘要，再与该 APK 的 `.sha256` 内容比较。文件校验不能替代 Android 安装签名验证。

<details>
<summary>故障排查</summary>

报告安装问题时注明 Android 版本、设备 ABI、完整 APK 文件名和系统提示。连接或播放问题同时提供 Server 版本及最小复现步骤。

</details>

## 支持与授权

本仓库提供平台安装说明和官方发行资产。使用问题与功能建议请提交到[主仓库 Issues](https://github.com/HaoweiLi97/ScrapeFun/issues)；账号、激活或私密日志请联系 `scrapefun@outlook.com`。报告安全问题请按[安全说明](./SECURITY.md)私密提交。

新的商业许可声明见 [LICENSE](./LICENSE)，完整条款见[软件使用许可协议](./EULA.md)。个人、家庭及组织内部可正常使用；Pro 需有效授权，软件再分发、转售、客户交付和收费托管须单独书面授权。该声明不追溯改变既有授权；现有资产以其随包许可为准，第三方组件继续适用各自许可证。

[发行与兼容性说明](https://github.com/HaoweiLi97/ScrapeFun/blob/main/RELEASE_POLICY.md) · [第三方组件说明](https://github.com/HaoweiLi97/ScrapeFun/blob/main/THIRD_PARTY_NOTICES.md) · [支持流程](./SUPPORT.md)
