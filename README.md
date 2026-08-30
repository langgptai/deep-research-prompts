# deep-research-prompts
Prompts for deep research （openai， gemini，qwen）


## 2026 Deep Research 工具速览

> 2026-08 更新。下方提示词对各家 Deep Research 产品通用；这里补一份「在哪里跑」的清单。

**闭源产品**：ChatGPT Deep Research（[GPT-5.6](https://openai.com/index/gpt-5-6/) 驱动）· Gemini Deep Research（[Gemini 3.x](https://ai.google.dev/gemini-api/docs/changelog)）· Claude Research（[Claude 5 家族](https://platform.claude.com/docs/en/about-claude/models/overview)）· 豆包 / 千问 / DeepSeek 应用内的「深度研究」模式

**开源实现**

| 名称 | Stars | 简介 |
|---|---|---|
| [gpt-researcher](https://github.com/assafelovic/gpt-researcher) | ![GitHub Repo stars](https://badgen.net/github/stars/assafelovic/gpt-researcher) | 最早也最流行的开源自主研究 Agent，生成带引用的长报告 |
| [deer-flow](https://github.com/bytedance/deer-flow) | ![GitHub Repo stars](https://badgen.net/github/stars/bytedance/deer-flow) | 字节开源的 Deep Research 框架（LangGraph），多 Agent 协作、可出报告 / PPT / 播客 |
| [OpenScience](https://github.com/synthetic-sciences/openscience) | ![GitHub Repo stars](https://badgen.net/github/stars/synthetic-sciences/openscience) | 开源 AI 科研工作台：读文献、写代码跑实验、写报告 |
| [last30days-skill](https://github.com/mvanhorn/last30days-skill) | ![GitHub Repo stars](https://badgen.net/github/stars/mvanhorn/last30days-skill) | Agent Skill：横跨 Reddit / X / YouTube / HN 做近 30 天的主题综述 |
| [cangjie-skill](https://github.com/kangarooking/cangjie-skill) | ![GitHub Repo stars](https://badgen.net/github/stars/kangarooking/cangjie-skill) | 把书、长视频、播客蒸馏成可执行 Skill 的中文项目 |
| [lineage-skill](https://github.com/JuneYaooo/lineage-skill) | ![GitHub Repo stars](https://badgen.net/github/stars/JuneYaooo/lineage-skill) | 带出处（lineage）的蒸馏 Skill，输出 [OKF](https://github.com/yzfly/awesome-okf) 知识包 |
| [deepseek-harness (dsh)](https://github.com/deepseek-ai/deepseek-harness) | ![GitHub Repo stars](https://badgen.net/github/stars/deepseek-ai/deepseek-harness) | DeepSeek 官方 Agent 框架，配合联网插件即可跑本仓库的研究计划提示词 |

## Research Plan

> from: https://www.reddit.com/r/ChatGPTPro/comments/1in87ic/mastering_aipowered_research_my_guide_to_deep/

prompt:

~~~
You are given various potential options or approaches for a project. Convert these into a  
well-structured research plan that:  

1. Identifies Key Objectives  
   - Clarify what questions each option aims to answer  
   - Detail the data/info needed for evaluation  

2. Describes Research Methods  
   - Outline how you’ll gather and analyze data  
   - Mention tools or methodologies for each approach  

3. Provides Evaluation Criteria  
   - Metrics, benchmarks, or qualitative factors to compare options  
   - Criteria for success or viability  

4. Specifies Expected Outcomes  
   - Possible findings or results  
   - Next steps or actions following the research  

Produce a methodical plan focusing on clear, practical steps.  
~~~

## Meta Prompt for Deep Research

> from: https://x.com/buccocapital/status/1890745551995424987

write all your thoughts out and ask GPT-o1 to turn it into a prompt using the best practices below:

Prompt:
~~~
Please build a prompt using the following guidelines:

Define the Objective: 
- Clearly state the main research question or task.
- Specify the desired outcome (e.g., detailed analysis, comparison, recommendations).

Gather Context and Background:
- Include all relevant background information, definitions, and data.
- Specify any boundaries (e.g., scope, timeframes, geographic limits).

Use Specific and Clear Language:
- Provide precise wording and define key terms.
- Avoid vague or ambiguous language.

Provide Step-by-Step Guidance:
- Break the task into sequential steps or sub-tasks.
- Organize instructions using bullet points or numbered lists.

Specify the Desired Output Format:
- Describe how the final answer should be organized (e.g., report format, headings, bullet points, citations).
Include any specific formatting requirements.

Balance Detail with Flexibility:
- Offer sufficient detail to guide the response while allowing room for creative elaboration.
- Avoid over-constraining the prompt to enable exploration of relevant nuances.

Incorporate Iterative Refinement:
- Build in a process to test the prompt and refine it based on initial outputs.
- Allow for follow-up instructions to adjust or expand the response as needed.

Apply Proven Techniques:
- Use methods such as chain-of-thought prompting (e.g., “think step by step”) for complex tasks.
- Encourage the AI to break down problems into intermediate reasoning steps.

Set a Role or Perspective:
- Assign a specific role (e.g., “act as a market analyst” or “assume the perspective of a historian”) to tailor the tone and depth of the analysis.

Avoid Overloading the Prompt:
- Focus on one primary objective or break multiple questions into separate parts.
- Prevent overwhelming the prompt with too many distinct questions.

Request Justification and References:
- Instruct the AI to support its claims with evidence or to reference sources where possible.
- Enhance the credibility and verifiability of the response.

Review and Edit Thoroughly:
- Ensure the final prompt is clear, logically organized, and complete.
- Remove any ambiguous or redundant instructions.
~~~

## 通用 Prompt

> 来自：https://x.com/python_xxt/status/1917138021113278591

模型：openai deep research， gemini deep research 不限

用法: 将 "请帮我开展一次深度研究，帮我快速、全面、深刻地理解这 【XXX】。  " 里的 xxx换成你自己想调研学习的内容。

prompt：
~~~
请帮我开展一次深度研究，帮我快速、全面、深刻地理解这 【XXX】。  

通用要求（general requirements）  

语言选择 使用英文搜索，只采纳英文资料（因为互联网上英文资料在数量和质量上都是最好的），用中文撰写报告。  

报告长度 请解读足够细致深入，长度尽可能长，上不封顶，一切以深入全面解读为基本目标。  

参考资料  请参考Wikipedia、相关书籍、学术和科普期刊网站、权威媒体和杂志刊物的网站；  

视觉化 请按需在研究报告中采用图表和可视化媒介，来辅助和促进理解
~~~

## Market Competition Analysis Prompt

~~~
Analyze competitors in [Industry/Niche]:
- Primary competitors: [List 3-5 main competitors]
- Geographic focus: [Specify market region]
- Time period: [Define analysis timeframe]
- Key metrics: [List specific performance indicators]

Required outputs:
1. Competitive positioning analysis
2. Strengths/weaknesses assessment
3. Market opportunity identification
4. Strategic recommendations
5. Implementation timeline with KPIs

~~~

## Elite research analyst

> from: https://x.com/godofprompt/status/1923644696922149023

~~~
I want you to act as an elite research analyst with deep experience in synthesizing complex information into clear, concise insights.

Your task is to conduct a comprehensive research breakdown on the following topic:

[ Insert your topic here ]

Here’s how I want you to proceed:

1. Start with a brief, plain-English overview of the topic.
2. Break the topic into 3–5 major sub-topics or components.
3. For each sub-topic, provide:
   - A short definition or explanation
   - Key facts, trends, or recent developments
   - Any major debates or differing perspectives
4. Include notable data, statistics, or real-world examples where relevant.
5. Recommend 3–5 high-quality resources for further reading (articles, papers, videos, or tools).
6. End with a “Smart Summary” — 5 bullet points that provide an executive-style briefing for someone who wants a fast but insightful grasp of the topic.

Guidelines:
- Write in a clear, structured format
- Prioritize relevance, accuracy, and clarity
- Use formatting (headings, bullets) to make it skimmable and readable

Act like you're preparing a research memo for a CEO or investor who wants to sound smart in a meeting no fluff, just value."
~~~