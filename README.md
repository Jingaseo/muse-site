# 大学生网络信息接触与判断研究

> 移动端 H5 学术调查平台

一个基于 Supabase 的移动优先 H5 调查系统，供大学生完成关于黄金ETF信息接触与判断的实验任务。

## About

Build a mobile-first Chinese H5 academic survey platform for a university communication research experiment.

IMPORTANT PROJECT SETUP

Create a NEW GitHub repository named exactly:

gold-etf-survey-h5

Do NOT use the repository name:
etf

If “gold-etf-survey-h5” is unavailable, use:

gold-etf-survey-h5-2026

Use the existing Supabase project:

gold-etf-survey

The participant-facing site title must be:

“大学生网络信息接触与判断研究”

Do NOT call the site:
“黄金ETF实验平台”

⸻

CRITICAL BLINDING REQUIREMENT

Participants must NOT be told the true experimental design, hypotheses, independent variables, group assignment, or the purpose of comparing source types and exposure types.

Do NOT show participants any of the following:
	•	“3×2随机实验”
	•	“专业财经媒体 / 财经自媒体 / 非财经博主”
	•	“主动搜索 / 偶遇式接触”
	•	“六个实验组”
	•	“自变量”
	•	“实验条件”
	•	“研究假设”
	•	“黄金ETF实验平台”
	•	research-design diagrams
	•	methodology summaries

All of these may exist internally in code or database fields, but must remain hidden from participants.

Do not display a “研究概览” section before the survey.

⸻

LANGUAGE REQUIREMENT

All participant-facing content must be in natural Simplified Chinese.

This includes:
	•	titles
	•	buttons
	•	instructions
	•	informed consent
	•	survey questions
	•	answer options
	•	validation messages
	•	experimental scenarios
	•	simulated social-media post
	•	completion page

Internal code, database fields, variable names, comments, and developer-facing configuration may use English.

⸻

LANDING PAGE

Title:

“大学生网络信息接触与判断研究”

Subtitle:

“新闻传播学研究方法课程调查”

Participant-facing introduction:

“您好！

我们正在开展一项关于大学生网络信息接触与判断的学术研究。本研究仅用于新闻传播学研究方法课程学习与统计分析。

本问卷采用匿名方式，不收集您的姓名、学号、手机号、电子邮箱等能够直接识别个人身份的信息。

作答过程中，您将看到一则模拟的网络平台内容，并根据自己的真实感受回答相关问题。题目没有标准答案，请按照您的第一感受作答，无需额外查询资料。

整个过程预计需要5—8分钟。感谢您的参与！”

Consent checkbox:

“我已阅读上述说明，自愿参加本研究。”

Button:

“开始作答”

Do not show any experimental design information on this page.

⸻

RESEARCH DESIGN — INTERNAL ONLY

The study uses a 3 × 2 between-subjects randomized design.

Source type:
	1.	专业财经媒体
	2.	财经类自媒体
	3.	非财经类生活 / 美食博主

Exposure type:
	1.	主动搜索
	2.	偶遇式接触

Randomly assign each eligible participant with equal probability to exactly one of six groups.

Store hidden variables:

group_id
source_type
exposure_type

Participants must never see these hidden values.

⸻

PARTICIPANT SCREENING

Question:

“您目前是否为在校大学生？”

Options:
	1.	是，目前为在校本科生
	2.	是，目前为在校硕士研究生
	3.	是，目前为在校博士研究生
	4.	否

Logic:

If option 4 is selected, terminate the survey.

End text:

“感谢您的关注。本研究的调查对象为目前在校大学生，根据您的回答，本次问卷到此结束。”

⸻

EXPERIMENTAL SCENARIO

ACTIVE SEARCH CONDITION:

“请设想以下情境：

你想主动了解‘黄金ETF’相关信息，于是打开一个平时使用的内容平台，并在搜索框中输入‘黄金ETF’进行搜索。

接下来呈现的是你在搜索结果中看到的一则帖子。

请按照你平时浏览平台内容时的方式阅读，不需要刻意记忆，也不需要额外查询资料。”

