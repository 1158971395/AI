# CODE REDESIGN TASK: AI Insights → Medium Style

## Current State
The website at `C:\Users\1158971395\.openclaw\workspace\AI-pages` is a simple knowledge base. 
It's on GitHub: `1158971395/AI`, deployed via Cloudflare Pages at jonathanxu.xyz.

## Requirements

Redesign ALL HTML files to look like Medium.com — clean, minimal, content-first.

### Design Spec
- **Body font**: Georgia (serif) for article content, like Medium
- **UI font**: -apple-system, sans-serif
- **Background**: #fafafa (warm off-white)
- **Card background**: #ffffff
- **Text color**: #1a1a1a
- **Secondary text**: #757575
- **Accent blue**: #1a73e8
- **No borders/radii**: 0px border radius, sharp corners like Medium
- **Max content width**: 700px for articles, centered
- **Max homepage width**: 1040px

### Content Style: 新智元 Level Quality

Rewrite article content with professional, in-depth analysis like 新智元 (a top Chinese AI media outlet).

**Style guidelines:**
- Start each article with a **核心洞察** (Core Insight) blockquote — one punchy thesis statement
- Use numbered sections: `01 | 02 | 03` style headers
- Include **comparison tables** for data
- Add **行业启示** (Industry Implications) section
- Use bold for key data points
- Include a **关键数据一览** table at bottom
- Remove ALL weak phrases like "值得注意的是"、"这意味着" — be direct
- NO "AI生成总结图" or similar labels anywhere
- Each article should feel like a professional analyst report

### Data Visualization
Data should be shown VISUALLY, not as plain text:
- Use HTML `<div class="data-cards">` with 3-6 data cards per article
- Each data card: `<div class="data-card"><div class="value">数字</div><div class="label">说明</div></div>`
- Use comparison tables: `| 公司 | 投入 | 困境 |`
- Use `<div class="highlight-box">` for key insights
- For metrics: always show **对比数据** (industry avg alongside, e.g. NPS 76 vs industry 30-50)

### Per-File Changes

#### 1. index.html (Homepage)
- Title: "AI Insights" (remove "· 深度阅读")
- Hero: title + one-line subtitle
- Article list: LEFT IMAGE (200x134px, object-fit:cover) + RIGHT TEXT
- Thumbnails: ryt-bank-summary.png, bigtech-ai-debt.png, qoderwork-design-desk.png
- Card: tag | title (20px bold) | excerpt (2 lines) | date · source
- Footer: "© 2026 AI Insights · By 徐章皓 · Powered by OpenClaw 🤖"
- Nav: Home | 金融科技 | 商业分析 | About

#### 2. Article Pages (3 files)
STRUCTURE (top to bottom):
1. Cover image (top, 100% width, max-height:400px, object-fit:cover)
2. Tag label (uppercase, small, blue)
3. Title (34px, bold, tight letter-spacing: -0.4px)
4. Date · Author/Source
5. Excerpt line (16px, #757575)
6. Body content in Georgia serif 18px
7. Data cards section
8. Key data summary table at bottom
9. Original link: 📎 <a>查看原文</a>
10. Footer

FILES:
- `20260519-bigtech-ai-debt.html` — 大厂迷途
- `20260518-揭秘全球首家ai原生银行ryt-bank-7个月破120万用户.html` — Ryt Bank
- `20260519-qoderwork-design-desk.html` — QoderWork

#### 3. about/index.html
Simple About page in same Medium style.

#### 4. Deletions
- Delete `categories/` folder entirely (all empty)
- Delete `feed.xml` (not needed)
- Delete `TASK.md` after completion

### Content Preservation
- ALL article text content must be preserved
- ALL .png images must stay (just change display style)
- ALL links must work

### Technical Requirements
- UTF-8 encoding on all files (use `fs.writeFileSync(path, content, 'utf8')` in Node.js, NOT PowerShell Set-Content)
- Responsive design for mobile
- After completion: git add -A, git commit -m "Redesign: Medium style", git push

## IMPORTANT: Encoding Warning
DO NOT use PowerShell Set-Content for writing HTML files — it will corrupt Chinese characters. Use Node.js fs.writeFileSync with 'utf8' encoding.

## Start
Execute this task now. Read each file, redesign it according to the spec, then commit and push.
