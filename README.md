# AI & Stadsbyggnad — Interaktiv showcase

Interaktiv före/efter-visualisering som visar hur AI kan användas inom stadsplanering.

## Snabbstart

1. Öppna `index.html` i webbläsaren — klart!

## Publicera på GitHub Pages

```bash
# 1. Skapa repo på github.com (t.ex. "ai-stadsbyggnad")

# 2. I terminalen:
cd ai-stadsbyggnad
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/DITT-ANVÄNDARNAMN/ai-stadsbyggnad.git
git push -u origin main

# 3. På github.com → Settings → Pages → Source: "main" → / (root) → Save

# 4. Vänta 1-2 minuter, sidan finns på:
#    https://DITT-ANVÄNDARNAMN.github.io/ai-stadsbyggnad/
```

## Lägg till nya platser

### 1. Lägg till bilder

Skapa en mapp under `platser/` med ett original + visionsbilder:

```
platser/
  ny-plats/
    original.jpg        ← Originalfotot
    scenario1.jpg        ← AI-vision 1
    scenario2.jpg        ← AI-vision 2
    scenario3.jpg        ← AI-vision 3
    scenario4.jpg        ← AI-vision 4
```

### 2. Uppdatera konfigurationen

Öppna `index.html` och hitta `const LOCATIONS = [...]` i JavaScript-sektionen. Lägg till:

```javascript
{
  id: "ny-plats",
  title: "Platsens namn",
  subtitle: "Kort beskrivning",
  folder: "platser/ny-plats",
  ready: true,                      // false = "Kommer snart"
  scenarios: [
    { id: "scenario1", label: "Namn", desc: "Beskrivning", icon: "🏗️" },
    { id: "scenario2", label: "Namn", desc: "Beskrivning", icon: "🌱" },
    { id: "scenario3", label: "Namn", desc: "Beskrivning", icon: "🏊" },
    { id: "scenario4", label: "Namn", desc: "Beskrivning", icon: "🏠" },
  ],
},
```

**OBS:** `id` i scenarios måste matcha filnamnet (utan .jpg).

### 3. Publicera

```bash
git add .
git commit -m "Lade till ny plats"
git push
```

GitHub Pages uppdateras automatiskt inom 1-2 minuter.

## Bildstorlekar

Rekommenderade storlekar:
- **Porträttbilder:** 900×1200 px (3:4)
- **Landskapsbilder:** 1200×900 px (4:3)
- **Format:** JPEG, kvalitet 80-85%
- **Max filstorlek:** ~400 KB per bild

## Mässtips

- Tryck **Helskärm**-knappen för presentation
- Funkar på iPad/pekskärm — dra med fingret
- Funkar offline om alla bilder är nedladdade
