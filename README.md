# DouAi

DouAi 是抖音增强模块，作者 **yudigaga**。

当前正式版：**0.1.75** / versionCode **76**。

## 0.1.75 更新

重新打包既定的黑边回退结果：恢复原有单一更新回调，撤回创建绑定与 holder 恢复增量。保留下载分类选择、评论回复、素材识别及独立回复悬浮提示。一屏一条、保留完整画面并接受比例所需留白，不新增裁剪或视频交界黑带修复；设备实际表现仍待复验。

沿用 R8 和原正式签名。按用户要求跳过真机验证，完整说明区分本地回归、DEX/APK 契约与实际设备行为。备份中的密钥如选择包含，将明文保存；目录权限与本地音频文件不随 JSON 转移。

[完整更新说明](https://github.com/yudigaga/DouAi/blob/v0.1.75/docs/release-0.1.75.md)

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

推荐流和顶部标签筛选、组件隐藏与透明度、播放手势与速度、画面裁切和沉浸显示、原生下载扩展、下载任务与取消、评论和语音工具、自动回复与自动评论、关注/粉丝 UID 名单与群聊范围、模型配置和分层提示词、测试对话及图片/视频素材、配置导入与导出。

功能以当前适配和设置页面为准。未匹配或有多个候选的宿主方法不会任意选择 Hook 目标。仅适配抖音 40.6.0，不保证其他版本兼容。

感谢 [Miuix](https://github.com/compose-miuix-ui/miuix) 提供 UI。依赖与设计参考见源码仓库中的第三方说明。
