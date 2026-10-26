# 📂 Projects — Siddhi Vinayak

Detailed documentation of my projects, their technologies, implementation status, and engineering decisions.

---

## 1. SCORE SPHERE — Jury Website

**Repository:** [vinayaksiddhi/jury-website](https://github.com/vinayaksiddhi/jury-website)  
**Deployment:** [jury-website.vercel.app](https://jury-website.vercel.app)  
**Associated With:** PALS BMSIT (May 2026 – Oct 2026)  
**Status:** ✅ Deployed & Functional

### Description
A modern real-time jury evaluation and multi-event scoring platform built for hackathons, innovation challenges, startup pitch competitions, project expos, and technical demo days. Developed in collaboration with PALS BMSIT, the platform eliminates chaotic spreadsheets and scoring discrepancies by providing evaluators with an authenticated, criteria-based judging workflow while administrators manage evaluation cycles and unveil final rankings through an animated, cinematic stage experience.

### Technology Stack
| Layer | Technologies |
|-------|-------------|
| Frontend | Next.js 14+ (App Router), TypeScript, Tailwind CSS, shadcn/ui, Framer Motion, GSAP, Lucide React |
| Backend | Next.js API Routes / Route Handlers, Prisma ORM |
| Database | PostgreSQL (Neon Serverless PostgreSQL) |
| Authentication | NextAuth / Auth.js, bcrypt password hashing |
| Typography & Aesthetics | Orbitron, Inter, JetBrains Mono, glassmorphism UI |

### Key Modules & Capabilities
- **Public & Event Landing:** Event countdown, registered teams count, evaluator metrics, live status pulse, criteria directory, and jury code of conduct.
- **Judge Portal:** Secure role-based login, isolated team assignment view, 10-criteria rating matrix (1-10 scale), auto-weighted total computation, draft state preservation, submission lock, and qualitative feedback box.
- **Admin Mission Control:** Real-time evaluator completion tracker, hidden dynamic leaderboard, evaluation window toggling (open/close), formal score tiebreaker resolution, CSV/PDF summary generation, and full audit logging.
- **Cinematic Finale Reveal:** Stage-ready animated leaderboard with GSAP score count-ups, ranking re-sort animations, top-3 podium reveal, glitch transitions, and particle confetti celebrations.

### The 10 Weighted Evaluation Criteria (10% Each)
1. **Innovation & Creativity (10%):** Originality and uniqueness of the solution.
2. **Technical Implementation (10%):** Code architecture, modern stack execution, and code quality.
3. **Problem Solving (10%):** Effectiveness in resolving the primary core problem.
4. **User Experience (10%):** Interface polish, usability, accessibility, and navigation design.
5. **Feasibility & Scalability (10%):** Viability in the real world and sustainable growth roadmap.
6. **Presentation Skills (10%):** Delivery clarity, slide deck articulation, and live demo quality.
7. **Effort & Skill (10%):** Technical ambition and engineering difficulty accomplished.
8. **Time Management (10%):** Completeness of deliverables within the strict hackathon timeframe.
9. **Learning & Adaptability (10%):** Rapid skill adoption and problem iteration shown during the event.
10. **Impact & Viability (10%):** Positive social, commercial, or environmental value proposition.

### Engineering Decisions & Security
- **PostgreSQL with Prisma ORM:** Relational integrity for foreign key constraints between Judges, Teams, Criteria, and Scores.
- **Double-Blind Scoring Integrity:** Evaluator scores are confidential and isolated until Admin unlocks the finale leaderboard.
- **State Guard Rails:** Evaluator submissions are locked once finalized to prevent unauthorized post-submission edits.
- **Performance:** Optimized client-side bundling with Next.js App Router for instant score input responsiveness.

---

## 2. DecentraVote — Decentralized Voting DApp

**Repository:** [vinayaksiddhi/DecentraVote](https://github.com/vinayaksiddhi/DecentraVote)  
**Status:** ✅ Complete (Hardhat Local Network)

### Description
A full-stack decentralized voting application where all candidate data, vote counts, election status, and voter eligibility are read directly from the Solidity smart contract on-chain. No backend database, no mocked data.

### Technology Stack
| Layer | Technologies |
|-------|-------------|
| Smart Contract | Solidity ^0.8.20 |
| Blockchain | Hardhat (Local Network, Chain ID 31337) |
| Frontend | React 19, Vite, Tailwind CSS |
| Web3 | ethers.js v6, MetaMask |

### Key Features
- **Direct blockchain integration** — Zero mocking, all data from on-chain
- **One-vote-per-wallet enforcement** — EVM-level `require(!hasVoted[msg.sender])` prevention
- **Real-time VoteCast event listener** — Dynamically updates tallies without page refreshes
- **MetaMask integration** — Automatic account/chain switching detection
- **Transaction lifecycle tracking** — Signature Pending → Submitted → Confirmed → Reverted
- **Owner-only admin panel** — Election management with irreversible close warning

### Engineering Decisions
- ethers.js v6 for modern provider patterns and typed contract interactions
- Complete separation of blockchain and frontend concerns via custom hooks
- Comprehensive revert error decoding for accurate user feedback

### Known Limitations
- Configured for Hardhat Local (not deployed to public testnet/mainnet)
- Requires MetaMask browser extension

### Future Improvements
- Deployment to a public Ethereum testnet (Sepolia/Goerli)
- Candidate registration through the UI
- Voter registration and eligibility management

---

## 3. ALUM-SPHERE — Alumni-Student Networking Platform

**Repository:** [vinayaksiddhi/ALUM-SPHERE](https://github.com/vinayaksiddhi/ALUM-SPHERE)  
**Status:** ✅ Complete

### Description
A modern alumni-student connection platform featuring real-time mentorship matching, instant messaging, project collaboration, and collegiate Q&A discussions.

### Technology Stack
| Layer | Technologies |
|-------|-------------|
| Frontend | Next.js (App Router), React 19, Tailwind CSS v4, Framer Motion |
| UI Components | Radix UI primitives, Lucide Icons, Glassmorphism design |
| Authentication | Clerk |
| Database | PostgreSQL (Supabase) |
| ORM | Prisma Client with prisma/adapter-pg |
| Real-Time | Supabase Realtime (WebSockets & Broadcasts) |

### Key Features
- **Matchmaking engine** — Connects students with alumni based on college, department, graduation year, and expertise
- **Real-time WhatsApp-style chat** — Sub-100ms delivery via Supabase Broadcast
- **Connection request system** — Track pending/accepted/rejected statuses
- **Optimistic UI** — Messages appear instantly while resolving in the background
- **Q&A and Discussions** — Collegiate Q&A with real-time commenting and like systems
- **Project Showcases** — Students can share projects with technology tags

### Engineering Decisions
- Supabase Broadcast for high-speed chat delivery directly between browsers
- Prisma Server Actions to bypass RLS friction while maintaining security
- Debounced WebSocket listeners to consolidate rapid changes into single server fetches

### Known Limitations
- Requires Supabase and Clerk accounts for deployment

---

## 4. Event Planner

**Repository:** [vinayaksiddhi/event_planner](https://github.com/vinayaksiddhi/event_planner)  
**Deployment:** [event-planner-genk.vercel.app](https://event-planner-genk.vercel.app/)  
**Status:** ✅ Deployed

### Description
A web application for managing events and registrations, deployed on Vercel.

### Technology Stack
| Layer | Technologies |
|-------|-------------|
| Language | JavaScript |
| Deployment | Vercel |

---

## 5. ProofVault — Document Integrity Platform

**Status:** 🔬 Concept / Early Development

### Description
A blockchain-backed document verification platform exploring how PostgreSQL, Docker, and blockchain can work together to ensure tamper-proof document integrity.

### Planned Technologies
- PostgreSQL for document metadata storage
- Docker for containerized deployment
- Blockchain-based verification for integrity proofs

### Current State
This project is in the concept and early development phase. No public repository is available yet.

---

## 6. Portfolio

**Repository:** [vinayaksiddhi/Portfolio](https://github.com/vinayaksiddhi/Portfolio)  
**Status:** ✅ Available

A personal portfolio website built with JavaScript.

---

## Notes

- All project descriptions are based on actual repository code and README content
- "Complete" status means the core functionality is implemented and the code is public
- "Concept" status means the idea exists but implementation is partial or not yet public
- Deployment links were verified as accessible at the time of writing
