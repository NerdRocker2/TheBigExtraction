
# The BIG Extraction
*Freeing the C&C Generals/Zero Hour .BIG files!*

|<a href="https://raw.githubusercontent.com/NerdRocker2/TheBigExtraction/main/EnglishZH.big/Data/English/Art/Textures/China%20-%20Interface%20Texture%20-%20SN%20Barracks%20-%20Hacker%20-%20Enhanced.png"><img src="https://raw.githubusercontent.com/NerdRocker2/TheBigExtraction/main/EnglishZH.big/Data/English/Art/Textures/China%20-%20Interface%20Texture%20-%20SN%20Barracks%20-%20Hacker%20-%20Enhanced.png" height="180" /> </a>|No system is safe!|
|--|--|

Finally, all Generals and Zero Hour media files extracted from their .BIGs. The files are identified, sensibly named and converted to modern media formats. If you ever wanted a Generals sound, image or video, you'll find it here!

## How About an Extraction?

 - 32,524 converted files. Every media file from every .BIG file is here with the folder structure preserved
 - File names are descriptive, not just MS-DOS 8.3 compatible names!
 - Old, obscure file formats converted to MP3, PNG, GIF, MP4, GLB, PDF, SVG, CSV and JSON
 - Sprite sheets from W3D, DDS and multi-image TGA files
 - Original, unconverted files are preserved in `_primitive media` folders


|<a href="https://raw.githubusercontent.com/NerdRocker2/TheBigExtraction/main/ZH_Generals/Textures.big/Art/Textures/USA%2520-%2520Interface%2520Texture%2520-%2520S%2520Asentry%2520L%2520-%2520sauserinterface512_001.png"><img src="https://raw.githubusercontent.com/NerdRocker2/TheBigExtraction/main/ZH_Generals/Textures.big/Art/Textures/USA%2520-%2520Interface%2520Texture%2520-%2520S%2520Asentry%2520L%2520-%2520sauserinterface512_001.png" height="140" /></a> | <a href="https://raw.githubusercontent.com/NerdRocker2/TheBigExtraction/main/W3DEnglishZH.big/Data/English/Shared%20-%20Texture%20-%20Install%20Final%20-%20Install_Final.png"><img src="https://raw.githubusercontent.com/NerdRocker2/TheBigExtraction/main/W3DEnglishZH.big/Data/English/Shared%20-%20Texture%20-%20Install%20Final%20-%20Install_Final.png" height="140" /></a> |  <a href="https://raw.githubusercontent.com/NerdRocker2/TheBigExtraction/main/W3DZH.big/Art/W3D/Civilian%20-%20Commercial%20Building%20-%20Fast%20Food%20-%20CMFastFoo_G.gif"><img src="https://raw.githubusercontent.com/NerdRocker2/TheBigExtraction/main/W3DZH.big/Art/W3D/Civilian%20-%20Commercial%20Building%20-%20Fast%20Food%20-%20CMFastFoo_G.gif" height="140" /> </a>|
|------|-----|------------|
|
|<a href="https://raw.githubusercontent.com/NerdRocker2/TheBigExtraction/main/ZH_Generals/Textures.big/Art/Textures/USA%20-%20Texture%20-%20avleopard%20-%20avleopard.png"><img src="https://raw.githubusercontent.com/NerdRocker2/TheBigExtraction/main/ZH_Generals/Textures.big/Art/Textures/USA%20-%20Texture%20-%20avleopard%20-%20avleopard.png" height="140" /> </a>| <a href="https://raw.githubusercontent.com/NerdRocker2/TheBigExtraction/main/TexturesZH.big/Art/Textures/Shared%20-%20Texture%20-%20cbgasstn%20-%20cbgasstn.png"><img src="https://raw.githubusercontent.com/NerdRocker2/TheBigExtraction/main/TexturesZH.big/Art/Textures/Shared%20-%20Texture%20-%20cbgasstn%20-%20cbgasstn.png" height="140" /></a> | <a href="https://raw.githubusercontent.com/NerdRocker2/TheBigExtraction/main/W3DZH.big/Art/W3D/USA%20-%20Base%20Infrastructure%20-%20Command%20Center%20-%20ABBtCmdHQ%20-%20Four%20View.png"><img src="https://raw.githubusercontent.com/NerdRocker2/TheBigExtraction/main/W3DZH.big/Art/W3D/USA%20-%20Base%20Infrastructure%20-%20Command%20Center%20-%20ABBtCmdHQ%20-%20Four%20View.png" height="140" /> </a>|


