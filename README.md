# RTV — Ray Tracing Visual

**RTV (Ray Tracing Visual)** is a modified shader build based on the ray-tracing tutorial and code by **timetravelbeard**.

These shaders are intended for visual enhancements, such as ray tracing in the Bedrock Edition; however, opinions on them can vary from person to person.

The main focus is voxel-based ray tracing, global illumination, and light bounce. It also includes ray-traced reflections, configurable shadows, temporal accumulation, and denoising to help keep the image cleaner over time.

RTV comes with several quality presets and a range of settings for lighting, water, glass, shadows, and color. You can adjust the balance between image quality and performance to suit your setup.

## Features

- **Ray-Traced Global Illumination** — Adds indirect lighting and light bounce throughout the scene.
- **Voxel-Based Ray Tracing** — Traces rays through a voxelized scene for lighting and reflection effects.
- **Ray-Traced Reflections** — Reflections are traced against scene data, with adjustable settings for supported surfaces.
- **Ray-Traced Shadows** — Configurable ray-traced shadows, alongside shadow map options.
- **Temporal Accumulation** — Reuses previous frames to help reduce persistent noise while maintaining detail.
- **Spatial Denoising** — Uses edge-aware filtering to reduce visible noise while taking surface normals and depth into account.
- **Animated Water** — Includes animated surface ripples, adjustable reflections, and underwater depth absorption.
- **Glass Refraction** — Adjustable refraction and distortion for glass surfaces.
- **Day and Night Lighting** — Night illumination follows Minecraft's world time, with a separate control for moonlight and sky bounce.
- **Color Controls** — Adjust saturation, vibrance, exposure, and tone mapping.
- **Quality Presets** — Choose between Low, Medium, High, and Extreme.

## Driver aceleration 

Driver acceleration is a unique feature that reduces screen resolution to achieve a higher frame rate (FPS); you can enable it by following the guide below:

https://github.com/user-attachments/assets/a429e3b2-325d-4f03-9d4e-5bf4fe5f05a2

This feature utilizes OpenGL techniques within the Minecraft system to offload shader rendering to the GPU, preventing the exhaustion of system resources—similar to frame generation.
However, there are limits to how small or large you can set the values, as shown below.:

1. **from 1 : is off or no upscaling and image degradation**
2. **from 2 to 4 : is upscaling and image reduction, here the image is a little blurry and some glitches on Global Illumination**
3. **from 4 - 11: is the biggest decrease, the image has more artifacts and is blurry but gets higher fps**
4. **from 11 - 100 : not recommended, the image is very blurry and not playable and the driver is destroyed for rendering the scene**

For me, if you use 2-4, it's the best and there aren't many artifacts.

  

## Version & Requirements

- **Shader version:** 0.3
- **Shader loader:** Iris Shaders
- **Graphics API:** OpenGL 4.3 or newer
- **Shader language:** GLSL 4.30 compatibility
- **Required Iris feature:** Custom Images
- **Shaders can only be used from version 1.21.8 up to 26.2.**




## Performance

Ray tracing can be demanding, especially at higher settings. Start with the Low or Medium preset if performance is an issue, then increase the quality as needed. High and Extreme use more ray-tracing steps and can have a greater performance cost.

Actual performance will depend on your GPU, render resolution, Minecraft setup, and selected settings.

## Credits & License

RTV is a modified build based on the ray-tracing tutorial and code by **timetravelbeard**.

The original project credits and MIT license notices are retained. This is a modified version, not a claim of ownership over the original shader code.

**License: MIT.** Please keep `LICENSE.txt` and the original copyright and license notices intact when redistributing this shader or substantial portions of its code.

Original creator: [timetravelbeard on YouTube](https://youtube.com/@timetravelbeard3588)

Have fun exploring and tweaking RTV!
