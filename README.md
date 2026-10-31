# VanillRust-WGPU Shaders ([Horizon Launcher](https://playhorizon.dev/) Minecraft Rust Edition)
The native WGSL shader pack built for [Horizon github](https://github.com/horizon-rust/horizon) Minecraft Java rewrite in Rust [@ludovic111](https://github.com/ludovic111).<br>
<img width="1600" height="540" alt="VanillRust" src="https://github.com/user-attachments/assets/bbc478d4-06db-4558-b28d-1d6ada7ef84a" />


⚠️ This is an early. It may cause:
* Varying stability
* Bugs

## ⚙️ Technical Approach & Horizon API Limitations, Story of Project and About Me

#### About the Shader Implementation
The current graphics API in Horizon doesn't have a dedicated stage for computing shadows and is significantly limited when it comes to shader support. <br>
To overcome this, **VanillRust-WGPU** utilizes **Screen-Space Ray-Marched Shadows** as a software ray marching approach to detect occlusions and blockages. 
* *Note:* This acts like software ray tracing for obstacle searching, but it is **not full hardware Ray Tracing**. If you don't see a shadow, it simply means the screen-space camera is not currently capturing the object blocking the light.<br>

Due to the incomplete API, almost every feature in this pack had to be implemented through clever mathematical workarounds and custom logic.

---

#### ⚠️ Current Horizon API Limitations
In the current version of the Horizon graphics engine, it is physically impossible to implement fully feature-complete shaders and traditional shadow maps because the engine does not yet pass full world geometry data to the pipeline.

**Key Technical Constraints:**
* **No Shadow Pass:** There is no dedicated render pipeline or framebuffer pass to generate sun/moon shadow maps (Shadow Mapping).
* **Temporary Shader Limitations:** Native shader support on Horizon was previously cut/disabled due to critical technical stability issues, making current shader development extremely constrained.
* **No G-Buffer:** The engine outputs a flat visual stream without exporting surface properties, block normals, scene depth maps, or material IDs.
* **No Denoiser:** Software ray marching attempts at this stage introduce visible grain/noise because there is no spatial or temporal denoiser implementation in the pipeline.
* **Early-Stage API:** Advanced graphics pipelines, shader pass hooks, and lighting/weather vector passes are planned for future engine releases, but are not available yet.

#### Story and Me:
I downloaded Horizon, played for 2 hours, and wanted to see what kind of FPS I could get with shaders on my potato laptop. But Horizon didn't have shaders, so I decided to create them myself (reaching version 2.0.0 in just 6 hours of coding from zero). I had zero prior experience with WebGPU or WGPU, and I didn't even know how to code. From there, one thing led to another, and I published this pack on GitHub.

A bit about me: I'm Maksym, 18 years old. My potato laptop severely limits what I can run, but I love working on interesting projects across completely different niches (basically, just a passionate tech enthusiast).<br>

---
🚀 Performance Presets:
* **Lite**: For integrated graphics. Reduced effect quality for better performance.
* **Quality**: Higher effect quality for discrete GPUs (RTX/RX/GTX) with maximized volumetric steps and more rendering steps.
(Actual performance depends on resolution, render scale, game settings, drivers, and hardware).


### 📦 How to Install
1. Download the desired `.hshader` latest version file from the [Releases page](https://github.com/jahzmo99/VanillRust-WGPU-Horizon-/releases) and in Horizon, open Options → Horizon Settings → Shader Packs → Open Pack Folder and place it Or in directory for example: `/horizon-launcher/versions/v?.?.??/shaderpacks`
2. Enable VanillRust-WGPU in game via Horizon Settings > Shader Packs.
Compatibility note: This pack targets a specific version of Horizon's shader implementation. Check compatibility before using it with newer builds.

---

# Screenshots in Quality:
<table>
  <tr>
    <td><img width="540" src="https://github.com/user-attachments/assets/42ddbb22-393f-46a8-bf90-a1125fa17cbc" /></td>
    <td><img width="540" src="https://github.com/user-attachments/assets/ffe4d856-d1c7-4024-a8f7-0413c31ff983" /></td>
  </tr>
  <tr>
    <td><img width="540" alt="2026-10-29_15 25 55" src="https://github.com/user-attachments/assets/7e470c54-8681-488a-9c2d-3a1db00be554" /></td>
    <td><img width="540" alt="2026-10-29_15 27 49" src="https://github.com/user-attachments/assets/c8240fb0-892b-4cf0-809c-169bf206abc8" /></td>
  </tr>
  <tr>
    <td><img width="540" alt="2026-10-29_19 09 04" src="https://github.com/user-attachments/assets/d497218b-fb6c-4ab0-a9c7-62cc72bf5a5c" /></td>
    <td><img width="540" alt="2026-10-29_18 39 05" src="https://github.com/user-attachments/assets/527eaf63-fd25-4ca6-bc8c-8ee03449a9ff" /></td>
  </tr>
  <tr>
    <td><img width="540" alt="2026-10-29_18 49 56" src="https://github.com/user-attachments/assets/cf38efeb-b5d8-4627-bca8-0a085cdd0596" /></td>
    <td><img width="540" alt="2026-10-29_16 05 39" src="https://github.com/user-attachments/assets/0973469c-da42-4257-bae5-5a5d1d781d92" /></td>
  </tr>
  <tr>
    <td><img width="540" alt="2026-10-29_18 49 34" src="https://github.com/user-attachments/assets/acef9e23-892a-4c5d-b4a9-aced545c1dcc" /></td>
    <td><img width="540" alt="2026-10-29_15 03 08" src="https://github.com/user-attachments/assets/bce1f61e-6c46-4262-a6df-1844faa05228" /></td>
  </tr>
</table>


---

### 📸 Settings & Hardware Benchmark And Gameplay (My low-end laptop Intel Core i5-6200U, Intel HD Graphics 520, 8GB RAM DDR3-2133Mhz at Single-Channel)👇
`Medium Minecraft Settings (12 Chunks, Simulation: 5 Chunks, VSync: OFF, Fullscreen 1080p, Biome Blend: OFF, Smooth Lighting: ON, Clouds: OFF, Particles: Minimal, Mipmap Levels: 4, Entity Shadows: ON, Entity Distance: 50%, See-Through Leaves: ON, Weather Effect Radius: 3 Blocks, LOD Distance: OFF, Far Detail: FULL, Cave Culling: ON, Entity Culling: OFF, Chunk Updates: 2 per frame, Sky: ON, Fog: OFF, Weather: ON, Resolution Scale: 100%, Anti-Aliasing: OFF, Graphics API: Vulkan)`<br>
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

# 📊 Hardware Benchmark (Tested in Version 2.0.0 VanillRust, You can get up to 2x FPS on Dual-Channel RAM on same HD520):
>Using the exact same settings mentioned above without changes. These are medium settings that balance visual quality, suitable for decent PCs rather than a potato like mine. In my case, using a potato, I test 3 modes as shown in the photos below, while the description underneath provides details without screenshots using low settings. I record the values always in the exact same spot and in the same world where weather switching is disabled and time is frozen. A command teleports me precisely to the same coordinates and aims the crosshair at the exact same point. I wouldn't call this the easiest scene, nor would I call it the hardest, because the FPS I recorded can drop or rise if I move away from this testing location. This is closer to an average and stable scene

## Without Shaders (My laptop already struggles with medium settings: 42 FPS and 24 ms, CPU at 21%, and HD 520 at 98% load):<br>
<img width="1920" height="1080" alt="2026-10-29_08 51 48" src="https://github.com/user-attachments/assets/1cdea281-0899-40d9-a7da-041c54999eaa" /><br>
<img width="1920" height="1080" alt="Снимок экрана 2026-10-29 105452" src="https://github.com/user-attachments/assets/1d20ff0e-920f-4fe9-9ced-49b281cd64c5" /><br>
If lower the settings to 4 chunks and set everything to minimum, can reach 117-120 FPS (without reducing the resolution). And by reducing the render scale to 50% (from 1920x1080 down to 960x540), it jumps to 198-202 FPS.


## VanillRust-WGPU *Lite* Active (dropped to 23 FPS and 45.5 ms, but the CPU load decreased by 3% — CPU at 18% down from 21%, and HD 520 at 99%):<br>
<img width="1920" height="1080" alt="2026-10-29_08 55 48lite" src="https://github.com/user-attachments/assets/65039a67-acc2-4057-9601-25f693839c33" /><br>
<img width="1920" height="1080" alt="Снимок экрана 2026-10-29 110912lite" src="https://github.com/user-attachments/assets/4371b08c-d8af-4f50-a1d0-2266842569de" /><br>
If lower the settings to 4 chunks and set everything to minimum, can reach 42 FPS (without reducing the resolution). And by reducing the render scale to 50% (from 1920x1080 down to 960x540), it goes up to 72 FPS.

## VanillRust-WGPU *Quality* Active (absolute torture for the HD 520 at 10 FPS and 102.5 ms, while the CPU unloaded by another 1% and is sitting at 17% load, while the HD 520 is at 99%):<br>
<img width="1920" height="1080" alt="2026-10-29_09 14 13" src="https://github.com/user-attachments/assets/947583a3-6789-4eeb-9688-cf18d65d0d6c" /><br>
<img width="1920" height="1080" alt="Снимок экрана 2026-10-29 112327quality" src="https://github.com/user-attachments/assets/9c4e7548-1fbd-4f70-b180-cf9180adfa61" /><br>
If lower the settings to 4 chunks and set everything to minimum, can reach 12 FPS (it looks like the integrated HD 520 graphics heavily struggle with the Quality shader even with graphics lowered at 1080p). And by reducing the render scale to 50% (from 1920x1080 down to 960x540), it becomes 21 FPS.
<br>
### 💡 Conclusion:
In version 2.0.0 (where this benchmark was conducted), across all three scenarios, the VRAM usage stubbornly stayed fixed at 1.3 GB and refused to grow. In contrast, in version 1.5.0, VRAM usage exceeded 2.2 GB, which used to cause driver crashes.

---

🛠️ Development Status:
This project is experimental and under active development.
Features, performance, and compatibility may change between versions.
Bug reports and reproducible performance tests are welcome.

👥 Credits / Authors:
* Claude Sonnet 5.5 (Anthropic AI) — WebGPU/WGSL code refactoring and optimization.
* Me — jahzmo99: Concept, prompting, testing, debugging, and performance evaluation.

📄 Disclaimer and Licence:<br>
This is an independent community project and is not an official Horizon release. Horizon and its associated trademarks belong to their respective owners. Licensed under **MIT**, Not an official Minecraft product, no Minecraft assets are included!
