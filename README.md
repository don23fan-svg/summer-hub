Summer Hub — Project Files
This is the knowledge base for the Summer Hub family app. Upload these files to the
Claude Project so future chats have the full picture.
Files
index.html — THE APP. The complete, current Summer Hub. This is the live file that
gets uploaded to GitHub Pages (renamed to index.html at the repo root). All editable
config (REWARDS, TIER_WEIGHTS, SPARKS_BY_KID, REQUIRED, OPTIONS, SCHEDULE)
lives near the top of the <script> block. This is the source to edit for any change.
Code.gs — THE BACKEND. The Google Apps Script that powers cross-device sync. Lives
in the Apps Script editor attached to the "Summer Hub Data" Google Sheet, deployed as a
web app ("execute as me," "anyone with the link"). Its /exec URL is hardcoded into
index.html as SCRIPT_URL. Only re-deploy via "Manage deployments → Edit → New version"
to keep the same URL.
SETUP.md — the one-time backend setup guide (create Sheet, paste Code.gs, deploy,
authorize, copy URL). Already completed, kept for reference / re-setup.
reward-qa.html — DIAGNOSTIC ONLY, do not deploy. A standalone page that previews the
mystery-box reward odds at each milestone using the same engine as the app. Regenerate
it whenever REWARDS or TIER_WEIGHTS change so it stays in sync.
PROJECT_INSTRUCTIONS.md — the text to paste into the Project's custom-instructions
box (not the knowledge base). Primes every chat with the app's architecture, decisions,
and Ben's working preferences.
Deploy reminder
To update the live app: edit index.html → on GitHub, upload the new file (replacing the
old index.html) → commit → Pages republishes in ~1-2 min. Same URL, home-screen icons
keep working. Have one device load it on good wifi first so any data migration writes
cleanly before other devices open.
The live URL
Hosted on GitHub Pages under account don23fan-svg. Exact URL is in the repo's
Settings → Pages ("Your site is live at …"). Pattern: https://don23fan-svg.github.io/REPO-NAME/
