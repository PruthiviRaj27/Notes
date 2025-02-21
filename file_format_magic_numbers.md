# File Format Magic Numbers Cheat Sheet

## Detail Explanation
Magic numbers are unique identifiers found at the beginning of files that help determine their format. These byte sequences enable software and operating systems to recognize file types even when the file extension is missing or incorrect. This cheat sheet lists the magic numbers for various file formats, including video, audio, image, archive, document, executable, and database files.

## Steps to Read a File in Hex in Terminal
To check the magic number of a file in a terminal, follow these steps:

### On Linux/macOS:
1. Open a terminal.
2. Use the `xxd` command to view the first few bytes of the file in hex format:
   ```sh
   xxd -l 16 -c 16 <filename>
   ```
   Example:
   ```sh
   xxd -l 16 -c 16 example.pdf
   ```
   Output:
   ```
   00000000: 2550 4446 2d31 2e34 0a25 c7ec e5f8 0a34  %PDF-1.4.%.....4
   ```
   The magic number `25 50 44 46` (`%PDF`) confirms it is a PDF file.

3. Alternatively, use the `hexdump` command:
   ```sh
   hexdump -C -n 16 <filename>
   ```

### On Windows (Using PowerShell):
1. Open PowerShell.
2. Run the following command to view only the first line of hex output:
   ```powershell
   Format-Hex <filename> | Select-Object -First 16
   ```

These methods allow you to verify file types based on their magic numbers.

## 1. Video Formats
| Format | Magic Number (Hex) | ASCII Equivalent |
|---------|------------------|------------------|
| **MPEG Transport Stream (.ts)** | `47` | G |
| **MPEG Program Stream (.mpg, .mpeg)** | `00 00 01 BA` or `00 00 01 B3` | N/A |
| **MP4 (.mp4, .m4v, .m4a, .mov, .3gp)** | `66 74 79 70` (within first 4-12 bytes) | `ftyp` |
| **AVI (.avi)** | `52 49 46 46` | `RIFF` (followed by `AVI `) |
| **Matroska (.mkv, .webm)** | `1A 45 DF A3` | N/A |
| **FLV (.flv)** | `46 4C 56` | `FLV` |
| **QuickTime (.mov)** | `00 00 00 ?? 66 74 79 70 71 74` | `ftypqt` |
| **WMV (.wmv, .asf)** | `30 26 B2 75 8E 66 CF 11 A6 D9 00 AA 00 62 CE 6C` | N/A |

## 2. Audio Formats
| Format | Magic Number (Hex) | ASCII Equivalent |
|---------|------------------|------------------|
| **MP3 (.mp3)** | `FF FB` or `49 44 33` | ID3 (if metadata present) |
| **WAV (.wav)** | `52 49 46 46` (followed by `WAVE`) | `RIFF` |
| **FLAC (.flac)** | `66 4C 61 43` | `fLaC` |
| **AAC (.aac)** | `FF F1` or `FF F9` | N/A |
| **OGG (.ogg, .opus, .oga)** | `4F 67 67 53` | `OggS` |
| **AIFF (.aiff, .aif, .aifc)** | `46 4F 52 4D` (followed by `AIFF`) | `FORM` |

## 3. Image Formats
| Format | Magic Number (Hex) | ASCII Equivalent |
|---------|------------------|------------------|
| **JPEG (.jpg, .jpeg)** | `FF D8 FF` | N/A |
| **PNG (.png)** | `89 50 4E 47 0D 0A 1A 0A` | `.PNG....` |
| **GIF (.gif)** | `47 49 46 38 37 61` (GIF87a) or `47 49 46 38 39 61` (GIF89a) | `GIF87a` or `GIF89a` |
| **BMP (.bmp)** | `42 4D` | `BM` |
| **TIFF (.tif, .tiff)** | `49 49 2A 00` (Little-endian) or `4D 4D 00 2A` (Big-endian) | `II*.` or `MM.*` |
| **WEBP (.webp)** | `52 49 46 46` (followed by `WEBP`) | `RIFF` |

## 4. Archive & Compression Formats
| Format | Magic Number (Hex) | ASCII Equivalent |
|---------|------------------|------------------|
| **ZIP (.zip, .apk, .jar, .docx, .xlsx, .pptx)** | `50 4B 03 04` | `PK..` |
| **RAR (.rar)** | `52 61 72 21 1A 07 00` | `Rar!....` |
| **7z (.7z)** | `37 7A BC AF 27 1C` | `7z..'..` |
| **GZIP (.gz, .tar.gz, .tgz)** | `1F 8B` | N/A |
| **BZIP2 (.bz2)** | `42 5A 68` | `BZh` |
| **TAR (.tar)** | No fixed magic number but contains `ustar` at offset 257 | `ustar` |

## 5. Document Formats
| Format | Magic Number (Hex) | ASCII Equivalent |
|---------|------------------|------------------|
| **PDF (.pdf)** | `25 50 44 46` | `%PDF` |
| **DOC, XLS, PPT (Old MS Office formats)** | `D0 CF 11 E0 A1 B1 1A E1` | N/A |
| **DOCX, XLSX, PPTX (Modern MS Office)** | `50 4B 03 04` (ZIP-based) | `PK..` |
| **RTF (.rtf)** | `7B 5C 72 74 66` | `{\rtf` |
| **EPUB (.epub)** | `50 4B 03 04` (ZIP-based) | `PK..` |

## 6. Executable & Binary Formats
| Format | Magic Number (Hex) | ASCII Equivalent |
|---------|------------------|------------------|
| **Windows EXE/DLL (.exe, .dll, .sys)** | `4D 5A` | `MZ` |
| **Linux ELF Executable (.elf, .so, .o)** | `7F 45 4C 46` | `.ELF` |
| **Mac Mach-O Executable (.mach, .dylib)** | `FE ED FA CE` (32-bit) or `FE ED FA CF` (64-bit) | N/A |

## 7. Database & Virtual Machine Formats
| Format | Magic Number (Hex) | ASCII Equivalent |
|---------|------------------|------------------|
| **SQLite Database (.sqlite, .db)** | `53 51 4C 69 74 65 20 66` | `SQLite f` |
| **Java Class File (.class)** | `CA FE BA BE` | N/A |
| **Virtual Hard Disk (.vhd)** | `63 6F 6E 65 63 74 69 78 00` | `conectix` |
