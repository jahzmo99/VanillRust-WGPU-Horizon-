# VanillRust-WGPU Shaders (Horizon Engine)

The first-ever native WGSL/HLSL shader pack built from scratch for the Minecraft Java rewrite in Rust - **Horizon**.

## ✨ Current Features (v1.5.0)
- **Vanilla-friendly Lighting:** Soft and natural global illumination for the Overworld.
- **Emissive Ores & Blocks:** Glowing Diamonds, Gold, Iron, Redstone, and Blaze mobs in the Nether.
- **Optimized Performance:** Carefully refactored code to save your VRAM and prevent leaks.
- **Fixed First-Person Shadows:** Glitch-free rendering from the 1st person camera view.

## 🚀 Performance Presets
- **Lite Preset:** Tailored for integrated graphics. Runs smoothly at **40+ FPS** in the End on **Intel HD 520** (uses only ~600MB VRAM).
- **Quality Preset:** High-end settings for discrete gaming GPUs (RTX/RX) with maximized volumetric steps.

## 📦 How to Install
1. Download the preferred `.hshader` file.
2. Place it inside your `horizon-launcher/versions/v0.2.93/shaderpacks` directory.
3. Launch the game, open shader settings, and select **VanillRust-WGPU**!

---
⏳ *Next Mega Update (Coming Soon): Black Hole overhaul for the End Dimension (Interstellar style), underwater fog rewrite, and lens flare effects!*

## 👥 Credits
- **Claude (Anthropic AI)** — Assisted with WebGPU/WGSL code refactoring, math calculations, and core shader optimization for lower-end integrated GPUs.
