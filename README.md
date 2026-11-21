# EverThere: app for judges

EverThere is an app that puts a parent's live AI avatar on a caregiver's screen to comfort a child. This guide takes about five minutes. You need a microphone and internet, plus either a browser or an Android phone or tablet.

## 1. Open the app

**Fastest: in a browser.** Open **https://everthere-web.m-vamshikrishna22.workers.dev** in Chrome, Edge or Safari, on a laptop, tablet or phone. Allow the microphone when the call asks. It is the same app as the APK, built from the same code. A wide window (700px or more) gets the classroom-tablet layout, with the "Who's teaching?" PIN switch.

**Or install the Android APK:**

> **Download:** https://github.com/mallelavamshi/everthere-app/releases/latest/download/EverThere.apk
> (release page: https://github.com/mallelavamshi/everthere-app/releases/latest)

1. Open the download link on your Android device and download the APK.
2. Open the file. If Android asks, allow installs from this source (Settings, then Install unknown apps).
3. Open **EverThere**.

The API is live at https://everthere-api.m-vamshikrishna22.workers.dev, so there is nothing else to set up. Source code: https://github.com/mallelavamshi/everthere

## 2. Try the demo (no account needed)

On the Welcome screen tap **Try the demo ✨**, then choose one:

| Choice | You become |
| --- | --- |
| **Peek as a Parent 👩‍👧** | Sarah Johnson, Mia's mom |
| **Peek as a Teacher 🍎** | Ms. Jess Parker, Butterflies Room, Little Acorns Daycare |

Both are already set up with a seeded world. Mia's Daddy is the app maker's own Napster digital twin (his real face and voice, used with his consent). Every other face is AI-generated. To switch persona, open the profile menu (round avatar button, top right) and tap **Sign out**.

## 3. What to try: a guided tour

1. **As a Parent (Sarah).** The bottom tabs are Home, My Avatar, Sessions and Caregivers. Alerts is the bell icon at the top, not a tab.
   - From Home, open the **comfort plan** for Mia: Mommy's nicknames, tone, favorites, the song, and the locked safety rules that can't be edited.
   - Open **Sessions**. The flagged session is Mia's seeded boo-boo session (the one with a flag on it). Read its summary and transcript.
   - Open **Caregivers** to see the daycare and the home caregivers, and the per-caregiver transcript switch.
2. **As a Teacher (Ms. Jess), on a phone or a tablet.**
   - Open the profile menu (the round avatar button at the top right, "Open profile"), tap **Sign out**, then **Try the demo** and **Peek as a Teacher**.
   - **On a tablet (700px or wider),** Peek as a Teacher sets the tablet up for you, and a **"Who's teaching?"** sheet opens on the roster. Pick **Jess Parker** and enter PIN **1234**. (You can also close the sheet without picking. The roster still opens, and the chip at the top, "Who's teaching? · Switch", reopens it.) On a phone there is no sheet.
   - Open the **roster** and tap **Mia**.
   - Pick the reason **Missing Mommy**. If asked which parent to call, pick Mommy. Tap **💛 Call Mommy's avatar**. Allow the microphone when asked. Mommy's avatar greets Mia.
   - Say **"I fell and hurt my knee"**. An orange banner slides in: that is the live `flag_concern` tool firing. The avatar answers warmly and tells the child to show the grown-up.
   - Optional: tap **🎵 Song** ("Our song") to hear Mommy's avatar sing "Twinkle, Twinkle, Little Star". A toast says 🎵 Singing "Twinkle, Twinkle, Little Star".
   - **End** the call, then do the **check-in** (Calmer, Same, or Still upset) and tap **Send to Sarah**.
3. **Back as the Parent (Sarah).** Open the profile menu, **Sign out**, then **Peek as a Parent**. The summary usually arrives within about a minute, and up to about 4 minutes if Napster's webhook is delayed. Then **Sessions** shows the new session with its summary and mood, and the **bell (Alerts)** shows "💛 Mia's comfort session" and "⚑ Heads up about Mia" for the knee. Open the session for the transcript.
4. **On a tablet (700px or wider), switch teacher.** Tap the **"Who's teaching? · Switch"** chip (or the teacher's name once chosen) and enter PIN **1234** for Jess Parker (**2468** for Tanya Brooks, the daycare admin). PIN switching only appears on tablet-sized screens of 700px or wider. A phone gives you the plain teacher view.

Calls are capped at 10 minutes, with a warning at 8.

## 4. Things to know

- **Mic permission.** The first call asks to record audio. On Android tap **While using the app** (if you denied it, enable it in Android Settings, Apps, EverThere, Permissions, Microphone). In a browser click **Allow** (if you blocked it, click the microphone or lock icon in the address bar). The child's camera is never used in a call.
- **"EverThere is resting."** If a call won't start and you see "EverThere is taking a little rest", the shared demo budget was reached ($120 total, and 200 calls a day per demo user). Try again later. It is a deliberate guard, not a crash.
- **The nanny path is not in the demo.** Try the demo only offers Parent and Teacher. Home caregivers are set up with real accounts, which you can create yourself.
- **Nightly reset.** The demo world resets every night at 08:00 UTC, so sessions you create will disappear then and every judge sees a fresh world.
- **Demo accounts are shared.** Other judges may be using them at the same time. Writes work, but you can't delete the accounts.
- **Voices.** Mia's Daddy speaks in the maker's own cloned voice (his Napster digital twin). The other demo parents use stock voices. Avatars use Napster's v1 photo mode, so lip-sync is softer than v2 video.
- **No push notifications when the app is closed.** Alerts are in-app, and local notifications appear while the app is open.
- **Want the full path?** You can sign up for real as a parent and make an avatar from your own photo. The consent step applies to you.

## 5. Troubleshooting

| Symptom | Try |
| --- | --- |
| APK won't install | Allow installs from your browser or file manager in Settings. Needs a reasonably current Android version. |
| Photos or avatars don't load | Check internet. Pull to refresh. |
| "All our avatars are busy hugging" | Napster allows only a few live calls at once. Wait a minute and retry. |
| Avatar can't hear you | Check the microphone permission, and that the device isn't muted. |
| Avatar video is slow to appear the first time | A fresh avatar takes several seconds to prepare. Wait for it. |
| No summary after a call | It usually arrives within about a minute, and up to about 4 minutes if the webhook is delayed (a background sweep picks up late ones). |
| "The demo is waking up — try again in a moment" | Shown by Try the demo when the demo is busy, resting or rate limited. Wait a minute and tap Try the demo again. |
| No "Who's teaching?" sheet | The screen is narrower than 700px. Use a tablet. |
| Stuck or odd state | Open the profile menu, Sign out, and use Try the demo again. |
