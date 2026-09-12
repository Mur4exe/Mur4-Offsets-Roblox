<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&height=180&color=0:e31b23,100:17181c&text=Mur4%20Offsets&fontSize=52&fontColor=ffffff&desc=External%20Offsets%20%E2%80%A2%20Auto-Updated%20%E2%80%A2%20Live-Verified&descSize=16&descAlignY=68&animation=fadeIn" width="100%" />

# 🎯 Mur4 Offsets (External)

**Fresh Roblox offsets — extracted live from the client, verified in memory, delivered in minutes.**

[![Website](https://img.shields.io/badge/🌐_Website-Live%20Offset%20Browser-e31b23?style=for-the-badge)](https://mur4exe.github.io/Mur4-Offsets/#home)
[![Join Discord](https://img.shields.io/badge/Discord-Join%20Server-5865F2?style=for-the-badge&logo=discord&logoColor=white)](https://discord.gg/xQzrwQCSjg)
[![Roblox](https://img.shields.io/badge/Roblox-Live%20Client-e31b23?style=for-the-badge&logo=roblox&logoColor=white)](https://www.roblox.com)
[![Status](https://img.shields.io/badge/Auto%20Update-Every%20Roblox%20Patch-00b06f?style=for-the-badge&logo=githubactions&logoColor=white)](https://discord.gg/xQzrwQCSjg)

<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/4/4b/Roblox_Logo_2022.svg/960px-Roblox_Logo_2022.svg.png" alt="Roblox" width="220"/>

</div>

---

## 🎬 Video

<div align="center">

<video src="https://files.catbox.moe/szip1j.mp4" controls muted loop playsinline width="100%"></video>

**[▶ Watch the video](https://files.catbox.moe/szip1j.mp4)**

</div>

---

## 📌 What is this?

**Mur4 Offsets** is a community project that publishes **external memory offsets** for the Roblox client (RobloxPlayerBeta.exe).

Every time Roblox updates, our automated dumper attaches to the **live client**, extracts fresh offsets, **verifies them in real memory**, and posts the full package to our Discord — usually within **minutes** of the update going live.

> ⚡ **Zero paste.** Nothing is copied from other dumper projects. Every single offset is extracted from the running client and re-verified in memory.

---

## 🖼️ What you get

| File | Description |
|---|---|
| `Mur4_Offsets_<version>.txt` | Human-readable dump, namespace format |
| `Mur4_Offsets_<version>.h` | Ready-to-use C++ header — drop it straight into your project |
| `offsets_<version>.json` | Machine-readable JSON for automated tools & bots |

All files are tagged with the exact Roblox version they were extracted from, and filtered versions (`not working` offsets removed or annotated) are shipped automatically after live-testing.

### Example output

```cpp
// Mur4 Offsets (External) — By: Mur4t
// Roblox Version : version-c5aecda2245e4fae

namespace Humanoid {
    inline constexpr uintptr_t Health     = 0x124;
    inline constexpr uintptr_t WalkSpeed  = 0x130;
    inline constexpr uintptr_t JumpPower  = 0x140;
    // ...
}

namespace Lighting {
    inline constexpr uintptr_t Ambient    = 0xD0;
    inline constexpr uintptr_t FogColor   = 0xF4;
    // ...
}
```

---

## 🧪 How offsets are verified

<div align="center">

```
  ┌──────────────┐      ┌───────────────┐      ┌──────────────────┐
  │  Lua writes  │ ───► │  Dumper scans │ ───► │  Offset found    │
  │ unique value │      │ client memory │      │  (class + prop)  │
  └──────────────┘      └───────────────┘      └────────┬─────────┘
                                                        │
                                                        ▼
  ┌──────────────┐      ┌───────────────┐      ┌──────────────────┐
  │  ✅ Alive    │ ◄─── │  12s sampling │ ───► │  ✅ Constant    │
  │  value moves │      │ phase tracking│      │  value stable    │
  └──────────────┘      └───────────────┘      └──────────────────┘
```

</div>

1. **Sentinel pass** — unique sentinel values are written through Roblox properties inside a sandboxed lab
2. **Memory scan** — the dumper finds those values in the live client and records their offsets
3. **Live verification** — every offset is re-sampled over time; properties whose values track the script's phases are marked **LIVE**, stable ones are marked **STABLE**, dead addresses are **removed or annotated before release**

Typical result: **246 LIVE / 136 STABLE / 0 DEAD** out of ~380 extracted offsets.

---

## 🚀 Why external?

These offsets are built for **external tools** — anything that reads or writes Roblox memory from outside the process:

- 🗺️ ESP / radar / loot trackers
- 🎯 aimbot support data (positions, camera)
- ⚡ speed / fly / noclip style memory tools
- 💡 fullbright / no-fog rendering tools
- 🤖 automation & research projects

*(This is not an executor / script-hub — it's the offset map that external tools are built on.)*

---

## 📥 Get the latest dump

<div align="center">

### 👉 [**OPEN THE WEBSITE**](https://mur4exe.github.io/Mur4-Offsets/#home) 👈

**`mur4exe.github.io/Mur4-Offsets`** — live offset browser, direct downloads

### 👉 [**JOIN THE DISCORD SERVER**](https://discord.gg/xQzrwQCSjg) 👈

**`discord.gg/xQzrwQCSjg`**

Get pinged on every Roblox update with fresh, verified offsets.
Releases channel • Support • Community

</div>

---

## ⚠️ Disclaimer

Mur4 Offsets is provided **for educational and research purposes only**.
We do not develop or distribute game cheats, exploits, or any malicious software.
Use of third-party tools may violate Roblox's Terms of Service — you are responsible for your own actions. **By: Mur4t**

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=rect&height=3&color=e31b23&width=100%25"/>

**Mur4 Offsets** · *Live-extracted. Memory-verified. Always fresh.*

</div>
