✅ Test Task: Investigate and Fix "Undo Move" Button Functionality

🔍 Issue Summary

The "Undo Move" button in the ChessFi app is currently not working as expected. Clicking the button does not reverse the last move on the chessboard or update the game state accordingly.

🎯 Task Objective

Ensure the "Undo Move" button properly reverts the most recent move in a valid game session, updates the board UI, and maintains sync with the underlying chess engine.

📋 Acceptance Criteria

 - Clicking "Undo Move" removes the last move made on the board.
 - The chess state is reverted.
 - The UI updates correctly to reflect the new board position.
 - The move history (if displayed) is updated accordingly.
 - The button is disabled when no moves have been made.
 - Works consistently for both white and black players.

⚙️ Technical Details

 - Frontend Framework: React.js
 - Chess Logic: chess.js (or similar)
 - UI Styling: Tailwind CSS
 - Game State: Likely managed via React useState or global context

🧪 Test Steps

 - Start a new game as a player
 - Make a valid move (e.g., e4)
 - Click the "Undo Move" button

Observe:

 - Board state should revert to the position before the move
 - Internal chess state should reflect the reverted move
 - Repeat to ensure multiple undos work
 - Try undoing when no moves exist — button should be disabled or no-op

🧩 Bonus (Optional)

 - Animate the undo move for better UX
 - Add a confirmation prompt (if desired)
 - Disable undo during live/betting games if it's not allowed