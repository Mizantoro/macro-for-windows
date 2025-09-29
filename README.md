# Windows Macro

This repository contains a simple macro program for Windows.

> ⚠️ **Warning:** This program is provided as-is and may contain bugs. Incorrect configuration of Virtual-Key Codes or macro timing may cause unexpected behavior or high CPU usage. Use with caution.


## Configuration

The program reads settings from `config.txt`.

### `config.txt` Syntax

1. **First line:** Contains two variables:  
   - **Delay** between each macro step (in milliseconds)  
   - **Rate** indicating how often the macro checks for input (higher numbers give quicker responses but increase CPU usage)  

2. **Second line:** The button that activates the macro.  

3. **Subsequent lines:** Define the macro actions. These can be:  
   - **Button presses** (using Virtual-Key Codes)  
   - **`SetCursorPos` function**: requires two parameters on the same line for `x` and `y` coordinates  
   - **`Sleep` function**: specifies a pause in milliseconds
     
4. **Button syntax:**
  - Buttons must be specified according to [Virtual-Key Codes](https://learn.microsoft.com/en-us/windows/win32/inputdev/virtual-key-codes).
  - After each button name, a `0` or `1` indicates the action:  
    - `0` — press down  
    - `1` — release  

### Example `config.txt`
```txt
80 10
VK_XBUTTON2
I 0
I 1
Sleep 500
A 0
A 1
Sleep 1000
SetCursorPos 100 100
Y 0
Y 1
VK_LBUTTON 0
VK_LBUTTON 1
```

### Virtual-Key Codes Reference

| VK Name | Button / Key Description |
|---------|--------------------------|
| VK_LBUTTON | Left mouse button |
| VK_RBUTTON | Right mouse button |
| VK_CANCEL | Cancel (Ctrl+Break) |
| VK_MBUTTON | Middle mouse button |
| VK_XBUTTON1 | Extra mouse button 1 |
| VK_XBUTTON2 | Extra mouse button 2 |
| VK_BACK | Backspace |
| VK_TAB | Tab |
| VK_CLEAR | Clear |
| VK_RETURN | Enter |
| VK_SHIFT | Shift |
| VK_CONTROL | Control (Ctrl) |
| VK_MENU | Alt |
| VK_PAUSE | Pause |
| VK_CAPITAL | Caps Lock |
| VK_KANA | Kana input mode |
| VK_HANGUL | Hangul input mode |
| VK_IME_ON | IME On |
| VK_JUNJA | Junja input mode |
| VK_FINAL | Final input mode |
| VK_HANJA | Hanja input mode |
| VK_KANJI | Kanji input mode |
| VK_IME_OFF | IME Off |
| VK_ESCAPE | Escape |
| VK_CONVERT | Convert (IME) |
| VK_NONCONVERT | NonConvert (IME) |
| VK_ACCEPT | Accept (IME) |
| VK_MODECHANGE | Mode change (IME) |
| VK_SPACE | Spacebar |
| VK_PRIOR | Page Up |
| VK_NEXT | Page Down |
| VK_END | End |
| VK_HOME | Home |
| VK_LEFT | Left arrow |
| VK_UP | Up arrow |
| VK_RIGHT | Right arrow |
| VK_DOWN | Down arrow |
| VK_SELECT | Select |
| VK_PRINT | Print |
| VK_EXECUTE | Execute |
| VK_SNAPSHOT | Print Screen |
| VK_INSERT | Insert |
| VK_DELETE | Delete |
| VK_HELP | Help |
| 0 | Number 0 |
| 1 | Number 1 |
| 2 | Number 2 |
| 3 | Number 3 |
| 4 | Number 4 |
| 5 | Number 5 |
| 6 | Number 6 |
| 7 | Number 7 |
| 8 | Number 8 |
| 9 | Number 9 |
| A | Letter A |
| B | Letter B |
| C | Letter C |
| D | Letter D |
| E | Letter E |
| F | Letter F |
| G | Letter G |
| H | Letter H |
| I | Letter I |
| J | Letter J |
| K | Letter K |
| L | Letter L |
| M | Letter M |
| N | Letter N |
| O | Letter O |
| P | Letter P |
| Q | Letter Q |
| R | Letter R |
| S | Letter S |
| T | Letter T |
| U | Letter U |
| V | Letter V |
| W | Letter W |
| X | Letter X |
| Y | Letter Y |
| Z | Letter Z |
| VK_LWIN | Left Windows key |
| VK_RWIN | Right Windows key |
| VK_APPS | Application key / Menu key |
| VK_SLEEP | Sleep key |
| VK_NUMPAD0 | Numpad 0 |
| VK_NUMPAD1 | Numpad 1 |
| VK_NUMPAD2 | Numpad 2 |
| VK_NUMPAD3 | Numpad 3 |
| VK_NUMPAD4 | Numpad 4 |
| VK_NUMPAD5 | Numpad 5 |
| VK_NUMPAD6 | Numpad 6 |
| VK_NUMPAD7 | Numpad 7 |
| VK_NUMPAD8 | Numpad 8 |
| VK_NUMPAD9 | Numpad 9 |
| VK_MULTIPLY | Numpad * |
| VK_ADD | Numpad + |
| VK_SEPARATOR | Numpad separator |
| VK_SUBTRACT | Numpad - |
| VK_DECIMAL | Numpad . |
| VK_DIVIDE | Numpad / |
| VK_F1 | F1 |
| VK_F2 | F2 |
| VK_F3 | F3 |
| VK_F4 | F4 |
| VK_F5 | F5 |
| VK_F6 | F6 |
| VK_F7 | F7 |
| VK_F8 | F8 |
| VK_F9 | F9 |
| VK_F10 | F10 |
| VK_F11 | F11 |
| VK_F12 | F12 |
| VK_F13 | F13 |
| VK_F14 | F14 |
| VK_F15 | F15 |
| VK_F16 | F16 |
| VK_F17 | F17 |
| VK_F18 | F18 |
| VK_F19 | F19 |
| VK_F20 | F20 |
| VK_F21 | F21 |
| VK_F22 | F22 |
| VK_F23 | F23 |
| VK_F24 | F24 |
| VK_NUMLOCK | Num Lock |
| VK_SCROLL | Scroll Lock |
| VK_LSHIFT | Left Shift |
| VK_RSHIFT | Right Shift |
| VK_LCONTROL | Left Control |
| VK_RCONTROL | Right Control |
| VK_LMENU | Left Alt |
| VK_RMENU | Right Alt |
| VK_BROWSER_BACK | Browser Back |
| VK_BROWSER_FORWARD | Browser Forward |
| VK_BROWSER_REFRESH | Browser Refresh |
| VK_BROWSER_STOP | Browser Stop |
| VK_BROWSER_SEARCH | Browser Search |
| VK_BROWSER_FAVORITES | Browser Favorites |
| VK_BROWSER_HOME | Browser Home |
| VK_VOLUME_MUTE | Volume Mute |
| VK_VOLUME_DOWN | Volume Down |
| VK_VOLUME_UP | Volume Up |
| VK_MEDIA_NEXT_TRACK | Media Next Track |
| VK_MEDIA_PREV_TRACK | Media Previous Track |
| VK_MEDIA_STOP | Media Stop |
| VK_MEDIA_PLAY_PAUSE | Media Play/Pause |
| VK_LAUNCH_MAIL | Launch Mail |
| VK_LAUNCH_MEDIA_SELECT | Launch Media Select |
| VK_LAUNCH_APP1 | Launch Application 1 |
| VK_LAUNCH_APP2 | Launch Application 2 |
| VK_OEM_1 | OEM 1 (typically ;) |
| VK_OEM_PLUS | OEM Plus (+) |
| VK_OEM_COMMA | OEM Comma (,) |
| VK_OEM_MINUS | OEM Minus (-) |
| VK_OEM_PERIOD | OEM Period (.) |
| VK_OEM_2 | OEM 2 (/ ?) |
| VK_OEM_3 | OEM 3 (` ~) |
| VK_GAMEPAD_A | Gamepad A |
| VK_GAMEPAD_B | Gamepad B |
| VK_GAMEPAD_X | Gamepad X |
| VK_GAMEPAD_Y | Gamepad Y |
| VK_GAMEPAD_RIGHT_SHOULDER | Gamepad Right Shoulder |
| VK_GAMEPAD_LEFT_SHOULDER | Gamepad Left Shoulder |
| VK_GAMEPAD_LEFT_TRIGGER | Gamepad Left Trigger |
| VK_GAMEPAD_RIGHT_TRIGGER | Gamepad Right Trigger |
| VK_GAMEPAD_DPAD_UP | Gamepad D-Pad Up |
| VK_GAMEPAD_DPAD_DOWN | Gamepad D-Pad Down |
| VK_GAMEPAD_DPAD_LEFT | Gamepad D-Pad Left |
| VK_GAMEPAD_DPAD_RIGHT | Gamepad D-Pad Right |
| VK_GAMEPAD_MENU | Gamepad Menu |
| VK_GAMEPAD_VIEW | Gamepad View |
| VK_GAMEPAD_LEFT_THUMBSTICK_BUTTON | Gamepad Left Thumbstick Button |
| VK_GAMEPAD_RIGHT_THUMBSTICK_BUTTON | Gamepad Right Thumbstick Button |
| VK_GAMEPAD_LEFT_THUMBSTICK_UP | Gamepad Left Thumbstick Up |
| VK_GAMEPAD_LEFT_THUMBSTICK_DOWN | Gamepad Left Thumbstick Down |
| VK_GAMEPAD_LEFT_THUMBSTICK_RIGHT | Gamepad Left Thumbstick Right |
| VK_GAMEPAD_LEFT_THUMBSTICK_LEFT | Gamepad Left Thumbstick Left |
| VK_GAMEPAD_RIGHT_THUMBSTICK_UP | Gamepad Right Thumbstick Up |
| VK_GAMEPAD_RIGHT_THUMBSTICK_DOWN | Gamepad Right Thumbstick Down |
| VK_GAMEPAD_RIGHT_THUMBSTICK_RIGHT | Gamepad Right Thumbstick Right |
| VK_GAMEPAD_RIGHT_THUMBSTICK_LEFT | Gamepad Right Thumbstick Left |
| VK_OEM_4 | OEM 4 ([ {) |
| VK_OEM_5 | OEM 5 (\ |) |
| VK_OEM_6 | OEM 6 (] }) |
| VK_OEM_7 | OEM 7 (' ") |
| VK_OEM_8 | OEM 8 |
| VK_OEM_102 | OEM 102 (\ <) |
| VK_PROCESSKEY | Process Key |
| VK_PACKET | Packet Key |
| VK_ATTN | Attn |
| VK_CRSEL | CrSel |
| VK_EXSEL | ExSel |
| VK_EREOF | ErEOF |
| VK_PLAY | Play |
| VK_ZOOM | Zoom |
| VK_PA1 | PA1 |
| VK_OEM_CLEAR | OEM Clear |

