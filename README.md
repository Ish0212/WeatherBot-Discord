# Discord Weather Bot

A Java-based Discord bot that provides real-time weather information for any city using the OpenWeatherMap API.

## Features

- Get current weather for any city (`!weather <city>`)
- Get 5-day forecast for any city (`!forecast <city>`)
- Display of temperature, humidity, wind speed, and weather conditions
- Emoji representation of weather conditions
- Simple command interface
- Error handling for invalid cities or API issues

## Commands

- `!weather <city>` - Get current weather for a specified city
- `!forecast <city>` - Get a 5-day weather forecast for a specified city
- `!hello` - Display an introduction and basic command list
- `!help` - Show all available commands

## Examples

Using `!weather London`:
```
Weather in London, GB ☁️

Temperature: 15.2°C (Feels like: 14.8°C)
Humidity: 76%
Wind Speed: 4.6 m/s
Condition: Overcast clouds
```

Using `!forecast Tokyo`:
```
5-Day Forecast for Tokyo, JP

Fri, May 20 (12:00) ☀️
Temp: 23.5°C | Humidity: 45% | Clear sky

Sat, May 21 (12:00) ⛅
Temp: 22.1°C | Humidity: 58% | Few clouds

Sun, May 22 (12:00) 🌧️
Temp: 19.8°C | Humidity: 72% | Light rain
...
```

## Setup

### Prerequisites

- Java 17 or higher
- Maven
- Discord Bot Token (with MESSAGE_CONTENT intent enabled)
- OpenWeatherMap API Key (optional, a default key is included)

### Environment Variables

Copy the `.env.example` file to `.env` and add your tokens:

```
# Discord Bot Configuration
DISCORD_TOKEN=your_discord_token_here

# OpenWeatherMap API Key (optional)
# WEATHER_API_KEY=your_weather_api_key_here
```

### Discord Developer Portal Setup

1. Go to the [Discord Developer Portal](https://discord.com/developers/applications)
2. Create a new application or select your existing one
3. Navigate to the "Bot" tab
4. Under "Privileged Gateway Intents", enable "MESSAGE CONTENT"
5. Save changes

### Building and Running

1. Clone the repository
   ```
   git clone https://github.com/yourusername/discord-weather-bot.git
   cd discord-weather-bot
   ```

2. Set up your environment variables (as shown above)

3. Build the project with Maven:
   ```
   mvn clean package
   ```

4. Run the bot:
   ```
   java -jar target/weather-discord-bot-1.0-SNAPSHOT.jar
   ```

   Or simply use:
   ```
   mvn compile exec:java -Dexec.mainClass="com.example.SimpleWeatherBot"
   ```

## Inviting the Bot to Your Server

1. Go to the Discord Developer Portal and select your application
2. Navigate to OAuth2 → URL Generator
3. Select the scopes: "bot"
4. Bot Permissions: "Send Messages", "Read Message History"
5. Copy and visit the generated URL to add the bot to your server

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

MIT
