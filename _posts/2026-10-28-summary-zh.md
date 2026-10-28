---
layout: default
title: "Horizon Summary: 2026-10-28 (ZH)"
date: 2026-10-28
lang: zh
---

> 从 99 条内容中筛选出 10 条重要资讯。

---

**科技新闻**
1. [macOS 仍信任被攻破的 eMudhra 证书](#item-tech-news-1) ⭐️ 8.0/10
2. [苹果宣布搭载 PROLED XDR 触控屏的 MacBook Pro](#item-tech-news-2) ⭐️ 7.0/10
3. [Google DeepMind 推出支持对话与音频的 Genie 4](#item-tech-news-3) ⭐️ 7.0/10
4. [EmbeddingGemma-2 零训练音频增强跃居 MAEB 榜首](#item-tech-news-4) ⭐️ 7.0/10
5. [通用反馈也能驱动事后自蒸馏](#item-tech-news-5) ⭐️ 7.0/10
6. [Qwen 权重中嵌入 32 位 RISC-V CPU](#item-tech-news-6) ⭐️ 7.0/10
7. [Google 提出“睡眠框架”缓解大模型持续学习遗忘](#item-tech-news-7) ⭐️ 7.0/10
8. [长鑫存储据称将限量生产 HBM3E](#item-tech-news-8) ⭐️ 7.0/10

**AI 创作者雷达**
1. [AI 智能体能否胜任专业税务任务？](#item-ai-creator-1) ⭐️ 6.0/10
2. [Gemini 4 Carbon：信息仍不足的模型预告](#item-ai-creator-2) ⭐️ 2.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [macOS 仍信任被攻破的 eMudhra 证书](https://emudhra.we-have-a-problem.com/apple.html) ⭐️ 8.0/10

这份报告称，macOS 系统信任库可能仍接受已被攻破的 eMudhra 证书，因此使用系统信任库的 Git 及其他系统自带工具可能受到影响。报告指出，Apple 目前提供的缓解方式需要手动修改证书链，而且后续系统更新可能撤销这一修改；这些说法尚未在所给材料中得到独立技术验证。

hackernews · galadran · 10月28日 11:03 · [社区讨论](https://news.ycombinator.com/item?id=50271640)

**「背景」** macOS 会通过受信任的根证书建立证书链，以验证网站或其他服务证书的可信性；苹果说明，配置描述文件管理的受信任根证书通常不必随配置文件重复包含。citetool-1-2

**「实际影响」** macOS 开发者和管理员需要确认所使用的 Git、curl 及其他工具是否依赖系统证书存储，并评估 Apple 建议的手动修复；若系统更新会恢复被撤销的证书，修复后仍需再次检查。

**「社区讨论」** 评论者认为问题不只涉及 Git，还可能波及依赖 macOS 系统信任库的其他工具；但也有人表示尚未确认 Homebrew 版本的 Git 和 curl 是否受影响。多名评论者批评手动编辑证书链且可能被系统更新覆盖的缓解方式，并建议开发者查看 Apple 自己的修复指引。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://support.apple.com/en-us/103723">Lists of available trusted root certificates in macOS - Apple Support</a></li>

</ul>
</details>

**标签**: `#macOS security`, `#TLS certificates`, `#Git`, `#certificate authorities`, `#developer tooling`

---

<a id="item-tech-news-2"></a>
### [苹果宣布搭载 PROLED XDR 触控屏的 MacBook Pro](https://www.apple.com/macbook-pro/proled-xdr-display/) ⭐️ 7.0/10

苹果宣布重新设计 MacBook Pro，加入 PROLED XDR 触控显示屏，并降低机身重量。帖子列出的规格显示，14 英寸机型从 3.5 磅降至 3.0 磅，16 英寸机型从 4.7 磅降至 4.0 磅，均约减重 15%，机身厚度也减少近 1 毫米。这些信息描述的是苹果的发布声明和讨论中转述的规格，当前材料没有提供独立测试或更多兼容性细节。

hackernews · etothet · 10月28日 17:10 · [社区讨论](https://news.ycombinator.com/item?id=50276940)

**「相关技术背景」** OLED 像素可自行发光，不需要 LCD 的独立背光层，因此显示模组有望更薄、更轻；这也是评论中将屏幕更换与整机减重联系起来的原因。将触控加入面向鼠标和键盘设计的桌面操作系统，则会引出界面控件尺寸与触控适配问题。

**「使用影响」** Mac 用户将面临触控输入与传统 macOS 桌面交互并存的设计问题；如果系统控件仍保持较小尺寸，触控操作可能不如鼠标精确，应用开发者也可能需要重新评估界面对手指操作的适配。

**「社区争议」** 一位评论者认为触控屏会暴露 macOS 控件过小、难以用手指准确操作的问题，并为此增加投诉和缺陷。另一位评论者则更关注重量下降，认为 OLED 不需要背光、层数更少可能有助于减重；这些是社区观点和推测，并非独立验证的工程结论。

**标签**: `#Apple`, `#MacBook Pro`, `#OLED displays`, `#Touchscreen computing`, `#Laptop hardware`

---

<a id="item-tech-news-3"></a>
### [Google DeepMind 推出支持对话与音频的 Genie 4](https://therundownai.beehiiv.com/p/google-ai-worlds-can-now-talk-back) ⭐️ 7.0/10

据《The Rundown AI》报道，Google DeepMind 推出了 Genie 4 世界模型：它能根据提示实时生成可探索的场景，并原生生成背景音和音乐；场景中的角色也可以与用户进行实时对话。用户可通过键盘移动，并用文本提示在场景内修改内容，模型据称会在输入之间保持场景连贯。报道还展示了一个模拟的 Apptronik Apollo 人形机器人在 Genie 世界中下棋，由“Gemini 4 Argon”规划棋步；Genie 4 目前处于面向受信测试者的研究预览阶段，后续将向 Google AI Ultra 订阅者和 Gemini API 合作伙伴开放。

rss · The Rundown AI · 10月28日 10:00

**「背景」** “世界模型”指能够生成并持续更新可交互环境的模型，而不只是输出静态图像或视频；外部报道将 Genie 4 描述为支持实时交互模拟、原生音频和场景控制的系统。该模型目前仍以研究预览形式提供给受信任测试者，后续才会扩大到 Google AI Ultra 用户和开发者，因此文中的机器人演示不等于已向公众开放的机器人训练产品。

**「使用影响」** 普通用户目前不能直接使用 Genie 4；开发者和研究机构需要等待后续访问资格，且下棋演示展示的是模拟机器人训练方向，并不等于 Apollo 已经获得了可部署的现实世界能力。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.testingcatalog.com/icymi-google-deepmind-previews-genie-4-with-native-audio/">Google DeepMind previews Genie 4 with native audio</a></li>
<li><a href="https://www.unite.ai/google-deepmind-rolls-out-genie-4-world-model-in-research-preview/">Google DeepMind Rolls Out Genie 4 World Model in Research Preview</a></li>

</ul>
</details>

**标签**: `#Google DeepMind`, `#World Models`, `#Generative AI`, `#Robotics`

---

<a id="item-tech-news-4"></a>
### [EmbeddingGemma-2 零训练音频增强跃居 MAEB 榜首](https://www.reddit.com/r/MachineLearning/comments/1xho7pr/r_taking_embeddinggemma2_577m_from_rank_26_to_1/) ⭐️ 7.0/10

一项 Reddit 自报实验称，通过 PCA 将 EmbeddingGemma-2（577M）的第 2 层和第 6 层 Conformer 表征压缩至 256 维，并注入其终端投影矩阵未使用的零空间，在不训练模型的情况下将 MAEB 宏平均分从 49.3% 提高到 54.4%，音频子榜排名从第 26 升至第 1。作者称文本嵌入保持逐位不变，文本到音频检索变化不超过 0.05 个百分点，但该方法需要完整的 768 维表示、失去 Matryoshka 截断选项，并会使 spoken-topic 分类从 57.2% 降至 21.3%、spoken-intent 从 97.6% 降至 88.3%；这些结果目前只是未经独立验证的个人实验报告。

reddit · r/MachineLearning · /u/JeanMichelRanu · 10月28日 13:34

**「相关概念」** EmbeddingGemma-2 的最终投影矩阵将 512 维文本表示映射到 768 维空间，因此其输出只占据其中一个 512 维子空间；与该子空间正交的 256 维方向构成可用于注入额外音频特征的零空间。该实验还利用 Conformer 的中间层表示，因为不同层可能保留不同的说话人、韵律、情绪和语义信息，而最终层更偏向与文本对齐的内容。

**「对开发者的影响」** 开发者现在可以尝试 Hugging Face 上提供的 \`BrunoHays/embeddinggemma-2-nullspace-audio\` 权重和推理示例，但这套无训练增强需要保留完整的 768 维输出才能维持文本子空间与音频特征的正交性，因此不适合依赖 512/256/128 维截断的现有流程；同时，作者报告的语音意图和主题任务存在明显下降，部署前应按具体任务重新评测。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/BrunoHays/embeddinggemma-2-nullspace-audio">BrunoHays/embeddinggemma-2-nullspace-audio - Hugging Face</a></li>

</ul>
</details>

**标签**: `#audio embeddings`, `#representation learning`, `#benchmarking`, `#Conformer models`

---

<a id="item-tech-news-5"></a>
### [通用反馈也能驱动事后自蒸馏](https://www.reddit.com/r/MachineLearning/comments/1xhv8yp/how_much_does_the_hint_matter_a_generic_feedback/) ⭐️ 7.0/10

一项面向多步金融推理的研究在 GPT-OSS-20B 上测试了事后自蒸馏：学生模型找出自己首次出错的步骤并生成批评，冻结的副本再依据该前缀和批评进行反向 KL 蒸馏。研究者称，将批评替换为固定的通用反馈语句，仍能获得约 3 个百分点的完整增益；使用大 6 倍模型生成批评也没有带来明显改进。该方法 Fin-SD 据称比依赖完整参考答案的 OPSD 少用 9.5% 的 token，但这些结果目前限于这一金融推理设置和模型。

reddit · r/MachineLearning · /u/jhzyu · 10月28日 17:52

**「方法背景」** 后见之明自蒸馏是一种训练方法：模型先生成多步解答并定位自己的第一个错误，再让冻结的模型根据错误之前的前缀和反馈进行推理，最后通过反向 KL 散度将结果蒸馏回学生模型。这里的“特权信息”指完整参考答案或详细批评所提供、但模型在实际推理时通常无法获得的额外指导。

**「实际影响」** 如果这一结果在其他任务中成立，训练流程可能无需为每个样本生成详细批评，从而降低反馈生成的 token 成本；但使用者不应将其视为普遍结论，仍需在不同模型、数据集和推理任务上验证通用反馈是否有效。

**标签**: `#self-distillation`, `#LLM reasoning`, `#machine learning research`, `#training efficiency`

---

<a id="item-tech-news-6"></a>
### [Qwen 权重中嵌入 32 位 RISC-V CPU](https://www.reddit.com/r/LocalLLaMA/comments/1xhmo1q/someone_built_a_32bit_riscv_cpu_directly_inside/) ⭐️ 7.0/10

一篇 Reddit 帖子介绍了 Qwenputer 项目，声称将一台 32 位 RISC-V CPU 直接嵌入 Qwen 模型权重，使模型能够在内部执行指令。项目页面提供了名为 “Qwen3.5-4B-Qwenputer” 的 Hugging Face 模型、技术说明和在线演示，但目前提供的材料只有帖子及其链接，尚无独立验证可确认其实现方式、可靠性或性能。帖子作者认为，这类设计可能与工具调用和计算机操作系统有关，但这仍属于推测。

reddit · r/LocalLLaMA · /u/LatentSpacer · 10月28日 12:26

**「技术背景」** Qwenputer 基于 Qwen 3-Next/3.5 的混合架构：其中四分之三的注意力层使用带状态矩阵的 Gated DeltaNet 线性循环神经网络。该项目的代码仓库此前将 CHIP-8 机器（包括 CPU、大数运算库和内存）编译进 Qwen 3.5-4B 的 Transformer 层并附加到原模型上，因此这次项目是在已有“把机器编译进模型权重”思路上的进一步实现，而不是从普通文本生成模型开始的独立 CPU 模拟器。 

**「对开发者的实际影响」** 开发者现在可以基于公开的实验代码，研究将 RV32IM（含 Zba 和大数协处理器）编译进 Qwen3.5 层、而非通过外部工具执行指令；不过这仍是实验性实现，不能据此直接认定 Qwen 已具备可靠的工具调用或计算机使用能力。相关项目还声称通过了 RISC-V 测试并运行 MicroPython，但这些结果仍需要独立复现。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://divagr.com/blog/qwenputer">Qwenputer : a fully functioning, deterministic RISC - V CPU inside...</a></li>
<li><a href="https://github.com/divagr18/qwenputer">GitHub - divagr 18/ qwenputer : A computer , compiled into the weights ...</a></li>
<li><a href="https://github.com/divagr18/qwenputer/tree/main/experimental/riscv">qwenputer/experimental/riscv at main · divagr18/qwenputer</a></li>
<li><a href="https://github.com/divagr18/qwenputer/blob/main/experimental/riscv/README.md">qwenputer/experimental/riscv/README.md at main · divagr18 ...</a></li>
<li><a href="https://startupfortune.com/a-developer-compiled-a-working-risc-v-cpu-into-a-4b-parameter-models-weights/">A developer compiled a working RISC-V CPU into a 4B parameter ...</a></li>

</ul>
</details>

**标签**: `#RISC-V`, `#Large Language Models`, `#Neural Networks`, `#Model Internals`, `#Computer Use`

---

<a id="item-tech-news-7"></a>
### [Google 提出“睡眠框架”缓解大模型持续学习遗忘](https://research.google/blog/the-sleep-framework-a-new-way-for-llms-to-retain-knowledge-in-continual-learning/) ⭐️ 7.0/10

Google Research 提出“睡眠框架”，让大语言模型在主动交互和离线巩固阶段之间周期切换，把短期上下文整合进长期参数，以缓解持续学习中的灾难性遗忘。Google 声称，该框架在 1000 万 token 长上下文、持续翻译和数学推理测试中超过 GPT-4、监督微调（SFT）等基线；目前提供的信息未说明实验规模，也没有独立验证，因此这属于研究方报告的结果，而非已确立的普遍性能结论。

telegram · zaihuapd · 10月28日 01:46

**「概念背景」** 持续学习要求模型在接收新信息后继续适应，同时保留此前获得的知识；如果直接按顺序微调，模型可能出现“灾难性遗忘”，即新任务学习损害旧任务能力。Google 的说明将这一问题与“清醒—睡眠”式的学习划分联系起来：模型在交互中获取信息，再通过离线阶段进行巩固，而不是把所有学习都视为同一种在线更新过程。

**「实际影响」** 对于需要持续吸收新知识的模型开发者，这一框架提示训练流程可加入独立的离线巩固阶段，而不必只依赖连续在线更新；但在采用前仍需核实其在目标任务上的遗忘率、训练成本和与现有模型的兼容性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://research.google/blog/the-sleep-framework-a-new-way-for-llms-to-retain-knowledge-in-continual-learning/">The sleep framework : A new way for LLMs to retain knowledge in...</a></li>
<li><a href="https://linux.do/t/topic/3087522">“睡眠”框架：大语言模型在持续学习中保留知识的一种新途径 | Google ...</a></li>

</ul>
</details>

**标签**: `#持续学习`, `#大语言模型`, `#灾难性遗忘`, `#机器学习研究`

---

<a id="item-tech-news-8"></a>
### [长鑫存储据称将限量生产 HBM3E](https://www.reuters.com/world/china/chinas-cxmt-start-advanced-ai-memory-production-despite-poor-yields-sources-say-2026-10-28/) ⭐️ 7.0/10

据两名知情人士透露，长鑫存储已向多家国内 AI 芯片设计公司送样 HBM3E，并计划在未来两个月启动限量生产。消息人士称，其当前良率约为 20% 至 30%，低于 SK 海力士约 70% 的水平；测试性能更接近 SK 海力士上一代 HBM3，预计售价也将高于海外同类产品。上述信息来自匿名消息源，尚不能视为已被公开验证的量产能力。

telegram · zaihuapd · 10月28日 06:19

**「相关概念」** HBM3E 是面向 AI 芯片的高带宽内存产品，制造良率指生产出的芯片中通过测试、可交付使用的比例。长鑫存储此次计划限量生产，核心前提是先解决高带宽内存供应受限与先进制造良率偏低之间的矛盾。

**「实际影响」** 如果计划按消息推进，国内 AI 芯片公司可能获得国产 HBM3E 样品和有限供货，但较低良率将限制可获得数量，并可能通过更高售价增加整机或芯片厂商的供应成本；采购方仍需进一步验证性能、良率和稳定供货能力。

**标签**: `#HBM3E`, `#AI芯片`, `#存储器`, `#中国半导体`, `#出口管制`

---

## AI 创作者雷达

<a id="item-ai-creator-1"></a>
### [AI 智能体能否胜任专业税务任务？](https://surgehq.ai/blog/dayjob-tax) ⭐️ 6.0/10

一项名为 Dayjob: Tax 的评测，计划考察 AI 智能体完成 50 个专业税务任务的表现。现有材料只有项目标题、公司博客链接和社区讨论，缺少任务设计、评分标准、模型配置及可复核结果，因此无法据此判断评测结论或通用智能体是否适合实际报税。受影响的场景主要是税务申报等高风险专业工作，准确率、人工复核和配套工作流仍是关键限制。

hackernews · landonxi · 10月28日 15:46 · [社区讨论](https://news.ycombinator.com/item?id=50275626)

**「为什么值得关注」** 这项评测把 AI 智能体放进了真实专业税务任务这一高风险场景，值得关注的是它如何被测量，而不只是是否得到较高分。社区中已有使用者提到 AI 生成的税务结果出现错项和金额错误，但这些个案不能代表整体性能，也不能替代对该评测原始结果的核验。

**「可做角度」** 可做角度：从“50 个税务任务到底测出了什么”切入，拆解专业 AI 智能体评测必须公开的任务边界、评分标准、模型配置、人工复核和错误代价，讨论通用模型能力与可靠税务工作流之间的差距。

**「社区怎么说」** 评论中既有人表示 AI 能帮助整理复杂报税材料、发现汇率等问题，也有人分享了金额近 2000 美元的退款差异、字段填写错误和多次返工经历。更集中的质疑是：如果只是把文件和任务交给通用智能体，而没有专业税务工作流与基础设施，这样的测试可能难以说明 AI 在真实报税中的可靠性。

**标签**: `#AI智能体`, `#税务自动化`, `#专业工作评测`, `#可靠性与准确率`, `#AI工作流`

---

<a id="item-ai-creator-2"></a>
### [Gemini 4 Carbon：信息仍不足的模型预告](https://blog.google/innovation-and-ai/models-and-research/gemini-models/introducing-gemini-4-carbon/) ⭐️ 2.0/10

目前材料只有题为“Gemini 4 Carbon”的链接和社区讨论，没有正文、发布细节或可核验的技术数据，因此无法确认其具体能力、发布时间和可用性。评论中有人提到手机端仍显示 Gemini 3.8 Pro，也有人认为未正式发布模型时展示基准测试缺乏意义；这些属于社区观察，不能替代官方发布信息。

hackernews · acossta · 10月28日 17:01 · [社区讨论](https://news.ycombinator.com/item?id=50276792)

**「内容切入角度」** 可做角度：从“模型名称或基准测试先出现，但用户暂时无法确认如何使用”这一信息断层出发，梳理 Gemini 4 Carbon 当前已知与未知的部分，避免把预告当成正式发布。

**「社区讨论」** 部分评论集中质疑 Google Gemini 产品线的命名、套餐层级和实际入口，另一些评论认为在模型尚未发布时公布基准测试的参考价值有限。个别评论提到此前类似模型可能存在延迟发布或可用性不清的情况，但这不能代表整体用户体验或官方状态。

**标签**: `#Google`, `#Gemini`, `#模型发布`, `#基准测试`

---