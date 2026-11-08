# App Support

Shared static support site for independent iOS apps by Marko Peng. Plain HTML/CSS, local SVG, system fonts, no JavaScript, build step, backend, cookies, analytics, or third-party dependencies.

## GitHub Pages

Publish `main` from `/ (root)` in Settings → Pages → Deploy from a branch. Keep `.nojekyll`. This is a project site at https://markogoodman.github.io/app-support/; do not add a CNAME or change the separate blog repository or account domain.

- Directory: https://markogoodman.github.io/app-support/
- BoxCount privacy: https://markogoodman.github.io/app-support/boxcount/privacy/
- BoxCount support: https://markogoodman.github.io/app-support/boxcount/support/

## Add an app

1. Create `<app-name>/privacy/index.html` and `<app-name>/support/index.html` using the existing pages as layout examples. Use lowercase URL slugs.
2. Replace all app-specific text, page titles, descriptions, contact details, and navigation. Inspect that app’s source and confirm unknown facts before publishing. Do not reuse BoxCount privacy claims without verification.
3. Add an app card and links to root `index.html`. Add local assets under `assets/` if needed.
4. Nested pages use `../../assets/styles.css`, `../../` for the directory, and `../privacy/` or `../support/` for sibling pages. Preserve the project-site path when using absolute URLs.
5. Check keyboard navigation, focus visibility, light/dark appearance, narrow screens, and all direct public URLs after deploying.

## Update policies

Recheck actual app behavior and SDKs; update the app-specific policy and effective date when behavior changes. Keep support information consistent. Commit descriptive changes so Git history preserves previous policies. Recheck the App Store Connect privacy answers against the exact release build. Do not publish placeholder contact details or unverified privacy promises.

## Source review and release limits

BoxCount source reviewed locally on November 8, 2026: `TileCalculator/Core/Repository.swift` and `ProjectStore.swift` store local JSON; `Core/Models.swift` defines stored project content; `Core/Calculator.swift` defines calculations and shared text; `ProjectEditor.swift` uses Apple ShareLink; `MyApp.swift`, `ContentView.swift`, `Package.swift`, and the Xcode project were also inspected. No app network calls, analytics, advertising, StoreKit, accounts, cloud sync, or third-party packages were found. No app source is included in this public repository.

The support email `marko958m@gmail.com` was explicitly confirmed by the owner for public support and privacy inquiries. US$1.99 upfront pricing and absence of subscriptions/IAP were supplied by the owner and match the app README; App Store Connect configuration and the final distributed binary were not available for verification. There is no fabricated App Store link or claim that the app is already available to download. Check the final release build, App Store pricing/privacy answers, and backup behavior before app release. Device backup is disclosed conditionally; no permanent deletion, encryption, or universal “no data anywhere” guarantee is made. Email providers and GitHub hosting operate separately from the offline app.

## Local preview

From the parent directory run `python3 -m http.server 8000 --directory .` and visit `/AppSupport/`. No installation or build is needed.
