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

视频教程：[https://space.bilibili.com/3709626/lists/4391504](https://space.bilibili.com/3709626/lists/4391504)  

### 架构

系统：Windows 10、Linux、MacOS  
开发环境：Python 3.10  
技术栈：FastAPI、LayUI、SQLite  


## 在线预览

[V0.1.3传送门（暂停）](http://124.221.164.49:51888/)

## 下载

洛曦AI官方网站：[https://ikaros.us.kg/](https://ikaros.us.kg/)  

购买咨询：QQ:327209194  

QQ频道：[https://pd.qq.com/s/f247aeq3j](https://pd.qq.com/s/f247aeq3j)  

<div>
  <img src="https://github.com/user-attachments/assets/57b1f968-9519-488d-8a35-7ca95408ea80" style="width: 250px;">
</div>

## 更新日志
- v0.3.0
  - 2025-01-15 22:51:32 +0800 : 美化：对绝大多数页面的UI进行了美化，统一样式到common.css
  - 2025-01-15 22:24:46 +0800 : 新增：过滤页面新增“音频合成前的文本切分”开关，用于控制文本切分功能，补充完善文本切分功能的调用
  - 2025-01-15 21:51:57 +0800 : 补充：预留 弹幕监听助手的其他类型消息的处理
  - 2025-01-15 21:49:28 +0800 : 新增：入场、礼物、关注答谢话术的消息优先级设置
  - 2025-01-15 21:45:52 +0800 : 开播大屏 1. 优化了队列管理： 在添加新音频时记录当前播放项 如果当前播放项被优先级排序顶到后面，强制将其移回队首 确保正在播放的音频- 始终在队首位置 2. 改进了播放列表显示： 为当前播放项添加视觉标记 通过 CSS 类区分播放状态 3. 优化了删除逻辑： 区分删除正在播放的音频和队列中的其他音频 只有删除当- 前播放的音频时才触发 playNextback
  - 2025-01-15 20:19:33 +0800 : 修复：闲时任务 优先级错误的bug
  - 2025-01-15 20:19:33 +0800 : 修复：TTS合成日志打印错误的bug
  - 2025-01-15 20:17:59 +0800 : 修复：消息优先级获取失败的bug
  - 2025-01-15 16:59:55 +0800 : 开播大屏 1. 封装了 updateQueueLength() 函数，统一处理音频队列长度的更新通知，减少代码冗余 2. 将部分非关键日志改为 console.log - 输出，减少界面日志区域的干扰
  - 2025-01-15 16:44:37 +0800 : 开播大屏 1. 添加了更详细的音频状态监听： loadeddata事件：确认音频加载成功 play事件：确认开始播放 详细的错误码处理 2. 增加了超时- 检测机制： 5秒内如果没有开始播放，自动跳到下一个 避免音频卡死在加载状态 3. 完善了日志记录： 记录音频加载、播放、完成的全过程 记录具体的错误信息和播放速度
  - 2025-01-15 16:36:16 +0800 : 定时任务添加了批量导入功能： 1. 前端： 新增单条/批量导入切换 批量导入支持JSON格式，包含触发周期和内容数组 统一设置触发类型 2. 后- 端： 新增 AddScheduleTasksMessage 模型和批量添加接口 支持多条任务同时导入
  - 2025-01-15 16:30:06 +0800 : 本次更新主要完成了本地问答的批量导入功能： 1. 新增导入方式切换（单条/批量） 2. 批量导入支持JSON格式数据，每个对象包含关键词数组和- 回答数组 3. 统一设置触发类型和最低相似度 4. 优化了表单验证，根据当前选择的导入方式进行验证
  - 2025-01-15 16:03:37 +0800 : 1. 匹配算法优化： 合并 fuzzy_match 和 similarity_match 为统一的 match_keywords 函数 添加详细日志记录，优化匹配逻辑 2. 前端界- 面优化： 添加算法说明提示 增加用户名和昵称搜索框 3. 后端功能完善： 添加用户名和昵称的搜索功能 完善超管权限和搜索逻辑
  - 2025-01-15 15:39:47 +0800 : 补充：遗漏的本地问答动态变量替换（cur_time）
  - 2025-01-15 14:11:59 +0800 : 优化：TTS合成后音频存储路径增加用户名前缀，用于隔离用户数据，防止多用户使用时的混乱
  - 2025-01-15 13:58:48 +0800 : 优化：/llm/chat接口支持流式响应，前端同样进行适配
  - 2025-01-15 13:37:18 +0800 : 新增：AnythingLLM的兼容，LLM部分新增 直接对话测试的功能，对应后端增加了/llm/chat 接口（目前只支持非流式）
  - 2025-01-15 09:16:11 +0800 : 修改：时间获取type 4，改为1000的循环，避免音频合成循环覆盖
- v0.2.1
  - 2025-01-10 20:12:00 +0800 : 补充：闲时任务 机制为待播放音频队列更新闲时 且使用LiveTalking 删减情况下，将会启动300ms的播放中检测，限制闲时任务频繁发送：闲时- 任务删除机制-待合成消息队列更新闲时
  - 2025-01-10 17:12:00 +0800 : 修复：弹幕监听助手、快手平台下，弹幕消息无法在开播大屏显示的bug
- v0.2.0
  - 2025-01-10 16:25:32 +0800 : 优化：配置页面增加帮助侧边栏，方便用户跳转视频教程
  - 2025-01-10 10:44:52 +0800 : 优化：定时任务-发送文案的文案列表改为列表随机完后进行重置操作，避免单轮循环中文案重复问题；部分日志输出
  - 2025-01-10 10:44:52 +0800 : 新增：OpenAI接口新增配置参数max_tokens/top_p/temperature/frequency_penalty/presence_penalty
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

