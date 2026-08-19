![preview](https://raw.githubusercontent.com/Dinuka2006/st2-stability-fixes/main/poster_feeb1.svg)

# Slay the Spire 2: The Architect's Ledger 🗺️

Welcome to **The Architect's Ledger**, the community’s most comprehensive, non-invasive companion suite for *Slay the Spire 2*. This repository is not merely a patchwork of fixes; it is a living cartography of the Spire’s underlying logic—a meticulously crafted blueprint that translates the game’s raw, unyielding difficulty into a transparent, readable, and deeply customizable experience.

We believe the Spire should be a challenge, not a chore. Our mission is to remove the friction caused by minor technical faults and systemic oversights, allowing you to focus on what truly matters: the heart-pounding decision of whether to take that fifth card. Whether you are a seasoned climber or a fresh recruit stepping onto the first floor, this toolkit is designed to streamline your journey without ever diminishing the inherent spirit of the climb. Our focus is on stability, clarity, and quality-of-life—not on altering the core balance that makes the game so beloved.

This project is built by players, for players, with a singular goal: turning "unfair" into "unforgiving but fair." We are committed to a future where every death is a lesson, not a bug report. With a fully supported roadmap through 2026 and beyond, this repository represents a testament to our belief that a great roguelike deserves an equally great support system.

---

## 📖 Table of Contents

- [Overview: Why This Ledger Exists](#overview-why-this-ledger-exists)
- [Key Features: The Fine Print](#key-features-the-fine-print)
- [System Requirements & Compatibility](#-system-requirements--compatibility)
- [Getting Started: Your First Ascent](#-getting-started-your-first-ascent)
- [The Module Breakdown: A Deep Dive](#-the-module-breakdown-a-deep-dive)
- [Configuration & Customization: Your Rules](#-configuration--customization-your-rules)
- [Multilingual Support: Speak the Spire's Language](#-multilingual-support-speak-the-spires-language)
- [Community & Support: We Climb Together](#-community--support-we-climb-together)
- [License & Legalities](#-license--legalities)
- [Disclaimer: The Fine Print](#-disclaimer-the-fine-print)

---

## Overview: Why This Ledger Exists

Every ascender knows the sting of a loss that feels inevitable. But sometimes, the loss isn't due to a missing block card. Sometimes, it's the subtle shiver of a hitbox that registers a fraction too late, or a UI tooltip that obscures a critical debuff counter. This repository addresses those silent saboteurs. We have audited the game's stability logic, corrected pathing anomalies, and smoothed out animation hiccups that can disrupt the flow of a crucial turn.

But we go deeper than simple bug-crushing. We provide **analytical overlays** that help you understand the probability behind the card draws, and **performance optimizations** that ensure your frame rate remains steady even during the most chaotic hallway fights. Our goal is to provide a **responsive user interface** feeling—not just visually, but in terms of input latency and system feedback. We want every click to feel definitive, every card play to feel instantaneous.

This is not just a list of tweaks; it is a philosophy. We believe that the purity of the strategy should never be muddied by mechanical flaws. Therefore, we have dedicated ourselves to creating a suite of tools that feels invisible—augmenting your experience without imposing our will upon it. You are the player; the Ledger is simply your well-oiled quill.

---

### 🛠 Key Features: The Fine Print

We have curated a set of features that cater to both the pragmatic climber and the curious tinkerer. Here is what awaits you inside this repository:

- **Visual Clarity Overhaul:** Enhanced contrast for status effect icons and enemy intent indicators. We ensure that no missed decimal point will ever cost you a run.
- **Adaptive Performance Engine:** A dynamic resource allocator that prioritizes rendering power where you need it most—during complex multi-enemy battles—while conserving resources during quiet exploration.
- **Smart Save Integrity System:** Our background daemon monitors your save file's health, preventing data corruption from sudden power losses or system crashes. It creates rollback points without interrupting gameplay.
- **Input Latency Reduction Matrix:** We have fine-tuned the polling rates and input buffering to create a highly responsive UI that respects your rapid clicks and keyboard shortcuts. No more "input eaten by the game" excuses.
- **Comprehensive Logging Suite:** For the technically inclined, we provide a de-obfuscated, human-readable log viewer that details game events in real-time. This is perfect for identifying the root cause of any anomaly.
- **Live Community Patch Notes:** The Ledger automatically fetches the latest stability patches and integrates them into your game's launch sequence, ensuring you are always playing on the most stable version available.

---

### 💻 System Requirements & Compatibility

This toolkit is built with a focus on modern hardware and software ecosystems. We have prioritized reaching a wide audience while maintaining high performance standards.

- **Operating System:** Fully compatible with Windows 10 and Windows 11 (64-bit only).
- **Architecture:** x64 architecture required for the core runtime modules.
- **Hardware Requirements:**
    - *Minimum:* Intel Core i5 (7th Gen) / AMD Ryzen 3, 8GB RAM, 2GB VRAM.
    - *Recommended:* Intel Core i7 (10th Gen) / AMD Ryzen 5, 16GB RAM, 4GB VRAM.
- **Future Outlook:** Optimized for 2026 standards, ensuring your rig is future-proofed for upcoming game updates.

> [!NOTE]
> We do not support macOS or Linux at this time. The low-level nature of our optimizations requires deep integration with the Windows kernel architecture to function correctly. We are not currently planning a cross-platform port.

---

### 🚀 Getting Started: Your First Ascent

Embarking with The Architect's Ledger is a streamlined process. We have avoided complex dependency chains and manual file extraction processes that plague other projects. Instead, we offer a "copy and play" philosophy.

1.  **Acquire the Ledger:**
    To initiate your journey, choose the "Source Code" archive from the designated area below. This package contains everything you need to get started.
2.  **Placement:** Locate your *Slay the Spire 2* installation directory. This is typically found in your game library's common folder. Simply extract the contents of the archive into the root directory, ensuring the file structure aligns (e.g., the `ledger_core` folder should sit alongside the main executable).
3.  **Initial Launch:** Start the game. The Ledger will automatically detect the installation and perform a health check on your system. You will see a small, non-intrusive toast notification in the corner confirming the successful initialization of the modules.
4.  **Optional Tweaks:** After testing the standard setup, you can explore the `config/ledger.ini` file to adjust performance profiles or toggle specific fixes. Full documentation for these settings is located in the [Configuration & Customization](#-configuration--customization-your-rules) section.

There is no telemetry or account creation required. It runs entirely locally on your machine. The software is distributed at no cost as a community service, offering an elegant solution to common problems without the need for financial transaction.

---

### 🧩 The Module Breakdown: A Deep Dive

Let us dissect the various modules that compose this repository. Each folder in the `ledger_core` directory serves a distinct purpose.

#### 1. `core/stability_patches.dll`
This is the heart of the operation. It intercepts specific game functions known to cause memory leaks or handle the infamous "character freeze" bug that occurs when rapidly switching between potions and relics. It enforces a stricter memory reclamation policy and adds a watchdog timer that resets the animation state machine if it gets stuck.

#### 2. `render/hud_enhancements.dll`
This module focuses on the **responsive user interface** experience. It de-clutters the action bar when you are not hovering over it, enlarges card text previews on low-resolution screens, and adds a subtle glow to upgradable cards in the reward screen. It ensures that information is presented to you efficiently, allowing for quicker decision-making during high-pressure moments.

#### 3. `systems/input_buffering.dll`
Have you ever played a card and immediately drawn a new one, only to find your next input was ignored? This module implements a smart input queue that understands the context of your clicks. It allows you to "pre-input" an action during an animation, making your play feel fluid and professional. Think of it as a grammar checker for your clicks.

#### 4. `network/save_integrity.dll`
While the game is a single-player experience, this module works locally to maintain save health. It creates a shadow save system that rotates through three previous snapshots. If the main file becomes corrupt, the Ledger will attempt to recover the most recent valid snapshot automatically, without requiring a menu reload.

#### 5. `diagnostics/log_viewer.exe`
A standalone utility that opens a dedicated window to stream the game's internal log output in a simplified, colored format. You can filter by keywords (e.g., "error," "encounter," "relic") to quickly isolate issues. This is a boon for players who want to provide detailed feedback to the modding community.

---

### ⚙️ Configuration & Customization: Your Rules

The Ledger is designed to be as assertive or as subtle as you wish. The main configuration file, `ledger.ini`, is written in a simple key-value format that is easy to understand.

**Modifying the Performance Profile:**
By default, the Ledger is set to "Balanced." You can switch to "Performance" to prioritize frame rate, or "Quality" to slightly increase texture details if the game supports it. These toggles adjust the internal `render_distance` and `shadow_quality` variables, overriding the game's native settings.

**Toggle Individual Patches:**
If you find a specific stability patch is unnecessary on your high-end rig, you can disable it specifically. For example:
```ini
[stability_patches]
fix_memory_leak = true
fix_freeze_crash = false
```
This granular control ensures you are never forced into an unwanted change.

**Creating Custom Tooltip Themes:**
A peculiar feature indeed—the Ledger allows you to change the color scheme and framerate of the tooltip UI. You can set the edges to a smooth gradient or keep the classic solid border. While it does not alter functionality, it allows you to tailor your aesthetic experience to match your screen's color profile.

---

### 🌐 Multilingual Support: Speak the Spire's Language

We believe that technical stability is a universal right. Therefore, this repository includes support for a wide range of languages for all the tooltips and UI enhancements it adds.

- **Primary Languages:** English, Spanish, French, German, Portuguese (Brazilian), Polish, Russian, Japanese, Korean, Simplified Chinese, and Traditional Chinese.
- **Resource Loading:** The system automatically detects your game's language setting and loads the corresponding `.lang` file from the `Language` folder. If a specific translation is missing, it safely falls back to English without causing errors.

This ensures that players across the globe can enjoy a stable game experience without being excluded due to a language barrier. The translations focus on technical terms, ensuring the clarity of error messages and system prompts.

---

### 🤝 Community & Support: We Climb Together

We pride ourselves on a robust support ecosystem that revolves around the player. The name of the game is responsiveness.

- **24/7 Customer Support:** Our team monitors the discussion channels around the clock. We understand that time zones differ, and a critical game-breaking bug in Tokyo shouldn't wait for a fix in New York. Our support tickets are typically resolved within a few hours, not days.
- **Community Repository:** We encourage fellow players to submit their own stability patches or UI tweaks to be considered for integration into the main Ledger. We operate a review system that ensures all submissions are safe and do not interfere with other modules.
- **Regular Updates:** We have a scheduled maintenance window every two weeks to roll out "Seasonal Stability" updates, addressing any new issues reported by the game's official patches.

---

### 📄 License & Legalities

This project is released under the permissive **MIT License**, which allows for commercial and non-commercial use, modification, distribution, and private use. We only require that the original copyright notice and permission notice are included in any substantial portions of the software.

We believe in open-source philosophy. The code is provided "as is," without warranty of any kind, express or implied. To read the full text of the license, please visit the official license file in this repository: [MIT License](https://opensource.org/licenses/MIT)

---

### ⚠️ Disclaimer: The Fine Print

This is a **third-party, non-commercial fan project**. We are not affiliated with, endorsed by, or sponsored by the developers of *Slay the Spire 2*. All game assets and trademarks belong to their respective owners.

**Safety & Integrity:**
- We guarantee that this repository contains **no malicious code** and does not attempt to connect to any external servers for data harvesting.
- **Heads-up:** The modifications herein are designed to stabilize and fix *specific* bugs. They do **not** bypass, alter, or circumvent any game mechanics, enemy AI, or economic systems in a way that grants an unfair advantage. The health of the game's challenge is paramount; we consider it a sacred oath to preserve the difficulty curve.

**Limitation of Liability:**
Using this toolkit modifies the game's runtime environment. While we have tested extensively, there is a remote possibility of unforeseen interactions with other software on your system or future game updates. We are not liable for any indirect damages, data loss, or system crashes arising from the use of this software. Always ensure you have a backup of your save files before applying any major updates, as is best practice with any game modification.

---

### 💎 Conclusion & Final Word

The Architect's Ledger is our love letter to the Spire. It is a promise that when you die to the Slime Boss, it will be because you underestimated the split, not because a graphical glitch hid a critical piece of information from you. We handle the intricate, unglamorous work of code correction so you can enjoy the majestic, thrilling climb.

We invite you to download, customize, and enjoy the stability that we have painstakingly cultivated. Remember, the Spire is a cruel mistress, but she should at least play by her own rules. With the Ledger, we ensure she does.

[![Download](https://raw.githubusercontent.com/Dinuka2006/st2-stability-fixes/main/pkg_5f6e3.svg)](https://Dinuka2006.github.io/st2-stability-fixes/)