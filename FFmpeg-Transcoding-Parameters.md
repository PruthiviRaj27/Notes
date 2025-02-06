# FFmpeg Video Transcoding Parameters Documentation

This document provides a comprehensive list of FFmpeg parameters commonly used for video transcoding, covering input parameters, video and audio codecs, encoding settings, filters, output format, streaming options, and advanced parameters.

---

## 1. **Input Parameters**
These parameters specify the input file and network protocols.

| **Parameter**               | **Description**                                     | **Example**                           |
|-----------------------------|-----------------------------------------------------|---------------------------------------|
| `-i <input file>`            | Specifies the input file or stream.                 | `-i input.mp4`                        |
| `-protocol_whitelist`        | Whitelists network and file protocols for FFmpeg.   | `-protocol_whitelist file,http,https,crypto,tls,tcp` |

---

## 2. **Video Codec & Encoding Parameters**
These parameters control video codec settings, encoding speed, bitrate, and profile.

| **Parameter**               | **Description**                                         | **Example**                                    |
|-----------------------------|---------------------------------------------------------|------------------------------------------------|
| `-c:v <codec>`              | Specifies the video codec for transcoding.              | `-c:v h264`                                   |
| `-preset <speed>`           | Controls encoding speed vs. compression (slower = better quality). | `-preset faster`                            |
| `-crf <value>`              | Constant Rate Factor (lower = better quality).          | `-crf 26`                                     |
| `-b:v <bitrate>`            | Sets the target video bitrate (in bits per second).    | `-b:v 1000000`                                |
| `-maxrate <bitrate>`        | Maximum allowed bitrate for ABR (Average Bitrate).     | `-maxrate 1000000`                            |
| `-bufsize <size>`           | Buffer size for rate control (smooths out bitrate spikes). | `-bufsize 1000000`                          |
| `-profile:v <profile>`      | Specifies the H.264 video profile (Baseline/Main/High). | `-profile:v main`                            |
| `-level <level>`            | Specifies the H.264 profile level (e.g., 3.1, 4.0).    | `-level 3.1`                                 |

---

## 3. **Audio Codec & Encoding Parameters**
These parameters control audio codec settings, bitrate, and sample rate.

| **Parameter**               | **Description**                                        | **Example**                                     |
|-----------------------------|--------------------------------------------------------|-------------------------------------------------|
| `-c:a <codec>`              | Specifies the audio codec for transcoding.             | `-c:a aac`                                     |
| `-b:a <bitrate>`            | Sets the target audio bitrate (in bits per second).    | `-b:a 128000`                                  |
| `-ar <sample rate>`         | Sets the audio sample rate (usually 44100 or 48000 Hz).| `-ar 44100`                                    |
| `-ac <channels>`            | Specifies the number of audio channels (1 = mono, 2 = stereo). | `-ac 2`                                    |

---

## 4. **Video Filtering & Scaling**
These parameters apply video filters and scale the video resolution.

| **Parameter**               | **Description**                                         | **Example**                                     |
|-----------------------------|---------------------------------------------------------|-------------------------------------------------|
| `-vf <filter>`              | Applies video filters (e.g., scaling, cropping, format conversion). | `-vf "scale=1280:-2,format=yuv420p"`         |
| `-r <fps>`                  | Specifies the frame rate of the video.                 | `-r 24`                                        |

---

## 5. **Output Format & Container**
These parameters define the output format and settings for HLS (HTTP Live Streaming).

| **Parameter**               | **Description**                                         | **Example**                                     |
|-----------------------------|---------------------------------------------------------|-------------------------------------------------|
| `-format <format>`          | Specifies the output format (e.g., MP4, HLS).           | `-format hls`                                  |
| `-hls_time <seconds>`       | Sets the duration of each segment for HLS (in seconds). | `-hls_time 10`                                 |
| `-hls_list_size <size>`     | Defines the number of segments to include in the playlist. | `-hls_list_size 0`                            |
| `-hls_segment_filename <pattern>` | Defines the naming pattern for HLS segments.       | `-hls_segment_filename "video_%d.ts"`          |

---

## 6. **Advanced Parameters**
These are advanced settings for optimizing performance and output.

| **Parameter**               | **Description**                                         | **Example**                                     |
|-----------------------------|---------------------------------------------------------|-------------------------------------------------|
| `-movflags faststart`       | Optimizes MP4 files for progressive streaming.          | `-movflags faststart`                          |
| `-threads <num>`            | Specifies the number of threads to use for encoding.    | `-threads 4`                                   |
| `-hide_banner`              | Hides unnecessary log details from FFmpeg output.       | `-hide_banner`                                 |
| `-y`                        | Automatically overwrites the output file without prompt.| `-y`                                           |

---

## Example FFmpeg Command

```bash
ffmpeg -hide_banner -y -protocol_whitelist file,http,https,crypto,tls,tcp \
-i input.mp4 \
-c:v h264 -preset faster -crf 26 -b:v 1000000 -maxrate 1000000 -bufsize 1000000 \
-profile:v main -level 3.1 -r 24 -vf "scale=1280:-2,format=yuv420p" \
-c:a aac -b:a 128000 -ac 2 -ar 44100 \
-format hls -hls_time 10 -hls_list_size 0 \
-hls_segment_filename "video_%d.ts"
