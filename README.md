# The BIG Extraction
*Freeing the C&C Generals/Zero Hour .BIG files!*

Finally, all Generals and Zero Hour media files extracted from their .BIGs, identified, sensibly named and converted to modern media formats. If you ever wanted a Generals sound, image or video, you'll find it here.

## Features

 - Every media file from every .BIG file is here with the folder structure preserved
 - 26,400 files in total from 36 BIG archives and 136 loose media files
 - Files names are descriptive, not just MS-DOS 8.3 compatible names!
 - Old, obscure file formats converted to MP3, PNG and MP4
 - Sprite sheets from DDS textures and multi-image TGA files
 - File types extracted:
	 - WAV -> MP3
	 - BMP and TGA -> PNG
	 - BIK -> MP4 (H.264 encoded)
	 - DDS texture -> PNG (with alpha where applicable)


## File Naming Convention

Most file names are remarkably descriptive by deducing information from the following sources:

 - File name
 - Directory structure
 - BIG name
 - .INI file references
 - Voice transcription of voice files

Here's the general format. Some fields may be missing if they're not applicable or deducableL

```text
Faction - Function - Context or Action - Sequence - Transcript - Original basename.extension
```

Only meaningful fields are included. The stable first fields make normal alphabetical sorting useful.

- **Faction:** `USA`, `China`, `GLA`, or `Shared`.
- **Function:** examples include `Unit Voice`, `General Challenge Taunt`, `Weapon Sound`, `Ambient Audio`, `Music` and `Terrain Texture`.
- **Context or Action:** the unit, speaker, cinematic role, interface element, sound event, texture purpose, or other useful description.
- **Sequence:** an INI event number, campaign-dialog order, voice variation, or an ordered phase such as Attack, Sustain, and Decay.
- **Transcript:** included only for an accepted voice transcription.
- **Original basename:** always retained at the end so that the derivative can be traced back to the unmodified source.

Examples:

```text
China - Unit Voice - Battle Master Tank - Attack - 01 - For the Red Army - vbatata.mp3
GLA - Campaign Mission 01 - Scorpion - 105 - The Chinese are close - mg1sc105.mp3
USA - General Challenge Taunt - Air Force General - 001 - ... - tairf001.mp3
Shared - Ambient Audio - Amb Desert Market Walla Loop - 02 - ... - addmwl1b.mp3
China - Campaign Video Mission 05 - MD China 05 - campaign transition movie - MD_China05_0.mp4
```

## How Names Were Deduced From INI Files

A large chunk of the media files are references in 1 of 325 INI files. It's where we find the descriptions used in the Function, Context/Action and Sequence parts of the file name. 

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
The speech files we're not well documented in the INI files. So we actually put each file through speech recognition and included what was actually said in the file name. This should make searching for a particular line of dialog dead simple!

Using whisper.cpp, we were able to successfully get 6,212 transcripts out of the 6,629 voice files.

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

## Rendering DDS Textures as PNG Images

DDS stands for **DirectDraw Surface**. The file type is focused on textures rather than images. For each texture, we render a 2D version of it.

This is a representative view. Textures can be viewed from different angles, lighting, etc. We only rendered it from one angle under consistent conditions. There may be some that didn't render in a useful way.

This collection contains 7,111 DDS files. Their headers identify 3,964 DXT1 textures, 3,138 DXT5 textures, and 9 DXT3 textures. Most are 256×256, 128×128, or 64×64.

## Building Sprite Sheets from TGA and DDS

The original game packed many icons and frames into one larger TGA or DDS. In such cases, we turned these into sprite sheets so you can see them all at once. You'll find a lot of sprite sheets in:

``ZH_Generals/Textures.big/Art/Textures``

## I Hope You Find This Useful
This is something I've been dreaming about for a while and I finally did it. If you had the same dream, hopefully I saved you a whole lot of effort!
