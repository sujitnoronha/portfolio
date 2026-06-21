---
date: 2025-01-10
authors: [sujit]
categories:
  - Projects
  - Raspberry Pi
tags:
  - self-hosting
  - mkdocs
  - portfolio
---

# Building My Portfolio Site on a Raspberry Pi

I decided to host my personal portfolio on my Raspberry Pi instead of using a generic platform. Here's how I set it up...

## Why Self-Host?

- **Full control** over the stack and design
- **No platform lock-in** — I own my content
- **Learning opportunity** — sysadmin, networking, deployment
- **Cost** — basically free after hardware

## The Stack

| Component | Choice |
|-----------|--------|
| Static Site Generator | MkDocs Material |
| Hosting | Raspberry Pi 4 |
| Web Server | Nginx |
| SSL | Let's Encrypt |
| CI/CD | GitHub Actions |

## Setup Process

### 1. Environment

```bash
python3 -m venv ~/blog-venv
source ~/blog-venv/bin/activate
pip install mkdocs-material
```

### 2. Project Structure

```
portfolio/
├── docs/
│   ├── blog/
│   │   └── posts/
│   ├── about.md
│   ├── contact.md
│   ├── index.md
│   └── projects.md
└── mkdocs.yml
```

### 3. Deployment

[Details on nginx config, SSL, etc.]

## Lessons Learned

1. **MkDocs Material is incredible** — the blog plugin, search, and theming are top-notch
2. **Virtual environments are your friend** — keeps the Pi's system Python clean
3. **Start simple, iterate** — don't over-engineer v1

## Next Steps

- [ ] Set up automatic deployment via GitHub Actions
- [ ] Add analytics (privacy-friendly)
- [ ] Experiment with custom plugins

---

*Have you self-hosted a site? What was your experience?*
