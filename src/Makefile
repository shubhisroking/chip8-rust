.PHONY: all
all: web

.PHONY: web
web:
	cd chip8_core && cargo build --release
	cd wasm && wasm-pack build --target web --out-dir pkg
	cp wasm/pkg/wasm.js web/
	cp wasm/pkg/wasm_bg.wasm web/

.PHONY: serve
serve: web
	cd web && python3 -m http.server 8000

.PHONY: clean
clean:
	cd chip8_core && cargo clean
	cd desktop && cargo clean
	cd wasm && cargo clean
	rm -rf wasm/pkg web/wasm.js web/wasm_bg.wasm
