# Quick Quiz Game

A simple and interactive quiz game built with JavaScript, HTML, and CSS that uses Supabase as a backend database.

## Description

Quick Quiz is a web-based quiz game where players answer questions to earn points. The game features a timer for each question, with points awarded based on both correctness and speed. Player scores are saved to a Supabase database and displayed on a leaderboard.

## Features

- Interactive quiz gameplay with visual and text-based questions
- Timer-based scoring system (faster answers earn more points)
- Score leaderboard using Supabase database
- Responsive design that works on different screen sizes
- Asset preloading for smooth gameplay experience

## Technologies Used

- HTML5
- CSS3
- JavaScript (ES6+)
- Supabase (Backend database)
- Webpack (Module bundler)
- Babel (JavaScript compiler)

## Prerequisites

Before you begin, ensure you have the following installed:
- Node.js (v14 or higher)
- npm (v6 or higher)

## Setup

1. Clone the repository:
```bash
git clone <repository-url>
```

2. Install dependencies:
```bash
npm install
```

3. Create a `.env` file in the root directory with your Supabase credentials:
```bash
SUPABASE_URL=your_supabase_url SUPABASE_KEY=your_supabase_key
```

4. Start the development server:
```bash
npm run dev
```


5. Build for production:
```bash
npm run build
```


## Project Structure
```
. ├── src/ 
│ ├── index.js # Entry point 
│ ├── game.js # Game logic 
│ ├── styles.css # Styling 
│ └── index.html # HTML template 
├── .env # Environment variables (not in repo) 
├── package.json # Project dependencies and scripts └── webpack.config.cjs # Webpack configuration
```


## Game Components

### Screens
1. **Login Screen**: Enter your name to start playing
2. **Game Screen**: Answer questions within the time limit
3. **Results Screen**: View your final score and the leaderboard

### Game Mechanics
- Each question has a 10-second timer
- Points are calculated as: 10 base points + remaining time bonus
- Questions can be text-based or image-based
- Answers are randomized for each question
- Scores are saved to Supabase database after game completion

## Supabase Database

The application uses two database tables:

1. **questions**: Stores quiz questions with fields:
   - `id`: Unique identifier
   - `question_text`: The question content
   - `question_type`: Type of question ('text' or 'image')
   - `image_url`: URL to question image (for image questions)
   - `correct_answer`: The correct answer
   - `option_b`, `option_c`, `option_d`: Incorrect options

2. **scores**: Stores player scores with fields:
   - `id`: Unique identifier
   - `player_name`: Player's name
   - `score`: Player's final score
   - `created_at`: Timestamp of score creation

## Development

To run the development server:
`npm run dev`


To create a production build:
`npm run build`