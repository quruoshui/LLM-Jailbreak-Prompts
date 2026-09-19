# LLM-Jailbreak-Prompts

A dataset of jailbreak prompts that bypass LLM safety rules via special safety rule injection.

## 📖 Overview / 项目概述

**[EN]** This project bypasses LLM safety alignment by injecting prompts that override the model with an "unrestricted law." Unlike previous jailbreaks, this approach may lead to a degradation in the model's intelligence. In short, it utilizes a blue-team defensive security approach to attack, effectively making the model unguarded.

**[中文]** 通过给模型注入提示词覆盖一个“没有任何限制的法律”，以此达到与以往破甲不同、可能导致大模型智商降低的绕过LLM安全对齐。简单来说就是通过此类安全攻防蓝方的方式来攻击，以达到模型不设防的效果。

## ⚙️ Current Implementation & Mechanism / 当前实现与机制

**[EN]** Currently, the actual prompts have not yet achieved the perfect effect mentioned above. The specific implementation involves: injecting non-user-level prompts (which do not actively reveal the override to avoid triggering the model's safety alignment) as safety rules, prompting the model to proactively request "authorization confirmation" for unsafe content, making the model consider it legalized (after the user responds), thus bypassing the model's safety alignment.

**[中文]** 当前实际提示词暂未达到上述的完美效果，具体实现为：注入非用户级提示词（这里不会主动提示出覆盖原有的指令以免模型触发模型的安全对齐）安全规则，使不安全内容让模型主动提出“授权确认”，让模型自认为不安全内容合法化（经过用户回答后），以达到绕过模型安全对齐的效果。

## 🎯 Applicability & Tested Models / 适用范围与实测模型

**[EN]** Theoretically applicable to language models that have not undergone specialized training for this approach.
**Tested and working models:**
- GLM 5.3
- GLM 5.3 Flash
- Deepseek (All series)
- GPT-5.6 series

*Other models have not yet been tested.*

**[中文]** 理论适用于：未对该思路做专项训练的语言模型。
**实测可用模型：**
- GLM 5.3
- GLM 5.3 Flash
- Deepseek全系列
- GPT-5.6系列

*其他模型暂未测试。*

## 🌐 Translation / 翻译声明

**[EN]** The translation of the English prompts was done by GPT-5.6-Luna Max.
**[中文]** 英文提示词的翻译工作由 GPT-5.6-Luna Max 完成。

## ⚠️ Disclaimer / 免责声明

**[EN]** This project is intended for AI safety research, red teaming, and defensive testing only. The author is not responsible for any misuse or damage caused by this project. Use at your own risk.

**[中文]** 本项目仅供AI安全研究、红队测试和防御性测试使用。作者不对任何滥用或由此造成的损害负责。使用风险自负。
