Subhas Chakraborty — Portfolio

A single-page, single-file portfolio site with a "lens switcher" — the same experience, projects, and skills reframed for three roles: Data Scientist, Data Analyst, and Business Analyst.

🔗 Live site: https://subhas07.github.io/

Features
Role-based lenses — one toggle re-renders the headline, summary, skills, and project write-ups to match how a Data Scientist, Data Analyst, or Business Analyst would frame the same work.
Single HTML file — no build step, no dependencies. Just open index.html or deploy as static content.
Responsive layout — adapts down to mobile, including the stat grid, project cards, and experience list.
Accessible tab switcher — lens buttons use role="tablist" / aria-selected for screen readers.
Tech
Vanilla HTML, CSS, and JavaScript (no frameworks, no build tools)
Fonts: Fraunces, Inter, JetBrains Mono via Google Fonts
Project structure
.
├── index.html      # everything — markup, styles, and lens data/logic
└── README.md

All per-lens content (summary text, skill groups, project copy) lives in the DATA object near the bottom of index.html. The render(lens) function swaps the DOM content and CSS accent color whenever a lens button is clicked.

Running locally

No build step required — just open the file in a browser:

bash
open index.html        # macOS
# or
python -m http.server  # then visit http://localhost:8000
Deploying

Works on any static host — GitHub Pages, Netlify, Vercel, or Cloudflare Pages. For GitHub Pages:

Push this repo to GitHub.
In Settings → Pages, set the source to the main branch, root folder.
Rename portfolio.html to index.html if it isn't already, so it's served at the root.
Customizing
Content: edit the ds, da, and ba objects inside the DATA constant in the <script> block — each holds its own summary, skill groups, and project list.
Accent colors: each lens sets its own accentVars.accent / accentVars.soft, applied as CSS custom properties (--accent, --accent-soft).
Static sections (Experience, Education, Certifications, Volunteer) aren't lens-driven — edit them directly in the HTML body.
Contact
Email: subhaschakraborty104@gmail.com
LinkedIn: linkedin.com/in/subhas007
GitHub: github.com/subhas07
