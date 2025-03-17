# Tune Prism: Professional Vocal Remover, Song Key Finder & BPM Detection Tool

## The All-in-One Music Analysis & Separation Suite

Tune Prism is a powerful desktop application that combines three essential music production tools:

1. **Advanced Vocal Remover** - Accurately extract vocals from any song
2. **Precise Song Key Finder** - Instantly identify the musical key of your tracks
3. **Professional BPM Finder** - Detect tempo with exceptional accuracy

Split any track into 4 high-quality stems: vocals, drums, bass and other instruments. Powered by Facebook's state-of-the-art [HTDemucs model](https://github.com/adefossez/demucs).

Built with Rust, Tauri, PyTorch and React for maximum performance and reliability.

## ✨ Key Benefits

- **100% FREE & Open Source** - Professional-grade audio tools at no cost
- **Complete Privacy** - Works entirely offline with no data collection
- **No Internet Required** - Process your music without an internet connection
- **No Account Needed** - No sign-ups, subscriptions or hidden fees

## Features

### 🎤 Professional Vocal Remover
- Extract crystal-clear vocals from any song
- Create instrumental versions for karaoke or remixing
- Isolate vocals for sampling or vocal practice
- Perfect for DJs, producers, and music enthusiasts

### 🎵 Song Key Finder
- Instantly identify the musical key of any track
- Improve your DJ mixes with harmonic mixing
- Find compatible songs in complementary keys
- Essential for musicians practicing with backing tracks

### 🥁 BPM Finder
- Accurately detect the tempo of any song
- Perfect for DJs creating seamless transitions
- Organize your music library by tempo
- Sync tracks to video projects at the right speed

## Demo: Easy-to-Use Interface
Simply drag a track in, extract stems, identify key and BPM, then drag your stems out. No complicated setup required!

https://github.com/user-attachments/assets/584cf59e-ef4b-4f24-913d-dc52d7549609

## Try it Out
For M1 macs running MacOS, there's a prebuilt binary available on the releases page. Currently, that's the only platform we have built and tested the app on. Porting to other platforms is a bit of work and we only have MacBooks for testing. If you can make the app run on Linux or Windows machines, we will happily accept your PR.

## Why Choose Tune Prism?

- **Free Forever** - Unlike subscription-based alternatives that cost $10-20/month
- **Protect Your Privacy** - Your audio never leaves your computer
- **Open-Source Transparency** - Community-verified code you can trust
- **No Internet Dependency** - Use anywhere, even without Wi-Fi
- **Professional Quality** - Commercial-grade results without the price tag

## Common Use Cases
- **Music Producers**: Remove vocals to create remixes or isolate specific elements
- **DJs**: Find the key and BPM of tracks to create harmonic mixes
- **Singers**: Practice with instrumental versions of your favorite songs
- **Content Creators**: Extract music elements for videos and podcasts
- **Music Teachers**: Isolate instrument parts for educational purposes

## Building Locally

These instructions have been tested to work on an M1 Macbook Pro running MacOS 

### Requirements

#### Rust and Cargo
You can install Rust using [rustup](rustup.rs). I don't know what the MSRV is but I used `v1.79.0` while building the app. 

```bash
$ rustc --version
rustc 1.79.0 (129f3b996 2024-06-10)

$ cargo --version
cargo 1.79.0 (ffa9cf99a 2024-06-03)
```
#### Node and NPM
```bash
$ brew install node@20

$ node --version 
v20.14.0

$ npm --version
10.7.0
```

#### PyTorch

You can either use `libtorch` or provide the path to a PYTORCH installation. I found it easier to use `libtorch` directly. 

```bash
$ wget https://download.pytorch.org/libtorch/cpu/libtorch-macos-arm64-2.2.0.zip
$ unzip libtorch-macos-arm64-2.2.0.zip
```

#### Misc Dependencies

```bash
$ brew install libomp
```

### Building the app

- Clone the repo
```bash
$ git clone https://github.com/hedonhermdev/tune-prism && cd tune-prism
```

- Install npm dependencies
```bash
$ npm install
```

- Download the models
You can use the ``get_models.sh`` script to download the models
```bash
$ ./get_models.sh
```

- Copy `libtorch` to the repo. 
```
$ cp PATH_TO_LIBTORCH ./libtorch
$ export LIBTORCH=$(realpath ./libtorch) 
```

After this you're all set to start building the app. 

```bash
$ npm run tauri build
$ npm run tauri dev # for development
```

# Contributing

Just open a PR :)

## Keywords
vocal remover, song key finder, bpm finder, vocal extraction, stem separation, audio analysis tool, music production software, dj tools, remove vocals from songs, find song key, detect bpm, free vocal remover, open source audio tools, offline music analyzer
