# Dashboards-are-Dead-Project

- Project B aims to convert Overture's monthly release metrics into a single, LLM readable text artifact that conatins all context an LLM would need to answer questions about monthly map data releases reliably. We want to figure out how we can structure data, so the LLM can answer questions and refuse to answer certain questions reliably.

- this file will have key data statistics, schema and theme descriptions, and pre-injected prompts and instructions.

- The release metrics are csv or tabular files grouped by theme and key columns

- The main question is: How do you format summary stats AND instruct an LLM so it answers release questions accurately without hallucinating? So, from the raw data, we can likely just have an LLM read it and format it likely in a database. 


OKR 1 - Build a comprehensive LLM -readable artifact 
O: Ship a file that communicates Overture's release statistics enough for an LLM to answer a proposed set of 10 questions 
KR1: File contains enough stats and schema context that the 10 predefined test questions are all theoretically answerable (i.e. the data needed exists in the file)
KR2: LLM can answer at least 8/10 pre-defined test questions using only the file as context(no web search or external knowledge) 
KR3: File can be read by at least 2 different LLMs (e.g. Claude + ChatGPT) and both achieve 8/10 accuracy

OKR2 - Find prompt instructions that prevent hallucination
O: Identify which prompt instructions produce accurate, data-backed answers on Overture release stats
KR1: Test 3+ prompt variations (e.g. "cite your source", "refuse if unsure", "show your reasoning") and rank by accuracy score
KR2: 0/10 test questions answered with a fabricated number present in the file
KR3: Document 3 hallucination patterns observed during testing and the prompt fix that resolved each

OKR 3 — Deliver a format + prompt recommendation
O: Produce a usability report Overture can act on to deploy this artifact
KR1: Test 2+ stat formats (markdown table vs. plain prose) — pick winner based on accuracy score across the 10 test questions
KR2: Deliver 5 reusable prompt templates with accuracy scores attached to each
KR3: One-page recommendation: which format + which prompts, backed by test results as evidence


2. Prevent hallucinations
3. Format + prompt recommendation


