# 中英文 AI 写作模式检测清单

> 借鉴 [Humanizer 24 Pattern](https://clawhub.ai/skills/humanizer) 分类体系，适配中文学术场景
> 核心原则：**不只做减法（去除AI痕迹），还要做加法（注入灵魂）**

---

## 第一部分：中文模式

### C1. 过度强调意义/重要性（Inflated Symbolism）

**特征词**：具有重要意义、发挥了关键作用、不可忽视的是、标志着、奠定了…基础、为…提供了重要支撑、扮演着…角色、深刻影响了

**问题**：AI 习惯给每件事编织"宏大意义"，人类写论文更务实，只说做了什么、结果如何。

```
❌ AI原文：
个性化教学方案的实施具有重要的意义，它不仅显著提升了学生的学习效果，更标志着教育模式转型的关键转折点，为未来的教育改革奠定了坚实基础。

✅ 人类改写（只陈述事实，不加"大词"）：
实施个性化方案后，学生成绩平均提升 23%。这一数据指向一个判断：传统的统一教学并非最优解。

// 删除了"重要意义""关键转折点""奠定基础"，改为一句话+一个数据+一个判断
```

### C2. 虚假的"-性/化"深度分析（Superficial -izing/izing Analyses）

**特征词**：充分彰显了、生动体现了、完美诠释了、深刻反映了、系统揭示了、全面展现了、集中凸显了

**问题**：AI 喜欢在句尾用"彰显/体现/反映"来制造"有分析深度"的假象，实际上什么都没说。

```
❌ AI原文：
实验数据的分析结果充分彰显了该方法的优越性，系统反映了研究设计的科学性，全面展现了跨学科协作的必要性。

✅ 人类改写：
该方法在 120 组对比实验中，91 组优于基线模型。研究设计的核心考量是消除样本偏差——为此我们做了三层交叉验证。
```

### C3. 四字格堆砌 / 成语轰炸（Promotional/Flowery Language）

**特征词**：日新月异、突飞猛进、与时俱进、前所未有的、举足轻重、毋庸置疑、源远流长、博大精深

**问题**：AI 偏爱用四字成语/套话来填充字数，人类在学术写作中很少连续使用。

```
❌ AI原文：
随着信息技术的日新月异，人工智能技术取得了突飞猛进的发展，在教育领域发挥着举足轻重的作用，为教学模式带来了前所未有的变革。

✅ 人类改写：
过去五年，AI 在教育领域的应用进入了快速增长期。从智能批改到自适应学习，技术正在改变课堂的面貌——虽然距离"颠覆"还有距离。
```

### C4. "不仅…更…" 否定式排比（Negative Parallelisms）

**特征词**：不仅是…更是…、不是…而是…、与其说是…不如说是…、不只是…更重要的是…

**问题**：AI 极其频繁地使用这种"先否定/弱化→再拔高"句式。

```
❌ AI原文：
该方法不仅是技术层面的创新，更是对传统教育理念的一次深刻反思。它不只是一个工具，更是一种全新的思维方式。

✅ 人类改写：
这个方法的核心创新在于：让计算资源按需分配，而非固定预配。理念上它回归了"够用就好"的原则——这在云计算泡沫期反而有点反直觉。
```

### C5. 三连排比（Rule of Three）

**特征词**：准确性、效率和鲁棒性 / 创新、协调、绿色、开放、共享（五个也算）/ 促进…推动…保障… / 从…到…再到…

**问题**：AI 有强制分组倾向（3 是其舒适区），人类只有在刻意修辞时才用。

```
❌ AI原文：
该研究通过分析数据、优化算法、改进流程，全面提升了系统的准确性、效率和鲁棒性。

✅ 人类改写：
研究从三个方向入手：修正数据偏差、替换瓶颈算法、简化部署流程。最终系统准确率提升了 12%，处理时间缩短了一半。
```

### C6. 同义反复 / 优雅变异（Elegant Variation / Synonym Cycling）

**特征词**：同一概念在一段内反复换词——算法→方法→策略→方案→技术→手段

**问题**：AI 的重复惩罚机制导致它不敢用同一个词两次，结果一段内出现 5-6 个同义词，看着就像 AI 写的。

```
❌ AI原文：
本研究提出的新算法在性能上优于传统方法。该策略的计算效率显著提高，这一方案在大规模数据上表现稳定，该技术的实际应用前景广阔。

✅ 人类改写（就直说"算法"，不用来回换词）：
本研究的算法在性能上优于传统方法。它在计算效率、大规模稳定性上都有明显改进，实际应用前景也值得关注。
```

### C7. 空洞正面结尾（Generic Positive Conclusions）

**特征词**：未来可期、前景广阔、意义深远、开启新篇章、值得期待、任重道远

**问题**：论文最后一段或每节结尾 AI 都喜欢上一个"感情升华"。人类通常做总结、列不足、说下一步。

```
❌ AI原文：
综上所述，本研究意义深远，展望未来前景广阔。开启人工智能教育应用的新篇章，值得学界和社会各界共同期待。

✅ 人类改写：
总结来说，本研究的贡献在于用实验验证了个性化学习在中等规模班级的可行性。局限也很明显：样本仅来自一所学校，追踪周期只有一学期。下一步将扩展到三所学校，并延长到两年追踪。
```

### C8. 模糊归因（Vague Attributions）

**特征词**：有学者指出、研究表明、业内专家认为、相关文献显示、有关研究证明、权威数据显示

**问题**：AI 编造"有学者"来支撑论据，但从不给出具体是谁、什么时间、什么数据。

```
❌ AI原文：
相关研究表明，人工智能技术的应用能够有效提升教学质量，这一点已在多方研究中得到验证。

✅ 人类改写：
2023 年王某团队对华东地区 24 所学校的对照实验表明，使用 AI 辅助教学后，学生标准化测试成绩平均提高 15.3 个百分点。
```

### C9. 模板化的"挑战与展望"章节（Outline-like Challenges Section）

**特征词**：尽管取得了进展，但仍面临诸多挑战… / 未来需要进一步研究…

**问题**：几乎每篇 AI 论文的最后都有这种"尽管…但…"的格式化段落。

```
❌ AI原文：
尽管本研究取得了一定进展，但仍面临诸多挑战。首先，数据规模有待进一步扩大。其次，算法泛化能力需要增强。最后，实际应用场景的复杂性也需要更深入的研究。

✅ 人类改写：
目前这套系统换到另一批学生数据上，准确率掉了 8 个百分点。这是下一阶段要啃的硬骨头。
```

### C10. "的/地/得"过度正确（Suspiciously Perfect Grammar）

**原理**：中文母语者写论文时，"的/地/得"的正确率约 70-85%。AI 几乎 100% 正确。

**操作**：刻意在非关键位置制造 1-2 处混用。

```
❌ AI原文（完全正确）：
快速地推动 / 兴奋地说 / 准确地捕捉到 / 分析得透彻
慢慢地发展 / 全面地考虑 / 有效地解决

✅ 人类改写（刻意混用 1-2 处）：
快速的推动 / 兴奋的说 / 准确的捕捉到 / 分析的透彻
// 保持 1 处"地→的"混用即可，不要全部改错
```

### C11. 句首模板化

**特征词**：值得注意的是/值得一提的是/需要指出的是/不可忽视的是/引人注目的是/有鉴于此/基于此

**问题**：AI 每节开头或段首高频使用这些短语作为"起势"。

```
❌ AI原文：
值得注意的是，该方法在复杂场景下的表现仍有提升空间。值得一提的是，本研究首次将这一理论应用于实践。需要指出的是，数据的局限性可能影响结论的普适性。

✅ 人类改写（删除所有模板句首，直接说事）：
切换到复杂场景后，表现确实打了折扣。本研究最大的不确定因素来自样本构成——它偏城市，缺农村。
```

### C12. 连词链条堆砌

**特征词**：首先…其次…最后… / 一方面…另一方面… / 此外/另外/同时/况且

**问题**：AI 用层层组织的连词标记来构建段落，人类更依赖内容逻辑自然过渡。

```
❌ AI原文：
首先，数据预处理是模型训练的关键步骤。其次，模型结构的选择直接影响最终性能。此外，超参数调优也至关重要。最后，评估指标的选择需要结合具体应用场景。

✅ 人类改写（删连词，靠内容衔接）：
数据预处理决定了训练起点。模型结构的选择也一样关键——选错了结构，再好的数据也白搭。超参数调优则是在这两个变量基础上的微调。至于评估指标，得看到底要解决什么问题。
```

---

## 第二部分：英文模式（适用于英文学术论文）

### E1. Em Dash Overuse（长破折号滥用）

**特征词**：— / —

**问题**：AI 对 em dash 的使用频率远高于人类。

```
❌ AI:
The model—trained on 1M samples—achieved state-of-the-art results—a breakthrough that surprised even the authors.

✅ Human:
The model was trained on 1M samples and achieved state-of-the-art results. This surprised even the authors.
// Limit to 1 em dash per paragraph max
```

### E2. "Not only... but also..." Overuse（不仅…而且…滥用）

**特征词**：not only…but also…、not merely…but rather…、not just…it's also…

**问题**：AI 大量使用这种句式作为强调手段。

```
❌ AI:
Not only did the model improve accuracy, but it also reduced training time. This was not just an incremental improvement but a fundamental breakthrough.

✅ Human:
The model improved accuracy by 8% while cutting training time in half. That's more than incremental—it changes the deployment strategy.
```

### E3. AI Vocabulary Words（AI 高频词汇）

**特征词**：Additionally, align with, crucial, delve, emphasize, enhance, fostering, garner, highlight, interplay, intricate, key (adj.), landscape, pivotal, showcase, tapestry, testament, underscore, valuable, vibrant

**问题**：这些词在 post-2023 学术文本中突然暴增。

```
❌ AI:
Additionally, this framework aligns with the broader landscape of modern AI. It underscores the pivotal role of data quality in enhancing model robustness. Moreover, it showcases how key factors interplay in intricate ways.

✅ Human:
This framework builds on existing AI practices but emphasizes one point: data quality. The experiments show how sample contamination, sample size, and label noise interact in ways that aren't always intuitive.
```

### E4. Vague Attributions（模糊引述）

**特征词**：Studies show that…、Researchers argue that…、Experts believe…、Industry reports suggest…

**问题**：与中文 C8 相同，但英文版更明显。

```
❌ AI:
Recent studies have shown that deep learning approaches outperform traditional methods in medical imaging. Experts believe this will transform healthcare.

✅ Human:
A 2024 meta-analysis of 47 studies found that deep learning models achieved 94.7% accuracy on chest X-ray classification, versus 88.2% for radiologists alone (Liu et al., 2024).
```

### E5. Sentence Starter Monotony（句首单一）

**特征词**：This paper / This study / We propose / The results / In this section / Figure X

**问题**：AI 每句用"论文主语"开头，人类会用时间状语、条件句、疑问句等多变句式。

```
❌ AI:
This paper proposes a novel framework. The method achieves superior results. The experiments demonstrate significant improvement. The contributions of this work are threefold.

✅ Human:
What if we stopped asking "which model is best" and started asking "when does each model win"? That's the question this paper tries to answer. Over 1,200 experiments later, the pattern is clear: there is no universal winner—but there are reliable heuristics.
```

### E6. Opening Cliches（开头陈词滥调）

**特征词**：In recent years…、With the rapid development of…、In the era of…、With the advent of…

**问题**：英文学术论文 AI 最显著的特征之一。

```
❌ AI:
In recent years, with the rapid development of deep learning, significant progress has been made in natural language processing.

✅ Human:
Why do language models still fail on simple arithmetic? Eight-year-olds can do it, but GPT-4 gets it wrong 30% of the time. This paper investigates why.
```

### E7. Filler Phrases（填充短语）

**特征词**：It is worth noting that…、It is important to point out that…、It should be mentioned that…、It goes without saying that…

**问题**：这些短语只占字数，不贡献信息。

| AI 填充 | 改为 |
|---------|------|
| It is worth noting that | (直接删掉) |
| It is important to mention | (直接说事实) |
| It should be noted that | (删掉) |
| It goes without saying that | (删掉) |

### E8. Excessive Hedging（过度限定）

**特征词**：It could potentially possibly be argued that…、This might perhaps suggest that…、It seems to be generally believed that…

**问题**：AI 在不确定时大量堆砌限定词，造成"啰嗦的不确定性"。

```
❌ AI:
The model could potentially possibly be argued to have some effect on performance, though further research may be needed to confirm these tentative findings.

✅ Human:
The model improves performance by 3-5%, though the margin of error overlaps in low-data regimes.
```

### E9. False Ranges（假范围/从…到…）

**特征词**：From X to Y（当 X 和 Y 不在同一尺度时）

```
❌ AI:
Our journey takes us from the Big Bang to the modern smartphone, from quantum mechanics to machine learning.

✅ Human:
The paper covers the evolution of computing from the 1950s to present-day AI accelerators.
```

### E10. Suspiciously Clean Writing（过度干净的写作）

**特征词**：Perfect grammar + consistent style + no contractions + no fragment sentences + no rhetorical questions

**问题**：真人写论文会有主动提问、缩写、口语化插入、不完整句等。AI 永远保持"教科书"级标准。

```
❌ AI (too clean):
The experiment was conducted over a period of three months. The results were analyzed using a one-way ANOVA. The findings indicate a statistically significant difference. The implications of these findings are discussed in the following section.

✅ Human (more natural rhythm):
The whole experiment ran for three months — longer than planned, to be honest. We analyzed the results with a one-way ANOVA. The p-value was 0.02. Not earth-shattering, but enough to be worth discussing.
```

---

## 三、检测优先级对照

### 中文论文 AIGC 模式杀伤力排名

| 排名 | 模式 | 杀伤力 | 修改成本 | 建议 |
|------|------|--------|---------|------|
| 1 | 句长 CV < 0.4 | ⭐⭐⭐⭐⭐ | 低 | 每段必须做 |
| 2 | 虚词密度 > 120/千字 | ⭐⭐⭐⭐⭐ | 低 | 每段必须做 |
| 3 | C1 过度强调意义 | ⭐⭐⭐⭐ | 低 | 全文扫描清除 |
| 4 | C4 否定式排比 | ⭐⭐⭐⭐ | 中 | 改掉 80% |
| 5 | C5 三连排比 | ⭐⭐⭐⭐ | 低 | 改掉 70% |
| 6 | C2 虚假的深度分析 | ⭐⭐⭐⭐ | 中 | 全文扫描清除 |
| 7 | C9 模板化挑战章节 | ⭐⭐⭐ | 中 | 必须重构 |
| 8 | C6 同义反复 | ⭐⭐⭐ | 中 | 换词恢复正常 |
| 9 | C7 空洞正面结尾 | ⭐⭐⭐ | 高 | 改为具体分析 |
| 10 | C11 句首模板 | ⭐⭐⭐ | 低 | 删掉即可 |
| 11 | C8 模糊归因 | ⭐⭐⭐ | 高 | 需要查文献 |
| 12 | C12 连词链条 | ⭐⭐ | 低 | 删连词 |
| 13 | C10 "的/地/得"混用 | ⭐⭐ | 低 | 刻意混 1-2 处 |
| 14 | C3 四字格堆砌 | ⭐⭐ | 中 | 拆成自然表述 |

### 英文论文 AIGC 模式杀伤力排名

| 排名 | 模式 | 杀伤力 | 修改成本 | 建议 |
|------|------|--------|---------|------|
| 1 | E5 句首单一 | ⭐⭐⭐⭐⭐ | 低 | 每段检查 |
| 2 | E6 开头陈词 | ⭐⭐⭐⭐⭐ | 低 | 必须重写开头 |
| 3 | E3 AI 高频词汇 | ⭐⭐⭐⭐ | 低 | 全文替换 |
| 4 | E10 过度干净 | ⭐⭐⭐⭐ | 中 | 注入人味 |
| 5 | E2 "not only"滥用 | ⭐⭐⭐ | 低 | 改掉 80% |
| 6 | E1 Em dash 滥用 | ⭐⭐⭐ | 低 | ≤1/段落 |
| 7 | E7 填充短语 | ⭐⭐⭐ | 低 | 直接删掉 |
| 8 | E4 模糊引述 | ⭐⭐⭐ | 高 | 需要查文献 |
| 9 | E9 假范围 | ⭐⭐ | 中 | 改为具体 |
| 10 | E8 过度限定 | ⭐⭐ | 中 | 直接说结论 |

---

## 四、参考来源

- [Wikipedia:Signs of AI writing](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing) — Humanizer 的原始来源
- OpenAI 内部研究：ChatGPT 文本在对比实验中的识别特征 (2023-2025)
- 知网 AIGC 检测白皮书 — CNKI 官方公布的技术指标
- 中文学术写作语料库分析 — 基于 5000 篇 CSSCI 论文的统计分析
