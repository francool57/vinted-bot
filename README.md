# 🛍️ Vinted Discord Monitor Bot

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Discord.py](https://img.shields.io/badge/Discord.py-Latest-blue)
![License](https://img.shields.io/badge/License-MIT-green)

A sophisticated Discord bot for monitoring Vinted listings in real-time. Get instant notifications for new items matching your criteria with advanced filtering and multi-channel monitoring capabilities.

## ✨ Features

### Real-time Monitoring
- 🔄 Instant notifications for new Vinted listings
- 📊 Smart caching system to prevent duplicate notifications
- ⚡ Rate-limited request handling with adaptive delays
- 🎯 Multi-brand concurrent monitoring
- 🏥 Automatic health checking system

### Advanced Filtering
- 💰 Price range filters 
- 📏 Size filtering
- 🏷️ Multiple brand monitoring
- 🔍 Custom search terms with add/remove capability

### Monitoring Controls
- 🎯 Per-channel monitoring management
- 📊 Detailed performance statistics
- 🔄 Monitor restart capability
- 🧹 Complete monitor cleanup
- ⚡ Error threshold management

### User Interface
- 🎨 Rich Discord embeds for item display
- 🛍️ Direct purchase button
- 📈 Item statistics
- 💡 Intuitive slash commands
- 🚦 Status notifications

## 🚀 Installation

### Prerequisites
```bash
python -m pip install -r requirements.txt
```

### Configuration
1. Create a Discord bot and get your token
2. Open bot.py and change Bot token
3. Snipe those items

## 🛠️ Available Commands

| Command | Description |
|---------|-------------|
| `/start <brands> [search]` | Start monitoring specific brands with optional search term |
| `/stop <channel>` | Stop monitoring specific channel |
| `/restart_monitor <channel>` | Restarts specified channels monitor |
| `/filter <channel> [max_price] [sizes]` | Set price and/or sizes filter |
| `/delete_vinted` | Remove all channels starting with vinted |
| `/stats` | Displays all the monitoring channels and some stats |
| `/start_all` | Start monitoring predefined brands |

## 📊 Monitoring Features

### Health Checking
- Automatic monitoring of task health
- 30-minute success rate checking
- Error count tracking
- Adaptive rate limit handling

### Price Filtering
```python
/filter #sneakers 200 39,40,41,42
```
Sets price range from 0 to 200 and shoe sizes 39, 40, 41 and 42for the specified channel 

## ⚙️ Technical Features

### Rate Limiting Protection
- Adaptive delay system
- Exponential backoff on rate limits
- Configurable maximum retry delay
- Error threshold monitoring

### Error Handling
- Comprehensive exception catching
- Automatic retry mechanism
- Error notification system
- Logging with color coding

### Performance Optimization
- Asynchronous operation
- Request batching
- Memory-efficient caching
- Webhook reuse

## 🔧 Advanced Usage

### Multiple Brand Monitoring
```python
/start "nike,adidas,puma" "sneakers"
```
Monitors multiple brands with a search term filter

### Monitor Management
```python
/stop #sneakers  # Pause monitoring
/restart_monitor #sneakers # restart monitoring
```

## 📝 Best Practices

1. **Rate Limits**: Respect Vinted's rate limits by using appropriate delays
2. **Resource Usage**: Monitor memory usage and active tasks
3. **Error Handling**: Check logs regularly for issues
4. **Search Terms**: Use specific terms to reduce false positives

## ⚠️ Disclaimer

This bot is for educational purposes only. Always comply with Vinted's terms of service and API usage guidelines.

## 🔍 Logging

The bot includes a comprehensive logging system with:
- Color-coded console output
- File logging
- Timestamp tracking
- Error tracking
- Performance monitoring

## 🤝 Contributing

Contributions are welcome! Please:
1. Fork the repository
2. Create a feature branch
3. Submit pull requests
4. Report issues
5. Suggest improvements

## 📜 License

This project is licensed under the MIT License.

