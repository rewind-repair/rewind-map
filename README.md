# Rewind Jobs (rewind-map v3)

Phone web app for techs and admins: today's jobs, all open jobs, map, FedEx parts,
full ticket details, Teams status updates and the closure form.

Everything comes from Nord Claude's relay (Apps Script). The page holds no keys
except the Google Maps browser key, and no codes: each person's 6-digit code is
checked by the relay.

## Files (upload all to the repo root, replacing the old index.html)
- index.html — the app
- manifest.webmanifest, sw.js, icon-192.png, icon-512.png — home-screen install + offline

## One-time setup
1. Relay: paste rewind_relay_appscript.gs, save, Deploy → Manage deployments → edit → New version.
2. In the Apps Script editor run `makeAppCodes` and read the codes in the execution log.
   Send each tech their own code. `removeAppCode('123456')` takes access away.
3. First run of the app asks Apps Script for the Maps (geocoder) permission — run any
   function once in the editor and accept if prompted.

## Install on a phone
- iPhone: open the link in Safari → Share → Add to Home Screen.
- Android: open in Chrome → ⋮ → Install app (or Add to Home screen).
