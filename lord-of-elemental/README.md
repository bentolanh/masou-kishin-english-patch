# Masou Kishin – The Lord of Elemental: English patch

*Super Robot Taisen OG Saga: Masou Kishin – The Lord of Elemental* (PSP, 2010) —
魔装機神 THE LORD OF ELEMENTAL, disc ID **NPJH50804**.

**Current version: v1.31** · [Download from Releases](../../../releases/latest)

## What is translated

- **The whole story script** — every dialogue box, around 15,400 of them, read back
  against the Japanese in scene order.
- **Every battle quote**, around 13,700 lines, including the nameless enemies.
- **Menus, unit names, character names, weapons and spirit commands.**
- **The in-game glossary**, chapter titles, music titles, and the staff roll (with
  Japanese names written in Latin letters).
- Speaker names are shown in **orange** so they stand apart from the line being spoken.
- Choice prompts are laid out as **separate options** you pick between.

With the optional texture pack (PPSSPP only), the Japanese that the game draws as pictures
is translated too: the **prologue narration**, the map and battle UI labels, the battle
call-outs (CRITICAL, COUNTER, DODGE, AGAIN), the chapter card, and the **Will / Prana**
popup over a unit.

## 1. The ROM you need

Make an ISO from your own copy. It must match this exactly, or the patch will refuse to
apply:

| | |
|---|---|
| Title | スーパーロボット大戦ＯＧサーガ 魔装機神 THE LORD OF ELEMENTAL |
| Disc ID | `NPJH50804` (Japan, PSN release) |
| Size | 537,985,024 bytes |
| CRC32 | `66b342f4` |
| MD5 | `a2e4ee7060a73fb74c01bb95f00f72aa` |
| SHA-1 | `5ad027ea4d605b04b8201f6b7319d43f75b087f8` |

**If your copy is a CHD or CSO**, convert it back to a plain ISO first, then check the
hash. For a CHD: `chdman extractdvd -i game.chd -o game.iso` (or `extractcd`, depending on
how the CHD was made).

## 2. Apply the patch

Download `masou-kishin-lord-of-elemental-english-v1.31.xdelta` from the
[latest release](../../../releases/latest) and apply it to the ISO with any xdelta patcher:

- **Windows / macOS / Linux:** [Delta Patcher](https://github.com/marco-calautti/DeltaPatcher)
- **In a browser:** [Rom Patcher JS](https://www.marcrobledo.com/RomPatcher.js/)
- **Android:** UniPatcher
- **Command line:**

  ```
  xdelta3 -d -s original.iso masou-kishin-lord-of-elemental-english-v1.31.xdelta english.iso
  ```

The patch is xdelta rather than IPS because IPS cannot address files over 16 MB, and this
ISO is 538 MB.

**Check the result.** A correctly patched ISO is the same size as the original and has:

| | |
|---|---|
| CRC32 | `3a340c96` |
| MD5 | `feebd44a0b057c54aac45ee9d104a326` |
| SHA-1 | `e8e1e7d2f673d26e79ba7315cba79a9afc8fd42f` |

You can compress the patched ISO to CHD afterwards if your emulator prefers it.

## 3. Play

- **PPSSPP** on PC, Mac or Android is recommended, and the only way to use the texture pack.
- **A real PSP** with custom firmware should work too, since the patched executable is
  unencrypted, but the patch has only been tested in PPSSPP.

**Load an in-game save, not a save state.** A save state captures the game's memory, text
included, so one made before patching (or with an older version of the patch) brings the
old text back with it.

## 4. Texture pack (optional, PPSSPP only)

Some Japanese is drawn as pictures rather than text, so it can't be changed inside the
game file. The texture pack replaces those pictures at run time.

1. Download `masou-kishin-lord-of-elemental-english-textures-v1.31.zip` from the release.
2. Unzip it. You get a folder called `NPJH50804`.
3. Copy that folder into PPSSPP's `PSP/TEXTURES/` folder, so you end up with
   `PSP/TEXTURES/NPJH50804/textures.ini`.
4. In PPSSPP turn on **Settings → Tools → Developer tools → Replace textures**, then
   restart the game.

Textures show up straight away, even when you load a save state.

## Known issues

- The texture pack needs PPSSPP. A real PSP cannot replace textures, so on hardware those
  pictures stay Japanese; the text itself is fully translated either way.
- Recent PPSSPP versions match these textures by memory address. The pack has been checked
  in play on PPSSPP 1.19 (macOS), and PPSSPP 1.20 (Android) loads them at the same
  addresses. If a picture stays Japanese on your setup, please report it with a screenshot.
- A handful of lines are best readings where the Japanese was ambiguous.

## Reporting a problem

Open an issue and quote the English line as it appears on screen, or attach a screenshot.
Every line in the patch can be found from its wording.

## Version history

**v1.31** (2026-10-07) — first public release.
