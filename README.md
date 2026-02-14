# PNGuinnTranscoder

**PNGuinnTranscoder** is a lightweight Linux GUI tool for batch transcoding and sanitizing video files using FFmpeg.  

It removes metadata, chapters, and container fingerprints by fully re-encoding videos into a clean output format.

Built with Python + Tkinter. Minimal dependencies.

---

## Features

- Multi-file queue with sequential processing  
- Auto-renaming: spaces replaced with `_` + `_clean` suffix (e.g., `My Movie.mp4` → `My_Movie_clean.mp4`)  
- Cancel button to stop the queue safely  
- Custom folder picker with **Create Folder** button  
- Dark mode UI for reduced eye strain  
- Supports most common video formats: `.vob`, `.mp4`, `.m4v`, `.mkv`, `.avi`, `.mov`  
- Lightweight and Linux-native  

---

## Requirements

Linux system with:

- Python 3  
- Tkinter  
- FFmpeg (with libx264 support)

### Install dependencies

**Debian / Ubuntu:**

```bash
sudo apt install python3 python3-tk ffmpeg
```

**Fedora:**

```bash
sudo dnf install python3 python3-tkinter ffmpeg
```

**Arch Linux:**

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

1. Click **Add Files** and select one or more video files  
2. Choose an **Output Folder** or create a new folder in the dialog  
3. Click **Start Queue** to begin processing  
4. Files are automatically renamed using the pattern:  

```
Original_Name_clean.mp4
```

5. Monitor progress with the progress bar and status text  
6. Cancel the queue anytime with the **Cancel** button  

---

## What the tool does

Each file is:

- Fully decoded and re-encoded using H.264  
- Audio re-encoded to AAC  
- Metadata stripped  
- Chapters removed  
- Container rebuilt from scratch  

Resulting in a clean, normalized video file ready for storage, sharing, or archival.

---

## Project Structure

```
transcoder_gui.py
README.md
```

Single-file tool for simplicity.

---

## License

Personal / educational use. Modify freely.

---

## Future Ideas

- Drag & drop file support  
- ETA / estimated time remaining  
- Encoding presets (small, archival, streaming)  
- Subtitle/audio track selection  
- Queue save/load  
- Per-file output folders  
- Watch folder automation  

---

## Author

Developed as a lightweight Linux video sanitization and batch transcoding app: **PNGuinnTranscoder**
