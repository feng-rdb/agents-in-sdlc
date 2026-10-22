---
title: "第 12 课 - 使用 GitHub Pages 部署网站"
description: "使用 GitHub Copilot app 配置 Pages 工作流、审查拉取请求，并验证已发布的 Space Quiz。"
authors:
  - jamesmontemagno
lastUpdated: 2026-10-12
---

使用 GitHub Pages 部署 Space Quiz，让所有人都能访问。Copilot 可以准备工作流并指导部署，但仍需你负责审查更改并确认网站已上线。

本课将完成以下任务：

- 请 Copilot 配置 GitHub Pages 部署。
- 在合并前审查工作流和拉取请求。
- 跟进部署并验证已发布的网站。

## 场景

Space Quiz 已经位于 GitHub 存储库中，但仍需要一种简单的体验方式。使用 GitHub Pages 发布这个单文件网站后，用户便可通过公共 URL 访问，而且无需添加服务器或运行时依赖项。

## 请 Copilot 部署网站

在 `space-quiz` 的 Copilot app 会话中发送以下提示：

```plaintext
为此存储库启用 GitHub Pages。创建一个 GitHub Actions 工作流，在需要时构建网站并将其部署到 GitHub Pages。如果尚无 README，请添加一份介绍应用程序并说明如何在本地运行的 README。使用这些更改创建拉取请求，并在必需的检查通过后合并。持续监控部署，直到成功，然后报告线上网站的最终 URL。如果你没有启用 Pages 或合并的权限，请准确告知我需要批准或执行的操作；在网站上线之前，不要报告成功。
```

![三阶段示意图：已合并的 space-quiz 拉取请求；GitHub Actions 中成功运行的 Deploy website 工作流，包含 Build website、Upload artifact 和 Deploy to Pages 步骤；以及在 yourname.github.io/space-quiz/ 上线的 Space Quiz。](../../../_images/first-steps-app-pages-deploy.svg)

> [!WARNING]
> 此提示要求智能体创建并合并拉取请求，以及更改存储库的 Pages 设置。继续之前，请审查 diff、部署权限和 GitHub 的任何批准请求。

## 审查工作流并验证部署

1. 确认仅当存储库原本没有 README 时才添加 README。
2. 审查拉取请求中的更改，包括工作流的构建和部署步骤。
3. 仅在拉取请求所需检查通过后合并。
4. 跟进 GitHub Actions 部署运行，直到成功完成。
5. 打开报告的 URL，确认 Space Quiz 可以加载。

如果智能体无法启用 Pages 或合并拉取请求，请按照其提供的具体说明操作。只有部署成功且线上网站可以加载后，才能将任务视为完成。

## 总结和后续步骤

Space Quiz 现已作为线上网站提供，而且你已亲自验证部署，而不是依赖智能体的报告。继续学习[第 13 课：审查和后续步骤][next-lesson]。

[next-lesson]: ../13-review/
