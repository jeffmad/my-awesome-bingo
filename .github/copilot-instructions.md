# Bingo Mixer — AI Agent Guidelines

- [ ] `npm run lint`
- [ ] `npm run build`
- [ ] `npm run test`

## Quick Setup
- `npm install`
- `npm run dev`
- `npm run lint`
- `npm run test`

## What to edit
- UI lives in `src/components/`
- Game state lives in `src/hooks/useBingoGame.ts`
- Pure game logic lives in `src/utils/bingoLogic.ts`
- Types are in `src/types/index.ts`

## Project patterns
- React 19 functional components + hooks
- Tailwind CSS v4 via `@tailwindcss/vite`
- Immutable board updates: no in-place mutation
- Free space is center square index 12 and cannot be toggled

## Important conventions
- `gameState` is `'start' | 'playing' | 'bingo'`
- `winningSquareIds` is a `Set<number>`
- `onSquareClick` and `handleSquareClick` are the interaction flow
- Validate persisted localStorage state before applying

## Build/test commands
- `npm run dev`
- `npm run build`
- `npm run lint`
- `npm run test`

## Notes
- `vite.config.ts` sets `base` using `VITE_REPO_NAME`
- This is a browser-only app with no backend auth
