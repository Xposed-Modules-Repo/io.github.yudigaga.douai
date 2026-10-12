# DouAi

DouAi 是抖音增强模块，作者 **yudigaga**。

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

推荐流和顶部标签筛选、组件隐藏与透明度、播放手势与速度、画面裁切和沉浸显示、原生下载扩展、评论和语音工具、自动回复与自动评论、关注/粉丝 UID 名单与群聊范围、模型配置和分层提示词、测试对话及图片/视频素材。

功能以当前适配和设置页面为准。未匹配或有多个候选的宿主方法不会任意选择 Hook 目标。仅适配抖音 40.6.0，不保证其他版本兼容。

感谢 [Miuix](https://github.com/compose-miuix-ui/miuix) 提供 UI。依赖与设计参考见源码仓库中的第三方说明。
