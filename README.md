**Last updated: June 2023**

Also known as itag or format codes and way back they could be specified with the fmt parameter (e.g. `&fmt=22`).
Depending on the age and/or popularity of the video, not all formats will be available.

## DASH video

| Resolution | AV1 HFR High | AV1 HFR | AV1 | VP9.2 HDR HFR | VP9 HFR | VP9 | H.264 HFR | H.264 |
|-----------:|-------------:|--------:|----:|--------------:|--------:|----:|----------:|------:|
| | MP4 | MP4 | MP4 | WebM | WebM | WebM | MP4 | MP4 |
| **4320p** | | 402/571 | | | 272 | | | ~~138~~ |
| **2160p** | 701 | 401 | | 337 | 315 | (313) | (305) | (266) |
| **1440p** | 700 | 400 | | 336 | 308 | (271) | (304) | (264) |
| **1080p** | 699 | 399 | | 335 | 303 | (248) | 299 | (137) |
| **720p** | 698 | 398 | | 334 | 302 | 247 | 298 | 136 |
| **480p** | 697 | | 397 | 333 | | 244 | | 135 |
| **360p** | 696 | | 396 | 332 | | 243 | | 134 |
| **240p** | 695 | | 395 | 331 | | 242 | | 133 |
| **144p** | 694 | | 394 | 330 | | 278 | | 160 |

