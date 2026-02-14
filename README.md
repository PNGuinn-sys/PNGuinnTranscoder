# PNGuinnTranscoder

A simple Linux GUI tool for batch transcoding and sanitizing video files using FFmpeg.

This tool removes metadata, chapters, and container fingerprints by fully re-encoding
videos into a clean output format.

Built with Python + Tkinter. No heavy dependencies.

---

## Features

- Multi-file batch queue
- Clean re-encode (no metadata or chapters)
- Automatic output naming
- Progress bar per file
- Sequential processing
- Lightweight GUI
- Linux-native workflow
- Works with VOB / MP4 / M4V / MKV / AVI / MOV

---

## Requirements

Linux system with:

- Python 3
- Tkinter
- FFmpeg (with libx264 support)

### Install dependencies

Debian / Ubuntu:

```bash
sudo apt install python3 python3-tk ffmpeg
```

Fedora:

```bash
sudo dnf install python3 python3-tkinter ffmpeg
```

Arch:

```bash
sudo pacman -S python tk ffmpeg
```

Verify FFmpeg codec support:

```bash
ffmpeg -codecs | grep libx264
```

You should see `libx264` listed.

---

## Usage

Run the program:

```bash
python3 transcoder_gui.py
```

### Workflow

1. Click **Add Files**
2. Select one or more video files
3. Choose an output folder
4. Click **Start Queue**
5. Files will transcode sequentially

Output files are automatically named:

```
originalname_clean.mp4
```

---

## What the tool does

Each file is:

- decoded
- re-encoded using H.264
- audio re-encoded to AAC
- metadata stripped
- chapters removed
- container rebuilt from scratch

This creates a clean, normalized video file.

---

## Notes

- This is a transcoder, not a DVD ripper
- Input files must already exist on disk
- Encoding time depends on CPU speed
- No GPU acceleration (CPU encoding only)

---

## Project Structure

```
transcoder_gui.py
README.md
```

Single-file tool by design.

---

## License

Personal use / educational project.

Modify freely.

---

## Future Ideas

- Cancel queue button
- Encoding presets
- Drag and drop support
- Subtitle selection
- Audio track selection
- Batch folder mode
- Logging console
- Resume failed jobs
- Watch folder automation

---

## Author

Built as a lightweight Linux video sanitization pipeline.


