# UE5.8 Advanced Biplanar Shading Pipeline 🚀

An production-ready, highly optimized 2-layer biplanar master material for Unreal Engine 5.8 designed for massive environment assets, heavy geometry, and procedural landscapes. 

## 📌 Features & Optimization Details

* **Massive Texture Fetch Reduction:** Traditional triplanar mapping for a 2-layer setup requires up to **21 texture fetches**. This custom biplanar implementation cuts that number down to just **11 fetches**, drastically reducing GPU texture streaming bottlenecks.
* **Substrate & Legacy PBR Hybrid System:** Features a built-in toggle allowing seamless switching between the legacy Unreal Engine PBR shading model and the new next-gen **Substrate** framework within a single master architecture.
* **RVT (Runtime Virtual Texture) Support:** Fully integrated with Runtime Virtual Textures (RVT) for seamless landscape blending, allowing huge cliffs and procedural meshes to bake their material data directly into the world terrain.
* **Manual Normal Reconstruction:** Optimizes channel packing by storing normal components mathematically and reconstructing the Z vector in the pixel shader via `DeriveNormalZ`, saving valuable texture samplers.

## 🗺️ Future Roadmap
* [ ] **Anti-Tiling System:** Implementation of procedural break-ups (like stochastic sampling or macro-noise variations) to eliminate visible texture repetition on massive scales.

## 📁 How to Use
1. Download the `Biplanar_Shader_Release.zip` file from this repository.
2. Extract the content folder into your Unreal Engine 5.8 project directory.
3. Open `M_Master_Biplanar` to inspect the architecture, functions, and material parameters.
