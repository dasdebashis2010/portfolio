# Debashis Das — Portfolio Site

A single-file portfolio site (`index.html`) built around your background: IT Operations across VMware, Windows, and Azure, layered with OT/Process Control Network experience at Shell and Baker Hughes. No build tools, no dependencies to install — just HTML/CSS/JS, plus your `resume.pdf` sitting alongside it for the download button. Open `index.html` in a browser and it works.

## 1. A few things worth double-checking

The content is pulled directly from your resume, but two small things are worth a look before you publish:

- **Project write-up links**: the 4 project cards don't link anywhere yet (search `EDIT:` near line 443). Add a link if you write up any of them elsewhere, or leave as-is — the cards read fine without one.
- **GitHub profile**: there's no GitHub link in the Contact section (search `EDIT:` near line 540) since none was in your resume. Add one if you have a public profile you'd like linked.

Everything else — your name, title, bio, skills, all 3 roles, certifications, and awards — is already filled in from your resume.

## 2. Personalize further (optional)

Open `index.html` in any text editor to tweak anything:

- Skill bars: edit the label text and the `--val` percentage (0–1) — the current values are estimates based on years of experience per skill area, feel free to adjust
- Project cards: swap in different achievements if you'd rather highlight something else
- Contact links (email, LinkedIn, phone) are live and clickable as-is

You don't need to touch the `<style>` or `<script>` sections unless you want to change the look.

## 2. Preview it locally

Just double-click `index.html` to open it in your browser. To see it the way it'll actually behave when hosted (recommended, since some browsers restrict local files slightly differently), run a tiny local server from this folder:

```bash
python3 -m http.server 8000
# then open http://localhost:8000
```

## 3. Put it on GitHub

If you don't have git or a GitHub account yet: install [Git](https://git-scm.com/downloads) and create a free account at [github.com](https://github.com).

From inside this folder:

```bash
git init
git add .
git commit -m "Initial portfolio"
```

Create a new **empty** repository on GitHub (no README/license, since you already have one) named something like `portfolio` or `yourusername.github.io`, then:

```bash
git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO.git
git branch -M main
git push -u origin main
```

## 4. Host it free with GitHub Pages

1. On GitHub, open your repo → **Settings** → **Pages** (left sidebar).
2. Under "Build and deployment", set **Source** to `Deploy from a branch`.
3. Set **Branch** to `main` and folder to `/ (root)`, then **Save**.
4. Wait ~1 minute, then refresh — GitHub will show you the live URL.

Two naming options:
- Repo named `yourusername.github.io` → site is live at `https://yourusername.github.io`
- Repo named anything else (e.g. `portfolio`) → site is live at `https://yourusername.github.io/portfolio`

Every time you `git push` a change after this, the live site updates automatically within a minute or two.

## 5. Optional: custom domain

If you buy a domain later, add a `CNAME` file with just your domain name in it to the repo, then point your domain's DNS to GitHub Pages (GitHub's Pages settings page will show you exactly what records to add).

## Notes on the design

The visual language is built around your role: a "status bar" header like an industrial HMI, IT/OT content organized into two color-coded domains (teal for IT, amber for OT), project cards styled like equipment nameplates, and a timeline styled like a process line. All of it is standard HTML/CSS — no frameworks — so it'll keep working indefinitely with zero maintenance.