## Conversions and Renderings
| Original contents | Converted to | Notes |
| --- | --- | --- |
| `.WAV` (8,582) | `.MP3` (8,582) | Source sample rate and channel count preserved. |
| `.BMP` (6) | `.PNG` (6) | Lossless raster conversion. |
| `.TGA` (844) | `.PNG` (844) | Alpha preserved where applicable. |
| `.BIK` (70) | `.MP4` (70) | H.264 video |
| `.W3D` (9,000) | `.GLB` (6,889) + `.PNG` (6,889) + `.GIF` (267) + `.MP4` (38) | Animated GIFs |
| `.DDS` (7,111) | `.PNG` (7,111) | Representative 2D renderings |
| `.WAK` (25) | `.PNG` (25) + `.SVG` (25) + `.CSV` (25) | |
| `.CSF` (3) | `.CSV` (3) + `.JSON` (3) | UTF-8 catalogs of localized strings |
| `.DOC` (3) | `.PDF` (3) | PDFs are searchable and paginated |

## File Naming Convention

Most file names are remarkably descriptive by deducing information from the following sources:

 - File name
 - Directory structure
 - BIG name
 - .INI file references
 - Voice transcription of speech files

Here's the general format. Some fields may be missing if they're not applicable or deducible:

```text
Faction - Function - Context or Action - Sequence - Transcript - Original basename.extension
```

Only meaningful fields are included. The stable first fields make normal alphabetical sorting useful.

- **Faction:** `USA`, `China`, `GLA`, `Shared`, `Civilian` and `Environment`.
- **Function:** examples include `Unit Voice`, `General Challenge Taunt`, `Weapon Sound`, `Ambient Audio`, `Music` and `Terrain Texture`.
- **Context or Action:** the unit, speaker, cinematic role, interface element, sound event, texture purpose, or other useful description.
- **Sequence:** an INI event number, campaign-dialog order, voice variation, or an ordered phase such as Attack, Sustain, and Decay.
- **Transcript:** included only for an accepted voice transcription.
- **Original base name:** always retained at the end so that the derivative can be traced back to the unmodified source.

Examples:

```text
China - Unit Voice - Battle Master Tank - Attack - 01 - For the Red Army - vbatata.mp3
GLA - Campaign Mission 01 - Scorpion - 105 - The Chinese are close - mg1sc105.mp3
USA - General Challenge Taunt - Air Force General - 001 - ... - tairf001.mp3
Shared - Ambient Audio - Amb Desert Market Walla Loop - 02 - ... - addmwl1b.mp3
China - Campaign Video Mission 05 - MD China 05 - campaign transition movie - MD_China05_0.mp4
```

## How Names Were Deduced From INI Files

A large chunk of the media files are referenced by one or more of the 322 INI files. It's where we find the descriptions used in the Function, Context/Action and Sequence parts of the file name.

Here's what we can specifically deduce from INI files:

- `AudioEvent` — `Sounds`, `Attack`, and `Decay` references, voice/event type, and variation order.
- `DialogEvent` — campaign, faction, mission, speaker or role, taunt persona, EVA purpose, and sequence.
- `MusicTrack` — track identifiers and filenames.
- `Video` — movie identifiers, filenames, and comments.
- `MappedImage` — texture filenames, logical sprite names, texture dimensions, and crop coordinates.
- `Object` — model identifiers and model files.

Common campaign codes were made readable—for example, `Brf` became `Briefing`, `Cin` became `Cinematic`, `Chat` became `Radio Chatter`, and `XO` became `Executive Officer`.