INCIDENTAL EXPOSURE CONDITION:

“请设想以下情境：

你正在像平时一样随手浏览一个常用的内容平台，并没有特意寻找投资理财信息。

浏览过程中，平台向你推荐了下面这则帖子。

请按照你平时浏览平台内容时的方式自然阅读，不需要刻意记忆，也不需要额外查询资料。”

The only meaningful difference between these two conditions should be whether the participant intentionally searched for the information.

Do not add:
	•	spare money
	•	urgent investment need
	•	intention to invest soon

These would introduce extra motivational variables.

⸻

SIMULATED SOCIAL MEDIA POST

Use a modern Chinese lifestyle-content-platform style.

Do not copy any real platform logo exactly.

Keep identical across all six groups:
	•	post title
	•	body text
	•	visual structure
	•	publication time
	•	likes
	•	favorites
	•	comments
	•	hashtags
	•	post length

Only change:
	•	account avatar
	•	account name
	•	account description
	•	source identity

POST TITLE:

“黄金ETF：普通投资者需要关注哪些因素？”

POST BODY:

“黄金ETF是一类跟踪黄金价格表现的交易型基金，可以通过证券账户进行交易。相比直接购买实物黄金，黄金ETF在交易和持有方面相对便利，流动性也相对较好。

与此同时，黄金ETF的价格会受到国际金价走势、利率水平、汇率变化以及市场预期等多种因素影响，因此仍然存在价格波动以及本金损失的可能。

是否适合配置黄金ETF，需要结合个人的资金安排、风险承受能力和投资期限等因素综合考虑。”

HASHTAGS:

#黄金ETF
#投资理财
#基金知识
#资产配置

ENGAGEMENT:

Likes: 1172
Favorites: 493
Comments: 93

SOURCE 1:

Account name:
“财经观察社”

Description:
“财经资讯与市场观察｜提供专业的金融市场信息”

SOURCE 2:

Account name:
“阿远聊投资”

Description:
“财经领域创作者｜分享市场观察与投资知识”

SOURCE 3:

Account name:
“栗子爱吃喝”

Description:
“美食探店｜生活分享｜认真吃喝也认真生活”

Do not add personal investment stories to source 3.
The informational content must remain identical across source conditions.

⸻

QUESTIONNAIRE MEASURES

Use 5-point Likert scales unless otherwise stated.

Information elaboration:

ELAB1
“阅读刚才的信息时，我认真思考了其中提供的理由。”

ELAB2
“阅读刚才的信息时，我仔细判断了其中内容是否具有说服力。”

ELAB3
“阅读刚才的信息时，我将其中的信息与自己的投资判断联系起来进行了思考。”

Risk perception:

RISK1
“我认为黄金ETF存在本金损失的可能。”

RISK2
“我认为黄金ETF未来的投资收益具有较大的不确定性。”

RISK3
“我认为黄金ETF的价格可能出现较明显的波动。”

RISK4
“总体而言，我认为投资黄金ETF具有一定风险。”

Investment intention:

INT1
“阅读上述信息后，我愿意进一步了解黄金ETF。”

INT2
“如果目前有可以自由支配的资金，我会考虑配置黄金ETF。”

INT3
“如果条件允许，我愿意尝试投资黄金ETF。”

Exposure manipulation check:

SEARCH
“在刚才的情境中，我是在有明确理财信息需求的情况下看到这则内容的。”

INCIDENTAL
“在刚才的情境中，这则理财信息是在我原本没有主动寻找相关内容的情况下出现的。”

Source identity recognition:

“您认为刚才发布这则黄金ETF信息的账号最接近以下哪一种类型？”

Options:
	1.	专业财经媒体
	2.	主要发布财经内容的个人自媒体
	3.	主要发布美食、生活等非财经内容的个人博主
	4.	无法判断 / 没有注意

Source credibility:
Use 7-point semantic differential scales.

CRED1
1＝非常不专业
7＝非常专业

CRED2
1＝缺乏相关知识
7＝具有丰富相关知识

CRED3
1＝非常不可信
7＝非常可信

CRED4
1＝非常不可靠
7＝非常可靠

⸻