- HFR stands for "High Framerate", which means up to 60 FPS, whereas non-HFR is limited to 30 FPS
- Non-HFR 1080p+ H.264 and VP9 variants are not provided for HFR videos anymore
- Same IDs are reused for 360° videos
- 1440p+ H.264 variants are only provided for 360° videos anymore
- At the moment, AV1 variants are only provided for popular videos
- All AV1 variants can be HDR (no separate non-HDR AV1 variants are offered)
- **AV1 HFR High**: High refers to the bitrate. These variants have **~3-4 times** the bitrate of their normal counterparts. Additional side effect is providing AV1 HFR variants for low resolutions (<=480p). These variants are rare even among videos with AV1 variants. Found on [this video](https://www.youtube.com/watch?v=LXb3EKWsInQ).
- **AV1 HFR 4320p**: Format 571 has roughly 50% higher bitrate than 402. Sometimes only one of them is offered, sometimes both. Can be seen on [this video](https://www.youtube.com/watch?v=hVvEISFw9w0).

## DASH audio

| Code | Container | Audio Codec | Audio Bitrate | Channels | Still offered? |
|:-----|:----------|:------------|--------------:|---------:|---------------:|
| 139 | MP4 | AAC (HE v1) | 48 Kbps | Stereo (2) | Rarely, YT Music |
| 140 | MP4 | AAC (LC) | 128 Kbps | Stereo (2) | Yes, YT Music |
| (141) | MP4 | AAC (LC) | 256 Kbps | Stereo (2) | No, YT Music* |
| 249 | WebM | Opus | (VBR) ~50 Kbps | Stereo (2) | Yes |
| 250 | WebM | Opus | (VBR) ~70 Kbps | Stereo (2) | Yes |
| 251 | WebM | Opus | (VBR) <=160 Kbps | Stereo (2) | Yes |
| 256 | MP4 | AAC (HE v1) | 192 Kbps | Surround (5.1) | Rarely |
| 258 | MP4 | AAC (LC) | 384 Kbps | Surround (5.1) | Rarely |
| 327 | MP4 | AAC (LC) | 256 Kbps | Surround (5.1) | ?* |
| 338 | WebM | Opus | (VBR) ~480 Kbps (?) | Quadraphonic (4) | ?* |

- Surround audio can be found on some demo videos
- **YT Music**: These formats are offered on Youtube Music. Format 141 is only available to Premium users with High Quality option
- **Format 327, 338**: These have been found on this [Stereo 3D video](https://www.youtube.com/watch?v=QrhcfjPFaEk)

## Legacy (non-DASH)

| Code | Container | Video Codec | Video Res. | Audio Codec | Audio Bitrate | Channels | Still offered? |
|:-----|:----------|:------------|-----------:|:------------|--------------:|---------:|---------------:|
| 18 | MP4 | H.264 (Baseline, L3.0) | 360p | AAC (LC) | 96 Kbps | Stereo (2) | Yes, GDrive |
| (59) | MP4 | H.264 (Main, L3.1) | 480p | AAC (LC) | 128 Kbps | Stereo (2) | No, GDrive |
| 22 | MP4 | H.264 (High, L3.1) | 720p | AAC (LC) | 192 Kbps | Stereo (2) | Mostly*, GDrive |
| (37) | MP4 | H.264 (High, L4.0) | 1080p | AAC (LC) | 128 Kbps | Stereo (2) | No, GDrive |

- Always limited to 30 FPS
- **GDrive**: These formats are offered for Google Drive video previews. Note that the video player on GDrive displays incorrect codecs on rightclick -> stats
- **Format 22**: Available for most videos, except music and music videos (not limited to official music channels!)

## Livestreams (non-DASH)

| Code | Container | Video Codec | Video Res. | Audio Codec | Audio Bitrate | Still offered? |
|:-----|:----------|:------------|-----------:|:------------|--------------:|---------------:|
| 91 | MPEG-TS (HLS) | H.264 (Baseline, L1.1) | 144p | AAC (HE v1) | 48 Kbps | Yes |
| 92 | MPEG-TS (HLS) | H.264 (Main, L2.1) | 240p | AAC (HE v1) | 48 Kbps | Yes |
| 93 | MPEG-TS (HLS) | H.264 (Main, L3.0) | 360p | AAC (LC) | 128 Kbps | Yes |
| 94 | MPEG-TS (HLS) | H.264 (Main, L3.1) | 480p | AAC (LC) | 128 Kbps | Yes |
| 95 | MPEG-TS (HLS) | H.264 (Main, L3.1) | 720p | AAC (LC) | 256 Kbps | Yes |
| 96 | MPEG-TS (HLS) | H.264 (High, L4.0)  | 1080p | AAC (LC) | 256 Kbps | Yes |
| 300 | MPEG-TS (HLS) | H.264 (Main, L3.2) | HFR 720p | AAC (LC) | 128 Kbps | Yes |
| 301 | MPEG-TS (HLS) | H.264 (High, L4.2) | HFR 1080p | AAC (LC) | 128 Kbps | Yes |

- Non-HFR variants are limited to 30 FPS, HFR to 60 FPS
- Non-HFR variants for 720p and 1080p may not be offered if HFR is available
- Livestreams are also offered through DASH video (H.264, VP9) and DASH audio (AAC) streams

## Template youtube-dl formats

### For archiving videos: Only choose combinations that fit WebM (VP9+Opus) or MP4 (H.264+AAC)

```
bestvideo[ext=webm]+251/bestvideo[ext=mp4]+(258/256/140)/bestvideo[ext=webm]+(250/249)/best
```

### For archiving videos: Only choose combinations that fit WebM (VP9+Opus)

```
(313/315/337)+(251/250/249)
```

### For archiving audio: Choose any format that's best
AAC Surround 384 / Opus 160 / AAC 192 / AAC Surround 192 / AAC 128 / Opus 70 / AAC 96 / Opus 50 / AAC 48

```
258/251/22/256/140/250/18/249/139
```

### For streaming videos: Allow any combination

```
bestvideo+bestaudio/best
```

## youtube-dl usage example

### Archive videos
```
youtube-dl --download-archive youtube-dl.list --ignore-errors --write-info-json --add-metadata --write-sub --sub-lang en,de,ja --write-thumbnail --embed-subs -f "<format>" "<URL>"
```

### Archive audio
```
youtube-dl --download-archive youtube-dl.list --ignore-errors --write-info-json --add-metadata --write-sub --sub-lang en,de,ja --write-thumbnail --embed-thumbnail --extract-audio -f "<format>" "<URL>"
```
