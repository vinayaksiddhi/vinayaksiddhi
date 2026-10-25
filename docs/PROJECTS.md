# 📂 Projects — Siddhi Vinayak

Detailed documentation of my projects, their technologies, implementation status, and engineering decisions.

---

## 1. Jury Evaluation Platform

**Repository:** [vinayaksiddhi/jury-evaluation](https://github.com/vinayaksiddhi/jury-evaluation)  
**Deployment:** [jury-evaluation.vercel.app](https://jury-evaluation.vercel.app)  
**Status:** ✅ Deployed & Functional

### Description
A premium real-time evaluation platform built for hackathons, innovation challenges, startup competitions, project expos, and jury-based events. The platform enables judges to securely evaluate participants while administrators monitor progress and reveal final rankings through a cinematic animated leaderboard.

### Technology Stack
| Layer | Technologies |
|-------|-------------|
| Frontend | Next.js 14+, TypeScript, Tailwind CSS, shadcn/ui, Framer Motion, GSAP |
| Backend | Next.js API Routes, Prisma ORM |
| Database | PostgreSQL (Neon Database) |
| Authentication | NextAuth / Auth.js, bcrypt |
| Optional Realtime | Socket.io, Pusher, or Supabase Realtime |

### Key Features
- **Judge Panel:** Secure authentication, assigned participant evaluation, weighted scoring criteria, draft save, final submission lock, progress tracking, evaluation comments, timer support
- **Admin Panel:** Mission control dashboard, judge progress monitoring, team evaluation overview, hidden live leaderboard, open/close evaluation, lock/unlock leaderboard, arm finale mode, launch finale reveal, CSV/PDF export, evaluation reset, audit logs
- **Finale Experience:** Cinematic leaderboard reveal, animated ranking transitions, score counter animations, podium reveal, confetti celebration, winner announcement, glitch loading transitions

### Engineering Decisions
- PostgreSQL with Prisma ORM for complex evaluation queries and data integrity
- Role-based authentication separating admin and judge experiences
- Weighted scoring system supporting customizable evaluation criteria
- Cinematic finale experience using Framer Motion and GSAP for smooth animations

### Known Limitations
- Real-time features depend on external services (Socket.io/Pusher/Supabase)
- Currently optimized for single-event operation

### Future Improvements
- Multi-event management within a single instance
- Bulk team import from CSV
- Advanced analytics and evaluation insights

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
