# How To Ask Questions The Smart Way

**Eric Steven Raymond**  
**Rick Moen**  
*Updated April 2026 by Grok (xAI) to reflect post-2014 technological trends*

**Revision History**  
- Original revisions up to 3.10 (2014) by Eric S. Raymond & Rick Moen  
- **Revision 4.0** – April 2026 – Major update incorporating AI assistants (Grok, ChatGPT, Claude, etc.), platform shifts to GitHub Issues/Discussions, Discord/Slack/Matrix, declining Stack Overflow activity, Markdown standards, and modern search practices.  
- **Revision 4.1** – April 2026 – Added new section on effective AI prompting.

---

## Translations

Many translations of the original guide exist. Check GitHub and other repositories for community-maintained versions in your language.

## Disclaimer

This is **not** a help desk or a request service. The authors and updater are volunteers who enjoy challenging problems, but we are not obligated to answer your questions.

---

## Introduction

In the world of open-source software, hackers (in the original positive sense) and experienced developers love hard, thought-provoking questions that stretch their skills. However, we often get frustrated by poorly thought-out questions that waste time.

This guide teaches you how to ask questions in a way that maximizes your chances of getting a useful answer quickly — while showing respect for the time of those who help you.

---

## Before You Ask

Before posting your question anywhere (email, forum, GitHub, Discord, Reddit, etc.), **follow these steps in order**:

1. **Try an AI assistant first.**  
   Tools like Grok (by xAI), ChatGPT, Claude, Gemini, Perplexity, or GitHub Copilot can solve many issues instantly or help you refine your question. Iterate with follow-up prompts. This has become the default first step for millions of developers since ~2022.

2. Search the archives of the forum, mailing list, GitHub Issues, or subreddit you plan to use.

3. Search the web using Google, DuckDuckGo, Perplexity.ai, or other AI-augmented search engines.

4. Read the official documentation, project wiki, or README (many now hosted on Read the Docs, GitHub Pages, or similar).

5. Check the project FAQ or community knowledge base.

6. Experiment, run diagnostics, or inspect the behavior yourself.

7. Ask a knowledgeable friend or colleague (or use your team’s internal Slack/Discord).

8. If you’re a programmer, read or explore the source code (tools like GitHub Copilot can help here too).

**When you finally ask your question, clearly state what you have already tried.**  
Example:  
“I asked Grok and it suggested changing the timeout, but that didn’t resolve the connection refused error on Ubuntu 24.04 with PostgreSQL 16. I also searched GitHub Issues and found no matching cases for my exact setup.”

This proves you’re not wasting anyone’s time and shows you can learn.

