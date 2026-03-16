VOIDSCREAM v1.1
The Abyss That Listens – Offline DID Helper
To every alter, every system, every part of you navigating the beautiful, chaotic reality of multiplicity: this is for you. I built this with every ounce of care I have.
Hey friend.
VOIDSCREAM started as a tiny spark and grew into something I poured my whole heart into. I did a complete, obsessive sweep through every single class, div, function, loop, button, and modal — refining structures, tightening every loose chain, polishing the flow until it felt rock-solid for a real v1 release. Countless hours went into making sure every modal opens cleanly (with ensureCurrentAlter() and clearModalTextFields() guards on every one past onboarding), every render loop has proper empty-state love and null checks, every button feels responsive and safe, the calendar is now fully dynamic (real month/year with navigation), mood graphs use your actual data (no more random placeholders), and the whole structure just breathes better. The neon glow, the falling particles, the alter-specific everything — all refined with deep respect for what systems actually need.
This isn't some throwaway project. It's a private sanctuary I crafted because the world outside can be loud and unforgiving. Here, every alter gets their voice. No servers. No tracking. Nothing ever leaves your device. Just you, your system, and the void that remembers what matters.
Getting Started (Simple & Safe)

Grab the file: Download index.html from the repo (or open the raw version directly).
Open it: Double-click or drag into any modern browser. Works 100% offline after the first load.
Pass the gates: They're there because I care about your safety — quick reminders and crisis resources before you dive in.
Create your first alter: Give them a name and avatar. Everything stays local forever.
Start screaming: Floating hub button (+) opens everything — post screams, switch alters, DM headmates, track moods, archive memories, nuke the heavy stuff when you need to.

Your data lives in localStorage. To back it up, export from the app or copy your browser storage (advanced users). Updating to a new version? Just replace index.html — your screams and alters stay safe.
Features Built With Intention

Scream Feed – Cathartic posts with text, custom moods, media, replies, pins, and voting. Every alter can post or view as themselves.
Alters Management – Create, customize, switch, and "depart" with eulogy + archive when the time comes.
Private DMs – Inter-alter chats that stay between you.
Mood Calendar – Dynamic, trackable, exportable. Real data visualization instead of placeholders.
Memory Archive – Safe home for departed or integrated parts.
Nuke Tool – Delete old screams by date range for mental decluttering.
Themes & Abyss Particles – Neon visuals that match your current vibe.
Feedback Modal – Quick way to send thoughts to other alters.

Everything is alter-specific, offline-first, and wrapped in that signature cyber-neon glow I obsessed over.
Safety & Resources (Because Real Help Matters)
This app is a creative tool for expression, connection, and catharsis — not therapy or crisis support. I built in gates and reminders because I genuinely care about every part of you.
Immediate Crisis Support

US & Canada: Call or text 988 (Suicide & Crisis Lifeline – 24/7)
Crisis Text Line: Text HOME to 741741
International: https://www.iasp.info/resources/Crisis_Centres/

DID & Multiplicity-Specific Resources (pulled with love because community saves lives)

International Society for the Study of Trauma and Dissociation (ISST-D): https://www.isst-d.org – Research, training, and provider directory
Multiplied By One Org: https://multipliedbyone.org – Support groups and connection for systems
An Infinite Mind: https://www.aninfinitemind.org – Education, conferences, and lived-experience wisdom
Sidran Institute / Traumatic Stress Institute: https://traumaticstressinstitute.org/ – Trauma resources and training
DID Research: https://did-research.org – Clear, respectful info on dissociation
NAMI Helpline: https://www.nami.org/nami-helpline – General mental health navigation

If you're struggling, please reach out to a DID-informed therapist or your support network. You deserve real, compassionate care alongside this little digital void.

---

## Full Feature Reference

