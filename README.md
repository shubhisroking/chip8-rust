# CHIP-8 Emulator

A CHIP-8 emulator written in Rust. Which runs in the web browser (desktop soon ((maybe)))

## How to run

### Web version

1. Build for web:
```bash
cd src/wasm
wasm-pack build --target web
```

2. Start a web server:
```bash
cd src/web
python -m http.server 8000
```

3. Open http://localhost:8000 in your browser

## Controls

```
CHIP-8    Keyboard
1 2 3 C   1 2 3 4
4 5 6 D   Q W E R
7 8 9 E   A S D F
A 0 B F   Z X C V
```

## Games

The `roms/` folder has games like PONG, TETRIS, and INVADERS.