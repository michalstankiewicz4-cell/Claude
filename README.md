# 🧫 Petrie Dish - WebGPU Physics Simulator

> High-performance particle physics simulation with GPU-accelerated compute and real-time interaction matrix

[![Version](https://img.shields.io/badge/version-5.0--C1-blue.svg)](CHANGELOG.md)
[![WebGPU](https://img.shields.io/badge/WebGPU-enabled-green.svg)](https://gpuweb.github.io/gpuweb/)
[![License](https://img.shields.io/badge/license-MIT-orange.svg)](LICENSE)

## 📋 Overview

Petrie Dish is an advanced particle physics simulator featuring:
- **WebGPU compute shaders** for GPU-accelerated physics
- **16-color interaction matrix** with customizable attraction/repulsion
- **Real-time UI system** with draggable windows and live statistics
- **Zero-copy rendering** for optimal performance
- **Spatial hash optimization** for efficient collision detection

## 🚀 Current Version

**v5.0-C1 (Phase C1)** - WebGPU Zero-Copy Rendering
- ✅ GPU Buffer Manager implemented
- ✅ Compute shaders for physics calculations
- ✅ Text measurement cache (2-5× UI speedup)
- ⚠️ Legacy CPU code still present (removal planned for C2)

## 📁 Project Structure

```
Akcelerator/
├── src/
│   ├── core/           # Core initialization, settings, constants
│   ├── gpu/            # WebGPU: buffers, shaders, compute
│   ├── ui/             # UI system: windows, taskbar, renderer
│   ├── physics/        # Particle physics, spatial hash
│   ├── rendering/      # WebGL fallback, camera
│   └── utils/          # Helper functions, caches
├── dist/               # Compiled single-file versions
├── docs/               # Documentation
├── README.md           # This file
├── CHANGELOG.md        # Version history
├── TODO.md             # Planned features
└── KNOWN_ISSUES.md     # Bug tracker
```

## 🎯 Getting Started

### Requirements
- Modern browser with WebGPU support (Chrome 113+, Edge 113+)
- GPU with compute shader support

### Quick Start
```bash
# Open the single-file version
open dist/petrie-dish-v5.0-C1.html

# Or serve locally for development
python -m http.server 8000
# Navigate to http://localhost:8000
```

## 🔧 Development

### Version Naming Convention
```
Format: vMAJOR.MINOR-PHASE[-SUFFIX]

Examples:
v5.0-C1          # Current stable
v5.1-C2-dev      # Development version
v5.1-C2          # Next stable release
v6.0-D1          # Major architecture change
```

### Development Workflow
1. Create feature branch: `git checkout -b feature/gpu-migration`
2. Work on modular source in `src/`
3. Test thoroughly
4. Build single-file version to `dist/`
5. Update `CHANGELOG.md`
6. Merge to main

## 📊 Performance

- **Particle limit**: 100,000 particles
- **Physics**: GPU compute shaders
- **Rendering**: WebGPU zero-copy (fallback: WebGL)
- **UI**: Cached text measurements, optimized rendering

## 🛠️ Tech Stack

- **WebGPU** - GPU compute & rendering
- **WebGL 2.0** - Fallback rendering
- **Canvas 2D** - UI overlay
- **Pure JavaScript** - No frameworks

## 📖 Documentation

- [Changelog](CHANGELOG.md) - Version history
- [TODO](TODO.md) - Planned features
- [Known Issues](KNOWN_ISSUES.md) - Bug tracker
- [Architecture](docs/ARCHITECTURE.md) - System design (TODO)

## 🤝 Contributing

This is a personal research project. Suggestions welcome via issues!

## 📜 License

MIT License - See LICENSE file for details

## 🎓 Credits

Created by Michał Stankiewicz (@michalstankiewicz4-cell)
Based on particle physics research and WebGPU exploration

---

**Last Updated:** 2025-01-07  
**Status:** Active Development (Phase C2 in progress)
