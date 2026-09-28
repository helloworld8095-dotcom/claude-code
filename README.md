If you mean **Claude Code’s Cloud Session repo picker**, there are a few different GitHub connections in Claude, because apparently one GitHub integration was insufficient for humanity.

The most likely issue is **the Claude GitHub app doesn't have access to that specific repository**.

### Check this first

1. Go to GitHub → **Settings → Applications → Installed GitHub Apps**.
2. Find **Claude** / the Claude GitHub App.
3. Check **Repository access**.
4. If it's set to **Only select repositories**, make sure your repo is selected.
5. If it's already selected, disconnect/reconnect GitHub in Claude and try the Cloud Session again. Anthropic specifically recommends checking the GitHub App's repository access when repos don't appear. ([Claude Help Center][1])

### If it's a private repo

Claude's normal GitHub integration can access private repos, but you have to grant it access. Anthropic says that when a private repo doesn't appear, the usual cause is that the GitHub App hasn't been granted access to that repo. ([Claude Help Center][2])

If the repo belongs to a **GitHub organization**, there's another possible culprit: **SSO**. If that organization requires SSO, you may need to authorize Claude for that organization under GitHub's application settings. ([Claude Help Center][2])

### One important distinction

If you're talking about **Claude Code Cloud Sessions**, don't confuse that with Claude's regular **“Add from GitHub”** feature.

The regular GitHub connector lets Claude access repository files in chats/projects. Cloud Sessions are running Claude Code in a remote environment, so the repo has to be available to the Cloud Session's GitHub integration/environment. Anthropic's current documentation confirms that remote connectors such as GitHub are available across Claude surfaces, including Claude Code. ([Claude Help Center][3])

If **your repo is public and still doesn't appear**, that's a different problem. In that case, tell me **what you see in the Cloud Session repo picker** (or send a screenshot), because we can narrow down whether you're hitting a GitHub authorization problem, a Cloud Session limitation, or Claude simply failing to surface the repository.

[1]: https://support.claude.com/en/articles/14233555-set-up-code-review-for-claude-code?utm_source=chatgpt.com "Set up Code Review for Claude Code | Claude Help Center"
[2]: https://support.claude.com/en/articles/10167454-use-the-github-integration?utm_source=chatgpt.com "Use the GitHub integration | Claude Help Center"
[3]: https://support.claude.com/en/articles/11725091-when-to-use-desktop-and-web-connectors?utm_source=chatgpt.com "When to use desktop and web connectors | Claude Help Center"
