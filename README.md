# 🛍️ Vinted Discord Monitor Bot

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Discord.py](https://img.shields.io/badge/Discord.py-Latest-blue)
![License](https://img.shields.io/badge/License-MIT-green)

A high-performance Discord bot for monitoring Vinted listings in real-time. Get instant notifications for new items from your favorite brands with customizable filters and multi-channel monitoring capabilities.

## ✨ Features

### Real-time Monitoring
- 🔄 Instant notifications for new listings
- 📊 Smart caching to prevent duplicate notifications
- ⚡ Optimized request handling for faster performance
- 🎯 Support for multiple brands simultaneously

### Advanced Filtering
- 💰 Maximum price filters per channel
- 📏 Size filtering support
- 🏷️ Multi-brand monitoring
- 🔍 Custom search terms support

### Channel Management
- 🎯 Automatic channel creation
- 📊 Detailed statistics tracking
- 🔄 Easy monitor restart functionality
- 🧹 Bulk channel cleanup

### User Interface
- 🎨 Beautiful embedded messages
- 📈 Detailed item statistics
- 📊 Monitor performance tracking
- 💡 Intuitive slash commands

## 🚀 Getting Started

### Prerequisites
```bash
python -m pip install -r requirements.txt
```

### Running the Bot
```bash
python bot.py
```

## 🛠️ Commands

| Command | Description |
|---------|-------------|
| `/start <brands> [search]` | Start monitoring specific brands |
| `/start_all` | Start monitoring predefined brands |
| `/stop <channel>` | Stop monitoring specific channel |
| `/set_price_filter <channel> <max_price>` | Set maximum price filter |
| `/stats` | Display monitoring statistics |
| `/list_monitors` | List active monitoring channels |
| `/restart_monitor <channel>` | Restart specific monitor |
| `/clear_monitors` | Stop and clean up all monitors |
| `/help` | Display help information |

## 📊 Monitor Statistics

The bot provides detailed statistics for each monitoring task:
- Items processed
- New items found
- Uptime tracking
- Success rate
- Processing speed

## 🎯 Predefined Brands

The bot comes with support for monitoring these brands out of the box:
- Nike
- Stone Island
- C.P. Company
- Ralph Lauren
- Spider
- Essentials

## ⚙️ Performance Optimizations

- Smart caching system
- Efficient request batching
- Optimized data processing
- Memory usage management
- Rate limit handling

## 🔧 Advanced Configuration

### Price Filtering
```python
/set_price_filter #channel 100
```
Sets maximum price to 100 for the specified channel

### Multiple Brands
```python
/start "nike,adidas,puma"
```
Monitors multiple brands in a single channel

## 📝 Best Practices

1. **Rate Limiting**: The bot implements smart delays to avoid hitting rate limits
2. **Resource Management**: Efficient memory usage through deque implementation
3. **Error Handling**: Comprehensive error catching and recovery
4. **Monitoring**: Detailed logging system for troubleshooting

## 🤝 Contributing

Feel free to:
1. Fork the repository
2. Create a feature branch
3. Submit pull requests
4. Report issues
5. Suggest improvements

## 📜 License

This project is licensed under the MIT License - see the LICENSE file for details

## 📞 Support

If you need help:
1. Check the `/help` command
2. Review the documentation
3. Open an issue on GitHub
4. Contact the bot administrator

## ⚠️ Disclaimer

This bot is for educational purposes only. Always respect Vinted's terms of service and rate limits.

---
Made with ❤️ by the Vinted Monitor Bot Team
