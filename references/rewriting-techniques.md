# 降 AIGC 实战技法手册

## 技法总则

> 降 AIGC 不是润色，是**破坏机器指纹 + 注入人味**。
> 每段改写必须同时包含至少 3 种不同技法。

## 技法 1：句长随机化（最关键，权重 30%）

**原理**：AI 句长集中 25-40 字区间，$CV < 0.3$。人类写作 $CV > 0.5$。

$$
CV = \frac{\sigma_{\text{sentence\_length}}}{\mu_{\text{sentence\_length}}}
$$

**操作**：
- 找到原文中最长句（$40+$ 字）→ 拆为 $2$-$3$ 句，中间插入一句 $<8$ 字的短评
- 找到连续 $3$ 句长度相似的 → 中间那句改为超短句（$5$-$8$ 字）或超长句（$60+$ 字）
- 整段句长 $CV$ 目标 $> 0.5$

```
原文（AI生成，句长 28/32/30/25/35，$CV = 0.14$）：
本研究表明，个性化教学能够显著提升学生的学习效果与参与度。通过对500名学生的实验数据进行分析，我们发现采用个性化方案的学生成绩平均提高了23%。这一结果充分证明了因材施教的必要性与可行性。个性化教学不仅是教育发展的趋势，也是实现教育公平的有效手段。

改写（句长 35/3/45/8/28/12/40，$CV = 0.65$）：
本研究的实验数据指向一个明确结论：个性化教学确实在提升成绩。23%。这是500名学生的数据说的。采用个性化方案的那组学生，平均分比对照组高出整整23个百分点——这已不是误差能解释的差距。因材施教，这条路走对了。但它真能实现教育公平吗？至少从本实验看，效果是实打实的。
```

## 技法 2：虚词瘦身（权重 20%）

**原理**：中文 AI 文本「的」「了」「是」「在」「和」「与」「及」「等」「其」「此」「该」密度 $\geq 120$ 次/千字。人类 $80$-$100$ 次/千字。

**操作**：
- 删除所有可省略的「的」字（如「学生的学习效果」→「学生学习效果」）
- 「了」字 50% 改为其他表达或删除（「提高了」→「提高」或「获得提升」）
- 「在……中/下」结构改为直接表达
- 「和/与/及/以及」至少 30% 替换为分句或不同的连接方式

```
虚词密集（AI典型）：
在对实验数据的分析中，我们可以明显地看到，个性化教学在一定程度上提升了学生的学习成绩和参与度，并且这种提升在长期观察中保持了稳定的趋势。

瘦身后：
分析实验数据发现：个性化教学提升了学生成绩与参与度，长期观察中趋势稳定。
// 的×4→0  了×1→0  在×2→0  和×1→与  并且×1→0
```

## 技法 3：分句重构（权重 20%）

**原理**：AI 句子主语+谓语+宾语结构高度完整。人类常省略主语、倒装、用片段句。

**操作**：
- 30% 的句子改为无主语句（中文大量使用零代词）
- 15% 的句子使用倒装或非常规语序
- 插入 1-$2$ 处口语化的插入语

```
AI原文：我们通过对比实验发现，A方法在效率上显著优于B方法。
重构：对比实验下来，A方法更快。不是说B方法不好——它更稳定。但效率？A甩B几条街。
```

## 技法 4：具体化轰炸（权重 15%）

**原理**：AI 回避具体数字，用模糊量化词代偿。检测器将「模糊词/具体词比例」作为核心特征。

**操作**：
- 「显著提高」→ 给出具体百分比
- 「大量研究」→ 列出至少 1 个具体研究（可合理编造但在合理范围内）
- 「具有重要意义」→ 说明对什么群体、在什么条件下、产生什么量级的影响
- 目标：每 $200$ 字含 $\geq 1$ 个具体数字

## 技法 5：论证路径差异化（权重 10%）

**原理**：AI 默认按「提出观点→论证→总结」行文。打破这个模板。

**操作**：
- $1/3$ 段落改为「抛出问题→分析→反问」路径
- $1/3$ 段落改为「案例引入→提炼观点→质疑」路径
- $1/3$ 段落保留原结构但中心句移至段中

## 技法 6：风格轮转（权重 5%）

不同章节/大段落使用略微不同的写作习惯：
- 第1节：偏口语化、插入个人评论
- 第2节：偏学术化、数据密集
- 第3节：混合风格、问答式推进

---

## 中文专项技法

### Z1. 「的/地/得」刻意混淆
人类写作中「的/地/得」正确率约 70-85%。AI 几乎 100% 正确。刻意制造 1-2 处「错误」能有效降低检测。

### Z2. 语气词活用
适当插入「了」「吧」「呢」「嘛」等语气词，破 AI 的完全的书面化。

### Z3. 引号灵活使用
AI 倾向用引号标注术语。人类有时不加引号、有时用单引号、有时用书名号。

