# Flashcards for Study

A flashcard deck builder and review app built as a single React component. Create decks, add question/answer cards, and review them with a flip-to-reveal study mode — all stored locally in the browser with `localStorage`.

## Features

- **Deck management** — create decks with a name and description, rename/delete, switch between decks.
- **Card editor** — add, edit, and delete individual flashcards (question + answer).
- **Study / review mode** — flip cards to reveal answers, step through the deck card by card.
- **Night mode** — dark theme toggle for comfortable late-night study sessions.
- **Import/export decks** — back up or share decks as JSON.
- **No login, no backend** — everything stays on-device in `localStorage`, free forever.

## Tech Stack

- React (functional components + hooks: `useState`, `useEffect`)
- TypeScript (`Flashcard` and `Deck` types)
- shadcn/ui components (Button, Card, Input, Label)
- lucide-react icons (Moon/Sun for the theme toggle)
- Browser `localStorage` for persistence

## Quick Start

The component is a single file (`Flashcards for Study`, 367 lines). Drop it into any React project that already has shadcn/ui set up:

1. Place the file in your project (e.g. `src/components/Flashcards.tsx`).
2. Ensure the imports match your shadcn/ui setup:
   - `/components/ui/button`
   - `/components/ui/card`
   - `/components/ui/input`
   - `/components/ui/label`
3. Import and render `<Flashcards />` on any route/page.

```tsx
import Flashcards from './components/Flashcards'

export default function App() {
  return <Flashcards />
}
```

4. Open in a browser — decks persist across reloads via `localStorage`.

## Project Structure

```
.
├── Flashcards for Study   # The full React flashcard app (single file)
├── LICENSE               # License
└── README.md
```

## Notes

- Decks are stored under the `flashcardDecks` key in `localStorage` — private to the user's browser and device.
- To add spaced-repetition reminders, store `nextReview` timestamps per card and surface due cards on load.

Built by Girish Lade — [ladestack.in](https://ladestack.in)
