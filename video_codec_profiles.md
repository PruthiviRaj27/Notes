# H.264 (AVC) Profile & Level Support

| Profile        | Level | Maximum Resolution | Maximum Frame Rate | Bit Depth |
|---------------|-------|--------------------|--------------------|-----------|
| Baseline      | 1     | 128×96             | 30.9 fps           | 8-bit     |
| Baseline      | 1.1   | 176×144            | 30.3 fps           | 8-bit     |
| Baseline      | 1.2   | 320×240            | 20.0 fps           | 8-bit     |
| Baseline      | 1.3   | 352×288            | 30.0 fps           | 8-bit     |
| Main          | 2     | 352×288            | 30.0 fps           | 8-bit     |
| Main          | 2.1   | 352×480            | 30.0 fps           | 8-bit     |
| Main          | 2.2   | 720×480            | 15.0 fps           | 8-bit     |
| Main          | 3     | 720×480            | 30.0 fps           | 8-bit     |
| Main          | 3.1   | 1280×720           | 30.0 fps           | 8-bit     |
| Main          | 3.2   | 1280×720           | 60.0 fps           | 8-bit     |
| High          | 4     | 1920×1080          | 30.1 fps           | 8-bit     |
| High          | 4.1   | 1920×1080          | 30.1 fps           | 8-bit     |
| High          | 4.2   | 1920×1080          | 64.0 fps           | 8-bit     |
| High          | 5     | 2560×1920          | 30.7 fps           | 8-bit     |
| High          | 5.1   | 4096×2048          | 30.0 fps           | 8-bit     |
| High          | 5.2   | 4096×2048          | 63.3 fps           | 8-bit     |
| High 10       | 4.1   | 1920×1080          | 30.1 fps           | 10-bit    |
| High 10       | 4.2   | 1920×1080          | 64.0 fps           | 10-bit    |
| High 10       | 5     | 2560×1920          | 30.7 fps           | 10-bit    |
| High 10       | 5.1   | 4096×2048          | 30.0 fps           | 10-bit    |
| High 10       | 5.2   | 4096×2048          | 63.3 fps           | 10-bit    |
| High 4:2:2    | 4.1   | 1920×1080          | 30.1 fps           | 10-bit    |
| High 4:2:2    | 4.2   | 1920×1080          | 64.0 fps           | 10-bit    |
| High 4:2:2    | 5     | 2560×1920          | 30.7 fps           | 10-bit    |
| High 4:2:2    | 5.1   | 4096×2048          | 30.0 fps           | 10-bit    |
| High 4:2:2    | 5.2   | 4096×2048          | 63.3 fps           | 10-bit    |
| High 4:4:4    | 4.1   | 1920×1080          | 30.1 fps           | 12-bit    |
| High 4:4:4    | 4.2   | 1920×1080          | 64.0 fps           | 12-bit    |
| High 4:4:4    | 5     | 2560×1920          | 30.7 fps           | 12-bit    |
| High 4:4:4    | 5.1   | 4096×2048          | 30.0 fps           | 12-bit    |
| High 4:4:4    | 5.2   | 4096×2048          | 63.3 fps           | 12-bit    |

## Notes

- **Profiles:**
  - **Baseline:** Low-complexity applications, 8-bit 4:2:0 chroma sampling.
  - **Main:** Supports interlaced video, 8-bit 4:2:0 chroma sampling.
  - **High:** Higher compression efficiency, 8-bit 4:2:0 chroma sampling.
  - **High 10:** Supports up to 10-bit color depth, 4:2:0 chroma sampling.
  - **High 4:2:2:** Supports up to 10-bit color depth, 4:2:2 chroma sampling.
  - **High 4:4:4:** Supports up to 12-bit color depth, 4:4:4 chroma sampling.

- **Levels:** Define constraints on resolution, frame rate, and bit rate.
- **Bit Depth:** Higher bit depth allows more color variations.

