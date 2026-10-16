# Quest, Match and Learn Puzzle Challenge API
> Backend API for Quest, Match and Learn Puzzle Challenge
> Software Engineering 1 — A.Y. 2026-2027

## Team Information
Developer: Trisha Joy Gutierrez (@trishajoy), Gian Carlo Erivera, Donnalyn Mae Nares, Eron Hona
Course/Section: BSCS 3-1
Group Name: Team 4

## Game Concept
Title: Quest, Match and Learn Puzzle Challenge
One-Line Pitch: Match the tiles, complete the puzzle, answer the quiz, and pass the level!

Genre: Educational Puzzle Game
Platform: Mobile (Android/iOS) and Desktop/Web
Core Loop: Match Tiles → Complete Puzzle → Answer Quiz → Earn Points → Pass Level → Next Level

Win Rule: Complete tile matches + answer quiz correctly = Pass Level
Lose Rule: Fail requirements or use all attempts = Try Again

## Tech Stack
Runtime: Node.js 22 LTS or newer
Web Framework: Express 5
Database: PostgreSQL 16 or newer
ORM & Migrations: Sequelize 6 + sequelize-cli

## Setup
git clone https://github.com/trishajoy/quest-match-and-learn-puzzle-challenge.git
cd quest-match-and-learn-puzzle-challenge
npm install

## Environment Variables
DB_HOST=127.0.0.1
DB_PORT=5432
DB_NAME=quest_match_learn
DB_USER=postgres
DB_PASSWORD=your_password
PORT=3001
NODE_ENV=development
HUB_API_KEY=dev-hub-key

## Database Commands
npm run db:create
npm run db:migrate
npm run db:seed
npm run db:check
npm run db:reset
npm run dev

## API Endpoints
GET    /api/v1/health              200 OK
GET    /api/v1/game-info           200 OK
GET    /api/v1/player/:id          200 OK
POST   /api/v1/player              201 Created
PUT    /api/v1/player/:id          200 OK
GET    /api/v1/level/:id           200 OK
GET    /api/v1/level/:id/questions 200 OK
POST   /api/v1/question/:id/validate 200 OK
GET    /api/v1/leaderboard         200 OK
POST   /api/v1/admin/questions      200 OK
POST   /api/v1/hub/sync-github      200 OK

## What "Completed" Means
A player has completed the game when they have successfully finished all levels — matching every tile pair and answering the final level's quiz questions. Players can still progress even if they answer some questions incorrectly, but they must earn enough points and complete the puzzle to unlock the next level.

## Database Tables
1. players — Player accounts & profile data
2. admins — Administrator credentials & access levels
3. levels — Level configurations: tile layouts, difficulty, puzzle images
4. questions — Quiz questions, answer options, and correct answers per level
5. game_progress — Player's saved progress: completed levels, scores, lives remaining

Submitted by: Team 4 — Gian Carlo Erivera, Donnalyn Mae Nares, Trisha Joy Gutierrez, Eron Hona
