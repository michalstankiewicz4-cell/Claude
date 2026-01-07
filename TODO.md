# TODO List

> Planned features and improvements for Petrie Dish

---

## 🔥 Priority 1 - v5.1-C2 (Full GPU Migration)

**Target:** 2025-01-20

### Code Cleanup
- [ ] **Remove legacy CPU physics** (~500 lines)
  - [ ] Delete `updateParticles()` CPU function
  - [ ] Remove CPU collision detection
  - [ ] Clean up particle update loops
- [ ] **Audit codebase** for GPU migration completeness
  - [ ] Identify all CPU physics references
  - [ ] Document GPU equivalents
  - [ ] Create migration checklist

### GPU Optimization
- [ ] **Optimize compute shader dispatch**
  - [ ] Benchmark workgroup sizes (current: 256)
  - [ ] Test different buffer layouts
  - [ ] Profile GPU memory bandwidth
- [ ] **Improve buffer synchronization**
  - [ ] Minimize CPU-GPU transfers
  - [ ] Batch buffer updates
  - [ ] Implement dirty flag system
- [ ] **Shader optimization**
  - [ ] Review WGSL code for efficiency
  - [ ] Add shader compilation caching
  - [ ] Optimize uniform buffer updates

### Testing & Validation
- [ ] **Performance benchmarking**
  - [ ] CPU vs GPU comparison (1k, 10k, 100k particles)
  - [ ] Frame time profiling
  - [ ] Memory usage tracking
- [ ] **WebGL fallback testing**
  - [ ] Test all features with WebGL path
  - [ ] Fix rendering artifacts
  - [ ] Ensure feature parity

---

## 📌 Priority 2 - v5.2 (Advanced Features)

**Target:** 2025-02-15

### User Experience
- [ ] **Simulation presets**
  - [ ] "Chaos" mode
  - [ ] "Harmony" mode
  - [ ] "Solar system" simulation
  - [ ] Custom preset editor
- [ ] **Export/Import system**
  - [ ] Export configuration to JSON
  - [ ] Import saved states
  - [ ] Share preset URLs
- [ ] **Replay system**
  - [ ] Record simulation states
  - [ ] Playback controls
  - [ ] Export to video (WebCodecs)

### Visualization
- [ ] **Advanced statistics graphs**
  - [ ] Real-time energy plot
  - [ ] Particle distribution histogram
  - [ ] Interaction heatmap
- [ ] **Visual effects**
  - [ ] Particle trails (GPU-based)
  - [ ] Glow effects
  - [ ] Collision sparks

---

## 💡 Priority 3 - Future Ideas

### Performance
- [ ] **Multi-pass compute shaders**
  - [ ] Separate position update and collision
  - [ ] Parallel spatial hash construction
  - [ ] GPU-side culling
- [ ] **WebAssembly integration**
  - [ ] WASM for heavy CPU tasks
  - [ ] Benchmark vs pure JS

### Features
- [ ] **Advanced physics**
  - [ ] Gravity wells
  - [ ] Magnetic fields
  - [ ] Particle bonds
  - [ ] Quantum effects simulation
- [ ] **3D mode**
  - [ ] WebGPU 3D rendering
  - [ ] Camera controls
  - [ ] Z-axis physics
- [ ] **Machine learning**
  - [ ] Pattern recognition
  - [ ] Emergent behavior analysis
  - [ ] Auto-optimization

### UI/UX
- [ ] **Mobile support**
  - [ ] Touch controls
  - [ ] Responsive UI
  - [ ] Performance optimizations
- [ ] **Themes**
  - [ ] Dark/light mode
  - [ ] Custom color schemes
  - [ ] Accessibility options

---

## 🐛 Bug Fixes (Ongoing)

- [ ] Fix WebGL fallback artifacts
- [ ] Handle GPU device loss gracefully
- [ ] Improve error messages
- [ ] Add input validation
- [ ] Memory leak detection

---

## 📚 Documentation (Ongoing)

- [ ] **Code documentation**
  - [ ] JSDoc comments for all functions
  - [ ] Architecture diagrams
  - [ ] Performance profiling guide
- [ ] **User guide**
  - [ ] Getting started tutorial
  - [ ] Feature walkthrough
  - [ ] Troubleshooting guide
- [ ] **API documentation**
  - [ ] Particle system API
  - [ ] GPU compute API
  - [ ] UI component library

---

## 🔄 Refactoring (Continuous)

- [ ] **Code organization**
  - [x] Split monolithic file into modules
  - [ ] Improve module boundaries
  - [ ] Reduce coupling
- [ ] **Type safety**
  - [ ] Consider TypeScript migration
  - [ ] Add JSDoc types
  - [ ] Runtime type checking
- [ ] **Testing**
  - [ ] Unit tests for core functions
  - [ ] Integration tests
  - [ ] Performance regression tests

---

**Legend:**
- 🔥 Critical / High Priority
- 📌 Important / Medium Priority
- 💡 Nice to have / Low Priority
- 🐛 Bug fix
- 📚 Documentation
- 🔄 Refactoring

**Last Updated:** 2025-01-07