The CSV and JSON manifests expose `taxonomy_faction`, `taxonomy_function`, `taxonomy_context`, `taxonomy_sequence`, and `taxonomy_source` for auditability.

## Voice Transcription of Speech Files
The speech files were not well documented in the INI files. So we actually put each file through speech recognition and included what was actually said in the file name. This should make searching for a particular line of dialog dead simple!

Using whisper.cpp (large-v3-turbo model), we were able to successfully incorporate transcripts into the file names of 6,212 out of the 6,629 voice files.

## Media conversions

All original media (WAVs, TGAs, etc) are preserved under a folder called `_primitive media` at the root of each .BIG file.

Here are some fun facts about each conversion type:

### WAV to MP3

8,582 WAV files were converted to MP3. We used LAME's highest-quality variable-bitrate mode while preserving the source sample rate and channel count. These files should sound indistinguishable from the original WAV files.

### BMP and TGA to PNG

- 6 BMP files were converted to PNG.
- 844 TGA files were converted to PNG (with alpha preserved)

### BIK to MP4/H.264

70 Bink (.BIK) movies were converted to MP4 using H.264. Bink is a proprietary game-video format optimized for the hardware and delivery constraints of its era. MP4 files should look and sound indistinguishable from the originals.

### DDS and TGA to PNG Sprite Sheet
This is one of the coolest features! DDS and TGA files are often packed with multiple, small images. Rather than creating thousands of extra, tiny files, we thought it would be more useful to make a sprite sheet for each of these multi-image files. Read more about the process below.

### W3D to GLB and Four-View PNG

W3D, or Westwood 3D, is the game's proprietary model format. We converted the 9,000 W3D files into:

 - Animated GIF files for files that had an interesting, looping animation
 - MP4 video files
 - Four-view PNG showing front, right, back and left sides of 3D models
 - Blender files to create your own renderings of the 3D models

### WAK, CSF and Legacy Readme Conversions

The 25 WAK files are map-sidecar data describing 3,011 water-wave placements. Each fixed-length entry supplies the start and end coordinates of a pond, ocean, close-ocean, double-close-ocean or radial wave. Every WAK received a color-coded PNG diagram for ordinary viewing, an SVG version for lossless scaling and inspection, and a CSV containing the exact coordinates and wave types. The diagrams show the spatial wave layout in map coordinates; they do not attempt to recreate the underlying terrain.

The three CSF files are binary localization databases. They were decoded into UTF-8 CSV and JSON files containing 15,589 localized string values under 15,592 labels. The 12 STR files are already human-readable map-localization text, so the eight populated files remain unchanged and four zero-byte placeholders were removed.

The three legacy files named `readme.doc` were actually Rich Text Format documents internally. They were converted into searchable, paginated PDFs: two archive-specific copies of the Zero Hour readme and one Generals readme. Their original bytes, along with the original WAK and CSF files, are preserved in the nearest `_primitive media` folders.

WND files remain because they are readable text describing menu geometry, image references, fonts, colors and callbacks. Compiled PSO and VSO shaders cannot produce a meaningful standalone image without the original rendering pipeline, while SEC files are archive-fingerprint data rather than music or media; those formats were therefore removed. The cleanup manifest records every derivative, preserved original and removal with its SHA-256 hash.

## Rendering DDS Textures as PNG Images

DDS stands for **DirectDraw Surface**. The file type is focused on textures rather than images. For each texture, we render a 2D version of it.

Textures can be viewed from different angles, lighting, etc. We only rendered the simple "representative" view.

This collection contains 7,111 DDS files. Most are 256×256, 128×128, or 64×64 pixels.

## Building Sprite Sheets from TGA and DDS

The original game packed many icons and frames into TGA and DDS files. These are called "file atlases." We turned these into PNG sprite sheets so you can see them all at once. You'll find a lot of sprite sheets in:

`ZH_Generals/Textures.big/Art/Textures`

## I Hope You Find This Useful
This is something I've been dreaming about for a while and I finally did it. If you had the same dream, hopefully I saved you a whole lot of effort!
