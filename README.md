# HookSiri - iOS Siri 远程控制插件

> **专业级 iOS 越狱插件 | 支持远程控制 Siri 语音输出 | 适用于开发者、安全研究员、自动化场景**

[![iOS](https://img.shields.io/badge/iOS-14.0+-blue.svg)](https://www.apple.com/ios/)
[![Jailbreak](https://img.shields.io/badge/Jailbreak-Required-red.svg)](https://www.theiphonewiki.com/wiki/Jailbreak)
[![License](https://img.shields.io/badge/License-Commercial-orange.svg)](LICENSE)
[![Theos](https://img.shields.io/badge/Built%20with-Theos-green.svg)](https://theos.dev/)

## 🎬 预览视频

<div align="center">
  <video width="400" controls>
    <source src="https://oss.banan.xin/video/IMG_4352.mov" type="video/quicktime">
    您的浏览器不支持视频播放，请 <a href="https://oss.banan.xin/video/IMG_4352.mov">点击这里</a> 下载观看
  </video>
</div>

## 📋 产品简介

**HookSiri** 是一款专业的 iOS 越狱插件，通过 MobileSubstrate 框架实现对 Siri 语音助手的深度定制。支持本地 HTTP 接口和云端控制中心两种方式，让您可以从任何地方远程控制 Siri 的语音输出内容。

### 🎯 核心特性

- ✅ **远程控制 Siri 语音输出** - 通过 HTTP API 或云端控制中心实时修改 Siri 回复内容
- ✅ **零延迟响应** - 进程内直接操作，毫秒级响应速度
- ✅ **多设备管理** - 支持云端控制中心统一管理多台 iOS 设备
- ✅ **跨平台兼容** - 支持 Web、iOS Shortcuts、Python、Node.js 等多种客户端
- ✅ **沙盒突破** - 创新的架构设计，完美绕过 iOS 沙盒限制
- ✅ **iOS 14-16 全版本支持** - 兼容主流 iOS 版本和越狱工具
- ✅ **极简部署** - 单文件部署，无第三方依赖

## 🔍 适用场景

### 开发者 & 安全研究员
- iOS 逆向工程研究
- Siri 语音助手行为分析
- 自动化测试场景构建
- 越狱插件开发参考

### 自动化 & 智能家居
- 智能家居语音控制集成
- 自动化脚本与 Siri 联动
- 远程设备语音交互
- 企业级自动化解决方案

### 教育与演示
- iOS 系统架构教学
- 越狱技术演示
- 安全研究案例展示
- 技术分享与培训

## 🛠 技术架构

### 核心优势

本插件采用**进程内微服务架构**，将控制服务直接嵌入目标进程，实现：

- **零延迟控制** - 无需跨进程通信，直接内存操作
- **沙盒免疫** - 服务运行在目标进程内，拥有同等权限
- **极简实现** - 核心代码精简高效，易于维护和定制

### 支持的控制方式

1. **本地 HTTP 接口** - 设备本地网络访问，适合局域网场景
2. **云端控制中心 (SCC)** - 支持公网部署，远程管理多设备

## 📦 系统要求

- **iOS 版本**: iOS 14.0 及以上
- **越狱环境**: 支持 unc0ver、checkra1n、Taurine、Odyssey 等主流越狱工具
- **依赖框架**: MobileSubstrate / Substrate / libhooker
- **网络要求**: 局域网或公网访问（云端控制需要）

## 🚀 快速开始

### 安装步骤

1. 下载 `.deb` 安装包
2. 通过 Cydia/Sileo/Zebra 等包管理器安装
3. 重启 SpringBoard 或设备
4. 访问 `http://<设备IP>:12345/set/<数字>` 测试控制接口

### 基础使用

```bash
# 设置 Siri 回复为指定数字
curl http://192.168.1.100:12345/set/520

# 通过 iOS Shortcuts 控制
# 创建快捷指令：获取 URL 内容 -> http://127.0.0.1:12345/set/888
```

## 📚 功能说明

### HTTP API 接口

- **设置目标值**: `GET /set/<value>` - 设置 Siri 下次回复的目标内容
- **响应格式**: 标准 HTTP 200 响应，支持 CORS 跨域
- **端口配置**: 默认 12345（可在源码中自定义）

### 云端控制中心 (SCC)

- **设备自动注册** - 首次启动自动上报设备信息
- **心跳保活机制** - 实时显示设备在线状态
- **指令队列管理** - 支持指令下发和执行状态反馈
- **多设备矩阵** - Web 界面统一管理所有设备

## 🔐 安全说明

- 本插件仅供**合法用途**使用，包括研究、开发、教育等场景
- 请勿用于任何违法或侵犯他人权益的行为
- 使用前请确保已获得设备的所有权或使用授权
- 建议在生产环境部署时配置适当的访问控制和认证机制

## 💼 商业授权

本项目采用**商业授权**模式，面向：

- 企业级自动化解决方案提供商
- iOS 安全研究机构
- 越狱插件开发者
- 技术培训机构

**授权包含**：
- 完整源代码访问权限
- 技术文档和 API 说明
- 定制化开发支持（可选）
- 后续版本更新

## 📞 联系方式

- **GitHub Issues**: 技术问题反馈
- **商业咨询**: sushushu86

## 🔗 相关资源

- [Theos 开发框架](https://theos.dev/)
- [MobileSubstrate 文档](http://www.cydiasubstrate.com/)
- [iOS 越狱社区](https://www.reddit.com/r/jailbreak/)

## 📄 许可证

本项目采用**商业许可证**，未经授权禁止：

- 商业使用
- 二次分发
- 代码逆向和破解

---

**⚠️ 免责声明**: 本插件仅供学习和研究使用。使用者需自行承担使用本插件可能带来的任何风险和责任。开发者不对任何直接或间接损失负责。

---

**关键词**: iOS越狱插件, Siri Hook, 远程控制, MobileSubstrate, Theos开发, iOS逆向工程, 越狱Tweak, Siri定制, 自动化控制, 进程注入, iOS安全研究, 语音助手控制, 云端控制中心, 企业自动化, iOS开发工具