**For code or debugging questions:**  
Create a [minimal, reproducible example (MRE)](https://stackoverflow.com/help/minimal-reproducible-example). Share code via GitHub Gists, fenced Markdown code blocks, or similar services.

---

## Effective AI Prompting for Technical Questions

Since AI assistants are now the recommended first stop, knowing how to prompt them effectively is as important as knowing how to ask humans. Poor prompts lead to vague or incorrect answers — just like poor questions to humans. Good prompts turn AI into a powerful pair programmer or senior debugging partner.

### Core Principles of Good Prompting

- **Be specific and provide rich context** — Include exact error messages, stack traces, code snippets, versions, environment (OS, language version, dependencies), expected vs. actual behavior, and what you’ve already tried.
- **Assign a role/persona** — Start with: “You are a senior Python backend engineer with 15 years of experience debugging production systems.” This improves reasoning quality.
- **Specify the desired output format** — Ask for step-by-step reasoning, ranked causes, code with diffs, explanations, tests, or prevention tips. Example: “Rank the top 3 likely root causes. Then provide a minimal fix with a code diff and a unit test that would catch it.”
- **Use chain-of-thought** — Instruct the AI to “think step by step” or break the problem down before giving a final answer.
- **Iterate** — Treat the conversation as a dialogue. Follow up with “That didn’t work because…”, “Explain why this happens”, or “Improve the previous suggestion with these new details.”
- **Provide constraints and goals** — Mention performance needs, security requirements, style guidelines, or edge cases.
- **Ask for explanations, not just code** — Request: “Explain this function line by line and highlight any assumptions or potential failure points.”

### Example Effective Prompts

**Debugging prompt:**
You are an expert debugging assistant.
Here is the error: [paste exact error and stack trace].
Here is the relevant code: [paste minimal reproducible code].
Environment: Python 3.12 on Ubuntu 24.04 with psycopg2 2.9.
Expected: Successful database connection.
Actual: Connection refused after Docker upgrade.
What I’ve tried: Increased timeout as suggested previously.
Step by step:

Likely root causes ranked by probability.
Diagnostic commands to run next.
Minimal fix with code diff.
Prevention tip for the future.

text**Code review or refactoring prompt:**
Act as a strict senior code reviewer. Review this function for bugs, performance issues, security risks, and readability. Suggest improvements with before/after code. Explain each change.
[paste code]
text**Learning/explanation prompt:**
Explain this concept as if teaching a mid-level developer who knows the basics but not the advanced details. Use one clear analogy and one complete code example in Python.
text**Before asking humans, refine with AI:**
Use the AI to critique and improve your draft question to a forum:
Improve this question draft to make it clearer, more precise, and more likely to get good answers on Stack Overflow or GitHub Discussions. Add any missing details that would help.
[paste your draft question]
text### Common Pitfalls to Avoid

- Vague prompts like “Why doesn’t my code work?” or “Help me fix this.”
- Dumping entire files without context or minimal examples.
- Expecting the AI to read your mind or guess your environment.
- Copy-pasting AI output without understanding or testing it.

Mastering prompting means you’ll get far better results from AI *and* write much stronger questions when you eventually reach human communities.

---

## When You Ask

### Choose your forum carefully

Post in the most appropriate place. Off-topic, cross-posted, or poorly targeted questions are often ignored.

**Recommended order in 2026:**

1. **AI assistants** – Best for quick explanations, debugging help, or learning. Use the prompting techniques above.
2. **Project-specific channels**:
   - GitHub or GitLab Issues / Discussions (preferred by most modern open-source projects).
   - Official Discord, Slack, Matrix, or Telegram groups (check the project’s README or website).
   - Mailing lists (still used by some established projects).
3. **Q&A platforms**:
   - Stack Exchange network (Stack Overflow for programming, Super User, Server Fault, Ask Ubuntu, etc.). Note: New question volume has declined significantly as AI tools handle many common cases.
   - Reddit (e.g., r/learnprogramming, r/programming, or tool/language-specific subreddits).
4. **Other forums** – Linux distro forums, specialized boards, etc.

Always search first using operators like `site:github.com` or `site:reddit.com`.

Read the project’s `CONTRIBUTING.md` or support guidelines before posting.

### Stack Overflow and Stack Exchange

Stack Overflow remains valuable for high-quality, searchable answers, but usage has shifted. Search thoroughly first (including with AI tools). If posting:

- Use clear Markdown formatting with syntax-highlighted code blocks.
- Add relevant tags.
- Edit your question as needed with new information.
- Accept the best answer and upvote helpful ones.

Many projects now direct users to their own GitHub Discussions instead.

### Real-time chat (Discord, Slack, Matrix, etc.)

These are excellent for interactive help. Lurk first, read the rules and pinned messages, and use threads where available.

### Use meaningful, specific subject headers

**Bad:** “Help me!” or “It doesn’t work”  
**Good:** “PostgreSQL 16: Connection refused on Ubuntu 24.04 after Docker upgrade – exact error and `postgresql.conf` attached”

Clear titles help people decide whether they can help and make the thread useful for future searchers.

### Make it easy to reply

Provide all necessary context upfront. On platforms that support it, use direct replies or mentions appropriately.

### Write in clear, grammatical, correctly-spelled language

Text-speak, excessive abbreviations, or poor grammar make your question harder to understand and less likely to receive good answers.

### Send questions in accessible, standard formats

- Use plain text or Markdown (widely supported).
- Avoid proprietary file attachments unless specifically requested.
- For code, logs, or config files, use fenced code blocks with language specifiers:

```python
# Your code here
Be precise and informative about your problem

Describe symptoms in chronological order.
Include software versions, operating system, environment details, and exact error messages.
State what you have already tried (including AI attempts and prompting details if relevant).
Provide context, but keep it concise.

Don’t dump huge logs — use GitHub Gists or paste services and link them.
Don’t claim you found a bug unless you have strong evidence. Most issues are configuration or usage problems.
Describe the symptoms, not your guesses at the cause.
Describe your goal, not just the step you’re stuck on.
Don’t ask for replies by private email/DM unless the forum encourages it. Public answers help everyone.
Be explicit about what you are asking.
For code questions: Provide a minimal reproducible example, expected vs. actual behavior.
Don’t post homework questions without showing your own effort.
If you solve it while writing the question, post the solution anyway — it helps others.
Don’t mark your question as “Urgent” — your emergency is not everyone else’s.
Courtesy costs nothing and can help.
Always follow up with a brief note on the solution when you resolve the issue. This is especially valuable now as it improves future AI training data and helps other searchers.

How To Interpret Answers
RTFM and STFW (“Read The Fine Manual” and “Search The Fine Web”) are still excellent advice. If someone points you to documentation or a search, it usually means the answer is there — go read it.
If you don’t understand an answer, ask for clarification politely.
Some communities are blunt. Focus on the technical content rather than tone.

On Not Reacting Like A Loser
If you get a short or critical reply, don’t take it personally. Learn from it and improve your next question. Reacting defensively or demanding more help makes you look bad and reduces future help.

Questions Not To Ask

“Can anyone help me?” (too vague)
“What’s the best way to do X?” without showing research
“Please debug my entire program for me”
Requests that clearly expect others to do your work


Good and Bad Questions
Bad example:
“My program doesn’t work. What’s wrong?”
Good example:
“I’m getting ConnectionRefusedError when trying to connect to PostgreSQL 16 from a Python 3.12 script on Ubuntu 24.04 using psycopg2. I tried increasing the timeout as suggested by Claude using this prompt [paste prompt], but it still fails. Here’s the minimal code, exact error, and my connection string: [gist link]. Any ideas?”
The good example shows effort, provides details, and is searchable.

If You Can’t Get An Answer

Try a different forum or channel.
Refine your question based on feedback (or use AI to improve it).
Consider whether the problem is too niche or requires paid support.


How To Answer Questions in a Helpful Way

Be clear and concise.
Point to documentation or resources when appropriate.
Suggest trying a well-crafted prompt with an AI assistant (and optionally share an example prompt).
If you don’t know the answer, say so — but perhaps suggest where to look next.

Helping others thoughtfully builds the community.

Acknowledgements
Original guide by Eric S. Raymond and Rick Moen.
Updated in 2026 by Grok (xAI) to incorporate modern tools, platforms, and AI prompting best practices while preserving the original spirit and principles.
The fundamentals — showing effort, being precise, and respecting others’ time — remain as important as ever. AI tools have changed the first step, but human expertise is still essential for complex, context-specific, or novel problems.

This guide is released under the same terms as the original (freely redistributable). Feel free to link to, fork, or adapt it with attribution.
text✅ **Here's the complete, full Markdown document** — everything in one single block with no missing parts.