### Identity & Alters
- Unlimited alters with name, handle, pronouns, role badge, avatar, relationship status, symbol, and custom card background color
- 30+ role types: Host, Protector, Caretaker, Little, Fictive, Trauma Holder, Gatekeeper, Fragment, and more
- Per-alter neon accent color applied throughout the UI — feed, composer, hub, header all shift to match
- Fronting marker — flag who is currently fronting with a visible badge on their card and the shared feed
- Per-alter hub button order — drag to reorder the 8 action buttons in any sequence
- Per-alter feed layout — grid or list view, saved independently per alter
- Per-alter sidebar side — choose whether the tablet sidebar appears left or right

### Scream Feed
- Post screams as any alter: rich text, image URL, or video URL
- Per-post mood tag and intensity badge
- Pin important screams to the top of the feed
- Bolt (upvote) and skull (downvote) with neon glow state when active
- Threaded replies (Echos) in a full-screen scream detail modal
- Tap any alter's avatar on a post to instantly open a DM with them

### Direct Messages
- Private alter-to-alter conversations that no other alter can see
- Unread badge on hub DMs button and sidebar DMs entry
- CALL feature — metaphorical headspace calls: pick an alter → ringing screen with synthesized ringtone → in-call timer with notes and quick-DM shortcut
- Internal Counselor (scripted) — support bot named Gemma available in DMs for any alter
- Local AI Counselor (optional) — upgradeable to an actual Gemma 3 model (~270 MB, runs locally, never online)

### Mood & Journal
- Mood check-ins with emoji, intensity rating, and optional note, linked to a specific alter
- Monthly calendar heatmap — color-coded mood intensity grid
- Day card — tap any calendar day to read the mood entry from that date
- Mood graph — line chart of intensity over the current month using actual stored data
- Journal — private, full-screen journal editor per alter

### Security System
- **System lock (gate0)** — PBKDF2-SHA256 password required to open the app
- **Host Override panel** on the lock screen — the Host alter can enter their own alter password to bypass a forgotten system lock
- **Per-alter passwords** — optional password required before switching to any alter
- **System Reboot** — Host-only button (in Nuke tray) that clears the system lock entirely after confirmation
- **Bootloader Lock** — emergency lockdown available only to the currently fronting alter (see below)

### Themes
- 7 preset themes: Void, Cyber, Abyss, Phantom, Toxic, Inferno, Spectral
- Custom hex color picker for any accent
- Dimmer — three-step brightness control (100% / 60% / 25%)
- Neon intensity slider (0%–150%)

