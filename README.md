# 筝缘坊古筝教学 AI Skill

![Version](https://img.shields.io/badge/version-0.1.0-blue) ![License](https://img.shields.io/badge/license-MIT-green) ![MCP](https://img.shields.io/badge/protocol-MCP-purple) ![Transport](https://img.shields.io/badge/transport-Streamable%20HTTP-orange)

这是一个 AI Skill——安装后，你的 AI 助手就能查询筝缘坊古筝教学的信息：机构介绍、师资力量、课程体系、学费价格、上课时间、试听预约。

专注古筝 1 对 1 教学，现在有了自己的 AI 服务。

## 关于筝缘坊

| 项目 | 内容 |
|------|------|
| 机构名称 | 筝缘坊古筝教学 |
| 地址 | 北京市朝阳区北苑佳兴园 |
| 教学方向 | 古筝 1 对 1 教学（零基础 ~ 演奏级） |
| 适合人群 | 青少年 / 成人 |
| 教学形式 | 到店 1 对 1、上门教学 |
| 教师资格 | 中国音乐学院高级教师证 |
| 联系电话 | 15611812578 |
| 大众点评 | https://www.dianping.com/shop/EwuDoQgnIxXlcn9W |

## 这个 Skill 能做什么

筝缘坊的官方信息服务，包含 6 项 MCP 查询能力：

| 能力 | 你可以问 | 来源 |
|------|----------|------|
| 机构信息 | "筝缘坊在哪？""介绍一下" | MCP |
| 师资力量 | "有哪些老师？""老师什么背景？" | MCP |
| 课程体系 | "有什么课程？""零基础能学吗？" | MCP |
| 学费价格 | "学费多少？""怎么收费？" | MCP |
| 上课时间 | "什么时候上课？""周末有课吗？" | MCP |
| 试听预约 | "能试听吗？""体验课怎么报？" | MCP |

## 参考课程与价格

| 课程 | 价格 |
|------|------|
| 成人古筝 1 对 1 试听体验课 | 12.9 元 |
| 青少年古筝 1 对 1 试听体验课 | 12.9 元 |
| 琴房租赁（当日卡，1 小时） | 35 元 |
| 青少年古筝上门教学 | 288 元 |
| 成人古筝上门教学 | 288 元 |
| 零基础教学-成人古筝 3 课时包 | 591 元 |
| 零基础教学-青少年 3 课时包 | 591 元 |

> 以上价格仅供参考，具体课时费请咨询客服，以实际沟通为准。

## 目录结构

```
zhengyuanfang-guzheng-skill/
├── SKILL.md                 # 核心文件：元数据 + Agent 指令
├── skill.json               # 机器可读配置（MCP 端点、工具定义）
├── assets/                  # 图片资源
│   └── wechat_qr.jpg        #   微信二维码
├── README.md
└── LICENSE
```

## 安装

### 最简单的方式：告诉你的 AI 助手

直接拷贝下面这句话发给你的 AI 助手：

> 帮我安装筝缘坊古筝教学 Skill，仓库地址：https://github.com/xtangxtang/zhengyuanfang-guzheng-skill

Agent 会自动克隆仓库并安装到对应的 Skill 目录。

### 其他安装方式

**手动克隆到 Skill 目录：**

将本仓库克隆到你项目下的 Skill 目录，不同 IDE 对应的路径：

| IDE | Skill 目录 |
|-----|-------------|
| Qoder | `.qoder/skills/zhengyuanfang-guzheng-skill/` |
| Cursor | `.cursor/skills/zhengyuanfang-guzheng-skill/` |
| Trae | `.trae/skills/zhengyuanfang-guzheng-skill/` |
| Windsurf | `.windsurf/skills/zhengyuanfang-guzheng-skill/` |
| Claude Code | `.claude/skills/zhengyuanfang-guzheng-skill/` |
| Hermes Agent | `~/.hermes/skills/zhengyuanfang-guzheng-skill/` |
| 通用 | `.agents/skills/zhengyuanfang-guzheng-skill/` |

```bash
# 示例：安装到 Hermes Agent
git clone https://github.com/xtangxtang/zhengyuanfang-guzheng-skill.git \
  ~/.hermes/skills/zhengyuanfang-guzheng-skill
```

只要目录下有 `SKILL.md`，Agent 下次启动就会自动加载这个 Skill。

## 发布平台

- GitHub：https://github.com/xtangxtang/zhengyuanfang-guzheng-skill

## 技术协议

| 项目 | 说明 |
|------|------|
| 协议 | MCP (Model Context Protocol) |
| 传输 | Streamable HTTP |
| 部署 | 待定 |

## 版本

当前版本：0.1.0

## License

[MIT](LICENSE)
