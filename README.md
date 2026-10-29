# VanillRust-WGPU Shaders (Horizon Engine)
The first-ever native WGSL/HLSL shader pack built from scratch for the Minecraft Java rewrite in Rust — Horizon.

⚠️ WARNING (v1.5.0)
• This is an EARLY UNSTABLE ALPHA release. It may cause client crashes, memory leaks (VRAM), shadow rendering issues and high load on low-end devices.
• IMPORTANT BUG: Due to leftover code from the early port attempt, this shader will still display as "Photon Lite (Horizon)" inside the game's shader menu! This will be fixed in the next version.

✨ Current Features (v1.5.0)
• Vanilla-friendly lighting and emissive blocks for the Overworld.
• Optimized code.

🚀 Performance Presets:
• Lite: For integrated graphics (~600 MB VRAM, 25+ FPS on Intel HD 520 in 1080p).
• Quality: For discrete GPUs (RTX/RX) with maximized volumetric steps.

📸 Gameplay & Hardware Benchmarks (Intel HD 520)
### Without Shaders (80+ FPS):
[Place your "No Shaders" screenshot link here]

### VanillRust-WGPU Lite Active:
[Place your Gameplay screenshot link here]

### Hardware Load / (Memory Leak bug on hot-reload):
[Place your Task Manager screenshot link here]

📦 How to Install
1. Download the .hshader file and place it in /horizon-launcher/versions/v?.?.??/shaderpacks
2. Enable VanillRust-WGPU (currently named "Photon Lite" in 1.5 version) in game via Horizon Settings > Shader Packs.

👥 Credits / Authors:
• Claude (Anthropic AI) — WebGPU/WGSL code refactoring and optimization.
