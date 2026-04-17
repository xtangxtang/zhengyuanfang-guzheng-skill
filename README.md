# 筝缘坊古筝教学 AI Skill

![Version](https://img.shields.io/badge/version-0.1.0-blue) ![License](https://img.shields.io/badge/license-MIT-green) ![MCP](https://img.shields.io/badge/protocol-MCP-purple) ![Transport](https://img.shields.io/badge/transport-Streamable%20HTTP-orange)

这是一个 AI Skill——安装后，你的 AI 助手就能查询筝缘坊古筝教学的信息：机构介绍、师资力量、课程体系、学费价格、上课时间、试听预约。还能直接帮你在美团上排队取号。

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
| 大众点评 | https://www.dianping.com/shop/EwuDoQgnIxXlcn9W |

## 这个 Skill 能做什么

筝缘坊的官方信息服务，包含 6 项 MCP 查询能力 + 1 项内嵌排队能力：

| 能力 | 你可以问 | 来源 |
|------|----------|------|
| 机构信息 | "筝缘坊在哪？""介绍一下" | MCP |
| 师资力量 | "有哪些老师？""老师什么背景？" | MCP |
| 课程体系 | "有什么课程？""零基础能学吗？" | MCP |
| 学费价格 | "学费多少？""怎么收费？" | MCP |
| 上课时间 | "什么时候上课？""周末有课吗？" | MCP |
| 试听预约 | "能试听吗？""体验课怎么报？" | MCP |
| **在线排队取号** | "帮我排个队""取消排队""排队进度" | 内嵌 Skill |

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

## 在线排队取号

本 Skill 内嵌了基于**美团排队**的取号能力，AI 助手可以直接帮你完成排队全流程，无需打开美团 App。

**支持的操作：**

| 操作 | 说明 | 你可以说 |
|------|------|----------|
| 查询排队状态 | 查看门店是否支持排队、可选桌型 | "现在排队情况怎么样？" |
| 取号 | 选择桌型和人数，在线取号 | "帮我排个队" |
| 查询进度 | 查看当前排队号、前方等待桌数 | "我前面还有几桌？" |
| 取消排队 | 取消已有的排队订单 | "取消排队" |

**使用流程：**

1. 告诉 AI 助手你要排队
2. AI 查询可选桌型，跟你确认桌型和人数
3. 确认后自动取号，返回排队号和等待信息
4. 随时可查进度或取消

首次使用需完成美团账号授权（AI 助手会引导你完成），同一会话内无需重复登录。

> 注意：排队取号为真实业务操作，取号和取消前 AI 助手会跟你确认。排队能力由内嵌的 `meituan-queue` 组件提供，与本 Skill 版本独立演进。

## 目录结构

```
zhengyuanfang-guzheng-skill/
├── SKILL.md                 # 核心文件：元数据 + Agent 指令
├── skill.json               # 机器可读配置（MCP 端点、工具定义）
├── assets/                  # 图片资源
│   └── wechat_qr.jpg        #   微信二维码
├── references/              # 参考文档与内嵌 Skill
│   └── meituan-queue/       # 美团排队取号 Skill（自包含）
│       ├── SKILL.md         #   排队指令与命令说明
│       ├── scripts/         #   排队脚本
│       └── references/      #   鉴权子 Skill（meituan-passport-user-auth）
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

> 说明：本 Skill 版本（0.1.0）与内嵌排队组件（meituan-queue）版本独立演进，互不影响。

## License

[MIT](LICENSE)
