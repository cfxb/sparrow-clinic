# sparrow.clinic

Professional website for Sparrow Neuropsychology, built with Jekyll.

## Where everything lives

| What | Where |
|------|-------|
| Source code | GitHub: [cfxb/sparrow-clinic](https://github.com/cfxb/sparrow-clinic) |
| Hosting | Cloudflare Pages (free) |
| Domain | sparrow.clinic (DNS managed by Cloudflare) |
| Local copy | `/Users/christo/Documents/claude/my-site/sparrow-clinic/` |

Cloudflare Pages is connected to the GitHub repo. When you push changes to the `main` branch, Cloudflare automatically rebuilds and deploys the site within a couple of minutes.

---

## How to edit content

Every page is a `.md` (Markdown) file. Edit the text below the `---` front matter block.

### Page files

| Page | File to edit |
|------|-------------|
| Home | `index.md` |
| About | `about.md` |
| Services | `services.md` |
| Referral | `referral.md` |
| Contact | `contact.md` |
| Privacy policy | `privacy-policy.md` |

### Other content files

| Content | File |
|---------|------|
| Home page service cards | `_data/services.yml` |
| Contact info (phone, fax, email, address) | `_data/contact.yml` |
| Navigation menu | `_data/navigation.yml` |
| BC hospitals table | `_data/hospitals.yml` |

### Markdown basics

```
## Heading
### Smaller heading

Normal paragraph text.

**bold text**   *italic text*

- Bullet item
- Another item

[Link text](https://example.com)

![Alt text](/assets/images/filename.jpg)
```

---

## Option 1: Edit on GitHub (easiest)

This is the simplest way to make quick edits from any device.

1. Go to [github.com/cfxb/sparrow-clinic](https://github.com/cfxb/sparrow-clinic)
2. Navigate to the file you want to edit (e.g. `about.md`)
3. Click the pencil icon (Edit this file)
4. Make your changes
5. Click **Commit changes** at the bottom

That's it. Cloudflare will automatically rebuild and deploy within a few minutes.

---

## Option 2: Edit locally and push

For larger changes, or to preview before publishing.

### First time setup (already done on your Mac)

Ruby 3.3.6 is installed via rbenv. The project is at:
```
/Users/christo/Documents/claude/my-site/sparrow-clinic/
```

### Edit, preview, and push

```bash
# 1. Go to the project folder
cd /Users/christo/Documents/claude/my-site/sparrow-clinic

# 2. Pull the latest from GitHub (in case you edited online)
git pull

# 3. Edit any .md file in a text editor

# 4. Preview locally
eval "$(rbenv init -)" && bundle exec jekyll serve
# Open http://localhost:4000 in your browser
# Press Ctrl+C to stop the server

# 5. Stage your changes
git add -A

# 6. Commit
git commit -m "Describe what you changed"

# 7. Push to GitHub (triggers Cloudflare deploy)
git push
```

### If `bundle exec jekyll serve` doesn't work

```bash
eval "$(rbenv init -)" && bundle install
```

Then try `bundle exec jekyll serve` again.

---

## Option 3: Edit with Claude Code

Open a terminal, navigate to the project, and use Claude Code to make changes conversationally.

```bash
cd /Users/christo/Documents/claude/my-site/sparrow-clinic
claude
```

Then ask Claude to make edits, e.g.:
- "Change the wait time on the referral page to 6-10 weeks"
- "Add a new service card for epilepsy"
- "Push my changes to GitHub"

Claude can edit files, preview the site, commit, and push for you.

---

## How deployment works

```
You edit files ──> push to GitHub ──> Cloudflare detects the push
                                          │
                                          ▼
                                   Builds the Jekyll site
                                          │
                                          ▼
                                   Deploys to sparrow.clinic
```

- Cloudflare runs `jekyll build` using the Gemfile in the repo
- Builds typically take under a minute
- You can check build status at: [Cloudflare Dashboard](https://dash.cloudflare.com) > Workers & Pages > sparrow-clinic > Deployments

---

## Adding images or files

1. Put images in `assets/images/` and documents in `assets/files/`
2. Reference them in markdown:
   ```
   ![Description](/assets/images/photo.jpg)
   [Download form](/assets/files/form.pdf)
   ```
3. Commit and push as usual

---

## Security notes

The GitHub repository is **public**, which means:

- **All source code and content is visible to anyone.** This is fine for a professional website — everything on it is public-facing content anyway.
- **No secrets in the repo.** Contact details (email, phone, fax, address) are in `_data/contact.yml`. These are already public on the live website, so having them in the repo is no different.
- **Do not put private files in the repo.** Patient data, internal documents, passwords, or anything confidential should never be added. The `.gitignore` file helps prevent accidental commits of build artifacts, but be mindful of what you add.
- **GitHub account security matters.** Anyone with access to your GitHub account (cfxb) can modify the site. Use a strong password and enable two-factor authentication (2FA) at [github.com/settings/security](https://github.com/settings/security).
- **Cloudflare account security also matters.** Your Cloudflare account controls DNS and hosting. Use a strong password and enable 2FA there as well.

If you'd prefer the source code to be private, you can change the repo visibility to **Private** at [github.com/cfxb/sparrow-clinic/settings](https://github.com/cfxb/sparrow-clinic/settings) > Danger Zone > Change visibility. Cloudflare Pages will still work with a private repo.

---

## Site structure reference

```
sparrow-clinic/
├── _config.yml              # Site settings (title, URL, plugins)
├── Gemfile                  # Ruby dependencies
├── _data/
│   ├── contact.yml          # Shared contact info used across pages
│   ├── navigation.yml       # Top navigation menu links
│   ├── services.yml         # Service cards on the home page
│   └── hospitals.yml        # BC hospital table on services page
├── _includes/               # Reusable HTML fragments (header, footer, etc.)
├── _layouts/                # Page templates (default, page, home)
├── _sass/                   # Stylesheets (SCSS)
├── assets/
│   ├── css/main.scss        # Main stylesheet entry point
│   ├── images/              # Site images
│   └── files/               # Downloadable files (referral forms)
├── index.md                 # Home page
├── about.md                 # About page
├── services.md              # Services page
├── referral.md              # Referral page
├── contact.md               # Contact page
└── privacy-policy.md        # Privacy policy
```
