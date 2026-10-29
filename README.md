# VanillRust-WGPU Shaders ([Horizon Launcher](https://playhorizon.dev/) Minecraft Rust Edition)
The native WGSL shader pack built for [Horizon github](https://github.com/horizon-rust/horizon) Minecraft Java rewrite in Rust [@ludovic111](https://github.com/ludovic111).<br>
[Place your Gameplay screenshot link here]

⚠️ WARNING (v1.5.0)
This is an early, unstable release. It may cause:<br>
* Client crashes
* VRAM memory leaks
* Shadow rendering issues
* High GPU load on low-end devices


Known issue: The shader pack may still appear as Photon Lite (Horizon) in the in-game shader menu due to leftover code from an earlier port attempt. This is fixed in a future version.

✨ Current Features (v1.5.0)
* Vanilla-friendly lighting for the Overworld
* Emissive effects for bright blocks and materials
* Rendering optimizations for different hardware configurations

🚀 Performance Presets:
* **Lite**: For integrated graphics. Reduced effect quality for better performance.
* **Quality**: Higher effect quality for discrete GPUs (RTX/RX/GTX) with maximized volumetric steps and more rendering steps.
(Actual performance depends on resolution, render scale, game settings, drivers, and hardware).

**📸 Gameplay & Hardware Benchmarks (My low-end laptop Intel Core i5-6200U, Intel HD Graphics 520, 8GB RAM DDR3-2133Mhz at Single-Channel)**
### Without Shaders (12 Chunks):<br>
[Place your "No Shaders" screenshot link here]<br>
[Place your "Settings" screenshot link here]
[Place your "Settings" screenshot link here]

### VanillRust-WGPU Lite Active:<br>
[Place your Gameplay screenshot link here]<br>
[Place your "Settings" screenshot link here]

### VanillRust-WGPU Quality Active:<br>
[Place your Gameplay screenshot link here]<br>
[Place your "Settings" screenshot link here]

### Hardware Load / (Memory Leak bug on hot-reload):<br>
[Place your Task Manager screenshot link here]

📦 How to Install
1. Download the desired .hshader file from the repository or the Releases page and place it in directory, for example: /horizon-launcher/versions/v?.?.??/shaderpacks
2. Enable VanillRust-WGPU (currently named "Photon Lite" in 1.5 version) in game via Horizon Settings > Shader Packs.
Compatibility note: This pack targets a specific version of Horizon's shader implementation. Check compatibility before using it with newer builds.

Screenshots:<br>
[Place your Gameplay screenshot link here]<br>
[Place your Gameplay screenshot link here]<br>
[Place your Gameplay screenshot link here]<br>
[Place your Gameplay screenshot link here]<br>
[Place your Gameplay screenshot link here]<br>
[Place your Gameplay screenshot link here]<br>
[Place your Gameplay screenshot link here]<br>
[Place your Gameplay screenshot link here]<br>
[Place your Gameplay screenshot link here]<br>
[Place your Gameplay screenshot link here]

🛠️ Development Status:
This project is experimental and under active development.
Features, performance, and compatibility may change between versions.
Bug reports and reproducible performance tests are welcome.

👥 Credits / Authors:
* Claude Sonnet 5.5 (Anthropic AI) — WebGPU/WGSL code refactoring and optimization.
* Me — jahzmo99: Concept, prompting, testing, debugging, and performance evaluation.

📄 Disclaimer
This is an independent community project and is not an official Horizon release. Horizon and its associated trademarks belong to their respective owners.
