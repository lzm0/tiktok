# TikTok Text-to-Speech CLI

This is a simple shell script to access the TikTok Text-to-Speech API.

This project currently relies on `afplay` in macOS for mp3 audio playback.

## Requirements

- afplay
- curl
- jq

## Installation

```bash
curl -sL https://raw.githubusercontent.com/lzm0/tiktok/main/tiktok -o tiktok
chmod +x tiktok
mv tiktok /usr/local/bin/tiktok
```

## Usage

```
Usage: tiktok [-v voice] [-o file] [text...]
Options:
  -v voice  Voice to use (default: en_us_001)
            see https://github.com/oscie57/tiktok-voice/blob/main/codes.md for available voices
  -o file   Output file, default is to play audio to the speakers
```

### Play to speakers

```bash
tiktok -v en_us_c3po 'Hello, world!'
```

### Save as mp3

```bash
tiktok -v en_us_c3po -o hello_world.mp3 'Hello, world!'
```

### Make a fortune quietly

```bash
fortune | tiktok
```

## Credits

- [tiktok-voice](https://github.com/oscie57/tiktok-voice) Simple Python script to interact with the TikTok TTS API
