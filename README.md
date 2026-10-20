# DouAi

DouAi 是抖音增强模块，作者 **yudigaga**。

当前正式版：**0.2.4** / versionCode **105**。

## 0.2.4 更新

备份实际导入成功后显示一次完成 Toast，修复 Android ICU 占位符正则兼容性。用户已确认 0.2.3 手机备份导入恢复；本版新增 Toast 及报告保存、外部分享接收仍需设备复验。

本地报告可导出独立浅色排版的一张完整长 PNG 或一份 A4 分页 PDF，包含当前统计、图表与已有 AI 分析，不重新请求 AI；保留文字分享。Android 10+ 分别保存到 Pictures/DouAi 和 Downloads/DouAi，Android 9 使用系统保存入口。PDF 为图片型，超限明确提示；分享前请核对报告中可见的作者、话题和最近记录。

本版累计纳入 MiniMax 独立语音来源、模型/音色刷新和高级设置；发送前持久化防重、私信按会话调度、受控历史诊断、设置搜索与局部文本编辑。MiniMax 目录需要主动刷新，原系统和第三方来源继续保留。旧的已提交或结果未知记录不会自动补发，语音具体拒绝原因与成功率仍需独立现场验证。

联系人名称、头像、开关和对话记录独立于自动回复当前模型；修改或删除联系人不会切换自动回复配置。图片与视频帧需要所选模型和接口支持视觉输入，视频只抽样画面，不包含音频。

沿用 R8 和原正式签名。182 个套件、1933 次完整回归执行通过，零失败、零错误、零跳过，包含本地宿主 DEX、22 项评论回复宿主合同和最终签名 APK 的 3 项合同检查；另 34 项工具检查通过。v3 签名、16 KiB ZIP 对齐和封存完整性通过，Lint 0 错误、57 条既有警告、0 新增。本版新增功能与真实服务尚未由代理执行真机验收。

[完整更新说明](https://github.com/yudigaga/DouAi/blob/v0.2.4/docs/release-0.2.4.md) · [统计与侧写口径](https://github.com/yudigaga/DouAi/blob/v0.2.4/docs/portrait-analysis.md)

## 免责协议

本项目仅用于学习与技术研究。用户的应用、配置、二次开发及使用行为和结果由用户自行决定并承担责任，与本项目及作者无关。完整责任边界见 [免责协议](DISCLAIMER.md)，APK 关于页也可查看。

- 正式包名：`io.github.yudigaga.douai`
- 作用域：`com.ss.android.ugc.aweme`
- 适配版本：抖音 40.6.0
- 环境：Android 9+，支持 libxposed API 102 的 LSPosed
- [源码仓库](https://github.com/yudigaga/DouAi)
- [本仓库正式版](https://github.com/Xposed-Modules-Repo/io.github.yudigaga.douai/releases)
- [GitHub 正式版](https://github.com/yudigaga/DouAi/releases)

## 安装

下载正式 APK 后安装，在 LSPosed 中启用 DouAi，作用域只选择抖音。完全退出并重新打开抖音，在抖音设置中的 DouAi 入口配置功能。模块应用提供框架连接、扫描诊断、隐藏桌面图标和关于入口。

首次从旧 `com.douai.module` Debug 版切换时，先卸载旧模块，再安装并启用正式版，避免重复 Hook。后续正式版使用同一签名，可直接更新。

## 功能

推荐流和顶部标签筛选、组件隐藏与透明度、播放手势与速度、画面裁切和沉浸显示、原生下载扩展、下载任务与取消、评论和语音工具、自动回复与自动评论、关注/粉丝 UID 名单与群聊范围、模型配置和分层提示词、测试对话及图片/视频素材、AI 消息联系人及独立对话、配置导入与导出。

功能以当前适配和设置页面为准。未匹配或有多个候选的宿主方法不会任意选择 Hook 目标。仅适配抖音 40.6.0，不保证其他版本兼容。

感谢 [Miuix](https://github.com/compose-miuix-ui/miuix) 提供 UI。依赖与设计参考见源码仓库中的第三方说明。
