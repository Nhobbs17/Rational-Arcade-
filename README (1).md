# Rational Arcade Game

A vibrant, colorful educational game platform for learning rational functions through visually engaging mini-games and challenges.

## 🎮 Features

- **Speed Round**: Timed asymptote identification game
- **Graph Matcher**: Drag-and-drop matching of graphs to equations  
- **True/False**: Quick-fire statement validation
- **Equation Builder**: Interactive rational function construction
- **Learn Mode**: Educational content with lessons and practice questions

## 🚀 Quick Start

### Prerequisites

- Node.js 18+ 
- npm or yarn package manager

### Installation

1. Clone the repository:
```bash
git clone <your-repo-url>
cd rational-arcade
```

2. Install dependencies:
```bash
npm install
```

3. Start the development server:
```bash
npm run dev
```

4. Open your browser to `http://localhost:5000`

## 🏗️ Project Structure

```
├── client/          # React frontend application
│   ├── src/
│   │   ├── components/  # Reusable UI components
│   │   ├── pages/       # Game pages and routes
│   │   ├── lib/         # Utilities and game logic
│   │   └── hooks/       # Custom React hooks
├── server/          # Express.js backend API
│   ├── index.ts     # Server entry point
│   ├── routes.ts    # API route definitions
│   └── storage.ts   # Data storage interface
├── shared/          # Shared types and database schema
└── package.json     # Dependencies and scripts
```

## 🛠️ Technology Stack

- **Frontend**: React 18, TypeScript, Vite
- **Backend**: Express.js, TypeScript
- **Database**: PostgreSQL with Drizzle ORM
- **UI**: Tailwind CSS, shadcn/ui components
- **State Management**: TanStack Query
- **Routing**: Wouter

## 📦 Available Scripts

- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run start` - Start production server
- `npm run db:generate` - Generate database migrations
- `npm run db:migrate` - Run database migrations

## 🗄️ Database Setup

### Option 1: PostgreSQL (Recommended for Production)

1. Set up a PostgreSQL database (locally or using a service like Neon, Supabase, or Railway)

2. Create a `.env` file in the root directory:
```env
DATABASE_URL=postgresql://username:password@localhost:5432/rational_arcade
```

3. Run migrations:
```bash
npm run db:generate
npm run db:migrate
```

### Option 2: In-Memory Storage (Development)

The app will automatically use in-memory storage if no database is configured. This is perfect for development and testing.

## 🚀 Deployment

### Deploy to Vercel

1. Install Vercel CLI:
```bash
npm install -g vercel
```

2. Deploy:
```bash
vercel
```

### Deploy to Railway

1. Connect your GitHub repository to Railway
2. Set environment variables in Railway dashboard
3. Deploy automatically on push

### Deploy to Render

1. Connect your GitHub repository to Render
2. Set build command: `npm run build`
3. Set start command: `npm start`

## 🔧 Environment Variables

| Variable | Description | Required |
|----------|-------------|----------|
| `DATABASE_URL` | PostgreSQL connection string | No (uses in-memory storage) |
| `NODE_ENV` | Environment (development/production) | No |
| `PORT` | Server port | No (defaults to 5000) |

## 🎯 Game Modes

### Speed Round
Fast-paced asymptote identification where players click on vertical asymptotes as quickly as possible.

### Graph Matcher
Match rational function graphs to their corresponding equations using drag-and-drop.

### True/False
Quick decision-making game testing knowledge of rational function properties.

### Equation Builder
Interactive tool for constructing rational functions with specific characteristics.

## 🏆 Scoring System

- Points awarded based on speed and accuracy
- Streak bonuses for consecutive correct answers
- Achievement system for milestones
- Leaderboards for competitive play

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/amazing-feature`
3. Commit changes: `git commit -m 'Add amazing feature'`
4. Push to branch: `git push origin feature/amazing-feature`
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🆘 Support

If you encounter any issues:

1. Check the [Issues](../../issues) page
2. Create a new issue with detailed description
3. Include steps to reproduce the problem

## 🎨 Customization

The app uses Tailwind CSS for styling. You can customize:

- Colors in `client/src/index.css`
- Components in `client/src/components/`
- Game logic in `client/src/lib/game-logic.ts`

Happy learning! 🎓✨