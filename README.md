# Ghost Job Detector 👻

A purely client-side web application built with HTML, CSS, and Vanilla JavaScript to analyze job posting URLs and determine the likelihood of them being "ghost jobs" based on textual heuristics.

## Features
- No backend required (Serverless).
- Bypasses CORS using the public `allorigins.win` proxy.
- Analyzes DOM text for red flags like 30+ day posting age, "evergreen" pipeline keywords, missing salaries, and vague buzzwords.
- Responsive, modern UI.

## How to Deploy to GitHub Pages (Zero Config)

Since this app is completely client-side, deploying it is incredibly fast.

1. **Create a Repository:** Go to your GitHub account and create a new public repository (e.g., `ghost-job-detector`).
2. **Upload Files:** Upload the `index.html` file and this `README.md` directly to the root of your new repository. Commit the changes.
3. **Enable GitHub Pages:**
   - In your repository, click on the **Settings** tab.
   - On the left sidebar, click on **Pages**.
   - Under "Build and deployment", look for "Source". Select **Deploy from a branch**.
   - Under "Branch", select the `main` (or `master`) branch, and leave the folder as `/ (root)`.
   - Click **Save**.
4. **Wait a minute:** GitHub will build your site. In a minute or two, refresh the Settings > Pages screen, and you will see a link at the top saying: *"Your site is live at https://[your-username].github.io/ghost-job-detector/"*

## Limitations & Known Issues
Major job boards (like LinkedIn, Indeed, Glassdoor) utilize sophisticated anti-bot software (like Cloudflare). Because this app relies on a public proxy to fetch HTML, these sites will frequently block the request or return a CAPTCHA page. The app includes logic to detect when a security check blocks the scrape and will alert the user gracefully.
