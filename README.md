# Planning Grosbill — Application Windows (.exe)

Projet Electron prêt à compiler en **.exe portable** (un seul fichier, sans installation).

## Prérequis (une seule fois)
Installer **Node.js LTS** : https://nodejs.org (prends la version "LTS").

## Compilation
Ouvre un terminal (PowerShell) dans ce dossier, puis :

```
npm install
npm run dist
```

Le fichier final apparaît ici :

```
release\Planning-Grosbill-portable.exe
```

C'est lui que tu copies/lances où tu veux. Aucune installation requise.

## Tester sans compiler
```
npm install
npm start
```

## Notes
- Les plannings (localStorage / IndexedDB) sont conservés entre les lancements.
- L'export JSON et les affiches/PDF (fenêtres pop-up) fonctionnent normalement.
- Icône : remplace `build\icon.ico` par ton logo (256×256) avant `npm run dist` si tu veux personnaliser.
- L'.exe portable ne peut être compilé que **sous Windows** (ou via une CI Windows). Sur Linux/Mac, utilise une machine Windows pour l'étape `npm run dist`.
