# ClassAegis · 课佑

**守护每一堂课，联通整座校园。**

ClassAegis 是面向校园内网的一体化终端管理开源项目，连接教室大屏、一体机与办公终端，让设备管理、信息发布和运维协作集中在同一套平台中。

[项目总览](https://github.com/ClassAegis/classaegis) · [架构与协议](https://github.com/ClassAegis/classaegis-docs) · [内网服务端](https://github.com/ClassAegis/classaegis-server) · [Windows 客户端](https://github.com/ClassAegis/classaegis-service)

## 我们在做什么

- **课佑集控**：面向管理员的内网服务端与 Web 管理台，提供设备接入、指令下发、执行回执和审计能力。
- **课佑管家**：运行在 Windows 终端上的客户端，连接平台与本机能力，提供消息通知、终端控制、软件管理和运维工具。
- **课佑中枢**：规划中的可选私有云端，用于多校协同、状态汇总与升级分发。
- **课佑随身**：规划中的移动管理端，面向教师和管理员提供便捷的设备管控入口。

## 以校园内网为中心

校园设备通过内网服务端接受管理；云端是可选的扩展层。设计上由内网服务端主动建立云连接，设备不直接连接云端，避免将校园设备暴露到公网。

Windows 客户端将通信、执行与界面分为独立组件：Core 负责平台通信与指令校验，Ability 执行本地能力，Service 呈现设备状态，Launcher 管理后台进程。高权限操作和采集功能应在设备所有者授权及学校管理制度范围内使用。

## 仓库导航

| 仓库 | 内容 |
| --- | --- |
| [classaegis](https://github.com/ClassAegis/classaegis) | 项目总览、产品规划与协作约定 |
| [classaegis-docs](https://github.com/ClassAegis/classaegis-docs) | 架构设计、协议规范与兼容性文档 |
| [classaegis-service](https://github.com/ClassAegis/classaegis-service) | Windows 客户端：Go 能力组件、Vue / Tauri 界面与安装工具 |
| [classaegis-server](https://github.com/ClassAegis/classaegis-server) | Java / Spring Boot 内网服务端、Vue 管理台与部署配置 |
| [classaegis-cloud](https://github.com/ClassAegis/classaegis-cloud) | 可选私有云端的规划与对接契约 |
| [classaegis-mobile](https://github.com/ClassAegis/classaegis-mobile) | Android 移动管理端的规划与开发入口 |

## 开发进展

项目正在持续开发，客户端与内网服务端已有实现，云端及移动端仍以规划和对接设计为主。功能覆盖、运行环境和验证范围以各仓库的 README、部署说明及测试记录为准；规划中的功能不代表已发布或已完成生产环境验收。

准备试用时，请从对应仓库的构建与部署说明开始；参与跨组件开发时，请先阅读协议仓库，保持指令、回执和接口约定一致。

## 一起参与

欢迎提交可复现的问题、文档改进、测试和代码贡献。开始前请阅读 [贡献指南](https://github.com/ClassAegis/classaegis/blob/main/CONTRIBUTING.md) 与 [行为准则](https://github.com/ClassAegis/classaegis/blob/main/CODE_OF_CONDUCT.md)。

安全问题请遵循对应仓库的 SECURITY.md，优先使用私密报告渠道；不要在公开 Issue 中发布未修复漏洞细节、访问凭据或真实设备数据。[查看安全策略](https://github.com/ClassAegis/classaegis/blob/main/SECURITY.md)。

## 开源许可

项目原创代码与文档采用 **GNU AGPL-3.0-only**，完整条款及适用范围见各仓库的 LICENSE。第三方依赖、运行时和随包组件保留各自的版权与许可证。
