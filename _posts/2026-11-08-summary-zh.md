---
layout: default
title: "Horizon Summary: 2026-11-08 (ZH)"
date: 2026-11-08
lang: zh
---

> 从 51 条内容中筛选出 4 条重要资讯。

---

**科技新闻**
1. [高盛据报限制银行家和交易员使用 Claude Code](#item-tech-news-1) ⭐️ 7.0/10
2. [Outlook.com 或拒收未配置 DMARC 域名的邮件](#item-tech-news-2) ⭐️ 7.0/10
3. [报告称中国模型占开源模型企业支出 89%](#item-tech-news-3) ⭐️ 7.0/10

**AI 创作者雷达**
1. [284B DeepSeek 的低配本地运行尝试](#item-ai-creator-1) ⭐️ 6.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [高盛据报限制银行家和交易员使用 Claude Code](https://www.thestateofai.com/news/goldman-sachs-claude-code-traders-bankers) ⭐️ 7.0/10

据报道，高盛已限制银行家、交易员等非工程岗位员工使用 Anthropic 的 Claude Code。现有信息未说明限制的具体范围、执行时间或是否永久实施；这反映出编码代理在金融机构中面临的安全、合规与按量计费成本问题，但并非已独立验证的部署评测结果。

hackernews · TheWiggles · 11月8日 18:16 · [社区讨论](https://news.ycombinator.com/item?id=50415628)

**「相关背景」** 彭博社此前报道，高盛在评估生产力与风险后，限制大多数员工使用面向编程的高级人工智能工具；这为此次针对 Claude Code 的限制提供了直接背景。\[来源报道\]

**「社区讨论」** 部分评论认为，真正的风险在于让半自动编码代理运行于同时可访问客户或交易信息、电子邮件、互联网及内部网络的办公电脑上，这种权限组合难以安全审计。另一些评论称，其所在组织收回 Claude 使用权限主要是因为持续超出预算，并指出缺乏稳定的标准化计费可能让采用固定价格和超额限流的竞争产品更具吸引力；这些是社区观点或个人经历，并非高盛已确认的原因。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.bloomberg.com/news/articles/2026-11-02/goldman-restricts-traders-and-bankers-from-using-some-ai-tools">Goldman Restricts Traders and Bankers From Using Some AI ...</a></li>

</ul>
</details>

**标签**: `#AI coding agents`, `#cybersecurity`, `#enterprise software`, `#financial technology`, `#AI governance`

---

<a id="item-tech-news-2"></a>
### [Outlook.com 或拒收未配置 DMARC 域名的邮件](https://mailroute.net/blog/outlook-rejecting-email-without-dmarc) ⭐️ 7.0/10

一篇文章称，Outlook.com 可能开始永久拒收来自未配置 DMARC 域名的邮件，但现有材料不足以确认这是面向所有发件域的统一政策。DMARC 用于声明域名的邮件认证策略；该报道引发了对 Outlook 过滤范围、通知透明度和邮件投递可靠性的讨论。

hackernews · xmddmx · 11月8日 19:20 · [社区讨论](https://news.ycombinator.com/item?id=50416158)

**「背景」** DMARC 是通过 DNS 发布的邮件认证与处理策略，用于让收件方根据 SPF、DKIM 及域名对齐结果判断邮件是否可信。此前已有资料称 Microsoft 自 2025 年 5 月 5 日起就要求发往 Outlook 的邮件具备 DMARC，Microsoft 也提供了相应的配置指南；此次报道所称变化，是这一要求开始以对缺少记录的域名返回永久失败的方式体现出来。

**「对发件方的影响」** 向 Outlook.com 发信的域名管理员应检查并配置 DMARC，同时核对退信日志中的 SMTP 5xx 错误；在政策范围尚不明确的情况下，不能仅凭这篇报道判断所有未配置 DMARC 的邮件都会被拒收。

**「社区讨论」** 部分评论者认为，拒收未配置 DMARC 本身合理，且 Outlook 会发送 5xx 永久失败通知；另一些自建邮件服务器管理员则称，即使 SPF、DKIM 和 DMARC 均正确，邮件仍可能因不公开的封锁名单而被接受后消失，因此质疑其过滤机制的透明度。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://dmarcguard.io/blog/microsoft-dmarc-enforcement/">Does Outlook Require DMARC? Yes, Since May 2025 | DMARCguard</a></li>
<li><a href="https://learn.microsoft.com/en-us/defender-office-365/email-authentication-dmarc-configure">Set up DMARC to validate email in Microsoft 365 - Microsoft ...</a></li>

</ul>
</details>

**标签**: `#Email Authentication`, `#DMARC`, `#Email Deliverability`, `#Microsoft Outlook`

---

<a id="item-tech-news-3"></a>
### [报告称中国模型占开源模型企业支出 89%](http://z.ai/) ⭐️ 7.0/10

Menlo Ventures 一份报告称，在其对近 400 名美国企业决策者的调查中，中国模型占企业开源模型支出的 89%。其中，月之暗面 Kimi 占 61%，DeepSeek 占 15%，Z.ai 的 GLM 系列占 11%，Meta Llama 占 7%。不过，开源模型整体仅占企业模型支出的 4%，Anthropic 与 OpenAI 的 API 合计占 86%；这些数字来自报告转述，尚未经原始报告独立核实。

telegram · zaihuapd · 11月8日 03:26

**「口径说明」** 这里的“开源模型企业支出”是企业模型支出的一个子集，并不代表开源模型在企业市场中的整体份额。该调查针对近 400 名美国企业决策者，因此其 89% 的比例反映的是美国企业受访者报告的支出结构，而非全球所有企业的直接统计。

**「解读限制」** 企业不应将 89% 视为全球所有模型采购的份额：该调查对象是美国企业决策者，且“开源模型企业支出”的统计口径可能影响比较结果。对采购团队而言，更直接的结论是，调查显示开源模型在企业模型支出中的总体占比仍只有 4%。

**标签**: `#大语言模型`, `#开源模型`, `#AI产业`, `#企业软件`, `#市场分析`

---

## AI 创作者雷达

<a id="item-ai-creator-1"></a>
### [284B DeepSeek 的低配本地运行尝试](https://github.com/synchopate/llama-modchip) ⭐️ 6.0/10

GitHub 项目 Llama-modchip 声称可在 64GB 内存、无 GPU 的条件下运行 284B 参数的 DeepSeek 模型，但现有材料没有提供可复核的量化方案、推理速度、输出质量或硬件测试细节。项目的实际可用性和量化带来的性能损失仍需查看仓库与基准测试；受影响的主要是希望在普通工作站上进行大模型本地推理的用户。

hackernews · joshcsimmons · 11月8日 10:22 · [社区讨论](https://news.ycombinator.com/item?id=50411961)

**「为何值得关注」** 这个项目把“超大模型能否在低配硬件上运行”这一问题具体化了，但目前已确认的只是项目标题中的硬件与模型规模主张，尚不能据此判断它具备实用速度或可接受的效果。

**「内容切入角度」** 可做角度：从 64GB 内存运行 284B 模型的主张出发，拆解大模型本地推理中最关键的量化方案、速度和质量代价，而不是把“能启动”直接等同于“可用”。

**「社区讨论」** 评论一方面认为更低的硬件门槛正在让本地 AI 更容易尝试，并分享了低于 800 美元工作站运行其他模型的经验；另一方面，评论者强调激进量化可能带来明显质量下降，且有人在其他模型上未观察到该仓库相对 llama.cpp 的明确优势，也有人指出项目没有清楚说明量化细节。

**标签**: `#本地推理`, `#模型量化`, `#DeepSeek`, `#大模型硬件`, `#开源项目`

---