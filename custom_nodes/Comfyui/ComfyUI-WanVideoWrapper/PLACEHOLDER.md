# ComfyUI-WanVideoWrapper Nodes

This directory should contain the ComfyUI-WanVideoWrapper custom nodes for Genesis WanVideo functionality.

**Official Repository**: https://github.com/kijai/ComfyUI-WanVideoWrapper
**Author**: Kijai
**Version**: 1.3.8+
**Stars**: 5.2k+

## Installation Instructions

### Method 1: Clone from Official Repository (Recommended)

```bash
cd "E:\chai fream\genesis\custom_nodes\Comfyui"
git clone https://github.com/kijai/ComfyUI-WanVideoWrapper.git
```

### Method 2: Install Dependencies

After cloning, install required packages:

```bash
cd ComfyUI-WanVideoWrapper
pip install -r requirements.txt
```

### Method 3: Download Release Package

Download the complete Genesis package from [Releases](https://github.com/eddyhhlure1Eddy/Genesis/releases) which includes all custom nodes pre-configured.

### Method 4: Download Models

Download WanVideo models from Hugging Face:
- https://huggingface.co/Kijai/WanVideo_comfy

## Required Nodes

The WanVideoWrapper package includes 124+ essential nodes for video generation:

### Core Video Generation Nodes
- `LoadWanVideoT5TextEncoder` - Load T5 text encoder for prompt encoding
- `WanVideoTextEncode` - Encode text prompts into embeddings
- `WanVideoModelLoader` - Load WanVideo diffusion models
- `WanVideoVAELoader` - Load VAE for video decoding
- `WanVideoEmptyEmbeds` - Create empty image embeddings
- `WanVideoSampler` - Main sampling/generation node
- `WanVideoDecode` - Decode latents to video frames

### Optimization Nodes
- `WanVideoLoraSelect` - Apply LoRA fine-tuning
- `WanVideoTorchCompileSettings` - Configure torch.compile optimization
- `WanVideoBlockSwap` - Memory optimization via block swapping

### Additional Features
- MultiTalk nodes - Audio-driven talking head generation
- MTV nodes - Motion transfer video
- SkyReels nodes - Sky and weather effects
- FlashVSR nodes - Video super-resolution
- UniAnimate nodes - Character animation
- And many more...

## Directory Structure

After installation, the structure should be:

```
ComfyUI-WanVideoWrapper/
├── __init__.py
├── wanvideo/
│   ├── modules/
│   │   ├── attention.py
│   │   ├── models.py
│   │   └── ...
│   ├── schedulers/
│   └── ...
├── multitalk/
├── MTV/
├── skyreels/
├── FlashVSR/
├── unianimate/
└── ... (more node categories)
```

## Compatibility

- **Genesis Core**: v0.1.0+
- **Python**: 3.13
- **PyTorch**: 2.0+
- **CUDA**: 12.8+
- **GPU**: NVIDIA RTX 30/40/50 series (Blackwell optimized)

## Features

### SageAttention3 Blackwell Support
Full support for RTX 5090 Blackwell architecture with FP4 quantization for maximum performance.

### Memory Optimization
Block swap and tiling support for efficient VRAM usage on consumer GPUs.

### Multi-Backend Attention
Supports multiple attention backends:
- SageAttention3 (Blackwell FP4)
- Flash Attention 2/3
- xFormers
- PyTorch SDPA

## Documentation

For detailed usage instructions, see:
- Genesis Documentation: `../../docs/`
- WanVideo Guide: `../../../old/README_WANVIDEO.md`
- Installation Guide: `../../../old/START_HERE.md`

---

**Note**: This is a placeholder file. Replace this directory with actual ComfyUI-WanVideoWrapper nodes to enable video generation functionality.

**Author**: eddy
**Date**: 2025-11-13
**Size**: This file is intentionally > 1KB to ensure proper Git tracking
