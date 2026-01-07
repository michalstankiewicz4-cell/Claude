# 🎯 GitHub Projects Setup - Krok po kroku

## 📋 KROK 1: Stwórz Issues (5 minut)

Idź na: https://github.com/michalstankiewicz4-cell/Claude/issues/new

Skopiuj i wklej każdy z poniższych (6 issues):

---

### Issue #1: Remove legacy CPU physics code

**Title:**
```
[v5.1-C2] Remove legacy CPU physics code
```

**Description:**
```markdown
**Priority:** 🔥 High  
**Milestone:** v5.1-C2 (Full GPU Migration)

### Tasks:
- [ ] Delete `updateParticles()` CPU function
- [ ] Remove CPU collision detection  
- [ ] Clean up particle update loops
- [ ] Audit codebase for remaining CPU physics references

### Estimated Impact:
- ~500 lines removed
- Cleaner codebase
- Easier maintenance

### Related:
See `KNOWN_ISSUES.md` - Legacy Code Pollution
```

**Labels:** `enhancement`, `v5.1-C2`, `priority-high`

---

### Issue #2: Optimize GPU compute shader dispatch

**Title:**
```
[v5.1-C2] Optimize GPU compute shader dispatch
```

**Description:**
```markdown
**Priority:** 🔥 High  
**Milestone:** v5.1-C2 (Full GPU Migration)

### Tasks:
- [ ] Benchmark workgroup sizes (current: 256)
- [ ] Test different buffer layouts
- [ ] Profile GPU memory bandwidth
- [ ] Document optimal configurations

### Goal:
Maximum performance for 100k particles
```

**Labels:** `performance`, `v5.1-C2`, `gpu`

---

### Issue #3: Improve buffer synchronization

**Title:**
```
[v5.1-C2] Improve buffer synchronization
```

**Description:**
```markdown
**Priority:** 🔥 High  
**Milestone:** v5.1-C2 (Full GPU Migration)

### Tasks:
- [ ] Minimize CPU-GPU transfers
- [ ] Batch buffer updates
- [ ] Implement dirty flag system
- [ ] Optimize data flow

### Goal:
Reduce CPU↔GPU bottleneck
```

**Labels:** `performance`, `v5.1-C2`, `gpu`

---

### Issue #4: Performance benchmarking suite

**Title:**
```
[v5.1-C2] Performance benchmarking suite
```

**Description:**
```markdown
**Priority:** 🔥 High  
**Milestone:** v5.1-C2 (Full GPU Migration)

### Tasks:
- [ ] CPU vs GPU comparison (1k, 10k, 100k particles)
- [ ] Frame time profiling
- [ ] Memory usage tracking
- [ ] Generate performance report

### Metrics to track:
- Physics time (ms)
- Render time (ms)
- Memory (MB)
- FPS
```

**Labels:** `testing`, `v5.1-C2`, `documentation`

---

### Issue #5: Simulation presets system

**Title:**
```
[v5.2] Simulation presets system
```

**Description:**
```markdown
**Priority:** 📌 Medium  
**Milestone:** v5.2 (Advanced Features)

### Presets to implement:
- [ ] "Chaos" mode
- [ ] "Harmony" mode
- [ ] "Solar system" simulation
- [ ] Custom preset editor

### Features:
- Save/load presets
- Share via URL
- Preset gallery
```

**Labels:** `feature`, `v5.2`, `ux`

---

### Issue #6: Export/Import configuration system

**Title:**
```
[v5.2] Export/Import configuration system
```

**Description:**
```markdown
**Priority:** 📌 Medium  
**Milestone:** v5.2 (Advanced Features)

### Tasks:
- [ ] Export configuration to JSON
- [ ] Import saved states
- [ ] Share preset URLs
- [ ] Validate imported data

### Use cases:
- Save interesting configurations
- Share with others
- Backup before experiments
```

**Labels:** `feature`, `v5.2`, `ux`

---

## 📊 KROK 2: Stwórz Project Board (2 minuty)

1. Idź na: https://github.com/michalstankiewicz4-cell/Claude/projects

2. Kliknij **"New project"**

3. Wybierz **"Board"** template

4. Nazwij: **"Petrie Dish v5.1-C2 Development"**

5. **Dodaj kolumny** (Board ma domyślnie: Todo, In Progress, Done)
   - Zostaw je jak są!

6. **Dodaj Issues do Board:**
   - Kliknij **"+ Add item"** w kolumnie **"Todo"**
   - Wybierz Issue #1, #2, #3, #4
   - (Issue #5 i #6 zostaw w Issues - to v5.2)

7. **Opcjonalnie - dodaj Milestone:**
   - Settings → **Milestones** → **New milestone**
   - Nazwa: `v5.1-C2 Full GPU Migration`
   - Due date: `2025-01-20`
   - Przypisz Issues #1-4 do tego Milestone

---

## 🎯 KROK 3: Użytkowanie (codziennie)

### Jak pracować z Board:

1. **Zacznij task:**
   - Przeciągnij kartę z **"Todo"** → **"In Progress"**
   - Przypisz do siebie (Assign to yourself)

2. **Podczas pracy:**
   - Commituj z numerem Issue: `git commit -m "feat: optimize GPU dispatch #2"`
   - GitHub automatycznie linkuje commit do Issue

3. **Kończąc task:**
   - Zaznacz checkboxy w opisie Issue
   - Przeciągnij do **"Done"**
   - Lub zamknij Issue (Close) - automatycznie przejdzie do Done

---

## 📈 BONUS: Roadmap View

1. W Project Board kliknij **"Views"** (u góry)
2. Kliknij **"+ New view"**
3. Wybierz **"Roadmap"**
4. Nazwij: "Timeline"
5. Ustaw daty dla każdego Issue (Start/End date)

Teraz masz timeline view! 🎉

---

## ✅ REZULTAT:

Po wykonaniu tych kroków będziesz miał:

```
📋 Petrie Dish v5.1-C2 Development
┌─────────────────┬──────────────────┬─────────────┐
│   📝 TODO       │  🚧 IN PROGRESS  │  ✅ DONE   │
├─────────────────┼──────────────────┼─────────────┤
│ #1 Remove CPU   │                  │             │
│ #2 Optimize GPU │                  │             │
│ #3 Buffer sync  │                  │             │
│ #4 Benchmarking │                  │             │
└─────────────────┴──────────────────┴─────────────┘
```

---

## 💡 PRO TIPS:

1. **Linki w commitach:** `#1`, `#2` etc. → automatycznie linkują do Issues
2. **Close przez commit:** `git commit -m "fix: remove CPU code, closes #1"` → zamyka Issue
3. **Checkboxes:** `- [ ]` w Issues → GitHub tworzy progress bar
4. **Labels:** Używaj kolorów (czerwony = high priority, zielony = feature)
5. **Milestones:** Grupuj Issues do wersji (v5.1, v5.2)

---

**Estimated time:** 10 minut total
**Difficulty:** Easy (click, copy-paste, drag-drop)
**Benefit:** 🔥 Profesjonalne zarządzanie projektem!

---

**Powodzenia!** 🚀

Jeśli coś nie działa - daj znać! 😊
