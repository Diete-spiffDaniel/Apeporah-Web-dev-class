# Apeporah Web Development Course

A beginner-friendly web development course built as a static website. It uses plain HTML, CSS, and JavaScript; there is no package installation or build step.

## Pages

- `index.html` — Apeporah landing page and interactive lessons.
- `course.html` — searchable 12-topic course outline with links to individual lessons.
- `playground.html` — browser-based HTML, CSS, and JavaScript editor with a sandboxed live preview and a button to download your work as a standalone HTML website.
- `practice.html` — a game-style quiz with hints, XP, streaks, badges, and saved progress.
- `web-development-notes.md` — downloadable reference notes for all 12 course topics.

## Preview locally

Open `index.html` in a browser. The Course, Playground, and Practice links open the other pages; the course pages link to the downloadable study notes. To preview through a local server from this folder, run:

```powershell
python -m http.server 8000
```

Then visit `http://localhost:8000`.

## Deploy with GitHub Pages

1. Create a GitHub repository and add all four HTML pages, `web-development-notes.md`, and `README.md` to its root.
2. Push the files to the repository's `main` branch.
3. In the repository, open **Settings**, then **Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**.
5. Choose the `main` branch and `/ (root)` folder, then save.
6. Wait for the Pages deployment to finish and open the URL shown in the Pages settings.

## Deploy with Netlify

1. Sign in to Netlify and choose **Add new site**.
2. Connect the GitHub repository, or use Netlify Drop to upload the project folder.
3. Leave the build command empty and set the publish directory to the project root (or `.` if the form requires a value).
4. Deploy the site and open the generated URL.

## Before sharing

- Open the deployed URL on a phone-sized screen and a desktop screen.
- Check the course navigation, code tabs, chapter notes, and completion progress.
- Check the practice game's answers, hints, saved XP, and the downloadable notes link.
- In the playground, edit each code tab, confirm the live preview updates, and download the result as `my-website.html`.
- Confirm the preview image, web fonts, and all pages or links load as expected.
- Review the browser console for errors.
- Remember: lesson completion is stored in the visitor's browser with `localStorage`; progress is not synced between devices.
- The sample image and fonts are loaded from external services, so they require an internet connection.

This is a static educational demo. The playground runs learner code in a sandboxed browser frame. Course and game progress are stored in the visitor's browser; there are no accounts, database, server-side form handling, or cross-device sync.
