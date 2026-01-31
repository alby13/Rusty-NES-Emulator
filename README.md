
```
 ____  _   _ ____ _______   __  _   _ _____ ____  
|  _ \| | | / ___|_   _\ \ / / | \ | | ____/ ___| 
| |_) | | | \___ \ | |  \ V /  |  \| |  _| \___ \ 
|  _ <| |_| |___) || |   | |   | |\  | |___ ___) |
|_| \_\\___/|____/ |_|   |_|   |_| \_|_____|____/ 
```

#  Rusty NES Emulator

**Rusty NES** is a Nintendo Entertainment System (NES) emulator written in **Rust**, featuring a graphical user interface and customizable video/audio settings.

---

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

- **Resolution:** 256×240 native NES resolution with scaling, and a special custom CRT TV video option.

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
- Dynamic audio synchronization based on buffer fullness  
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

---

### 📋 Menu System

- **ESC** key toggles the pause menu  
- Built-in **ROM file picker** (filters for `.nes` files)  
- Runtime configuration for **video and audio settings**  
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

There should be a lot of NES games that work with this emulator, but I have not tested most of the NES library. A quick reference is to look up what mapper a game uses, because Mappers 0, 1, 2, 3, and 4 are supported. Games that use other mappers will refuse to start since they lack support.

Working:

- Castlevania II: Simon's Quest - Working ✅
- Contra - Working ✅
- Lolo's Adventure - Working ✅
- Megaman 1 - Working ✅ (Has a Whining/Whistle Sound)
- Megaman 2 - Working ✅ (Has a Whining/Whistle Sound)
- Super Mario Bros. - Working ✅
- Super Mario Bros. 2 - Working ✅
- Super Mario Bros. 3 - Working ✅

Partially Working:

- Kirby's Adventure

Not Working (Major Issues)

- Tetris

Not Supported:

- Mike Tyson's Punch Out
- Battletoads

## ⚠️ Important Note: If you encounter issues with video or sound, restart the emulator. There is a bug where previous games can cause issues with new ROM loads.

THIS IS A COMPLETELY CUSTOM CODE, NO NINTENDO COPYRIGHTED MATERIAL IS USED IN THIS. GAMES ARE NOT INCLUDED. GAMES ARE NOT RELEVANT TO THIS PROJECT'S CODE AS PROVIDED HERE.

## License
Proprietary Software. All rights reserved.
