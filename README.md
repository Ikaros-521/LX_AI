<div align="center">
  <a href="#">
    <img src="https://raw.githubusercontent.com/LuoXi-Project/LX_Project_Template/refs/heads/main/ui/logo.png" width="240" height="240" alt="点我跳转文档">
  </a>
</div>

<div align="center">

# ✨ 洛曦 AI  ✨

[![][python]][python]
[![][github-stars-shield]][github-stars-link]
[![][github-forks-shield]][github-forks-link]
[![][github-issues-shield]][github-issues-link]  
[![][github-contributors-shield]][github-contributors-link]

</div>

## 前言

### 介绍

AI 无人直播系统  
用户管理：同时多用户登录使用  
配置管理：支持同时运行多个配置，一台电脑多平台直播  
AI集成：对接主流LLM、TTS  
多平台支持：Windows/Linux/Mac OS  

### 架构

系统：Windows 10、Linux、MacOS  
开发环境：Python 3.10  
技术栈：FastAPI、LayUI、SQLite  


## 在线预览

[V0.1.3传送门](http://124.221.164.49:51888/)

## 下载

洛曦AI官方网站：[https://ikaros.us.kg/](https://ikaros.us.kg/)  

购买咨询：QQ:327209194  

QQ频道：[https://pd.qq.com/s/f247aeq3j](https://pd.qq.com/s/f247aeq3j)  

<div>
  <img src="https://github.com/user-attachments/assets/57b1f968-9519-488d-8a35-7ca95408ea80" style="width: 250px;">
</div>

## 更新日志

- v0.1.4
  - 2025-01-06 11:29:25 +0800 : 修复：配置列表 搜索配置 无法搜索的bug 以及 搜索数量不对的bug 以及 管理员不能搜其他用户数据的bug
  - 2025-01-06 10:19:10 +0800 : 优化：数据库 配置列表数据整理；删除日志表数据
  - 2025-01-06 10:14:48 +0800 : 修复：前端显示两次直播间消息的bug（根因：过滤触发后由于有其他任务的数据会走这发给前端显示，导致已显示数据在此显示。如果统一到此显- 示，则会有其他数据不完整的问题）
  - 2025-01-06 10:01:12 +0800 : 新增：弹幕模板、LLM回复模板功能（在消费者中调用）；修复：LLM响应内容长度过滤传参错误bug
  - 2025-01-05 23:52:38 +0800 : 优化：开播大屏 打开时自动连接WebSocket
  - 2025-01-05 21:01:10 +0800 : 新增：弹幕&回复模板 页面，新增功能“念弹幕”，补充对应的消息优先级和监听页的消息显示
  - 2025-01-05 14:31:39 +0800 : 修复：LiveTalking配置下，大屏合成音频没有走LT过的不过
  - 2025-01-04 18:03:58 +0800 : 新增：过滤新增用户名黑名单功能；优化：日志提示，过滤页面UI
  - 2025-01-04 18:03:58 +0800 : 新增：过滤新增弹幕过滤前后缀、弹幕触发前后缀、表情过滤功能

- v0.1.3
  - 2024-12-29 11:14:05 +0800 : 优化：密钥验证加入循环，方便使用；依赖补充- 版本号
  - 2024-12-27 16:56:22 +0800 : 新增：配置列表新增 首次进入更新配置任务状态- 功能，后端查询当前运行中任务情况已更新状态
  - 2024-12-26 11:06:02 +0800 : 优化：获取配置成功的提示隐藏；配置列表冻结- 右侧操作列
  - 2024-12-26 09:29:56 +0800 : 修复：proxy模型定义了json变量的bug，改为- json_data
  - 2024-12-25 17:30:42 +0800 : 修复：批量新增违禁词 插入没有检查用户ID导致- 的插入失败的bug；优化：common.js的add_config的提示直接使用后端返回的提示- 进行显示
  - 2024-12-25 17:23:15 +0800 : 修复：配置列表 编辑 配置页面，无法读取配置- 到配置dom渲染的bug；优化：配置列表的表格宽度
  - 2024-12-25 16:49:29 +0800 : 新增：用户登录校验账号过期时间
  - 2024-12-25 16:42:51 +0800 : 强制合并
  - 2024-12-25 16:38:39 +0800 : 新增：用户注册功能；新用户免费试用天数通过- config可以配置；优化：用户名密码校验提取到单独的js
  - 2024-12-25 11:26:44 +0800 : 优化：LiveTalking配置提示
  - 2024-12-25 11:26:44 +0800 : 修改：外置程序日志文件格式改为txt，方便普通- 用户查看
  - 2024-12-25 11:25:39 +0800 : 新增：log文件夹的提交忽略
  - 2024-12-25 11:24:17 +0800 : 新增：GSV的前端程序开关功能，配合config配置- 设置bat路径使用；GSV新增程序运行日志，可以手动获取运行日志内容；GSV新增合- 成音频功能，可以直接进行TTS合成测试；main控制外置程序初始化和退出关闭
  - 2024-12-24 10:54:05 +0800 : Merge branch 'main' of https://github.- com/LuoXi-Project/LX_AI
  - 2024-12-24 10:54:01 +0800 : 优化：前端消息提示
  - 2024-12-24 10:25:33 +0800 : 优化：TTS合成处理改为异步等待，避免音频合成- 错乱bug


[python]: https://img.shields.io/badge/python-3.10+-blue.svg?labelColor=black
[back-to-top]: https://img.shields.io/badge/-BACK_TO_TOP-black?style=flat-square
[github-action-release-link]: https://github.com/actions/workflows/LuoXi-Project/LX_Project_Template/release.yml
[github-action-release-shield]: https://img.shields.io/github/actions/workflow/status/LuoXi-Project/LX_Project_Template/release.yml?label=release&labelColor=black&logo=githubactions&logoColor=white&style=flat-square
[github-action-test-link]: https://github.com/actions/workflows/LuoXi-Project/LX_Project_Template/test.yml
[github-action-test-shield]: https://img.shields.io/github/actions/workflow/status/LuoXi-Project/LX_Project_Template/test.yml?label=test&labelColor=black&logo=githubactions&logoColor=white&style=flat-square
[github-codespace-link]: https://codespaces.new/LuoXi-Project/LX_Project_Template
[github-codespace-shield]: https://github.com/codespaces/badge.svg
[github-contributors-link]: https://github.com/LuoXi-Project/LX_Project_Template/graphs/contributors
[github-contributors-shield]: https://img.shields.io/github/contributors/LuoXi-Project/LX_Project_Template?color=c4f042&labelColor=black&style=flat-square
[github-forks-link]: https://github.com/LuoXi-Project/LX_Project_Template/network/members
[github-forks-shield]: https://img.shields.io/github/forks/LuoXi-Project/LX_Project_Template?color=8ae8ff&labelColor=black&style=flat-square
[github-issues-link]: https://github.com/LuoXi-Project/LX_Project_Template/issues
[github-issues-shield]: https://img.shields.io/github/issues/LuoXi-Project/LX_Project_Template?color=ff80eb&labelColor=black&style=flat-square
[github-license-link]: https://github.com/LuoXi-Project/LX_Project_Template/blob/main/LICENSE
[github-license-shield]: https://img.shields.io/github/license/LuoXi-Project/LX_Project_Template?color=white&labelColor=black&style=flat-square
[github-release-link]: https://github.com/LuoXi-Project/LX_Project_Template/releases
[github-release-shield]: https://img.shields.io/github/v/release/LuoXi-Project/LX_Project_Template?color=369eff&labelColor=black&logo=github&style=flat-square
[github-releasedate-link]: https://github.com/LuoXi-Project/LX_Project_Template/releases
[github-releasedate-shield]: https://img.shields.io/github/release-date/LuoXi-Project/LX_Project_Template?labelColor=black&style=flat-square
[github-stars-link]: https://github.com/LuoXi-Project/LX_Project_Template/network/stargazers
[github-stars-shield]: https://img.shields.io/github/stars/LuoXi-Project/LX_Project_Template?color=ffcb47&labelColor=black&style=flat-square
[pr-welcome-link]: https://github.com/LuoXi-Project/LX_Project_Template/pulls
[pr-welcome-shield]: https://img.shields.io/badge/%F0%9F%A4%AF%20PR%20WELCOME-%E2%86%92-ffcb47?labelColor=black&style=for-the-badge
[profile-link]: https://github.com/LuoXi-Project