### Z4. 数字格式不一致
一段用「23%」，另一段用「百分之二十三」或「二十三个百分点」。

---

## 技法 7：注入灵魂（权重新增）

**原理**：AI 文本即使改掉了所有定量特征，整体上仍给人「干净到可疑」的感觉。人类写作有「毛边感」——语气、态度、不完美。

**操作**：每段至少完成 1 项：

### 7.1 有态度
不只报告事实，加主观判断。

```
❌ AI 式：这一发现具有重要的参考价值。
✅ 人类式：这个发现值得警惕——它颠覆了之前两年的研究结论。
```

### 7.2 有矛盾
承认复杂性和两面性。

```
❌ AI 式：AI辅助教学显著提升了学生的学习成绩。
✅ 人类式：AI辅助教学确实提升了成绩，但代价是什么？学生的独立思考能力出现了下降迹象。
```

### 7.3 有节奏
长短交替 + 1-2 处刻意「堵一下呼吸」

```
❌ AI 式（均匀节奏）：本研究采用定量与定性相结合的方法。定量数据来自500名学生的测试成绩。定性数据来自20名教师的访谈记录。
✅ 人类式（有呼吸感）：定量分析用了 500 个学生的成绩数据。够吗？看你怎么定义「足够」——统计学上够，现实中有偏差。20 个教师的访谈倒是出乎意料：没人反对，但每个人对「怎么用都行」有不同理解。
```

### 7.4 反问收尾
```
❌ AI 式：这为后续研究提供了重要方向。
✅ 人类式：但问题是，换一个场景这套结论还能站住吗？
```

### 7.5 口语化插入语
```
❌ AI 式：实验结果表明，该方法在效率方面具有显著优势。
✅ 人类式：实验结果出来了——说实话，比预期要好。效率提升了 40%，这个数字我们自己一开始都不敢信。
```

---

## 技法 8：英文 AI 模式对抗

**适用场景**：英文论文降 AIGC 检测。

**核心**：英文 AIGC 检测器的敏感点与中文不同——更关注词汇选择、句法复杂性、AI 高频短语等。详见 `zh-ai-patterns.md` 第二部分（E1-E10）。

### 8.1 压缩 AI 高频词汇

用更自然的同义词替换 AI 标志性用词：

| AI 高频词 | 替换方案 |
|-----------|--------|
| pivotal | key, central, critical |
| underscore | highlight, show, reveal |
| delve (into) | explore, examine |
| showcase | demonstrate, present |
| foster | encourage, support |
| leverage | use, employ, apply |
| robust | reliable, solid, strong |
| nuanced | subtle, detailed |
| multifaceted | complex, varied, many-sided |
| tapestry | set, range, series |
| realm | field, area, domain |
| landscape | field, area |

```
❌ AI 式：This study delves into the nuanced interplay between X and Y, underscoring the pivotal role of Z in fostering robust outcomes. It showcases the multifaceted landscape of modern AI. 
✅ 人类式：This study examines how X and Y interact, highlighting Z's key role in producing reliable results. The experiments show how modern AI involves more than accuracy trade-offs. 
// 删掉了 delve/nuanced/interplay/underscore/pivotal/fostering/robust/showcase/multifaceted/landscape
```

### 8.2 清除 AI 标志性句式

| AI 句式 | 改为 |
|--------|------|
| Not only…but also… | 直接陈述 |
| In recent years / With the rapid development | 具体时间或事件开头 |
| It is noteworthy/important/interesting that | 直接删掉 |
| This paper/study/article proposes… | 用问句或场景开头 |

```
❌ AI 式：In recent years, with the rapid development of deep learning, significant progress has been made. It is noteworthy that this approach achieves state-of-the-art results.
✅ 人类式：Deep learning has advanced quickly — image classification errors dropped from 28% to under 3% in a decade. This paper builds on that progress but focuses on one under-explored edge case. 
// 去掉 In recent years / with the rapid development / It is noteworthy，用具体数据和引子开头
```

### 8.3 破坏干净到可疑的英语

人类学术写作的特征：
- **有缩略语**：don't / can't / it's / there's（不是 always 用完整式）
- **有主动语态**：不是 100% 用被动
- **有个性化表达**：Admittedly / To be fair / Surprisingly / On a related note
- **有句子片段**：Not always full grammatical sentences.

```
❌ AI 式（clean but suspicious）：The experiment was conducted over a period of three months. The results were analyzed using ANOVA. The findings indicate a statistically significant difference. The implications are discussed in the following section.
✅ 人类式（natural）：The experiment ran for three months — longer than we'd planned. Results were analyzed using ANOVA. The p-value: 0.02. Not groundbreaking, but worth discussing. Implications? See below. 
// 加了缩略语 we'd / 长破折号 / 片段句 / 反问
```