For more details, check [Advanced Video Coding (H.264) Wikipedia](https://en.wikipedia.org/wiki/Advanced_Video_Coding).


# HEVC (H.265) Profile & Level Support

| Profile          | Level  | Maximum Resolution     | Maximum Frame Rate | Bit Depth      |
|-----------------|--------|-----------------------|--------------------|---------------|
| Main / Main 10 | 1      | 176×144 (QCIF)        | 15 fps             | 8-bit / 10-bit |
| Main / Main 10 | 2      | 352×288 (CIF)         | 30 fps             | 8-bit / 10-bit |
| Main / Main 10 | 2.1    | 352×288 (CIF)         | 60 fps             | 8-bit / 10-bit |
| Main / Main 10 | 3      | 720×480 (SD)          | 30 fps             | 8-bit / 10-bit |
| Main / Main 10 | 3.1    | 1280×720 (HD)         | 30 fps             | 8-bit / 10-bit |
| Main / Main 10 | 4      | 1920×1080 (Full HD)   | 30 fps             | 8-bit / 10-bit |
| Main / Main 10 | 4.1    | 2048×1080 (2K)        | 30 fps             | 8-bit / 10-bit |
| Main / Main 10 | 4.1    | 1920×1080 (Full HD)   | 60 fps             | 8-bit / 10-bit |
| Main / Main 10 | 4.1    | 1280×720 (HD)         | 120 fps            | 8-bit / 10-bit |
| Main / Main 10 | 5      | 3840×2160 (4K)        | 30 fps             | 8-bit / 10-bit |
| Main / Main 10 | 5.1    | 3840×2160 (4K)        | 60 fps             | 8-bit / 10-bit |
| Main / Main 10 | 5.2    | 3840×2160 (4K)        | 120 fps            | 8-bit / 10-bit |
| Main / Main 10 | 6      | 7680×4320 (8K)        | 30 fps             | 8-bit / 10-bit |
| Main / Main 10 | 6.1    | 7680×4320 (8K)        | 60 fps             | 8-bit / 10-bit |
| Main / Main 10 | 6.2    | 7680×4320 (8K)        | 120 fps            | 8-bit / 10-bit |
| Main / Main 10 | 6.3    | 8192×4320 (8K Ultra-Wide) | 120 fps      | 8-bit / 10-bit |

## Notes

- **Profiles:**
  - **Main:** Standard HEVC profile with 8-bit 4:2:0 chroma sampling.
  - **Main 10:** Supports up to 10-bit color depth, allowing HDR support.

- **Levels:** Define constraints on resolution, frame rate, and bit rate.

- **Bit Depth:** Higher bit depth enables better color precision.

For more details, refer to [HEVC Wikipedia](https://en.wikipedia.org/wiki/High_Efficiency_Video_Coding).

# VP9 Profile & Level Support

| Profile          | Level  | Maximum Resolution     | Maximum Frame Rate | Bit Depth      |
|-----------------|--------|-----------------------|--------------------|---------------|
| Profile 0      | 1      | 426×240 (240p)        | 30 fps             | 8-bit          |
| Profile 0      | 2      | 640×360 (360p)        | 30 fps             | 8-bit          |
| Profile 0      | 3      | 854×480 (480p)        | 30 fps             | 8-bit          |
| Profile 0      | 4      | 1280×720 (720p HD)    | 30 fps             | 8-bit          |
| Profile 0      | 5      | 1920×1080 (1080p FHD) | 30 fps             | 8-bit          |
| Profile 0      | 6      | 2560×1440 (1440p QHD) | 30 fps             | 8-bit          |
| Profile 0      | 7      | 3840×2160 (4K UHD)    | 30 fps             | 8-bit          |
| Profile 0      | 8      | 7680×4320 (8K UHD)    | 30 fps             | 8-bit          |
| Profile 1      | 4      | 1280×720 (720p HD)    | 30 fps             | 8-bit / 10-bit |
| Profile 1      | 5      | 1920×1080 (1080p FHD) | 30 fps             | 8-bit / 10-bit |
| Profile 1      | 6      | 2560×1440 (1440p QHD) | 30 fps             | 8-bit / 10-bit |
| Profile 1      | 7      | 3840×2160 (4K UHD)    | 30 fps             | 8-bit / 10-bit |
| Profile 1      | 8      | 7680×4320 (8K UHD)    | 30 fps             | 8-bit / 10-bit |
| Profile 2      | 4      | 1280×720 (720p HD)    | 30 fps             | 10-bit / 12-bit |
| Profile 2      | 5      | 1920×1080 (1080p FHD) | 30 fps             | 10-bit / 12-bit |
| Profile 2      | 6      | 2560×1440 (1440p QHD) | 30 fps             | 10-bit / 12-bit |
| Profile 2      | 7      | 3840×2160 (4K UHD)    | 30 fps             | 10-bit / 12-bit |
| Profile 2      | 8      | 7680×4320 (8K UHD)    | 30 fps             | 10-bit / 12-bit |
| Profile 3      | 4      | 1280×720 (720p HD)    | 30 fps             | 10-bit / 12-bit |
| Profile 3      | 5      | 1920×1080 (1080p FHD) | 30 fps             | 10-bit / 12-bit |
| Profile 3      | 6      | 2560×1440 (1440p QHD) | 30 fps             | 10-bit / 12-bit |
| Profile 3      | 7      | 3840×2160 (4K UHD)    | 30 fps             | 10-bit / 12-bit |
| Profile 3      | 8      | 7680×4320 (8K UHD)    | 30 fps             | 10-bit / 12-bit |

## Notes

- **Profiles:**
  - **Profile 0:** 8-bit color, 4:2:0 chroma sampling.
  - **Profile 1:** 8-bit & 10-bit color, 4:2:2 or 4:4:4 chroma sampling.
  - **Profile 2:** 10-bit & 12-bit color, 4:2:0 chroma sampling (supports HDR).
  - **Profile 3:** 10-bit & 12-bit color, 4:2:2 or 4:4:4 chroma sampling.

- **Levels:** Define constraints on resolution, frame rate, and bitrate.
- **Bit Depth:** Higher bit depth supports better color accuracy and HDR.

For more details, check [VP9 Wikipedia](https://en.wikipedia.org/wiki/VP9).


# AV1 Profile & Level Support

| Profile      | Level  | Maximum Resolution     | Maximum Frame Rate | Bit Depth      |
|-------------|--------|-----------------------|--------------------|---------------|
| Main        | 2.0    | 426×240 (240p)        | 30 fps             | 8-bit / 10-bit |
| Main        | 2.1    | 426×240 (240p)        | 60 fps             | 8-bit / 10-bit |
| Main        | 3.0    | 640×360 (360p)        | 30 fps             | 8-bit / 10-bit |
| Main        | 3.1    | 640×360 (360p)        | 60 fps             | 8-bit / 10-bit |
| Main        | 4.0    | 854×480 (480p)        | 30 fps             | 8-bit / 10-bit |
| Main        | 4.1    | 854×480 (480p)        | 60 fps             | 8-bit / 10-bit |
| Main        | 5.0    | 1280×720 (720p HD)    | 30 fps             | 8-bit / 10-bit |
| Main        | 5.1    | 1280×720 (720p HD)    | 60 fps             | 8-bit / 10-bit |
| Main        | 5.2    | 1280×720 (720p HD)    | 120 fps            | 8-bit / 10-bit |
| Main        | 6.0    | 1920×1080 (1080p FHD) | 30 fps             | 8-bit / 10-bit |
| Main        | 6.1    | 1920×1080 (1080p FHD) | 60 fps             | 8-bit / 10-bit |
| Main        | 6.2    | 1920×1080 (1080p FHD) | 120 fps            | 8-bit / 10-bit |
| Main        | 7.0    | 3840×2160 (4K UHD)    | 30 fps             | 8-bit / 10-bit |
| Main        | 7.1    | 3840×2160 (4K UHD)    | 60 fps             | 8-bit / 10-bit |
| Main        | 7.2    | 3840×2160 (4K UHD)    | 120 fps            | 8-bit / 10-bit |
| Main        | 8.0    | 7680×4320 (8K UHD)    | 30 fps             | 8-bit / 10-bit |
| Main        | 8.1    | 7680×4320 (8K UHD)    | 60 fps             | 8-bit / 10-bit |
| Main        | 8.2    | 7680×4320 (8K UHD)    | 120 fps            | 8-bit / 10-bit |
| High        | 6.0    | 1920×1080 (1080p FHD) | 30 fps             | 10-bit / 12-bit |
| High        | 6.1    | 1920×1080 (1080p FHD) | 60 fps             | 10-bit / 12-bit |
| High        | 6.2    | 1920×1080 (1080p FHD) | 120 fps            | 10-bit / 12-bit |
| High        | 7.0    | 3840×2160 (4K UHD)    | 30 fps             | 10-bit / 12-bit |
| High        | 7.1    | 3840×2160 (4K UHD)    | 60 fps             | 10-bit / 12-bit |
| High        | 7.2    | 3840×2160 (4K UHD)    | 120 fps            | 10-bit / 12-bit |
| High        | 8.0    | 7680×4320 (8K UHD)    | 30 fps             | 10-bit / 12-bit |
| High        | 8.1    | 7680×4320 (8K UHD)    | 60 fps             | 10-bit / 12-bit |
| High        | 8.2    | 7680×4320 (8K UHD)    | 120 fps            | 10-bit / 12-bit |

## Notes

- **Profiles:**
  - **Main:** Supports 8-bit and 10-bit color depth, suitable for most standard content.
  - **High:** Supports 10-bit and 12-bit color depth with wider chroma sampling, useful for HDR and high-quality video applications.

- **Levels:** Define constraints on resolution, frame rate, and bitrate.

- **Bit Depth:** 
  - **8-bit:** Standard color depth for most SDR content.
  - **10-bit / 12-bit:** Higher color precision, useful for HDR content.

For more details, check [AV1 Wikipedia](https://en.wikipedia.org/wiki/AV1).