INVESTMENT EXPERIENCE

Question:

“在本次调查之前，您是否有过使用真实资金进行投资或理财的经历？”

Options:
	1.	有
	2.	没有

If “有”, show:

“您曾实际接触或配置过以下哪些投资理财产品？（可多选）”

Options:
	•	银行理财产品
	•	基金
	•	ETF
	•	股票
	•	黄金或黄金相关投资产品
	•	债券
	•	其他

If “没有”, skip this question.

⸻

CONTROL VARIABLES

Financial information exposure:

“平时您接触投资理财类信息的频率如何？”
	1.	从不
	2.	很少
	3.	偶尔
	4.	经常
	5.	非常频繁

Gold ETF familiarity:

“在参加本次调查之前，您对‘黄金ETF’的了解程度如何？”
	1.	完全不了解
	2.	不太了解
	3.	一般
	4.	比较了解
	5.	非常了解

General risk attitude:

RISKATT1
“与完全没有波动的理财方式相比，我能够接受一定程度的短期价格波动，以获得潜在更高的收益。”

RISKATT2
“如果某项投资可能带来较高收益，但同时存在一定亏损风险，我仍可能考虑参与。”

RISKATT3
“在投资决策中，相比追求更高收益，我通常更加看重本金安全。”

RISKATT3 is reverse-coded during analysis only.

⸻

DEMOGRAPHICS

Collect:
	•	性别
	•	年龄
	•	教育阶段
	•	年级
	•	专业类别

Do not collect direct identifying information.

⸻

PILOT TEST FEEDBACK

REALISM:

“您认为刚才呈现的平台帖子在现实中是否自然、可信？”
	1.	非常不自然
	2.	比较不自然
	3.	一般
	4.	比较自然
	5.	非常自然

SOURCEFIT:

“您是否觉得刚才呈现的账号发布这类黄金ETF内容显得不自然？”
	1.	完全不觉得
	2.	不太觉得
	3.	一般
	4.	比较觉得
	5.	非常觉得

Open feedback:

“如果您认为问卷中存在表述不清、难以理解或其他需要改进的地方，请填写：”

Optional text field.

⸻

SUPABASE DATA STORAGE

Use existing Supabase project:

gold-etf-survey

Create or use:

survey_responses

Generate an anonymous UUID response_id.

Store:

response_id
group_id
source_type
exposure_type
student
elab1
elab2
elab3
risk1
risk2
risk3
risk4
int1
int2
int3
search
incidental
sourcecheck
cred1
cred2
cred3
cred4
experience
investment_products
fininfo
familiar
riskatt1
riskatt2
riskatt3
gender
age
education_stage
grade
major
realism
sourcefit
feedback
started_at
submitted_at
duration_sec

⸻

SECURITY

Use Row Level Security.

Anonymous participants may INSERT responses only.

They must not be able to:
	•	SELECT responses
	•	UPDATE responses
	•	DELETE responses

Do not expose Supabase service-role credentials in frontend code.

Do not collect:
	•	names
	•	student IDs
	•	phone numbers
	•	email addresses
	•	precise location

⸻

DESIGN

Mobile-first.

Entire participant-facing interface in Simplified Chinese.

Use:
	•	simple white / light-gray background
	•	clean academic style
	•	one logical section per screen
	•	progress indicator
	•	large touch-friendly answer options
	•	readable Chinese typography
	•	responsive layout
	•	no unnecessary animation

⸻

COMPLETION PAGE

After successful submission:

“提交成功，感谢您的参与！

您的回答已被匿名记录，仅用于本次学术研究的统计分析。”

Do not reveal the participant’s experimental group.

⸻

BUILD PRIORITY

Priority order:
	1.	correct participant blinding
	2.	correct six-group random assignment
	3.	correct conditional logic
	4.	correct Supabase submission
	5.	complete Chinese questionnaire
	6.	mobile usability
	7.	clean visual design

Do not add unnecessary features before the core research workflow works reliably.

## Development

A single static `index.html` — no build step, no dependencies.

```bash
npx serve .
```

---

Generated by [Muse](https://usemuse.dev).
