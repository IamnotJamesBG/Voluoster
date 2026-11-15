# Voluost

Voluost is a volume booster for Android. Your phone stops at its maximum volume, and sometimes that maximum is not enough: a quiet podcast, an old recording, a pair of earbuds that were cheap for a reason. Voluost gives you more room above that ceiling, and it comes with bass and a real equalizer so the extra volume still sounds like music.

One dial, one sound screen, one settings page. No account, no sign-in, nothing to buy. Free.

**Current version: 1.0.3** for Android 6.0 and newer.

---

## Download

Get the APK from the [`Release/Free`](https://github.com/IamnotJamesBG/Voluoster/tree/main/Release/Free) folder. Grab the file with the highest version number in its name. The direct link to the current build is:

```
https://raw.githubusercontent.com/IamnotJamesBG/Voluoster/main/Release/Free/Voluost-v1.0.3.apk
```

Open the downloaded file to install it. Android will warn you that it comes from an unknown source, which is expected for anything not distributed through Play. Allow installs for your browser or file manager when it asks, and let the system installer finish the job.

---

## What it does

**It boosts.** From 0 up to +50 dB on top of whatever your phone is already doing, in 1% steps on the dial. The default is +7 dB, which is a sensible place to start. On Android 9 and newer the sound runs through the system's own dynamics processor, adding gain and then catching peaks with a limiter so things get louder without turning to crackle. On older phones it falls back to a different effect and still works.

**It boosts everything.** Games, videos, podcasts, voice notes, the browser, apps that never announce themselves. Where a phone allows it, the effect covers the whole output mix, so anything making sound gets louder. Where it does not, Voluost attaches to the apps that ask for audio effects, and the app tells you plainly which of the two you got instead of pretending.

**It has bass.** A slider from 0 to 100, produced by lifting the low end of the equalizer rather than by a second effect fighting it. Slide it up and the bottom comes up.

**It has an equalizer.** Five bands tuned to the frequencies your device actually exposes, each labelled with its real frequency. Seven presets: Flat, Bass, Vocal, Acoustic, Treble, Loudness and Custom. Move a band and it becomes Custom.

**It remembers separate tunings for separate headphones.** A curve that flatters a phone speaker sounds terrible on in-ear headphones, so Voluost keeps three setups: speaker, wired headphones and Bluetooth. Plug something in and the right one takes over on its own. You can also switch profiles by hand if you want to set up your Bluetooth tuning before you get in the car.

**It changes presets smoothly.** Pick a new preset and the bands glide to their new positions over about a third of a second, one after the other, so you can watch the curve change shape instead of blinking.

**It switches on from the shade.** Voluost adds a Quick Settings tile. Add it once and you can turn the boost on or off without opening the app. The tile says Boosting, Paused or Off so you always know where you stand.

**It keeps running.** A foreground service holds the boost while you leave the app, open something else or lock the screen. The ongoing notification has working Pause and Stop buttons, and tapping it brings you back.

**It recovers by itself.** Android gives audio effects to whatever asks last and takes them away when the output changes or the audio server restarts. Voluost checks every 20 seconds whether it still has control and reattaches if it lost it, so plugging in headphones or connecting Bluetooth does not need a restart.

**It tells you the truth.** The diagnostics screen shows which effect chain is attached, whether it is reaching the whole system or only the apps that announced themselves, how many apps it is serving right now, the output route, the sample rate and buffer, and whether background running and notifications are allowed. If the boost is not audible on your phone, that screen says why.

---

## The screens

**Boost** is the dial. Drag it, or use the plus and minus below it. Your level sits in the middle in dB with a zone name under it: Off, Light, Moderate, Loud, Very loud, Red. Below that is a status card with a dot, a plain sentence about what is happening, a pause button and the on/off switch, then two small cards showing your bass and EQ settings that take you to the sound screen.

**Sound** is where you tune things. The top tells you what you are listening on and which profile you are editing, then comes the bass switch and slider, the equalizer switch, the preset chips and the band sliders.

**More** has the small things: remember my level, restore after reboot, haptics, the automatic update check, audio diagnostics, Terms of Service, Privacy Policy, hearing safety, replay the intro, and the version number.

On first launch you get a short introduction instead: what the app does, how it sounds, what it will not do, and a last card offering to stop Android from shutting it down in the background. That one is optional, it opens the system dialog for you, and your answer is remembered.

---

## About that +50 dB

+50 dB is roughly a thousand times the signal power. On headphones that is enough to hurt, quickly. What Voluost does not claim is that all fifty of those decibels arrive cleanly. Past about +30 dB you are adding more distortion than volume, and past +40 dB the limiter is working hard enough to hear. The dial says so, the warning card says so, and this paragraph says so.

Start lower than you think you need, then give your ears a few minutes before going up. Ears are bad at noticing damage while it is happening.

---

## Permissions

Voluost asks for very little.

- **Modify audio settings** is what lets it attach audio effects at all. Nothing works without it.
- **Foreground service** keeps the boost alive after you leave the app.
- **Notifications** are how the Pause and Stop buttons reach you. Block them and the booster still works, but you lose the controls.
- **Battery optimisation exemption** is offered once, during the introduction, and is entirely optional. Without it Android may shut the service down after a while on aggressive phones.
- **Internet** exists for exactly one thing: checking whether a newer version has been published. That is a single request to one address and nothing else, no identifiers, no analytics, no usage data.
- **Install unknown apps** is only used when you tap Update Now!, so the update can be downloaded and handed to the system installer. Voluost never installs anything silently.

Turn off the automatic update check in More and the app will never touch the network again.

---

## Updating

Voluost looks in the `Release/Free` folder for a newer APK every so often, and when there is one it shows a small dialog with a Later button and an Update Now! button. Newer means newer: if the version you have is the same or ahead of what is published, the app stays quiet, so a build you installed early never nags you to go backwards.

Update Now! downloads the file inside the app with a progress bar and a cancel button, then launches Android's installer. If you would rather not grant the install permission, the button opens the download in your browser instead. Every release is signed with the same key, so updating keeps all of your settings.

---

## Questions people actually ask

**Does it work with Bluetooth?** Yes, and it keeps a separate tuning for it, which usually needs less bass than wired headphones.

**Will it damage my speaker?** Playing loud for a long time is not kind to a small speaker, and the distortion past +30 dB is real. Voluost warns you before you get there, and the red zone above +40 dB is meant to be visited, not lived in.

**Why does it say "session only" on my phone?** Some phones do not let an app attach effects to the whole output mix. Voluost then attaches to individual apps instead. The diagnostics screen shows exactly what is happening, and the boost still works in apps that cooperate.

**Do I need root?** No.

**Does it collect anything?** No account, no analytics, no tracking, no crash reporting. Nothing leaves the phone except the update check.

**What happens to my settings if I update?** They stay. Same signing key every time.

---

## Report a problem

The source is not public, but problems still get fixed. Open an issue here with your phone model, the Android version, and what the diagnostics screen says while the boost is running. That last part is usually the whole diagnosis.
