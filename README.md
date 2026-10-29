# AI 电商视频智能体 | Clipcat Skill

本仓库集成了 [Clipcat 官方 Skill](https://github.com/Clipcat-ai/clipcat-skill)，用于电商视频调研、参考视频结构分析和原创商品视频制作。

## 已集成
- [Clipcat Skill](skills/clipcat/SKILL.md)：官方 Agent Skill 命令说明
- 上游来源：https://github.com/Clipcat-ai/clipcat-skill

## Windows PowerShell 安装
在**自己的电脑**上先运行 `clipcat --version` 检查是否已安装，若未安装请先审查官方安装脚本，再执行：

```powershell
irm https://clipcat.ai/cli.ps1 | iex
clipcat --version
```

在 https://clipcat.ai/workspace?modal=settings&tab=apikeys 获取自己的 API Key，**只在本地**配置：

```powershell
clipcat config --api-key YOUR_API_KEY --base-url https://clipcat.ai
```

不要把密钥放进 GitHub 文件、提交记录或日志。

## 使用方法
在支持 Agent Skills 的客户端中加载 `skills/clipcat/SKILL.md`，并保证本机可以调用 Clipcat CLI。使用之前检查 `clipcat -h` 和相关子命令 `-h`。查看支持的视频模型执行 `clipcat models`。

示例任务：以桌脚垫产品照片与获得授权的参考视频，分析开场钩子、镜头节奏和卖点，先输出原创改编脚本与生成费用，**等我确认后**再生成。要求不出现真人、突出硅胶套体与约 1mm 的薄毛毡底，避免夸大宣传。

Clipcat 的视频生成可能产生费用，生成和发布前必须检查相关内容、费用与确认机制。平台接口覆盖范围以官方 CLI 为准；不能视为已接通拼多多发布接口。

## 运行说明
GitHub 仓库存放 Skill 配置与说明，并不会自动常驻运行 Clipcat。实际执行需要本地 Agent 或另行部署的执行器。 
