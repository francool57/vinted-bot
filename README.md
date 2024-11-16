# Vinted Monitor Bot Commands Documentation

  

| Command | Parameters | Description | Example | Permission Required |

|---------|------------|-------------|---------|-------------------|

| `/start` | `brands` (required)<br>`search` (optional) | Starts a new monitor for specified brands.<br>- Multiple brands separated by commas<br>- Optional search term to filter items<br>- Creates a new channel automatically<br>- Sets up webhook for notifications | `/start nike,adidas supreme` | Manage Channels |

| `/stop` | `channel` (required) | Stops monitoring for the specified channel.<br>- Cancels the monitoring task<br>- Keeps channel intact<br>- Webhook remains but stops sending | `/stop #nike-finds` | Manage Channels |

| `/stats` | None | Displays monitoring statistics:<br>- Total items processed<br>- New items found<br>- Active monitors count<br>- Bot uptime<br>- Success rate | `/stats` | None |

| `/list_monitors` | None | Shows all active monitoring channels:<br>- Lists all channels being monitored<br>- Shows channel mentions for easy navigation | `/list_monitors` | None |

| `/settings` | `channel` (required)<br>`refresh_rate` (optional)<br>`notification_type` (optional) | Configures monitor settings:<br>- Refresh rate (in seconds, min 2)<br>- Notification type (all/new_only/price_drops)<br>- Channel-specific settings | `/settings #nike-finds 5 new_only` | Manage Channels |

| `/filter` | `channel` (required)<br>`options` (required) | Sets item filters:<br>- Price range (min-max)<br>- Size filters<br>- Condition filters<br>- Location filters | `/filter #nike-finds price:10-50 size:M,L condition:new` | None |

| `/alerts` | `channel` (required)<br>`price` (optional)<br>`keywords` (optional) | Sets up custom alerts:<br>- Price drop notifications<br>- Keyword matches<br>- Special item conditions | `/alerts #nike-finds price<30 keywords:vintage,rare` | None |

| `/status` | `channel` (optional) | Shows monitor status:<br>- Current settings<br>- Items found<br>- Last check time<br>- Error rate | `/status #nike-finds` | None |

| `/reset` | `channel` (required) | Resets monitor settings:<br>- Clears filters<br>- Resets statistics<br>- Keeps monitor running | `/reset #nike-finds` | Manage Channels |

| `/help` | `command` (optional) | Shows help information:<br>- List of all commands<br>- Detailed command usage<br>- Examples | `/help start` | None |

  

## Additional Features

  

### Filter Options

-  **Price Range**: `price:min-max`

-  **Sizes**: `size:XS,S,M,L,XL`

-  **Conditions**: `condition:new,used,good`

-  **Brands**: `brands:nike,adidas,puma`

-  **Location**: `location:country_code`

  

### Notification Types

-  **all**: Send notifications for all items

-  **new_only**: Only send notifications for newly listed items

-  **price_drops**: Only send notifications for price drops

  

### Response Times

- Minimum refresh rate: 2 seconds

- Maximum refresh rate: 30 seconds

- Default refresh rate: 5 seconds

  

### Channel Naming Convention

- Automatically created channels follow the format: `vinted-{first_brand}`

- Example: `/start nike` creates channel `#vinted-nike`

  

### Error Handling

- Automatically retries on connection errors

- Reports errors in the command channel

- Maintains error logs for debugging

  

## Examples

  

### Basic Monitoring

```discord

/start nike

```

Creates #vinted-nike channel and starts monitoring Nike items

  

### Advanced Monitoring

```discord

/start nike,adidas vintage

```

Creates channel and monitors for vintage Nike and Adidas items

  

### Complex Filtering

```discord

/filter #vinted-nike price:20-100 size:M,L condition:new location:DE

```

Sets up filtering for new Nike items in Germany, size M or L, priced between 20-100

  

### Custom Alerts

```discord

/alerts #vinted-nike price<50 keywords:dunk,air,max

```

Sets alerts for Nike items under 50 containing keywords "dunk", "air", or "max"

  

## Best Practices

  

1.  **Channel Management**

- Keep monitor count under 10 per server for optimal performance

- Use specific search terms to reduce noise

- Regular cleanup of inactive monitors

  

2.  **Performance**

- Use appropriate refresh rates based on item volume

- Set relevant filters to reduce processing load

- Monitor error rates and adjust settings accordingly

  

3.  **Notifications**

- Use notification types based on needs

- Set up alerts for important items only

- Use keyword filtering effectively

  

## Troubleshooting

  

1.  **Common Issues**

- Rate limiting: Increase refresh rate

- Missing notifications: Check webhook permissions

- High error rate: Check network connection

  

2.  **Solutions**

-  `/reset` to clear problematic settings

-  `/stop` and `/start` to refresh connection

- Check Discord channel permissions
