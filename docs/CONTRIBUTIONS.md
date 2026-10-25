# 📋 Profile Maintenance Guide

How to update and maintain this GitHub profile README repository.

---

## Table of Contents
- [Updating the Introduction](#updating-the-introduction)
- [Adding a New Project](#adding-a-new-project)
- [Replacing the Banner](#replacing-the-banner)
- [Adding a New Technology](#adding-a-new-technology)
- [Updating Social Links](#updating-social-links)
- [Troubleshooting Statistics Cards](#troubleshooting-statistics-cards)
- [Checking Links](#checking-links)
- [General Maintenance](#general-maintenance)

---

## Updating the Introduction

1. Open `README.md`
2. Find the `## 👋 About Me` section
3. Update the text while keeping it:
   - Under ~150 words
   - Honest about your current status
   - Focused on what you build rather than generic statements
4. Update the typing SVG text if needed by modifying the `lines=` parameter in the Typing SVG URL

---

## Adding a New Project

### In README.md

1. Find the `## 🚀 Featured Projects` section
2. Copy an existing project table block
3. Replace with your new project details:
   - Project name and emoji
   - One-line description in the blockquote
   - "What it does" summary
   - Key engineering points (only verified features)
   - Technology badges
   - Status: use ✅ Deployed, ✅ Complete, 🔨 In Progress, or 🔬 Concept
   - Links to live demo and source code (only if they exist)

### In docs/PROJECTS.md

1. Add a new section following the existing format
2. Include: description, technology table, key features, engineering decisions, limitations, and future improvements

### Status Labels
- `✅ Deployed` — Live and accessible on the web
- `✅ Complete` — Core functionality implemented, code is public
- `🔨 In Progress` — Actively being developed
- `🔬 Concept` — Idea exists, implementation is partial or not yet public

### Rules
- Never claim a feature exists unless the code proves it
- Never invent deployment links
- Distinguish between your original work and forked repositories

---

## Replacing the Banner

1. Create or edit the SVG file at `assets/profile-banner.svg`
2. The banner should be:
   - **1200×300 pixels** for optimal display
   - Dark background (#0d1117) for GitHub dark mode compatibility
   - Still readable in light mode
   - No confidential information
3. The README references it as `./assets/profile-banner.svg`
4. After pushing, verify it renders correctly on your GitHub profile

---

## Adding a New Technology

1. Open `README.md` and find the `## 🛠️ Technical Skills` section
2. Choose the correct category (Languages, Frontend, Backend, etc.)
3. Add a badge using the shields.io format:
   ```markdown
   <img src="https://img.shields.io/badge/TECHNOLOGY_NAME-COLOR?style=for-the-badge&logo=LOGO_NAME&logoColor=white" alt="Technology Name" />
   ```
4. Find the correct logo name at [simpleicons.org](https://simpleicons.org/)
5. Only add technologies you have actually used or are actively learning
6. If you're only learning it, place it under "Currently Exploring"
7. Update `docs/TECH_STACK.md` with the project context

---

## Updating Social Links

### Adding Email
In `README.md`, find the comment `<!-- Add email badge when ready -->` and uncomment/replace:
```markdown
[![Email](https://img.shields.io/badge/Email-your@email.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:your@email.com)
```

### Adding LeetCode
In the `## 🧠 DSA & Problem Solving` section, uncomment the LeetCode badge and replace `YOUR_LEETCODE_USERNAME`.

### Updating LinkedIn
Find the LinkedIn badge URLs and update the `href` and display text.

---

## Troubleshooting Statistics Cards

### GitHub Stats Card Not Loading
- **Service:** [github-readme-stats](https://github.com/anuraghazra/github-readme-stats)
- The free tier has rate limits. If the card shows an error, it usually resolves within minutes.
- You can deploy your own instance on Vercel for unlimited requests.

### Streak Stats Not Loading
- **Service:** [github-readme-streak-stats](https://github.com/DenverCoder1/github-readme-streak-stats)
- Check if `https://github-readme-streak-stats.herokuapp.com` is available.
- Alternative: Use `https://streak-stats.demolab.com` as the base URL.

### Activity Graph Not Loading
- **Service:** [github-readme-activity-graph](https://github.com/Ashutosh00710/github-readme-activity-graph)
- The Vercel deployment may have rate limits.
- If it fails, the README remains readable without it.

### General Tips
- All stats widgets depend on third-party services — they may occasionally be unavailable
- Never fake statistics or contribution data
- The profile should look clean even without stats cards loading

---

## Checking Links

Before pushing updates, verify:

1. **Repository links:** Click each GitHub repository link
2. **Deployment links:** Visit each live demo URL
3. **Social links:** Verify LinkedIn URL opens correctly
4. **Image paths:** Ensure SVG files exist at `./assets/`
5. **External services:** Check that badge/stats URLs are responding

---

## General Maintenance

### Monthly
- Update project statuses if anything has changed
- Add new projects or remove discontinued ones
- Verify all deployment links are still live

### Quarterly
- Review and update the "About Me" section
- Update "Current Focus" if priorities have shifted
- Check if any technology badges need to be added or removed
- Verify stats card services are still functional

### When Adding New Repositories
- Consider featuring them in the README if they demonstrate significant work
- Update `docs/PROJECTS.md` with the details
- Update `docs/TECH_STACK.md` if new technologies were used
