# IdeaSpark
A single-page, single-file idea-management app for people who generate more ideas than they ever act on. Capture a raw idea, run it through a guided intake flow, watch it get a "maturity score," then argue with an AI co-founder about why it isn't dead yet.

**What it does:**

Vault — Your active ideas, each shown as a card with a category tag, description, and a maturity score (0–100) rendered as a progress bar. Ideas can be edited, tagged, or archived (sent to the Graveyard) directly from the card.

Intake flow — Dropping a new idea into the vault isn't a single text box. It's a 3-step guided interview (What problem does this solve? Who needs this most? What's your gut feeling about effort?) that walks the score up stage by stage (12 → 40 → 68 → 84) before the idea is saved — the idea is that the act of answering the questions is what makes it "real."

Collision Engine — Surfaces AI-suggested mashups between two existing ideas in your vault ("Collision Sparks"), which you can either explore further in chat or dismiss.

Graveyard — Archived ideas aren't deleted — they're parked, with the option to revive them later.

AI Chat (per idea) — Click any idea and it opens a chat with an AI "thinking partner" persona that pushes back, asks pointed follow-up questions, and occasionally nudges the maturity score up based on how the conversation develops.

Animated background — A canvas-based particle "constellation" (nodes + connecting lines, drifting and pulsing) rendered behind the whole UI for atmosphere.


**Tech stack**


-Plain HTML + CSS + vanilla JavaScript — no framework, no bundler, no npm install.

-Anthropic Messages API (claude-sonnet-4-20250514) called directly from the browser via fetch() for the idea-chat and collision features.

-Canvas 2D API for the animated background.

-All state (ideas, chatHistory, tag colors, etc.) lives in memory — nothing persists. Refreshing the page resets everything back to the 4 seed ideas.
