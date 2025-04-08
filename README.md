# Graphene Telegram Bot

A Telegram bot for the Graphene Web3 project on Solana, allowing users to get project information, view token stats, and purchase $GRAPH tokens directly through Telegram.

## Features

- Basic commands for project information
- Token statistics display
- Token purchase flow with wallet integration
- Admin commands for announcements and broadcasts
- Internationalization support (English and Russian)
- Twitter integration (optional)

## Setup

1. Clone the repository
2. Install dependencies:
   \`\`\`
   npm install
   \`\`\`
3. Copy `.env.example` to `.env` and fill in your configuration values:
   \`\`\`
   cp .env.example .env
   \`\`\`
4. Build the project:
   \`\`\`
   npm run build
   \`\`\`
5. Start the bot:
   \`\`\`
   npm start
   \`\`\`

## Development

For development with hot-reloading:
\`\`\`
npm run dev
\`\`\`

## Commands

- `/start` - Start the bot
- `/about` - Show project overview
- `/token` - Show current $GRAPH stats
- `/buy` - Start token purchase flow
- `/roadmap` - Display project roadmap
- `/site` - Link to main site
- `/help` - List all commands

### Admin Commands

- `/post <message>` - Send update to a linked Telegram channel
- `/broadcast <message>` - Send message to all users
- `/tweet` - Fetch and forward the latest tweet from @G3zGraph

## Token Purchase Flow

1. User initiates with `/buy`
2. User connects existing wallet or generates a new one
3. User selects currency (USDC or SOL) and enters amount
4. Bot provides swap details and confirmation
5. User signs transaction via wallet deep link
6. Bot confirms successful transaction and provides explorer link

## Project Structure

- `src/index.ts` - Main entry point
- `src/commands.ts` - Command handlers
- `src/admin.ts` - Admin command handlers
- `src/features/buy.ts` - Token purchase flow
- `src/services/` - Service modules for various functionalities
- `src/database.ts` - User database management
- `locales/` - Internationalization files

## License

MIT
