# ChessGame

A simple React + Vite chess app powered by chess.js.

## Getting started

1. Install dependencies
   - npm install

2. Run the dev server
   - npm run dev
   - Vite may start on `http://localhost:3000/` by default. If you need `5173`:
     - npm run dev -- --port 5173 --strictPort true

3. Build for production
   - npm run build

## Undo Move fix

The "Undo Move" button now correctly reverts both the chess engine state and the UI.

Changes made in `src/App.tsx` upon a successful undo:
- Clear selection and valid moves
- Close any active promotion modal and pending move
- Reset last-move highlight
- Refresh the `Chess` instance so React re-renders from the reverted FEN

This ensures the board, status, and move history remain in sync after undoing.

## Troubleshooting

- Vite shows port 3000 instead of 5173
  - This is normal; recent Vite versions can choose `3000`. You can force `5173` with:
    - npm run dev -- --port 5173 --strictPort true

- Error: Cannot find module `log/lib/abstract-writer` (from vite-configs-viewer)
  - This is from an optional dev dependency used by some Vite tooling. If it blocks local dev on a specific port, either run on the default port (works out-of-the-box), or remove the package if not needed.

## License

MIT
