# DouAi

DouAi 是抖音增强模块，作者 **yudigaga**。

当前正式版：**0.1.95** / versionCode **96**。

## 0.1.95 更新

累计更新分析页面与可选数据备份、模型流式/非流式和推理强度设置；修正评论回复分页、通知分组、严格线程回源及宿主 Task 合同。评论回复现在只把本人原评论、对方回复及对方附图作为 AI 输入，不再读取原作品媒体和描述，原生发送目标与防重校验保持。

联系人名称、头像、开关和对话记录独立于自动回复当前模型；修改或删除联系人不会切换自动回复配置。图片与视频帧需要所选模型和接口支持视觉输入，视频只抽样画面，不包含音频。

沿用 R8 和原正式签名。本地全量回归 171 个套件、1745 项通过，零失败、零错误、零跳过，包含宿主 DEX、评论回复宿主合同与最终 APK 契约；签名验证通过。按用户要求跳过真机验证，消息页实际显示、评论实际生成和发送仍需设备复验。

[完整更新说明](https://github.com/yudigaga/DouAi/blob/v0.1.95/docs/release-0.1.95.md) · [统计与侧写口径](https://github.com/yudigaga/DouAi/blob/v0.1.95/docs/portrait-analysis.md)

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
