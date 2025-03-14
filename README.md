# 📰 AstrBot Daily News

<div align="center">

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
![Python Version](https://img.shields.io/badge/Python-3.10%2B-blue)
![Platform](https://img.shields.io/badge/Platform-Windows%20%7C%20Linux%20%7C%20macOS-lightgrey)
[![PRs Welcome](https://img.shields.io/badge/PRs-Welcome-brightgreen)](CONTRIBUTING.md)
[![Contributors](https://img.shields.io/github/contributors/anka-afk/astrbot_plugin_daily_news?color=green)](https://github.com/anka-afk/astrbot_plugin_daily_news/graphs/contributors)
[![Last Commit](https://img.shields.io/github/last-commit/anka-afk/astrbot_plugin_daily_news)](https://github.com/anka-afk/astrbot_plugin_daily_news/commits/main)

</div>

<div align="center">

[![Moe Counter](https://count.getloli.com/get/@DailyNewsPlugin?theme=moebooru)](https://github.com/anka-afk/astrbot_plugin_daily_news)

</div>

每日 60 秒新闻推送插件 - 自动推送每日热点新闻，让你的群聊成员快速了解全球大事！

## ✨ 功能特性

- 🕒 支持定时推送，每日固定时间更新
- 📊 图文并茂，内容丰富
- 🔄 支持手动触发更新
- 🎯 支持多群组推送
- 📱 同时支持图片与文字模式
- 🌐 数据源可靠稳定

## 🛠️ 配置说明

在插件配置中设置以下参数:

```json
{
  "target_groups": {
    "description": "需要推送新闻的群组ID列表",
    "type": "list",
    "hint": "填写需要接收每日新闻推送的群号，如: [123456, 789012]",
    "default": []
  },
  "push_time": {
    "description": "每日推送时间",
    "type": "string",
    "hint": "每天的新闻推送时间，格式为 HH:MM，如: 08:00",
    "default": "08:00"
  },
  "show_text_news": {
    "description": "是否同时推送文字版新闻",
    "type": "boolean",
    "hint": "设置为true会同时发送图片和文字，false则只发送图片",
    "default": false
  }
}
```

## 📝 使用命令

### 查看插件状态

```
/news_status
```

显示当前配置的目标群组、推送时间、是否显示文字新闻，以及距离下次推送的剩余时间。

### 手动获取新闻

```
/get_news [模式]
```

支持的模式:

- `image` - 仅推送图片新闻
- `text` - 仅推送文字新闻
- `all` - 同时推送图片和文字新闻（默认）

此命令会将新闻推送到配置的所有目标群组。

## 🔄 版本历史

- v1.0.0
  - ✅ 实现基础的新闻监控与推送
  - ✅ 支持图片和文字两种模式
  - ✅ 支持定时和手动推送功能
  - ✅ 多群组推送支持

## 💡 使用提示

1. 为获得最佳体验，建议将推送时间设置在早晨（如 08:00），帮助群成员快速了解每日新闻
2. 如果群内成员更喜欢文字阅读，可以将 `show_text_news` 设为 true
3. 使用 `/news_status` 命令可随时查看插件运行状态和下次推送时间
4. 如遇特殊情况需要立即获取新闻，可使用 `/get_news` 命令手动触发

## 👥 贡献指南

欢迎通过以下方式参与项目：

- 🐛 提交 Issue 报告问题
- 💡 提出新功能建议
- 🔧 提交 Pull Request 改进代码

## 🌟 鸣谢

- 感谢 [每日 60 秒新闻 API](https://60s-api.viki.moe/v2/60s) 提供的数据支持
- 感谢所有为这个项目做出贡献的开发者！

---

> 信息知天下，六十秒读懂世界 📰
