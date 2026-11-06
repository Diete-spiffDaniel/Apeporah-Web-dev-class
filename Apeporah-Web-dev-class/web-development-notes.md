# Apeporah Web Development Notes

A practical beginner reference for the 12 chapters in the Apeporah web development course.

## 1. HTML: page structure

- HTML describes the meaning and structure of content; it is not a programming language.
- Start documents with `<!doctype html>`, then use `html`, `head`, and `body`.
- Put metadata and the page title in `head`; put visible page content in `body`.
- Use meaningful elements such as `header`, `nav`, `main`, `section`, `article`, and `footer`.
- Keep headings in a logical order. Use anchors for navigation and buttons for actions.
- Give informative images useful `alt` text; use `alt=""` for decorative images.
- Connect each form field to a visible `label`.

## 2. CSS: style and layout

- A CSS rule has a selector and declarations. A declaration is a property and a value.
- The cascade resolves competing rules using origin, importance, specificity, and source order.
- The box model contains content, padding, border, and margin. `box-sizing: border-box` simplifies sizing.
- Use Flexbox for a row or column and Grid for layouts with rows and columns.
- Save repeated values in custom properties such as `--brand-color` and use them with `var()`.
- Prefer flexible units such as `rem`, `%`, and `fr` where they fit the layout.
- Keep text readable with a sensible `max-width`; include visible keyboard focus styles.

## 3. JavaScript: basic programming

- Use `const` for bindings you do not reassign and `let` when a value needs to change.
- Common values include strings, numbers, booleans, arrays, objects, `null`, and `undefined`.
- Functions package reusable steps. Conditions choose a path; loops repeat work.
- Use descriptive variable names and keep functions focused on one task.
- Read errors in the browser console and fix the first relevant error before chasing later ones.

## 4. DOM and events

- The Document Object Model (DOM) is the browser's structured representation of a page.
- Use `querySelector()` to find the first matching element and `querySelectorAll()` to find all matches.
- Add behavior with event listeners for events such as `click`, `input`, and `submit`.
- Use `textContent` for plain text and `classList` to change visual state.
- Check that an element exists before attaching a listener.
- Events bubble upward through the DOM; event delegation can handle many child controls from one parent.

## 5. Forms and validation

- Use a `form` with a clear submit button and a visible label for every control.
- Choose input types such as `email`, `tel`, and `date` to match the expected value.
- Attributes such as `required`, `min`, `max`, and `pattern` provide built-in browser validation.
- Listen to the form's `submit` event so keyboard submission works too.
- `FormData` can collect named input values.
- Client-side validation helps visitors, but a server must validate again before trusting or storing data.
- Explain errors in text near the relevant field and preserve entered values when possible.

## 6. Responsive design

- Include the viewport meta tag so mobile browsers use the device's actual layout width.
- Start with a layout that works in a narrow column; add breakpoints when content needs more room.
- Prefer flexible tracks such as `minmax()`, `fr`, percentages, and `max-width` to fixed page-wide widths.
- Make images responsive with `max-width: 100%` and `height: auto`.
- Leave comfortable space around touch controls and do not rely on hover for essential information.
- Test real content at narrow and wide sizes, zoom in, and check for overlap and horizontal scrolling.

## 7. Accessibility

- Prefer semantic HTML before ARIA. Native buttons, links, headings, and form controls include useful behavior.
- Make every action available by keyboard and keep the focus indicator visible.
- Give controls clear accessible names and associate form labels with their inputs.
- Write useful alt text for meaningful images and empty alt text for decorative images.
- Keep contrast strong; never use color as the only way to distinguish states or instructions.
- Respect reduced-motion preferences and avoid flashing content.
- Test with keyboard-only navigation, browser zoom, and a screen reader when possible.

## 8. Browser tools and Git

- Browser DevTools can inspect elements and styles, show JavaScript errors, inspect requests, and emulate screen sizes.
- Reproduce a problem, read the first relevant console error, and narrow it to a small example.
- `git status` shows changed files; `git diff` reviews changes; `git add` stages them; `git commit` saves a checkpoint.
- Commit related changes with clear messages and review the diff before committing.
- A remote repository stores a copy of Git history for sharing and deployment.
- Never upload passwords, API keys, or private customer data to a public repository.

## 9. APIs and data

- An API defines how software can request or send data. Many web APIs use HTTP and return JSON.
- `fetch()` returns a Promise. Use `await` inside an `async` function to work with its response.
- Check `response.ok` and `response.status`; HTTP error responses do not automatically reject a fetch.
- `response.json()` parses a JSON response body asynchronously.
- Show loading, success, empty, and error states so people know what the page is doing.
- Cross-origin requests are governed by same-origin and CORS rules; the remote server must allow access.
- Never place private API keys in frontend JavaScript. Browser requests are visible to visitors.

## 10. Quality, security, and performance

- Resize and compress images; large files are a common cause of slow pages.
- Use descriptive page titles, concise descriptions, meaningful headings, and helpful link text.
- Load only the scripts, fonts, and styles the page needs.
- Use HTTPS for published sites.
- Treat form input and URL parameters as untrusted. Validate on a server and do not render untrusted input as HTML.
- Never put secrets in HTML or browser JavaScript; keep private credentials on a server.
- Collect only the information you need and explain how submitted data is used.

## 11. Testing and debugging

- Test behavior a visitor can see, not just internal code structure.
- Manual checks are valuable: follow links, submit forms, resize the page, and try keyboard navigation.
- Unit tests check a small function; integration tests check connected pieces; end-to-end tests follow a user workflow.
- Use the console for JavaScript errors and the Network panel for failed or slow requests.
- Reproduce a bug reliably, change one likely cause at a time, then repeat the same test.
- Check empty, invalid, loading, success, and error states, not only the ideal case.
- Before publishing, test a narrow screen, keyboard access, images, links, and browser-console output.

## 12. Publishing

- A static host serves files such as HTML, CSS, JavaScript, and images; this course needs no build command.
- Keep `index.html` at the published folder root so it opens as the home page.
- GitHub Pages and Netlify can publish a static project directly.
- After deployment, check the public URL, links, images, fonts, mobile layout, and browser console.
- Connect a custom domain through your registrar's DNS settings; changes can take time to appear.
- Do not publish private files, personal data, or secrets in a public repository.

## Before you share a page

- Does every link and button work?
- Can you use it with a keyboard?
- Does it fit a phone screen and a desktop screen?
- Are images described, text readable, and errors explained?
- Have you checked the browser console and network requests?
