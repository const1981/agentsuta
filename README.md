# SutaAgent

手机端「自托管多 AI Agent 管理控制台」。在手机上部署 / 配置 / 备份你的 Hermes、OpenClaw 等 AI Agent。

> 品牌 Suta（你已持有多个 suta* 域名）。本仓库为演进方向：未来 Hermes 只是被管理的一个 agent 类型。

## 基本信息
- 包名：`com.nxg.agentsuta`
- 应用名：SutaAgent
- 官网/下载：`https://Agent.suta.eu.cc`（DNS 由域名商配置）
- 仓库：`https://github.com/const1981/agentsuta`

## 状态
- 🚧 脚手架阶段（从 `hermes-agent-mobile-zh` v0.3.18 迁移并重命名而来）。
- 当前已包含：配置页（渠道/模型/技能/设置四 Tab）、网关控制、系统镜像备份还原、终端、技能市场基础。
- 后续路线图：多 Agent 列表与一键创建（Hermes / OpenClaw）、统一技能市场搜索安装、清理垃圾常驻功能。
- 🔴 **必做（臣哥钦定 2026-07-15）**：**扫码对接微信**——APP 内扫码连接/绑定微信渠道（对接哪种微信待确认：个人微信 QR 登录 / 企业微信 / 公众号）。

## 开发
- Flutter 3.24.x（CI 锁定版本；本地请用同版本以避免 `CardTheme`/`DialogTheme` 等 breaking 差异）。
- 本地编译（抓 Kotlin 错）：PowerShell 下 `.\gradlew.bat assembleDebug`，JAVA_HOME 指向 JDK 21。
- CI：GitHub Actions `Build Android APK`，出 arm64 release 包。

## 安全
- API Key 一律走 `~/.hermes/.env` 的 `${VAR}`，绝不硬编码进 Dart/Kotlin。
