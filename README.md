
 
 
 
Quest, Match and Learn Puzzle Challenge API
 
Backend API for Quest, Match and Learn Puzzle Challenge, an educational tile-matching puzzle game.
Software Engineering 1 — A.Y. 2026-2027
 
Team Information
 
- Developer: Trisha Joy Gutierrez (@trishajoy), Gian Carlo Erivera, Donnalyn Mae Nares, Eron Hona
- Course/Section: BSCS 3-1
- Group Name: Team 4
 
Game Concept
 
Title: Quest, Match and Learn Puzzle Challenge
One-Line Pitch: Match the tiles, complete the puzzle, answer the quiz that pops up, and pass the level to reach higher levels!
 
- Genre: Educational Puzzle Game
- Platform: Mobile (Android/iOS) and Desktop/Web
- Core Loop: Match Tiles → Complete Puzzle → Answer Quiz → Earn Points → Pass Level → Next Level
 
Win Rule: Complete required tile matches + answer quiz correctly = Pass Level
Lose Rule: Fail puzzle requirements or use all lives/attempts = Try Again
 
Tech Stack
 
- Runtime: Node.js 22 LTS or newer
- Web Framework: Express 5
- Database: PostgreSQL 16 or newer
- ORM & Migrations: Sequelize 6 + sequelize-cli
 
Setup Instructions
 
git clone https://github.com/trishajoy/quest-match-and-learn-puzzle-challenge.git
cd quest-match-and-learn-puzzle-challenge
npm install
 
Environment Variables
 
Copy .env.example to .env and configure your database credentials:
 
- DB_HOST: 127.0.0.1 — PostgreSQL host
- DB_PORT: 5432 — PostgreSQL port
- DB_NAME: quest_match_learn — Database name
- DB_USER: postgres — Database username
- DB_PASSWORD: your_password — Your database password — NEVER commit this file!
- PORT: 3001 — API server port
- NODE_ENV: development — Environment mode
- HUB_API_KEY: dev-hub-key — Game Hub synchronization key
 
Database Commands
 
npm run db:create     — Create the database
npm run db:migrate    — Run migrations
npm run db:seed       — Load seed data / initial questions
npm run db:check      — Verify database connection
npm run db:reset      — Reset and reseed database
npm run dev           — Start the development server
 
API Endpoints
 
- GET /api/v1/health — Health check — 200 OK
- GET /api/v1/game-info — Get game details — 200 OK
- GET /api/v1/player/:id — Get player profile — 200 OK
- POST /api/v1/player — Register new player — 201 Created
- PUT /api/v1/player/:id — Update player progress — 200 OK
- GET /api/v1/level/:id — Load level info — 200 OK
- GET /api/v1/level/:id/questions — Get quiz questions — 200 OK
- POST /api/v1/question/:id/validate — Submit answer — 200 OK
- GET /api/v1/leaderboard — Get top scores — 200 OK
- POST /api/v1/admin/questions — Add/update questions — 200 OK
- POST /api/v1/hub/sync-github — Sync GitHub — 200 OK
 
What "Completed" Means
 
A player has completed the game when they have successfully finished all levels — matching every tile pair and answering the final level's quiz questions. Players can still progress even if they answer some questions incorrectly, but they must earn enough points and complete the puzzle to unlock the next level.
 
Database Tables
 
1. players — Player accounts & profile data
2. admins — Administrator credentials & access levels
3. levels — Level configurations: tile layouts, difficulty, puzzle images
4. questions — Quiz questions, answer options, and correct answers per level
5. game_progress — Player's saved progress: completed levels, scores, lives remaining
 
Submitted by: Team 4 — Gian Carlo Erivera, Donnalyn Mae Nares, Trisha Joy Gutierrez, Eron Hona
 
 
 

