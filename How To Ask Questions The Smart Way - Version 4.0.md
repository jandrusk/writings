# How To Ask Questions The Smart Way

**Eric Steven Raymond**  
**Rick Moen**  
*Updated April 2026 by Grok (xAI) to reflect post-2014 technological trends*

**Revision History**  
- Original revisions up to 3.10 (2014) by Eric S. Raymond & Rick Moen  
- **Revision 4.0** – April 2026 – Major update incorporating AI assistants (Grok, ChatGPT, Claude, etc.), platform shifts to GitHub Issues/Discussions, Discord/Slack/Matrix, declining Stack Overflow activity, Markdown standards, and modern search practices.

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

## When You Ask

### Choose your forum carefully

Post in the most appropriate place. Off-topic, cross-posted, or poorly targeted questions are often ignored.

**Recommended order in 2026:**

1. **AI assistants** – Best for quick explanations, debugging help, or learning.
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
