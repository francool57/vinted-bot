# Vinted Bot Command Reference

## Monitoring Commands

| Command | Description | Usage | Example |
|---------|-------------|--------|---------|
| `/start` | Start monitoring for specific brands | `/start <brands> [search]` | `/start nike,adidas sneakers` |
| `/stop` | Stop monitoring a specific channel | `/stop <channel>` | `/stop #vinted-nike` |
| `/list_monitors` | Display all active monitoring channels | `/list_monitors` | `/list_monitors` |
| `/stats` | Show monitoring statistics | `/stats` | `/stats` |

## Filter Commands

| Command | Description | Usage | Example |
|---------|-------------|--------|---------|
| `/filter price_range` | Set minimum and maximum price | `/filter <channel> price_range <min>-<max>` | `/filter #vinted-nike price_range 20-100` |
| `/filter sizes` | Set acceptable sizes | `/filter <channel> sizes <size1,size2,...>` | `/filter #vinted-nike sizes S,M,L,XL` |
| `/filter conditions` | Set acceptable item conditions | `/filter <channel> conditions <condition1,condition2,...>` | `/filter #vinted-nike conditions new,like new` |
| `/filter colors` | Set color filters | `/filter <channel> colors <color1,color2,...>` | `/filter #vinted-nike colors black,white,red` |
| `/filter exclude_words` | Set words to exclude from titles | `/filter <channel> exclude_words <word1,word2,...>` | `/filter #vinted-nike exclude_words fake,replica,copy` |
| `/filter include_words` | Set required words in titles | `/filter <channel> include_words <word1,word2,...>` | `/filter #vinted-nike include_words vintage,rare` |
| `/show_filters` | Display current filters for a channel | `/show_filters <channel>` | `/show_filters #vinted-nike` |
| `/clear_filters` | Remove all filters from a channel | `/clear_filters <channel>` | `/clear_filters #vinted-nike` |

## Filter Options Details

### Price Range
- Format: `min-max` (in euros)
- Example values:
  - `10-50`: Items between 10€ and 50€
  - `0-100`: Items up to 100€
  - `50-`: Items from 50€ and up

### Sizes
- Common values: `XS`, `S`, `M`, `L`, `XL`, `XXL`
- Numeric sizes: `36`, `37`, `38`, `39`, `40`, `41`, `42`, `43`, `44`, `45`
- Can combine multiple: `S,M,L`

### Conditions
- Available options:
  - `new`: New with tags
  - `like new`: New without tags
  - `very good`: Very good condition
  - `good`: Good condition
  - `satisfactory`: Satisfactory condition

### Colors
- Common colors: `black`, `white`, `red`, `blue`, `green`, `yellow`, `pink`, `purple`, `brown`, `grey`
- Can combine multiple: `black,white,red`

### Word Filters
- Exclude words: Words that should NOT appear in the title
- Include words: Words that MUST appear in the title
- Case insensitive
- Comma-separated for multiple words
- Example:
  - Exclude: `fake,replica,copy,dupe`
  - Include: `vintage,rare,limited`

## Notes
- All commands are prefixed with `/`
- Channel names must include the `#` symbol
- Lists (sizes, colors, etc.) should be comma-separated
- Filters are channel-specific
- Filters persist between bot restarts
- Filters are applied before items are posted to Discord
