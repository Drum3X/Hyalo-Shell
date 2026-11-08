# Hyalo Shell

Drum3X'in liquid glass temalı Wayland masaüstü: **ShojiWM** compositor config'i
ve **Quickshell** ile yazılmış shell, kilit ekranı ve greeter.

```
shojiwm/      ShojiWM TypeScript config'i (src/index.tsx) — ~/.config/shojiwm
quickshell/   Quickshell QML (shell.qml = masaüstü, greeter.qml = giriş) — ~/.config/quickshell/hyalo
```

- Bar, dock ve paneller yarı saydam bir silüet çizer; asıl kırılmayı ShojiWM'in
  `ISLAND_GLASS` shader'ı `hyalo-*` layer namespace'lerine uygular.
- Kilit ekranı ve greeter camı kendileri çizer (`quickshell/shaders/frost.frag`).
- Shader'lar Qt 6 için derlenmelidir:
  `qsb --qt6 -o shaders/frost.frag.qsb shaders/frost.frag`.

NixOS entegrasyonu (paket, greetd, Home Manager modülleri) şuradaydı:
[Drum3X/Nix-Config @ 1538d48](https://github.com/Drum3X/Nix-Config/tree/1538d48).

`shojiwm/` ShojiWM'in MIT lisanslı varsayılan config'inden türetildi
(`shojiwm/LICENSE`). Geri kalanı GPL-3.0 (`LICENSE`).
