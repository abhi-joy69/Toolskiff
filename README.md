# ToolSkiff

**Free online tools that run in your browser. No sign-up, and your files stay on your device.**

ToolSkiff is a growing collection of simple, fast utilities for everyday tasks: working with images and PDFs, handling text, and doing quick calculations. Every tool has its own page and its own web address, so each one is easy to find, share and bookmark.

> **Status:** In development. The design and page layout are built. Tools and login are being added one at a time.

---

## Why ToolSkiff exists

Most online file tools ask you to upload your files to a server, make you create an account, or bury the tool under ads and pop-ups. ToolSkiff is built on a different idea:

- **Private by design.** Files are processed in your own browser. They are not uploaded to a server.
- **Free to use.** No payment and no sign-up needed to use any tool.
- **Fast and light.** Plain HTML, CSS and JavaScript, with no heavy frameworks.
- **Works everywhere.** Designed for phones first, since many people use tools on mobile data.
- **Clear and simple.** One task per page, in plain language, for people from any country.

---

## Tools

Each tool lives on its own page. Status shows what is built.

### Image tools
| Tool | What it does | Status |
|---|---|---|
| Compress image | Reduce JPG, PNG or WebP size to a target in KB | Planned |
| Resize image | Change width and height in pixels | Planned |
| Convert image | PNG to JPG, JPG to WebP, WebP to PNG | Planned |

### PDF tools
| Tool | What it does | Status |
|---|---|---|
| JPG to PDF | Turn photos into one PDF file | Planned |
| Merge PDF | Combine several PDFs into one | Planned |
| Split PDF | Separate a PDF into single pages | Planned |
| Rotate PDF | Fix sideways or upside-down pages | Planned |

### Text and developer tools
| Tool | What it does | Status |
|---|---|---|
| Word counter | Count words, characters and reading time | Planned |
| QR code generator | Make a QR code for any link or text | Planned |
| Password generator | Create strong random passwords | Planned |

### Calculators and converters
| Tool | What it does | Status |
|---|---|---|
| Loan EMI calculator | Monthly payment, interest and total cost | Planned |
| Unit converter | Length, weight and temperature | Planned |

More tools will be added over time, for example PDF compression, PDF to JPG, background removal, currency and time zone converters, and study and writing helpers.

---

## Features

**Built**
- Responsive homepage with tool search and categories
- Reusable tool page layout (title, tool area, how to use, FAQ, related tools)
- Light grey and teal design, with automatic dark mode
- Separate address (URL) for every page
- Pages for About, Contact, Privacy and Terms
- Sign-in page design

**In progress**
- Working tools, added one by one
- Optional account login with Supabase (email and Google)
- Saved tool history for signed-in users

**Planned**
- Multiple languages
- Installable app mode (PWA) and offline use
- More tools and categories

Login is always **optional**. Every tool works without an account.

---

## Privacy approach

- Image, PDF and text tools run locally in the browser using JavaScript.
- Files you choose are not sent to ToolSkiff servers.
- Accounts, if you create one, are handled by Supabase. Only an email address and saved history are stored.
- Some tools may call a public service when needed (for example, live currency rates). Those tools will say so on their page.

See the Privacy Policy page for details.

---

## Built with

| Part | Technology |
|---|---|
| Pages and structure | HTML |
| Design | CSS (custom, no framework) |
| Tool logic | JavaScript (plain) |
| PDF handling | `pdf-lib` (runs in the browser) |
| Login and database | Supabase (Auth and Postgres) |
| Hosting | GitHub Pages (free) |

---

## Folder structure

```
toolskiff/
├── index.html              Homepage
├── css/
│   └── style.css           All design: colors, layout, fonts
├── js/
│   └── main.js             Shared code (search, menu)
├── auth/
│   ├── config.js           Supabase project URL and anon key
│   └── auth.js             Sign in, sign up, sign out, Google login
├── login/
│   └── index.html          Sign-in page
├── tools/
│   ├── compress-image/
│   │   ├── index.html      The page (own URL, own SEO text)
│   │   └── tool.js         Code for this tool only
│   ├── resize-image/
│   └── ...                 One folder per tool
├── about/
├── contact/
├── privacy/
├── terms/
├── sitemap.xml             List of pages for search engines
└── robots.txt              Rules for search engines
```

**How to add a new tool:** copy an existing folder inside `tools/`, rename it to the new tool's name, then edit its `index.html` (title, description, text) and `tool.js` (the code). Finally, add a card for it on the homepage and a line in `sitemap.xml`.

---

## Run it on your computer

There is no build step.

1. Download or clone this repository.
2. Open `index.html` in your browser.

Some features (like login) work properly only on a web address, so for those, test on the live GitHub Pages site.

---

## Publish with GitHub Pages

1. Open the repository **Settings**, then **Pages**.
2. Under **Source**, choose **Deploy from a branch**.
3. Select the `main` branch and the `/ (root)` folder, then save.
4. After about a minute, the site is live at `https://abhi-joy69.github.io/toolskiff/`.

---

## Set up login (Supabase)

1. Create a project at supabase.com.
2. In **Project Settings, then API**, copy the **Project URL** and the **anon public key**.
3. Paste them into `auth/config.js`.
4. In **Authentication, then Providers**, turn on **Email**. Add **Google** later.
5. In **Authentication, then URL Configuration**, set the **Site URL** to your GitHub Pages address.

> **Security warning:** only the *anon* key belongs in this repository. Never commit the `service_role` key. This repository is public, and anyone could read and misuse it.

---

## Search engine setup

Each tool has its own page with a unique title, description and short guide, which helps people find the right tool on Google. Pages for tools that are not finished yet are marked `noindex`, and the mark is removed when the tool is ready.

After going live:
1. Replace the `YOURNAME` placeholder in the canonical links and `sitemap.xml` with your real address.
2. Add the site to Google Search Console and submit `sitemap.xml`.

---

## Roadmap

1. Design and page layout (done)
2. Login with Supabase
3. Image tools: compress, resize, convert
4. PDF tools: JPG to PDF, merge, split, rotate
5. Text tools and calculators
6. Accessibility and speed checks
7. Sitemap, Search Console and launch
8. More tools, languages and offline mode

---

## Contributing

Ideas and bug reports are welcome. Open an **Issue** to suggest a new tool or report a problem. Please describe what you expected and what happened, and mention your browser and device.

---

## License

All rights reserved by the repository owner, unless a license file states otherwise.

---

## Contact

Questions or tool requests: add your email here, or open an Issue on this repository.
