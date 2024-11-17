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
- 💰 Price range filters (minimum and maximum)
- 📏 Predefined size filtering
- 🏷️ Multiple brand monitoring
- 🔍 Custom search terms with add/remove capability
- ⏸️ Pause/Resume functionality per channel

### Monitoring Controls
- 🎯 Per-channel monitoring management
- 📊 Detailed performance statistics
- 🔄 Monitor restart capability
- 🧹 Complete monitor cleanup
- ⚡ Error threshold management

### User Interface
- 🎨 Rich Discord embeds for item display
- 🛍️ Direct purchase buttons
- 📈 Item statistics and favorite counts
- 💡 Intuitive slash commands
- 🚦 Status notifications

## 🚀 Installation

### Prerequisites
```bash
python -m pip install -r requirements.txt
```

Required packages:
- discord.py
- aiohttp
- requests
- colorama
- vinted-scraper

### Configuration
1. Create a Discord bot and get your token

## 🛠️ Available Commands

| Command | Description |
|---------|-------------|
| `/start <brands> [search]` | Start monitoring specific brands with optional search term |
| `/pause <channel>` | Pause monitoring for a specific channel |
| `/resume <channel>` | Resume monitoring for a paused channel |
| `/set_price_range <channel> [min_price] [max_price]` | Set price range filter |
| `/add_search <channel> <term>` | Add search term filter |
| `/remove_search <channel> <term>` | Remove search term filter |
| `/delete_vinted` | Remove all channels starting with vinted |
| `/start_all` | Start monitoring predefined brands |

## 📊 Monitoring Features

### Health Checking
- Automatic monitoring of task health
- 30-minute success rate checking
- Error count tracking
- Adaptive rate limit handling

### Price Filtering
```python
/set_price_range #sneakers 50 200
```
Sets price range from 50 to 200 for the specified channel

### Search Terms
```python
/add_search #sneakers "Nike Air Max"
```
Adds specific search term filter to the monitor

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
/pause #sneakers  # Pause monitoring
/resume #sneakers # Resume monitoring
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

---
Made with ❤️ by the Vinted Monitor Bot Team
