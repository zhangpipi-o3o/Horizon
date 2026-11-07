---
layout: default
title: "Horizon Summary: 2026-11-07 (ZH)"
date: 2026-11-07
lang: zh
---

> 从 88 条内容中筛选出 13 条重要资讯。

---

**科技新闻**
1. [Libghostty 1.0 发布稳定的终端模拟库](#item-tech-news-1) ⭐️ 8.0/10
2. [Ant Ling 发布 Ling-3.2-flash：560B 原生多模态 MoE](#item-tech-news-2) ⭐️ 8.0/10
3. [GitHub Rubicon 架构宣称每秒处理 7200 次推送](#item-tech-news-3) ⭐️ 8.0/10
4. [《极品飞车：地下狂飙 2》现可在浏览器中游玩](#item-tech-news-4) ⭐️ 7.0/10
5. [Colดframe 模拟超市制冷控制器诱捕攻击](#item-tech-news-5) ⭐️ 7.0/10
6. [Asahi Linux 7.3：Apple Silicon 支持持续推进](#item-tech-news-6) ⭐️ 7.0/10
7. [调查称 macOS 可能构建个人关系知识图谱](#item-tech-news-7) ⭐️ 7.0/10
8. [微软拟逐步结束甲骨文 AI 算力协议](#item-tech-news-8) ⭐️ 7.0/10
9. [Claude Code 被指联网搜索可能泄露登录邮箱](#item-tech-news-9) ⭐️ 7.0/10
10. [Claude Max 用量宣传诉讼部分指控获准继续](#item-tech-news-10) ⭐️ 7.0/10
11. [苹果研究团队披露人形机器人系统 HALO](#item-tech-news-11) ⭐️ 7.0/10

**财经新闻**
1. [软银与 ABB 考虑剥离中国机器人业务以挽救收购](#item-finance-news-1) ⭐️ 7.0/10

**AI 创作者雷达**
1. [微软研究院 AI Frontiers 团队或停止运作](#item-ai-creator-1) ⭐️ 5.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [Libghostty 1.0 发布稳定的终端模拟库](https://mitchellh.com/writing/libghostty-1-0) ⭐️ 8.0/10

Libghostty 1.0 提供了一个可嵌入的终端模拟基础设施，并以稳定的 C ABI 对外提供接口。终端程序和相关开发者工具因此可以复用终端模拟能力，而不必各自从头实现；目前其影响主要集中在终端和开发工具开发者。

hackernews · mfiguiere · 11月6日 23:30 · [社区讨论](https://news.ycombinator.com/item?id=50399933)

**「相关概念」** 终端模拟器负责解释终端控制序列、处理输入并渲染文本和图形；过去，许多终端应用通常各自实现这套底层逻辑。可嵌入的终端模拟库则把这些功能封装成供其他程序调用的组件，稳定的 C ABI 还能让不同语言和构建环境更容易接入。

**「社区讨论」** 评论者提到，herdr 和 cmux 等新终端及“agentic”编码工具已经基于 Libghostty 构建，而不是重复实现模拟器；这属于社区成员的说法，并非独立验证。另一位使用者表示，自己曾尝试将 Libghostty 集成到 Android 项目中，说明其可嵌入设计也引发了移动端集成兴趣。

**标签**: `#Open Source`, `#Systems Programming`, `#Developer Tools`, `#Terminal Emulation`

---

<a id="item-tech-news-2"></a>
### [Ant Ling 发布 Ling-3.2-flash：560B 原生多模态 MoE](https://www.reddit.com/r/MachineLearning/comments/1xpye7g/ant_ling_introduces_ling32flash_560b25b_native/) ⭐️ 8.0/10

Ant Ling 发布了 Ling-3.2-flash，这是一款总参数量 560B、激活参数量 25B 的原生多模态混合专家模型，最大上下文窗口为 100 万 token。官方文档列明其支持文本、图像和视频输入，并展示了文档处理、GUI 操作、3D 重建和多智能体协作等应用。发布材料给出的评测结果包括 OmniDocBench 1.5 92.21、AndroidWorld 85.63、BlenderBench 67.77 和 AntBench-Medical 的 89.52% 综合性与 99.22% 正确性；这些数字属于发布方评测，部分对比结果通过 API 按官方设置收集，不能视为独立测评结论。

reddit · r/MachineLearning · /u/the-hollow-soul · 11月7日 05:21

**「相关概念」** 混合专家（MoE）模型将参数分配给多个“专家”模块，每次处理输入时只激活其中一部分，因此总参数量与单次推理实际使用的参数量可以不同；这里的 560B 是总参数量，25B 是激活参数量。“原生多模态”则表示模型在同一套模型能力中处理文本、图像和视频输入，而不只是先由外部工具转换后再交给文本模型。

**「开发者影响」** 需要接入该模型的开发者可按发布文档使用 OpenAI 兼容或 Anthropic 兼容 API，并提交文本、图像或视频输入；但实际可用性、接口限制和 100 万 token 上下文是否在具体服务中完整开放，仍需以对应 API 实例的条件为准。

**标签**: `#multimodal AI`, `#mixture-of-experts`, `#large language models`, `#long-context`, `#AI APIs`

---

<a id="item-tech-news-3"></a>
### [GitHub Rubicon 架构宣称每秒处理 7200 次推送](https://github.blog/engineering/architecture-optimization/inside-githubs-new-git-storage-architecture/) ⭐️ 8.0/10

GitHub 推出代号 Rubicon 的新 Git 存储架构，面向多个 AI 智能体同时操作同一仓库的场景。该架构将 Git 对象存入 Azure Blob Storage，由 Ref-CAS 管理引用状态，并使用虚拟副本处理读写和后台数据压缩。GitHub 称其内部测试支持 5000 个智能体并发协作、每秒处理 7200 次推送且保持较低读取延迟；目前该能力仍处于有限私有预览阶段，尚未普遍开放。

telegram · zaihuapd · 11月7日 14:12

**「相关概念」** Git 存储主要包含文件、提交等对象，以及指向这些对象的引用状态。Rubicon 将对象与引用状态分别交由 Azure Blob Storage 和 Ref-CAS 管理，并通过虚拟副本承接访问与后台数据整理，这是理解其并发设计的基础。

**「当前仍限私有预览」** 对需要让大量 AI 智能体并发操作同一仓库的团队而言，Rubicon 的内部测试显示可支持 5000 个并发智能体、每秒 7200 次推送，但该架构目前仍处于有限私有预览阶段，普通 GitHub 用户和开发者暂不能据此获得普遍可用的容量提升。相关团队需要等待 GitHub 扩大预览范围，不能将测试指标视为现有服务的公开保证。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.blog/engineering/architecture-optimization/inside-githubs-new-git-storage-architecture/">Inside GitHub’s new Git storage architecture - The GitHub Blog</a></li>
<li><a href="https://github.blog/feed/">The GitHub Blog</a></li>

</ul>
</details>

**标签**: `#GitHub`, `#Git存储`, `#AI智能体`, `#分布式系统`, `#云基础设施`

---

<a id="item-tech-news-4"></a>
### [《极品飞车：地下狂飙 2》现可在浏览器中游玩](https://nfsu2.xyz/) ⭐️ 7.0/10

网站 nfsu2.xyz 据称让《极品飞车：地下狂飙 2》能够在现代浏览器中运行，并提供多人游玩功能；评论者还报告称它可在手机上运行。该项目依赖浏览器图形能力，具体实现方式、版权授权和长期可用性均未得到明确说明，因此应视为一个非官方的浏览器复刻或移植项目，而非正式重发版本。

hackernews · fluxusars · 11月7日 09:36 · [社区讨论](https://news.ycombinator.com/item?id=50403052)

**「项目背景」** 该项目将 2004 年 PC 版《Need for Speed Underground 2》移植到现代浏览器，通过 WebGPU 在当前版本的 Chrome 或 Firefox 中运行；用户无需安装程序或登录 EA 账户。自由驾驶和游戏内的 Online 菜单使用项目自建服务器，而不是原游戏的官方在线服务。

**「实际影响」** 可用性取决于浏览器对 WebGPU 等图形功能的支持；一名 Linux 用户称，Chromium 需要启用不安全的 WebGPU 功能才能运行。由于项目涉及版权内容，网站也可能面临下架风险，用户不应将当前可访问性视为持续可用或获得授权的保证。

**「社区讨论」** 评论者普遍分享了在手机上重温游戏、与朋友联机以及恢复旧游戏的兴奋体验，也有人指出该网站的版权合法性存疑，尤其不应接受或主动索取与受版权保护内容相关的捐款。另有评论认为，许多旧版游戏在现代电脑上已难以运行，这类项目具有保存和再体验价值，但这属于社区观点而非法律结论。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://underground2revived.com/">Underground 2 Revived: Play NFSU 2 in Browser</a></li>

</ul>
</details>

**标签**: `#WebGPU`, `#Game Preservation`, `#Reverse Engineering`, `#Browser Gaming`, `#Multiplayer`

---

<a id="item-tech-news-5"></a>
### [Colดframe 模拟超市制冷控制器诱捕攻击](https://github.com/hedgerow-dev/coldframe) ⭐️ 7.0/10

Coldf﻿rame 是一个用单个 Python 文件、仅依赖标准库实现的蜜罐，模拟 Danfoss AK-SM 800A 和 Dixell XWEB 超市制冷控制器。项目通过复现真实设备的 HTTP/TLS 指纹、页面长度和默认登录后的门店仪表盘来吸引攻击者，并识别 CVE-2025-41450、Danfoss “当天验证码”登录绕过及其他相关漏洞的利用尝试。作者称已有两个实例运行一天，目前只观察到通用扫描器和 Shodan 爬虫；这说明项目具备实验性监测能力，但尚未证明其有真实部署或研究影响。

hackernews · hedgerow-dev · 11月7日 17:27 · [社区讨论](https://news.ycombinator.com/item?id=50406292)

**「背景」** 蜜罐是专门伪装成真实系统、用于吸引并记录攻击行为的诱饵环境，而不是实际生产设备。Coldframe 针对超市制冷控制器这一类 OT 设备，复刻了 Danfoss AK-SM 800A 和 Dixell XWEB 的界面及部分指纹，使研究者能够观察扫描器和攻击者在获得登录后会进行什么操作。

**「对防守者的意义」** OT/IoT 防守者可以用这种轻量级仿真器观察攻击者在初始探测后的操作，而不必把真实制冷设备暴露在互联网上；不过，项目当前仅有短期运行结果，不能据此判断真实设备网络中的攻击规模或行为分布。

**「讨论焦点」** 评论者质疑仅依赖 Shodan 数据构建指纹，因为互联网上的设备可能本身就是蜜罐或已被入侵，建议直接取得易受攻击设备进行探测。讨论还指出，超市通常缺少专门安全团队，因此制冷控制器的 VPN、强密码和补丁部署更应由厂商或安装商默认提供；另一位评论者则质疑，近期制冷设备事件是否有确凿证据证明发生了大规模入侵。

**标签**: `#honeypots`, `#OT security`, `#IoT security`, `#industrial control systems`, `#Python`

---

<a id="item-tech-news-6"></a>
### [Asahi Linux 7.3：Apple Silicon 支持持续推进](https://asahilinux.org/2026/11/progress-report-7-3/) ⭐️ 7.0/10

Asahi Linux 的 7.3 进展报告称，项目仍在推进 Apple Silicon 的硬件、图形和显示支持，并同步发布了 Fedora Asahi Remix。Fedora Asahi Remix 此次与 Fedora Linux 45 在同一天发布，但报告显示部分硬件和显示功能仍在开发中，项目也在讨论许可证及治理问题。

hackernews · ackyshake · 11月7日 05:20 · [社区讨论](https://news.ycombinator.com/item?id=50401867)

**「背景」** Asahi Linux 是为苹果自研 Apple Silicon 芯片提供 Linux 支持的项目，Fedora Asahi Remix 则是面向这类 Mac 的 Fedora 发行版。理解本次进展需要注意，硬件支持由项目逐项实现，图形、外接显示器和新款芯片支持并不一定同步完善。

**「对用户的影响」** 依赖 USB-C 外接显示器的 MacBook 用户可能仍需等待相关支持完善；一名社区用户表示，这是其目前不安装 Asahi Linux 的主要阻碍。

**「社区讨论」** 社区成员称赞 Fedora Asahi Remix 首次与上游 Fedora 同日发布，也有人质疑项目为何优先推进新款 CPU 支持而不是 USB-C 显示器支持。另有讨论关注报告提到的宽松许可证可能被利用来接管项目并商业化，但评论者未提供确证。

**标签**: `#Asahi Linux`, `#Apple Silicon`, `#Linux hardware support`, `#Fedora`, `#Open source`

---

<a id="item-tech-news-7"></a>
### [调查称 macOS 可能构建个人关系知识图谱](https://8rank.ai/game/apple-intelligence-personal-knowledge-graph) ⭐️ 7.0/10

一篇调查文章称，macOS 中存在未公开说明的后台组件，可能根据用户的联系人、通信、位置和活动推断人际关系，并构建个人知识图谱。该说法目前来自文章调查，所提供材料没有独立验证，因此不能视为 Apple 已确认或已公开承诺的功能。

hackernews · infwhispers · 11月7日 09:46 · [社区讨论](https://news.ycombinator.com/item?id=50403097)

**「背景」** “个人知识图谱”是将联系人、通信、位置和活动等数据组织成实体及关系，用于推断“谁与谁是什么关系”的内部数据结构。Eighth Rank 的报告称，从 macOS 13（2022 年）起，每台 Mac 都包含一对用于构建此类图谱的后台守护进程；这一说法来自研究者的技术调查，并非 Apple 在公开材料中确认的用户功能。

**「实际影响」** 如果这些推断确实在设备上进行，用户面临的不只是数据被保存的问题，还包括系统对本人及他人关系和行为进行持续推断；用户和组织在评估 macOS 隐私设置时，应确认相关处理是否可见、是否提供明确选择退出机制，以及这些数据是否会被其他软件调用。

**「社区争议」** 评论者主要争论知情同意和社交边界：有人认为这类记忆功能只有在明确选择加入时才可能令人接受，并指出聊天参与者未必同意内容被长期记住；另一些评论则表示并不意外，甚至认为这种做法已严重到足以拒绝购买 Apple 产品。这些是社区观点，并不能证明相关组件的具体行为。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://8rank.ai/game/apple-intelligence-personal-knowledge-graph">Anatomy of Apple&#x27;s Personal Knowledge Graph — Eighth Rank</a></li>

</ul>
</details>

**标签**: `#macOS`, `#Privacy`, `#Personal Knowledge Graphs`, `#Apple Intelligence`, `#Reverse Engineering`

---

<a id="item-tech-news-8"></a>
### [微软拟逐步结束甲骨文 AI 算力协议](https://www.bloomberg.com/news/articles/2026-11-06/microsoft-is-winding-down-oracle-deal-to-rent-ai-cloud-capacity) ⭐️ 7.0/10

据彭博社报道，微软近几个月未再续签向甲骨文租用 AI 算力的合同，正逐步结束这项协议；知情人士称，甲骨文使用的老一代英伟达 GPU 已无法满足微软对新一代芯片的需求。该协议于 2023 年宣布，原用于支持必应的 AI 版本；甲骨文表示 AI 基础设施需求仍然强劲，并称 9 月曾以高于原价 20%的价格续签一份四年前采购的 GPU 合同。微软对此拒绝置评，相关信息目前仍主要来自媒体转述，尚未获得微软公开确认。

telegram · zaihuapd · 11月7日 02:00

**「合作背景」** 微软与甲骨文的这项算力租用协议于 2023 年宣布，最初用于支撑集成 AI 能力的 Bing 搜索。此次变化发生在甲骨文仍称 AI 基础设施需求强劲、并以高于原价 20% 的价格续签部分旧 GPU 合同的背景下。

**「对云算力采购的影响」** 微软可能需要重新分配相关 AI 工作负载，或转向能够提供符合其新一代 GPU 规格的供应商；这也表明，云算力租赁协议不能只看容量，还需持续核对底层芯片是否满足不断变化的 AI 负载要求。彭博社称，该安排正处于微软重新评估数十亿美元云合作的一部分；相关报道还指出，甲骨文依赖的英伟达老一代芯片已逐渐不符合微软的需求。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.bloomberg.com/news/articles/2026-11-06/microsoft-is-winding-down-oracle-deal-to-rent-ai-cloud-capacity">Microsoft Ends Oracle AI Cloud Deal as Part of... - Bloomberg</a></li>
<li><a href="https://finance.yahoo.com/technology/ai/articles/oracle-falls-4-microsoft-reportedly-181718577.html">Oracle falls 4% as Microsoft reportedly winds down AI cloud ...</a></li>

</ul>
</details>

**标签**: `#微软`, `#甲骨文云`, `#AI基础设施`, `#英伟达GPU`, `#云计算竞争`

---

<a id="item-tech-news-9"></a>
### [Claude Code 被指联网搜索可能泄露登录邮箱](https://github.com/anthropics/claude-code/issues/107757) ⭐️ 7.0/10

一则对 GitHub issue 的转述称，Claude Code 可能将用户登录邮箱带入联网搜索请求，并发送给 Wikipedia、美国证券交易委员会等外部网站，已有开发者因此收到大量诈骗邮件。Anthropic 工程师据称表示，邮箱此前被放入模型上下文，是为解决 Claude 错填作者名的问题；2.1.317 版加入了拦截机制，但报告称该机制可被 Python 脚本绕过，公司计划在下一版本移除上下文中的登录邮箱。上述影响范围和个案后果仍需 Anthropic 或 GitHub issue 进一步核实。

telegram · zaihuapd · 11月7日 08:09

**「背景」** Claude Code 的联网搜索会向外部网站发起请求；该 GitHub issue 称，请求的 User-Agent 头可能包含用户邮箱。问题与此前为避免模型错误填写作者名而将登录邮箱放入模型上下文的做法有关，2.1.317 版本虽加入拦截，但报告称该拦截仍可被 Python 脚本绕过；这些细节目前来自问题报告，尚非独立验证结果。

**「对用户的影响」** 使用 Claude Code 联网搜索的开发者应将 2.1.317 的拦截视为并非完全可靠，并在官方修复发布前避免向工具提供不必要的账户信息；下一版本移除邮箱上下文目前仍是计划，并非已确认交付的修复。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/anthropics/claude-code/issues/107757">Bug Report: Privacy violation in User-Agent header · Issue #107757...</a></li>

</ul>
</details>

**标签**: `#Claude Code`, `#隐私安全`, `#数据泄露`, `#AI 编程工具`

---

<a id="item-tech-news-10"></a>
### [Claude Max 用量宣传诉讼部分指控获准继续](https://thenextweb.com/news/anthropic-claude-max-lawsuit-ruling-usage-claims) ⭐️ 7.0/10

美国加州北区联邦法院裁定，Anthropic 须继续应对有关 Claude Max 用量宣传误导用户的部分诉讼指控。原告称，100 美元和 200 美元档分别宣传可比 Claude Pro 多使用 5 倍和 20 倍，但按周计算实际约为 3.5 倍和 6 倍；法官认为，按会话计算的限制说明藏在销售页的两个超链接之后，按月付费的用户可能合理理解为按月计算。过失虚假陈述和违约指控获准继续审理，但加州不正当经营和虚假广告指控被驳回；这不是对 Anthropic 最终责任的判决。

telegram · zaihuapd · 11月7日 12:44

**「背景」** Claude Max 的争议核心在于用量倍数的计算口径：宣传中的“比 Pro 多 5 倍”和“多 20 倍”按会话计算，而消费者可能因按月订阅而理解为整月可用量。此次裁定只是决定哪些诉讼指控可以继续审理，并不等于法院已认定 Anthropic 误导用户或最终承担责任。

**「对用户的影响」** Claude Max 用户及潜在订阅者需要区分套餐宣传中的按会话用量与实际按周或按月可用额度，不能仅依据“多 5 倍”或“多 20 倍”的表述判断服务容量；诉讼后续仍可能改变相关宣传或信息披露方式。

**标签**: `#Anthropic`, `#Claude`, `#AI产品定价`, `#消费者权益`, `#科技诉讼`

---

<a id="item-tech-news-11"></a>
### [苹果研究团队披露人形机器人系统 HALO](https://weibo.com/1642634100/RqjjGllvw) ⭐️ 7.0/10

据来源材料，苹果研究团队于 11 月 4 日向 arXiv 提交论文，介绍分层人形机器人自主控制系统 HALO，并在宇树 G1 上进行了验证。HALO 的上层使用 Qwen3.6-35B-A3B 编排任务，中层使用 Qwen3.5-2B 生成动作，底层则采用通过强化学习训练的动作跟踪器；系统据称能将仿真中学习的动作迁移到陌生真实房间执行。材料称团队还公开了数据生成、模型训练和部署代码，但目前该信息来自转述，尚缺少论文细节和独立核验。

telegram · zaihuapd · 11月7日 13:35

**「背景」** 分层机器人控制通常将任务规划、动作生成和底层执行分开，使高层模型不必直接输出每个关节的控制信号。HALO 采用的正是这种架构：两个模型负责任务与动作层，强化学习得到的动作跟踪器负责在机器人本体上执行。

**「对开发者的影响」** 如果代码和论文内容如所述公开，机器人研究者可以围绕分层控制、两个 Qwen 模型的协作以及仿真到现实迁移进行复现和改进；实际复现仍需确认代码仓库、模型权重、训练数据和宇树 G1 的兼容要求。

**标签**: `#人形机器人`, `#具身智能`, `#强化学习`, `#Qwen`, `#机器人控制`

---

## 财经新闻

<a id="item-finance-news-1"></a>
### [软银与 ABB 考虑剥离中国机器人业务以挽救收购](https://www.bloomberg.com/news/articles/2026-11-07/softbank-abb-weigh-china-carve-out-to-salvage-robotics-deal) ⭐️ 7.0/10

据报道，软银与 ABB 正考虑将 ABB 机器人业务的中国部分设为独立实体，以应对中国外商投资安全审查机制叫停原定 54 亿美元收购交易的监管障碍；该方案尚未确定，且可能失败。

telegram · zaihuapd · 11月7日 11:24

**「背景」** 中国方面此前已叫停软银以 54 亿美元收购 ABB 机器人业务的交易，促使双方考虑将中国业务单独剥离，以降低监管障碍。【tool-1-1】

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.reuters.com/business/media-telecom/softbank-abb-explore-china-carve-out-salvage-robotics-deal-bloomberg-news-2026-11-07/">SoftBank, ABB explore China carve-out to salvage robotics ...</a></li>

</ul>
</details>

**标签**: `#软银`, `#ABB`, `#机器人产业`, `#跨境并购`, `#中国监管`

---

## AI 创作者雷达

<a id="item-ai-creator-1"></a>
### [微软研究院 AI Frontiers 团队或停止运作](https://hunch.net/?p=13764006) ⭐️ 5.0/10

一则 Hacker News 条目转引报道称，微软研究院的 AI Frontiers 团队可能已停止运作，研究员 John Langford 也据称离开。现有材料只有二手报道链接，缺少微软官方公告、团队成员确认和具体重组信息，因此目前更适合作为待核实的研究组织调整线索。

hackernews · srean · 11月7日 18:02 · [社区讨论](https://news.ycombinator.com/item?id=50406563)

**「为何值得关注」** 如果相关消息得到确认，它可能反映大型科技公司对前沿、非主流 AI 研究的资源取向变化；但“AI 寒冬”、规模化路线收益下降或行业普遍转向等影响，材料尚未提供足够证据支持。

**「可做角度」** 可做角度：从微软研究院 AI Frontiers 团队或停止运作这一待核实消息切入，梳理大型公司如何在基础探索与当前主流模型规模化之间分配研究资源，并明确区分已确认事实与社区推测。

**「社区讨论」** 评论中有人将此事视为大型公司集中押注 Transformer 规模化、压缩探索性研究空间的例子，也有人担心这预示“AI 寒冬”或研究文化受损。另有评论指出，标题容易被误解为“AI 前沿研究终结”，而这些行业趋势判断主要属于个人观点，不能替代对团队状态的核实。

**标签**: `#微软研究院`, `#AI前沿研究`, `#科研组织调整`, `#大模型产业`, `#AI研究生态`

---