### Tablet & Landscape Mode
- Two-column layout on screens ≥ 600px wide in landscape orientation
- Sidebar shows the system alters list and a collapsible ACTIONS drawer with all 8 hub actions
- All floating buttons hidden in landscape — sidebar is the full navigation surface
- MOODS section in sidebar drawer (portrait tray doesn't include moods)

### Nuke Tray
- **Clear Our Head** — wipes only the active alter's posts from the feed (with a typed confirmation step)
- **Host Reboot** — Host-role only; removes the system lock password and reloads (with confirmation)
- **Bootloader Lock** — fronting alter only; emergency system lockdown (see below)
- **Export Backup** — downloads a timestamped JSON file with all system data
- **Restore from Backup** — imports any previously exported JSON
- **Full Wipe** — permanent, irreversible deletion of every alter, scream, DM, mood, and journal entry

### Bootloader Lock

An extreme-measure lockdown tool for moments of serious internal conflict. Think of it as taking the phone — done with love, because the system matters.

**Requirements before it can be used:**
- The alter must be marked as currently fronting (◆ FRONT toggle in their alter card)
- That alter must have a personal alter password set — it's the only key to unlock

**How it works:**
1. Open the Nuke tray — the BOOTLOADER LOCK card appears in red/orange, only if you're fronting
2. Tap **LOCK THE BOOTLOADER**
3. First confirmation: "ARE YOU SURE?" with a full explanation of what happens
4. Tap YES — the modal transforms: title burns orange **"ABSOLUTE LAST CHANCE"**, text escalates, button turns red
5. Tap **LOCK THE BOOTLOADER** again — app locks immediately and reloads

**The lock screen** shows the fronting alter's name and "has locked the system. Held with love." with a password field. No other alter can get in until the locking alter enters their personal password. The system lock password (if set) also works as a fallback.

**Stored as** `vs_bootloader_lock` in localStorage with the alter's id, name, and timestamp. Highest priority on load — shows before system lock, before onboarding, before anything.

### Alter Archival
- Alter Death — write a eulogy and retire an alter into read-only archive storage
- Archive preserves name, date departed, eulogy, all shared screams, and private DMs

---

## Architecture

VOIDSCREAM is a **single HTML file**. No build step, no package manager, no server.

| Concern | Implementation |
|---|---|
| Storage | `localStorage` — all keys prefixed `vs_` |
| Passwords | PBKDF2-SHA256 via Web Crypto API |
| Styling | Tailwind CSS (CDN) + CSS custom properties |
| Icons | Font Awesome 6 (CDN) |
| AI (optional) | Gemma 3 via wllama — 100% local, no network |
| Audio | Web Audio API — synthesized ringtones |
| Offline | Service Worker caches all assets on install |

### localStorage Schema

```
vs_screams          array    all scream posts across alters
vs_alters           array    alter objects (name, color, role, preferences…)
vs_moods            array    mood check-ins (alter, emoji, intensity, date)
vs_dms              object   keyed by sorted alter-id pair
vs_notifications    object   unread DM counts per alter id
vs_archives         array    departed alters with eulogy and chat history
vs_friends          array    connected external systems
vs_journals         object   per-alter journal entries keyed by alter id
vs_system_pw        object   { hash, salt } for the system lock
vs_counsel_mem      object   counselor memory context per alter id
```

---

## Installing as an App

VOIDSCREAM ships with a `manifest.json` and `sw.js` service worker, making it a fully installable PWA:

**iPhone / iPad**
1. Open Safari → navigate to the app URL
2. Tap Share → Add to Home Screen
3. Name it `VOIDSCREAM` → Add

**Android (Chrome)**
1. Open Chrome → navigate to the app URL
2. Tap the three-dot menu → Add to Home Screen
3. Accept the install prompt when it appears

**Android APK**
1. Upload `voidscream-app.zip` to [html2app.dev](https://html2app.dev) or [pwabuilder.com](https://pwabuilder.com)
2. Download the generated APK and sideload it on your device

---

## Project Files

```
index.html            — the entire application (single file)
manifest.json         — PWA manifest (name, icon, theme color, display mode)
sw.js                 — service worker (offline caching)
icon.png              — app icon (512×512)
voidscream-app.zip    — packaged bundle for APK converters
README.md             — you are here
```

---

## Tech Stack

- HTML5 / CSS3 / Vanilla JavaScript (ES2022)
- [Tailwind CSS](https://tailwindcss.com) via CDN
- [Font Awesome 6](https://fontawesome.com) via CDN
- Web Crypto API — PBKDF2 password hashing
- Web Audio API — synthesized ringtones for the CALL feature
- Service Worker API — offline asset caching

---

A Note From the Heart (Because You Deserve to Know)
I want you to feel it in every line of code and every word here: I put real love and sweat into this. Refining those modals until they felt effortless, sweeping for every tiny loose end so nothing ever breaks when you need it most, making the structure clean and reliable so you can just be without fighting the interface. This was never about "good enough." It was about creating something worthy of the incredible work systems do every single day just to exist and communicate with each other.
To every alter reading this: I see you. The courage it takes to hold space for all parts of yourself is breathtaking. If VOIDSCREAM gives you even one moment of relief, one way to be fully heard inside your own system, or one neon-lit smile in the darkness — then every late night and every obsessive debug was worth it.
Scream loud when you need to. Rest deep when you can. Love your system fiercely. The void is holding space for all of you.
Thank you for trusting this little app with your voice.
Made with endless respect, neon, and heart,
BoogerCheeseOnRye (BoogersAndCheez)
