# VanillRust-WGPU Shaders ([Horizon Launcher](https://playhorizon.dev/) Minecraft Rust Edition)
The native WGSL shader pack built for [Horizon github](https://github.com/horizon-rust/horizon) Minecraft Java rewrite in Rust [@ludovic111](https://github.com/ludovic111).<br>
[Place your Gameplay screenshot link here]

⚠️ This is an early, unstable release. It may cause:
* Shadow rendering issues
* Varying stability
* Bugs

Download the latest version from the [Releases page](https://github.com/jahzmo99/VanillRust-WGPU-Horizon-/releases).

🚀 Performance Presets:
* **Lite**: For integrated graphics. Reduced effect quality for better performance.
* **Quality**: Higher effect quality for discrete GPUs (RTX/RX/GTX) with maximized volumetric steps and more rendering steps.
(Actual performance depends on resolution, render scale, game settings, drivers, and hardware).


### 📦 How to Install
1. Download the desired `.hshader` file from the [Releases page](https://github.com/jahzmo99/VanillRust-WGPU-Horizon-/releases) and place it in directory, for example: `/horizon-launcher/versions/v?.?.??/shaderpacks`
2. Enable VanillRust-WGPU in game via Horizon Settings > Shader Packs.
Compatibility note: This pack targets a specific version of Horizon's shader implementation. Check compatibility before using it with newer builds.

---

### 📸 Settings & Hardware Benchmark And Gameplay (My low-end laptop Intel Core i5-6200U, Intel HD Graphics 520, 8GB RAM DDR3-2133Mhz at Single-Channel)👇
`Settings (12 Chunks, Simulation: 5 Chunks, VSync: OFF, Fullscreen 1080p, Biome Blend: OFF, Smooth Lighting: ON, Clouds: OFF, Particles: Minimal, Mipmap Levels: 4, Entity Shadows: ON, Entity Distance: 50%, See-Through Leaves: ON, Weather Effect Radius: 3 Blocks, LOD Distance: OFF, Far Detail: FULL, Cave Culling: ON, Entity Culling: OFF, Chunk Updates: 2 per frame, Sky: ON, Fog: OFF, Weather: ON, Resolution Scale: 100%, Anti-Aliasing: OFF, Graphics API: Vulkan)`<br>
<img width="1920" height="1080" alt="settings2" src="https://github.com/user-attachments/assets/7b8e23aa-5298-40db-bc73-797aaa1a13d2" /><br>
<details>
<summary><b>Click to view Full Settings Screenshots (5 images)</b></summary>
<br>

<img width="1920" height="1080" alt="settings1" src="https://github.com/user-attachments/assets/3224f8c9-7aea-46fd-8835-886c00ce4144" /><br>
<img width="1920" height="1080" alt="settings3" src="https://github.com/user-attachments/assets/a6d2c39c-2db5-4417-89d7-c15231d5013b" /><br>
<img width="1920" height="1080" alt="settings4" src="https://github.com/user-attachments/assets/b2b12dd3-2a59-41fe-95b1-9e3af44f93c8" /><br>
<img width="1920" height="1080" alt="settings5" src="https://github.com/user-attachments/assets/cd052e8f-b810-4d88-a230-aad142d982fe" /><br>
<img width="1920" height="1080" alt="settings6" src="https://github.com/user-attachments/assets/5d54184d-4cd9-486e-a1c2-d0afcd8337b6" />

</details>

---

# 📊 Hardware Benchmark:
>(using the exact same settings mentioned above without changes. These are medium settings that balance visual quality, suitable for decent PCs rather than a potato like mine. In my case, using a potato, I test 3 modes as shown in the photos below, while the description underneath provides details without screenshots using low settings. I record the values always in the exact same spot and in the same world where weather switching is disabled and time is frozen. A command teleports me precisely to the same coordinates and aims the crosshair at the exact same point. I wouldn't call this the easiest scene, nor would I call it the hardest, because the FPS I recorded can drop or rise if I move away from this testing location. This is closer to an average and stable scene)

## Without Shaders (My laptop already struggles with basic medium settings: 42 FPS and 24 ms, CPU at 21%, and HD 520 at 98% load):<br>
<img width="1920" height="1080" alt="2026-10-29_08 51 48" src="https://github.com/user-attachments/assets/1cdea281-0899-40d9-a7da-041c54999eaa" /><br>
<img width="1920" height="1080" alt="Снимок экрана 2026-10-29 105452" src="https://github.com/user-attachments/assets/1d20ff0e-920f-4fe9-9ced-49b281cd64c5" /><br>
If you lower the settings to 4 chunks and set everything to minimum, you can reach 117-120 FPS (without reducing the resolution). And by reducing the render scale to 50% (from 1920x1080 down to 960x540), it jumps to 198-202 FPS.


## VanillRust-WGPU *Lite* Active (dropped to 23 FPS and 45.5 ms, but the CPU load decreased by 3% — CPU at 18% down from 21%, and HD 520 at 99%):<br>
<img width="1920" height="1080" alt="2026-10-29_08 55 48lite" src="https://github.com/user-attachments/assets/65039a67-acc2-4057-9601-25f693839c33" /><br>
<img width="1920" height="1080" alt="Снимок экрана 2026-10-29 110912lite" src="https://github.com/user-attachments/assets/4371b08c-d8af-4f50-a1d0-2266842569de" /><br>
If you lower the settings to 4 chunks and set everything to minimum, you can reach 42 FPS (without reducing the resolution). And by reducing the render scale to 50% (from 1920x1080 down to 960x540), it goes up to 72 FPS.

## VanillRust-WGPU *Quality* Active (absolute torture for the HD 520 at 10 FPS and 102.5 ms, while the CPU unloaded by another 1% and is sitting at 17% load, while the HD 520 is at 99%):<br>
<img width="1920" height="1080" alt="2026-10-29_09 14 13" src="https://github.com/user-attachments/assets/947583a3-6789-4eeb-9688-cf18d65d0d6c" /><br>
<img width="1920" height="1080" alt="Снимок экрана 2026-10-29 112327quality" src="https://github.com/user-attachments/assets/9c4e7548-1fbd-4f70-b180-cf9180adfa61" /><br>
If you lower the settings to 4 chunks and set everything to minimum, you can reach 12 FPS (it looks like the integrated HD 520 graphics heavily struggle with the Quality shader even with graphics lowered at 1080p). And by reducing the render scale to 50% (from 1920x1080 down to 960x540), it becomes 21 FPS.
<br>
### 💡 Conclusion:
In version 2.0.0 (where this benchmark was conducted), across all three scenarios, the VRAM usage stubbornly stayed fixed at 1.3 GB and refused to grow. In contrast, in version 1.5.0, VRAM usage exceeded 2.2 GB, which used to cause driver crashes.

---

# Screenshots:
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

---

🛠️ Development Status:
This project is experimental and under active development.
Features, performance, and compatibility may change between versions.
Bug reports and reproducible performance tests are welcome.

👥 Credits / Authors:
* Claude Sonnet 5.5 (Anthropic AI) — WebGPU/WGSL code refactoring and optimization.
* Me — jahzmo99: Concept, prompting, testing, debugging, and performance evaluation.

📄 Disclaimer
This is an independent community project and is not an official Horizon release. Horizon and its associated trademarks belong to their respective owners.
