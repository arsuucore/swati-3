# For Swati 🐱🤿 — setup guide

This is a single self-contained page (`index.html`). Here's how to finish it and put it online.

## 1. Add her photos

Create a folder called `photos` next to `index.html`, and add 6 photos named:

```
photos/1.jpg
photos/2.jpg
photos/3.jpg
photos/4.jpg
photos/5.jpg
photos/6.jpg
```

- They show up one at a time on the loading screen, then again as the reward photo after each correct answer, then all together on the final "polaroid wall."
- If you skip this, the page still works fine — it just shows a cute 🐱 / 📷 placeholder instead.
- JPG or PNG both work. Square-ish photos look best.

## 2. Add the songs (optional but recommended)

Create a folder called `audio` next to `index.html`, and add these files (any of them you don't have can just be left out):

| File | Used for |
|---|---|
| `audio/udi-udi.mp3` | background music (loops, toggle button top-right) |
| `audio/kesariya.mp3` | preview button on the "song" question |
| `audio/apna-bana-le.mp3` | preview button on the "song" question |
| `audio/tum-hi-ho.mp3` | preview button on "what's our song" |
| `audio/me-gustas-tu.mp3` | preview button on "what's our song" |
| `audio/bairan.mp3` | preview button on "song that reminds you of us" |
| `audio/must-be-the-wind.mp3` | plays when the 6th heart flies away in the minigame |
| `audio/yumm.mp3` | plays when she copies the ice cream coupon code |
| `audio/pop.mp3` | small happy pop sound for correct answers / catching hearts |
| `audio/yay.mp3` | happy "yay!" sound when she hits Play on the very first screen |
| `audio/wrong.mp3` | a little "aww"/sad sound for wrong answers |

You'll need to source these audio clips yourself (e.g. trim a short clip from a song you've legally purchased/downloaded, or use a royalty-free "pop"/"whoosh" sound for `pop.mp3` and `must-be-the-wind.mp3`).

> Tip: keep clips short (5–15 seconds) and the same filenames as above — the page won't break if a file is missing, it'll just be silent for that sound.

## 3. Edit the content (no coding needed)

Open `index.html` in any text editor and scroll to the `EDIT ME` section near the top of the `<script>` tag. There you can change:

- `COUPON_CODE` — the code she'll send you back for the ice cream 🍦
- Each question's `caption` — the little handwritten note shown with the reward photo
- The questions/options/answers themselves, if anything needs tweaking

There's also an `intro-text` paragraph near the very top of the page (search for `EDIT ME: write your own little paragraph`, just above the `<script>` tag, inside `<section id="screen-intro">`) — that's the "Hello cutey!" message on the first screen. Edit it directly to whatever you want to say to her.

## 4. About the placeholders

If you open the page before adding photos/audio, that's expected and not a bug:
- Photos show a 🐱 placeholder instead of a real photo.
- Songs/sounds just stay silent (the page checks for the file and skips it gracefully if it's missing).

Once you add the real files to `photos/` and `audio/` with the exact names above, they'll automatically show up — no code changes needed.

## 4. Host it on GitHub Pages

1. Create a new GitHub repo (e.g. `for-swati`).
2. Upload `index.html`, plus your `photos/` and `audio/` folders, keeping that folder structure.
3. Go to **Settings → Pages**, set the source to your default branch (`main`) and root folder.
4. Wait a minute, then your page will be live at:
   ```
   https://<your-username>.github.io/for-swati/
   ```
5. Send that link to Swati! 💕

## How the experience flows

1. **Intro screen** — a dancing cat, "Hello cutey!" message (edit this!), and a Play button that plays a happy "yay" sound.
2. **Loading screen** — her photos cycle with "loading your favourite person..." then a Start button appears.
3. **Quiz** — 6 questions, multiple choice. Correct answers trigger confetti + a dancing mascot + a polaroid reveal of one of her photos with a handwritten caption. Wrong answers gently shake, play a little "aww" sound, and let her try again.
4. **Minigame** — after question 3, a "catch 5 hearts" game appears. Catching the 5th spawns a 6th heart that flies away dramatically with "must be the wind 💨".
5. **Finale** — score, a polaroid wall of all 6 photos, and the ice cream coupon code with a copy button.

Good luck Adarsh 🍦💕
