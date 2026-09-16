# skill-tree-app

A high-performance, desktop-only graph application for mapping personal development via Directed Acyclic Graphs (DAGs). Architected for zero-latency execution, it utilizes a custom React Flow canvas backed by Zustand and IndexedDB. Intensive layout calculations are offloaded to ELK.js Web Workers, and state synchronization is strictly decoupled to maintain a 60 FPS rendering pipeline. Includes a deterministic stack-based Markdown parser for rapid branch generation and a custom terminal-grade spatial navigation engine, allowing full canvas traversal and node manipulation without a mouse.

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
