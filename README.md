# An-Attention-Byte

This is a program made by **Pulkit Sachdev** as a submission for the hackathon:  
*"ByteSize Sage AI Hackathon: Master the Attention Economy with Gen AI"*.

The program converts videos input by the user into **five short, reel-worthy clips** suitable for Instagram Reels or YouTube Shorts.

---
test video used https://drive.google.com/file/d/15I4yGcQgx9YmZ3n5OTbnuw__a4JEOIX0/view?usp=drive_link
test video outputs https://drive.google.com/drive/folders/15sFml_06F-FOa2TLAVukbpucjyNrbxMv?usp=drive_link
a subtitled short video of the video you sent https://drive.google.com/file/d/1xJ7JBJvOIBZMtxg_UN_VBtptmSCACiQd/view?usp=drive_link
screen recording of program https://drive.google.com/file/d/1tECz5zPFu_S1MSJ-NszjcVSZUnwEVyWJ/view?usp=drive_link


## Features

- **Automatic Reel Extraction**: Selects the top 5 clips based on **audio peaks and sentiment**.  
- **Vertical 9:16 Format**: Converts clips to vertical format for social media.  
- **Full Subtitles**: Generates and overlays subtitles from the audio using **Whisper transcription**.  
- **Sentiment-Based Ranking**: Prioritizes clips with the most engaging / positive content.  
- **Frontend Demo**: Simple **Gradio interface** for uploading videos and downloading clips.

---

## Usage

1. Open `app.py` in **Google Colab**.  
2. Run all cells.  
3. Upload a video (short videos recommended for demo).  
4. The program will process the video and output **5 downloadable reels**.  
5. For longer videos, processing can take **several minutes per clip**.

> ⚠️ **Note:** Processing time depends heavily on the length of the input video and available GPU.  
> - 1–2 min video → ~5–10 minutes total  
> - 10–30 min video → can take 30–60+ minutes due to transcription and video rendering
> - “The pipeline works for any video. For demonstration purposes, we’re showing reels generated from a short segment due to time and resource constraints.”

---

## Demo

A **short demo** using a small test video can be run via the Gradio frontend:  
[Insert your Gradio shareable link here]

---

## Technical Details

- **Audio Processing**: `pydub` detects peaks and merges nearby segments.  
- **Transcription**: `faster-whisper` generates accurate subtitles.  
- **Sentiment Analysis**: `vaderSentiment` ranks clips by engagement potential.  
- **Video Processing**: `moviepy` resizes, overlays subtitles, and converts clips to vertical format.  
- **Frontend**: `Gradio` interface for easy video upload and download.

---

## Installation

Clone the repository:

```bash
git clone https://github.com/PulkitSachdev25/An-Attention-Byte.git
cd An-Attention-Byte
pip install -r requirements.txt
