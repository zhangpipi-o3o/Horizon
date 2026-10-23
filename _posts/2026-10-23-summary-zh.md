---
layout: default
title: "Horizon Summary: 2026-10-23 (ZH)"
date: 2026-10-23
lang: zh
---

> 从 83 条内容中筛选出 6 条重要资讯。

---

**科技新闻**
1. [Kimi K3.1-Pro 发布，支持百万上下文](#item-tech-news-1) ⭐️ 8.0/10
2. [Google 或扩大利用 Gmail 和 Google Photos 数据投放广告](#item-tech-news-2) ⭐️ 7.0/10
3. [OpenAI 介绍 Habitat 存储扩展方案](#item-tech-news-3) ⭐️ 7.0/10

**财经新闻**
1. [国办据称出台就业友好型人工智能应用意见](#item-finance-news-1) ⭐️ 7.0/10

**AI 创作者雷达**
1. [Kimi K3.1 Pro 与 Highspeed 版本引发性能和成本讨论](#item-ai-creator-1) ⭐️ 6.0/10
2. [Dessa 展示全双工语音交互](#item-ai-creator-2) ⭐️ 6.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [Kimi K3.1-Pro 发布，支持百万上下文](https://www.kimi.ai/blog/kimi-k3-1-pro) ⭐️ 8.0/10

Kimi 正式发布 K3.1-Pro，这是其 K3.1 系列首款、约三万亿参数级模型，支持 100 万 token 上下文，现已接入 Kimi、Work、Code 和 API。官方称该模型重点提升长流程编程、三维创作、金融研究和复杂智能体任务能力；其内部高难度测试的陈述级幻觉率由 K3 的 23.4% 降至 8.3%，但这不等同于日常使用错误率。标准版之外还提供速度约快 2—3 倍的 Highspeed 版本；完整模型权重尚未发布，Kimi 计划在 2026 年 11 月 4 日前开放，因此目前的性能数据仍主要来自官方或内部测试，尚待独立验证。

telegram · zaihuapd · 10月23日 17:14

**「开放权重与当前可用性」** “开放权重”通常意味着模型参数可供用户下载、部署和自行评估，不等同于仅通过云端 API 调用。K3.1-Pro 目前已接入 Kimi、Work、Code 和 API，但完整权重仍只是计划在 2026 年 11 月 4 日前发布，因此现阶段的开放性尚未兑现。

**「对开发者的影响」** 开发者目前可通过 Kimi、Work、Code 和 API 直接试用 K3.1-Pro，但暂时不能自行部署或审计完整模型；需要本地运行、私有化部署或基于权重进行微调的团队，仍需等待官方计划在 2026 年 11 月 4 日前发布完整权重。

**标签**: `#大语言模型`, `#开放权重`, `#AI编程`, `#智能体`, `#模型基准`

---

<a id="item-tech-news-2"></a>
### [Google 或扩大利用 Gmail 和 Google Photos 数据投放广告](https://www.theverge.com/tech/1017600/google-personal-intelligence-privacy-policy-ads-update) ⭐️ 7.0/10

据报道，Google 表示可能扩大将 Gmail 和 Google Photos 中的用户数据用于广告定向的范围。现有信息只表明这是一项可能的政策或做法变化，并非已经确认全面上线；这将使相关服务用户面临更直接的隐私与数据使用选择问题。

hackernews · JustSkyfall · 10月23日 19:34 · [社区讨论](https://news.ycombinator.com/item?id=50214218)

**「相关设置」** 争议围绕 Google 的“Personal Intelligence”（个性化智能）功能展开：用户将 Gmail、Google Photos 等内容连接到 Google 服务后，系统可据此提供更个性化的建议。此次政策更新引发关注，是因为相关说明将这些已连接数据与个性化广告使用联系起来，但这并不等同于广告投放已经全面启用。

**「对用户的实际影响」** 目前尚无证据表明这一做法已经全面推出；Google 现行隐私政策仍写明，不会根据 Drive、Gmail 或 Google Photos 中的内容展示个性化广告。不过，若政策最终改变，用户应重新检查广告个性化设置和隐私政策，尤其不要把报道中的“可能”误解为已确认的功能上线。

**「社区讨论」** 部分评论者认为这进一步说明应考虑离开 Google 服务，并推荐使用 Google Takeout 迁移到自托管的 Immich；也有评论指出，欧盟用户可依据《数字市场法》选择是否关联部分 Google 服务。另有评论将“可能”解读为最终一定会实施，但这属于个人判断，并非已证实的结果。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.theverge.com/tech/1017600/google-personal-intelligence-privacy-policy-ads-update">Now Google says it might use your Gmail and Google Photos ...</a></li>
<li><a href="https://9to5google.com/2026/10/23/google-will-target-ads-based-on-gmail-photos-data-if-personal-intelligence-is-enabled/">Google will target ads based on Gmail, Photos data if ...</a></li>
<li><a href="https://www.fastcompany.com/91579039/google-promised-not-to-show-ads-based-on-your-emails-ai-could-undo-that">Google promised not to show ads based on your... - Fast Company</a></li>
<li><a href="https://policies.google.com/privacy?hl=en&amp;gl=uk">Privacy Policy – Privacy &amp; Terms – Google</a></li>

</ul>
</details>

**标签**: `#Google`, `#Privacy`, `#Targeted Advertising`, `#Gmail`, `#Google Photos`

---

<a id="item-tech-news-3"></a>
### [OpenAI 介绍 Habitat 存储扩展方案](https://openai.com/index/scaling-storage-one-billion-users-part-two) ⭐️ 7.0/10

OpenAI 在第二篇技术案例中介绍，Habitat 通过多租户架构、全球缓存和 Azure Cosmos DB 扩展 ChatGPT 存储，以服务超过 10 亿用户。OpenAI 称，这套方案使读取速度提升了 12 倍；这是厂商发布的案例描述，来源未提供独立测量结果或更具体的部署细节。

rss · OpenAI 官方新闻 · 10月23日 17:00

**「技术背景」** 多租户可让多个用户或工作负载共享底层存储资源，全球缓存则可将常用数据放到更接近用户的位置，以减少读取延迟。该方案还使用 Azure Cosmos DB 作为数据库组件，但现有材料没有说明具体的数据模型、区域配置或缓存一致性策略。

**标签**: `#Distributed Systems`, `#Cloud Infrastructure`, `#Databases`, `#Caching`, `#Scalability`

---

## 财经新闻

<a id="item-finance-news-1"></a>
### [国办据称出台就业友好型人工智能应用意见](https://mp.weixin.qq.com/s/St8URoMYcV-voM7kLAK3Bw) ⭐️ 7.0/10

据所引材料，国务院办公厅印发意见，要求在推动人工智能应用的同时减缓其对就业的替代影响。意见提出优先在劳动力紧缺、环境高危岗位推广人工智能，并稳慎控制其在劳动密集型行业的应用范围、力度和节奏。

telegram · zaihuapd · 10月23日 12:54

**「背景」** 相关就业政策将高质量、充分就业列为经济社会发展的优先目标，并提出构建就业友好型发展方式，为此次针对人工智能就业影响的安排提供了政策背景。

**「影响」** 劳动密集型企业可能需要更审慎安排人工智能应用，并提前告知受影响员工、提供转岗支持；材料未提供文件日期、完整条文或实施细则，具体影响仍不确定。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://rsj.beijing.gov.cn/xxgk/2024zcwj/202610/t20261009_4895405.html">rsj.beijing.gov.cn/xxgk/2024zcwj/202610/t20261009_4895405.html</a></li>

</ul>
</details>

**标签**: `#人工智能`, `#就业政策`, `#劳动力市场`, `#国务院政策`

---

## AI 创作者雷达

<a id="item-ai-creator-1"></a>
### [Kimi K3.1 Pro 与 Highspeed 版本引发性能和成本讨论](https://www.kimi.ai/blog/kimi-k3-1-pro) ⭐️ 6.0/10

材料围绕 Kimi K3.1 Pro 和 K3.1 Pro Highspeed 展开，并附有 Kimi Code 模型文档及第三方评测链接，但没有提供完整的官方规格、发布日期或可复核测试细节。社区评论称，K3.1 Pro 在 Pac-Man 基准中以 93 分追平 Sonnet 5.5，单次测试成本和耗时约为 0.68 美元、11 分钟，对比 Sonnet 5.5 的 1.61 美元、14 分钟；这些数据仍属于第三方测试，不能据此确认普遍性能优势。讨论还涉及订阅额度体验和网络安全能力边界，部分用户称 99 美元月费方案在一次会话后约 47 分钟触发五小时配额限制，另有评论提到官方材料称其开放权重版本会刻意低于自身可达到的前沿网络攻击能力。

hackernews · Jowsey · 10月23日 16:59 · [社区讨论](https://news.ycombinator.com/item?id=50212065)

**「为什么现在值得注意」** 如果相关版本和第三方数据得到进一步核实，它可能影响代码模型的成本与选型比较；但目前性能领先、订阅额度的普遍性以及网络安全能力差异都尚未得到充分验证。

**「可做角度」** 可做角度：围绕“低价代码能力”与“实际可用性”之间的落差，核对 Kimi K3.1 Pro 的第三方基准、计费耗时、订阅配额和安全能力边界，而不是直接下结论称其全面超过其他模型。

**「社区怎么说」** 社区一方面关注 Pac-Man 基准中接近 Sonnet 5.5 的价格与成绩，另一方面质疑订阅方案的额度限制，并有人据此推断中美前沿模型差距正在缩小。也有用户分享了模型回答更直接、甚至带有争辩性的主观体验，但这些评论分别代表个体测试或感受，不能视为普遍结论。

**标签**: `#Kimi`, `#大模型评测`, `#代码生成`, `#模型定价`, `#AI安全`

---

<a id="item-ai-creator-2"></a>
### [Dessa 展示全双工语音交互](https://block.xyz/dessa) ⭐️ 6.0/10

Block 发布了名为 Dessa 的全双工语音模型展示，主张其交互方式更接近人类实时对话，模型可以在用户说话时同时响应。现有材料只有宣传标题、演示和社区评论，没有论文、代码、基准测试或实际产品信息，因此其技术优势和实际价值尚未得到公开证据验证。它可能涉及语音助手、实时对话和 AI 陪伴等场景，但目前无法确认具体影响。

hackernews · dsr12 · 10月23日 19:09 · [社区讨论](https://news.ycombinator.com/item?id=50213925)

**「为什么值得注意」** 这次发布把关注点从“语音作为模型的输入输出接口”推向了打断、抢话和同时说话等全双工交互方式。演示引发了对拟人化效果、使用价值及潜在用途的讨论，但这些影响仍未被产品数据或独立测试证实。

**「可做角度」** 可做角度：拆解全双工语音演示中“同时说话”和“自然对话”的差别，重点核查打断时机、语音表现与可验证评测，而不是仅凭拟人化观感判断模型能力。

**「社区怎么看」** 评论普遍注意到 Dessa 的全双工和拟人化表现，但对其价值判断存在分歧：有人认为语音本身可能就是主要卖点，也有人认为缺少足够的推理能力便难以提供独立价值。多位评论者还觉得演示中的频繁打断、笑声和“AI 伴侣”式对话显得生硬或令人不适；这些属于社区体验和推测，不能替代正式评测。

**标签**: `#全双工语音`, `#语音模型`, `#实时对话`, `#人机交互`, `#AI陪伴`

---