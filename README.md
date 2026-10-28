
# VanillRust-WGPU Shaders (Horizon Engine)

The first-ever native WGSL/HLSL shader pack built from scratch for the Minecraft Java rewrite in Rust — Horizon.

✨ Current Features (v1.5.0)
• Vanilla-friendly lighting and emissive blocks for the Overworld.
• Optimized code for VRAM efficiency and leak prevention.

🚀 Performance Presets
• Lite: For integrated graphics (~600 MB VRAM, 25+ FPS on Intel HD 520 in 1080p).
• Quality: For discrete GPUs (RTX/RX) with maximized volumetric steps.

📦 How to Install
1. Download the .hshader file and place it in /horizon-launcher/versions/v?.?.??/shaderpacks.
2. Enable VanillRust-WGPU in game via Horizon Settings > Shader Packs.
3. Enjoy

👥 Credits / Authors:
• Claude (Anthropic AI) — WebGPU/WGSL code refactoring and optimization.
