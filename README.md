
```
 ____  _   _ ____ _______   __  _   _ _____ ____  
|  _ \| | | / ___|_   _\ \ / / | \ | | ____/ ___| 
| |_) | | | \___ \ | |  \ V /  |  \| |  _| \___ \ 
|  _ <| |_| |___) || |   | |   | |\  | |___ ___) |
|_| \_\\___/|____/ |_|   |_|   |_| \_|_____|____/ 
```

#  Rusty NES Emulator

**Rusty NES** is a Nintendo Entertainment System (NES) emulator written in **Rust**, featuring a graphical user interface and customizable video/audio settings. RustyNES lets you customize the display to give you television features and coloration to let you produce the version of the game that you expect and give you a more accurate and realistic representation according to your memeories or wishes. This is a new spirit of emulator that diverges from traditional emulators, but at the same time uses techniques pioneered by full featured and feature rich emulators of the past.

---


## 🆕 New in v2 (5-14-2026)
Fixes, Upgrades, and Updates have been added to RustyNES v2.

- USB Joystick/Controller Support Added
- Fullscreen is added with a button pressing "F"
- New Video Options
- Sprite Viewer Added
- Improved Sound Engine
- Color Adjustments are more normal/accurate
- Hide Edges (Overscan) Added for Super Mario Bros. 3
- Fixed a bug where loading another game after a game was loaded caused overflow

Docs below will be updated to reflect the changes later.

## 🖥️ Core Architecture

The emulator emulates these components:

| Module | Description |
|--------|-------------|
| **CPU** | 6502 processor emulation |
| **PPU** | Picture Processing Unit for graphics rendering |
| **APU** | Audio Processing Unit for sound generation |
| **System Bus** | System bus connecting all components |
| **Cartridge** | ROM loading and management |
| **Mappers** | Memory mapper support for different cartridge types |

---

## ✨ Key Features

### 🖥 Display & Graphics

- **Resolution:** 256×240 native NES resolution with scaling, and a special custom CRT TV video options.

#### Video Modes
- **Default Mode**
  - Pixel-perfect output  

- **CRT/TV Mode**
  - Linear filtering  
  - 4:3 TV aspect ratio correction  
  - Appropriate approximation of screen croping to top and bottom scanlines  

#### Visual Effects
- Adjustable **brightness**
- **Contrast** control
- **Saturation** adjustment
- **Hue shift** (degree-based color rotation)
- Optional **scanline overlay** with configurable intensity (darkness)

#### Performance Overlay
- Real-time calculated **FPS Counter**

---

### 🔊 Audio

- **44.1 kHz** mono audio output  
- **4096-sample** audio buffer  
- Dynamic audio synchronization
- Automatic buffer management

---

### 🎮 Input

**Controller 1 Key Mapping**

| Key | NES Button |
|-----|------------|
| **X** | A |
| **Z** | B |
| **A** | Select |
| **S** | Start |
| **Arrow Keys** | D-Pad |

**USB Controller Support Added in v2**

---

### 📋 Menu System

- **ESC** key toggles the pause menu  
- Built-in **ROM file picker** (filters for `.nes` files)  
- Change **video and audio settings** Live
- Reproduce Classic TV Effects
- Multiple FPS modes:
  - **NTSC (60 Hz)**
  - **PAL (50 Hz)**
  - **Unlocked**
  - **Custom**

---

## ⚡ Performance

- Frame timing control with configurable target frame rates  
- **VSync** presentation  
- Audio-driven timing adjustments when not in **Unlocked** mode


## 🕹️ Compatibility

You can play many different NES games with this emulator! There should be a lot of NES games that work with this emulator, but I have not tested heavily. A quick reference is to look up what mapper a game uses, because Mappers 0, 1, 2, 3, and 4 are supported. Games that use other mappers will refuse to start since they lack support.

.

THIS IS A COMPLETELY CUSTOM CODE, NO NINTENDO COPYRIGHTED MATERIAL IS USED IN THIS. GAMES ARE NOT INCLUDED. GAMES ARE NOT RELEVANT TO THIS PROJECT'S CODE AS PROVIDED HERE.

## License
Proprietary Software. All rights reserved.
