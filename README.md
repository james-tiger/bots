# Bots Collection 🤖

A comprehensive collection of bot implementations for various platforms and use cases, demonstrating different bot development approaches and technologies.

## 📋 Table of Contents

- [About](#about)
- [Bot Types](#bot-types)
- [Technologies Used](#technologies-used)
- [Project Structure](#project-structure)
- [Getting Started](#getting-started)
- [Installation](#installation)
- [Configuration](#configuration)
- [Usage](#usage)
- [Features](#features)
- [API Documentation](#api-documentation)
- [Contributing](#contributing)
- [Troubleshooting](#troubleshooting)
- [License](#license)

## 📖 About

This repository contains a collection of bot implementations for various platforms including Discord, Telegram, Slack, and other messaging platforms. Each bot demonstrates different functionalities and use cases, from simple utility bots to complex AI-powered assistants.

## 🤖 Bot Types

### Discord Bots
- **Utility Bot**: Server management, moderation, and utility commands
- **Music Bot**: Play music from various sources
- **Game Bot**: Interactive games and entertainment
- **AI Assistant**: Natural language processing and responses

### Telegram Bots
- **News Bot**: Automated news updates and notifications
- **Weather Bot**: Real-time weather information
- **Task Manager**: Personal productivity and task management
- **Inline Bot**: Inline queries and quick responses

### Slack Bots
- **Team Bot**: Team collaboration and workspace management
- **Notification Bot**: Automated alerts and notifications
- **Integration Bot**: Third-party service integrations

### Web Bots
- **Chatbot**: Website customer support
- **Scraper Bot**: Data collection and web scraping
- **API Bot**: RESTful API interactions

## 🛠️ Technologies Used

### Programming Languages
- **Python**: Discord.py, python-telegram-bot, Flask
- **JavaScript/Node.js**: Discord.js, Telegraf, Express
- **Java**: JDA (Java Discord API)
- **C#**: Discord.Net, Telegram.Bot

### Frameworks & Libraries
- **Discord.py** / **Discord.js**: Discord bot development
- **python-telegram-bot** / **Telegraf**: Telegram bot APIs
- **Flask** / **Express**: Web server frameworks
- **SQLAlchemy** / **MongoDB**: Database management
- **Redis**: Caching and session management

### APIs & Services
- **Discord API**: Discord bot functionality
- **Telegram Bot API**: Telegram bot services
- **Slack API**: Slack workspace integration
- **OpenAI API**: AI-powered responses
- **Weather API**: Real-time weather data
- **News API**: News aggregation services

### Tools & Utilities
- **Docker**: Containerization
- **Git & GitHub**: Version control
- **Heroku** / **Railway**: Cloud deployment
- **PM2**: Process management
- **Logging**: Structured logging and monitoring

## 📁 Project Structure

```
bots/
├── discord-bots/
│   ├── utility-bot/
│   │   ├── main.py
│   │   ├── cogs/
│   │   ├── config.json
│   │   └── requirements.txt
│   ├── music-bot/
│   └── game-bot/
├── telegram-bots/
│   ├── news-bot/
│   │   ├── bot.py
│   │   ├── handlers/
│   │   ├── config.py
│   │   └── requirements.txt
│   ├── weather-bot/
│   └── task-bot/
├── slack-bots/
│   ├── team-bot/
│   └── notification-bot/
├── web-bots/
│   ├── chatbot/
│   └── scraper-bot/
├── shared/
│   ├── database/
│   ├── utils/
│   └── config/
├── docs/
│   ├── api-documentation.md
│   ├── deployment-guide.md
│   └── bot-setup-guides/
├── docker-compose.yml
├── .env.example
└── README.md
```

## 🚀 Getting Started

### Prerequisites

- Python 3.8+ or Node.js 14+
- Git
- API tokens for respective platforms
- Database (PostgreSQL, MongoDB, or SQLite)
- Redis (optional, for caching)

### Quick Start

1. **Clone the repository**
   ```bash
   git clone https://github.com/james-tiger/bots.git
   cd bots
   ```

2. **Choose a bot to run**
   ```bash
   cd discord-bots/utility-bot
   # or
   cd telegram-bots/news-bot
   ```

3. **Install dependencies**
   ```bash
   # For Python bots
   pip install -r requirements.txt
   
   # For Node.js bots
   npm install
   ```

4. **Configure environment variables**
   ```bash
   cp .env.example .env
   # Edit .env with your API tokens
   ```

5. **Run the bot**
   ```bash
   # For Python bots
   python main.py
   
   # For Node.js bots
   npm start
   ```

## 📦 Installation

### Local Development

1. **Install Python dependencies**
   ```bash
   pip install -r requirements.txt
   ```

2. **Install Node.js dependencies**
   ```bash
   npm install
   ```

3. **Set up database**
   ```bash
   # PostgreSQL
   createdb botdb
   
   # MongoDB
   mongod --dbpath ./data
   ```

### Docker Deployment

1. **Build and run with Docker Compose**
   ```bash
   docker-compose up -d
   ```

2. **Scale specific services**
   ```bash
   docker-compose up -d --scale discord-bot=2
   ```

### Cloud Deployment

#### Heroku
```bash
heroku create your-bot-app
heroku config:set BOT_TOKEN=your_token_here
git push heroku main
```

#### Railway
```bash
railway login
railway init
railway up
```

## ⚙️ Configuration

### Environment Variables

Create a `.env` file in each bot directory:

```env
# Discord Bot
DISCORD_TOKEN=your_discord_bot_token
DISCORD_GUILD_ID=your_guild_id

# Telegram Bot
TELEGRAM_TOKEN=your_telegram_bot_token
TELEGRAM_WEBHOOK_URL=your_webhook_url

# Database
DATABASE_URL=postgresql://user:password@localhost/botdb
REDIS_URL=redis://localhost:6379

# API Keys
OPENAI_API_KEY=your_openai_key
WEATHER_API_KEY=your_weather_key
NEWS_API_KEY=your_news_key

# General Settings
DEBUG=true
LOG_LEVEL=INFO
```

### Bot-Specific Configuration

Each bot has its own configuration file:

```json
{
  "prefix": "!",
  "owners": ["user_id_1", "user_id_2"],
  "features": {
    "music": true,
    "moderation": true,
    "games": false
  },
  "channels": {
    "logs": "channel_id",
    "welcome": "channel_id"
  }
}
```

## 💻 Usage

### Discord Bots

#### Utility Bot Commands
```
!help - Show available commands
!ping - Check bot latency
!userinfo @user - Get user information
!serverinfo - Get server information
!clear 10 - Delete last 10 messages
```

#### Music Bot Commands
```
!play <song> - Play a song
!skip - Skip current song
!queue - Show music queue
!volume <1-100> - Set volume
!stop - Stop music and disconnect
```

### Telegram Bots

#### News Bot Commands
```
/start - Start the bot
/news - Get latest news
/subscribe <category> - Subscribe to news category
/unsubscribe <category> - Unsubscribe from category
/settings - Configure preferences
```

#### Weather Bot Commands
```
/weather <city> - Get current weather
/forecast <city> - Get weather forecast
/setlocation <city> - Set default location
/alerts - Weather alerts for your location
```

### Slack Bots

#### Team Bot Commands
```
/standup - Start daily standup
/meeting <title> - Schedule a meeting
/reminder <time> <message> - Set a reminder
/stats - Team productivity stats
```

## ✨ Features

### Common Features
- **Multi-platform Support**: Discord, Telegram, Slack integration
- **Database Integration**: Persistent data storage
- **API Integration**: External service connections
- **Modular Design**: Easy to extend and customize
- **Error Handling**: Comprehensive error management
- **Logging**: Detailed logging and monitoring
- **Rate Limiting**: API rate limit handling
- **Caching**: Redis-based caching for performance

### Advanced Features
- **AI Integration**: OpenAI GPT integration
- **Natural Language Processing**: Intent recognition
- **Multi-language Support**: Internationalization
- **Webhook Support**: Real-time notifications
- **Scheduled Tasks**: Automated recurring tasks
- **User Management**: Role-based permissions
- **Analytics**: Usage statistics and metrics

## 📚 API Documentation

### Discord Bot API Endpoints

```
GET /api/stats - Get bot statistics
POST /api/command - Execute bot command
GET /api/guilds - List connected guilds
POST /api/message - Send message to channel
```

### Telegram Bot Webhooks

```
POST /webhook/telegram - Telegram webhook endpoint
GET /webhook/status - Webhook status check
```

### Authentication

All API endpoints require authentication:

```bash
curl -H "Authorization: Bearer your_api_token" \
     -X GET https://your-bot.herokuapp.com/api/stats
```

## 🔧 Development

### Adding New Bots

1. **Create bot directory**
   ```bash
   mkdir telegram-bots/new-bot
   cd telegram-bots/new-bot
   ```

2. **Create bot structure**
   ```bash
   touch bot.py config.py requirements.txt
   mkdir handlers utils
   ```

3. **Implement bot logic**
   ```python
   # bot.py
   import logging
   from telegram.ext import Application, CommandHandler
   
   async def start(update, context):
       await update.message.reply_text('Hello! I am your new bot.')
   
   def main():
       app = Application.builder().token("YOUR_TOKEN").build()
       app.add_handler(CommandHandler("start", start))
       app.run_polling()
   
   if __name__ == '__main__':
       main()
   ```

### Testing

```bash
# Run unit tests
python -m pytest tests/

# Run integration tests
python -m pytest tests/integration/

# Run specific bot tests
python -m pytest tests/discord_bot/
```

### Code Quality

```bash
# Format code
black .
isort .

# Lint code
flake8 .
pylint bot.py

# Type checking
mypy bot.py
```

## 🤝 Contributing

Contributions are welcome! Please follow these guidelines:

1. **Fork the repository**
2. **Create a feature branch**
   ```bash
   git checkout -b feature/new-bot-feature
   ```
3. **Make your changes**
4. **Add tests for new functionality**
5. **Ensure all tests pass**
   ```bash
   pytest tests/
   ```
6. **Follow code style guidelines**
7. **Commit your changes**
   ```bash
   git commit -m "Add new bot feature"
   ```
8. **Push to your fork**
   ```bash
   git push origin feature/new-bot-feature
   ```
9. **Create a Pull Request**

### Development Guidelines

- Write clear, documented code
- Add unit tests for new features
- Follow PEP 8 style guidelines
- Update documentation for new bots
- Test on multiple platforms when possible

## 🐛 Troubleshooting

### Common Issues

#### Bot Not Responding
- Check if bot token is correct
- Verify bot has necessary permissions
- Check if bot is online/running
- Review logs for error messages

#### Database Connection Issues
- Verify database URL is correct
- Check if database server is running
- Ensure database exists and is accessible
- Check firewall and network settings

#### API Rate Limiting
- Implement exponential backoff
- Use rate limiting libraries
- Cache frequently requested data
- Monitor API usage quotas

#### Memory Issues
- Monitor memory usage
- Implement garbage collection
- Use database for persistent storage
- Optimize data structures

### Debug Mode

Enable debug mode for detailed logging:

```python
import logging
logging.basicConfig(level=logging.DEBUG)
```

### Log Analysis

Check logs for common patterns:

```bash
# Search for errors
grep -i "error" bot.log

# Check API calls
grep -i "api" bot.log

# Monitor memory usage
grep -i "memory" bot.log
```

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👤 Author

**James Tiger**
- GitHub: [@james-tiger](https://github.com/james-tiger)
- Gmail: mohamed.ashraf.y.s.m@gmail.com

## 🙏 Acknowledgments

- Discord.py community for excellent documentation
- python-telegram-bot developers
- OpenAI for AI integration capabilities
- Contributors and beta testers
- Bot hosting platforms (Heroku, Railway, etc.)

## 📞 Support

If you need help or have questions:

1. **Check the documentation** in the `/docs` folder
2. **Search existing issues** on GitHub
3. **Create a new issue** with detailed information
4. **Join our Discord server** for community support
5. **Email support**: bots@james-tiger.dev

## 🔗 Useful Links

- [Discord Developer Portal](https://discord.com/developers/applications)
- [Telegram Bot API](https://core.telegram.org/bots/api)
- [Slack API Documentation](https://api.slack.com/)
- [Bot Hosting Guide](docs/deployment-guide.md)
- [Contributing Guidelines](CONTRIBUTING.md)

---

⭐ **If you found this project helpful, please give it a star!**

🤖 **Happy Bot Building!**
