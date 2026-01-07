# Petrie Dish Distribution Files

This directory contains compiled single-file versions of Petrie Dish.

## Current Version

**v5.0-C1** - `petrie-dish-v5.0-C1.html`
- WebGPU Zero-Copy Rendering
- GPU Buffer Manager
- Text measurement cache optimization
- **Status:** Current stable release

## File Naming Convention

```
Format: petrie-dish-vMAJOR.MINOR-PHASE[-SUFFIX].html

Examples:
petrie-dish-v5.0-C1.html          # Stable release
petrie-dish-v5.1-C2-dev.html      # Development version
petrie-dish-v5.1-C2-beta.html     # Beta testing
petrie-dish-v5.1-C2.html          # Next stable
```

## Usage

1. Download the HTML file
2. Open in browser with WebGPU support (Chrome 113+, Edge 113+)
3. No server required - works offline!

## Build Process

Production builds are created by concatenating all source modules:

```bash
node build/concat-modules.js
# Output: dist/petrie-dish-v5.x.html
```

## Version History

| Version | Date | File Size | Major Features |
|---------|------|-----------|----------------|
| v5.0-C1 | 2025-01-07 | 197KB | WebGPU compute, zero-copy rendering |

## Notes

- All versions are backward compatible with WebGL fallback
- Original source modules available in `/src/`
- For development, use modular version in root directory

---

**⚠️ Note:** To add the actual v5.0-C1 file, copy from uploads:
```
File location: /mnt/user-data/uploads/petrie-dish-v5_0-C1-FIXED2.html
Target: C:\Users\micha\source\repos\Akcelerator\dist\petrie-dish-v5.0-C1.html
```

This will be done in the next step after committing the project structure.
