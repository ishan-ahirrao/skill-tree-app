# skill-tree-app

add comprehensive summary here once done

# Dynamic Skill Tree Graph

A local-first, interactive graph application for mapping and tracking actionable, hierarchical skill trees for personal development. 

## Core Architecture
*   **Framework:** Next.js (App Router, Client-Side Rendering)
*   **Visual Engine:** React Flow
*   **Auto-Layout Engine:** ELK.js (Offloaded to Web Workers)
*   **State Management:** Zustand
*   **Local Persistence:** IndexedDB via Dexie.js
*   **UI/UX:** Tailwind CSS, shadcn/ui, cmdk

## Technical Constraints
*   **Local-First:** No backend databases or generic user authentication. Data is strictly maintained in the browser's IndexedDB.
*   **Performance Boundaries:** ELK.js layout calculations are strictly offloaded to Web Workers via JSON serialization to prevent main-thread blocking.
*   **Desktop-Only:** The canvas interaction model and Vim-style keyboard traversal are explicitly optimized for desktop viewports.

## Local Setup
1. Clone the repository.
2. Run `npm install`.
3. Run `npm run dev`.
4. Open `http://localhost:3000` (Desktop viewport required).
