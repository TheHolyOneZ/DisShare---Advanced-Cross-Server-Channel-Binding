# DisShare---Advanced-Cross-Server-Channel-Binding
DisShare is a powerful extension that enables seamless communication between Discord servers by creating channel bindings. With DisShare, server administrators can mirror messages between channels across different servers, allowing for unified discussions, announcements, and community engagement without requiring members to join multiple servers


> 💡 **Built for the Zygnal Ecosystem — to download and use this extension, you must be part of the Zygnal Ecosystem.**  
> This extension (cog) is part of the **Zygnal Ecosystem** and is only available through its supported platforms.  
> You can use it with:  
> - The **[Discord Bot Framework](https://github.com/TheHolyOneZ/discord-bot-framework)** — ideal for developers who want full control and flexibility *(includes an integrated extension marketplace)*, or  
> - The **[ZygnalBot](https://zygnalbot.de)** — a prebuilt, plug-and-play Discord bot *(also includes an integrated extension marketplace)*.  
>
> Browse and install extensions at [zygnalbot.com/extension](https://zygnalbot.com/extension).  
> For help or community discussions, join us on Discord: [discord.gg/sgZnXca5ts](https://discord.gg/sgZnXca5ts)





# DisShare - Cross-Server Channel Binding

## Overview
DisShare allows server administrators to create channel bindings between different Discord servers. Messages sent in bound channels can be automatically forwarded to channels in other servers, creating a seamless communication experience across server boundaries.

## Features
- **Channel Binding**: Connect channels across different Discord servers
- **Two-Way Communication**: Optional two-way binding for bidirectional message flow
- **Elegant Embeds**: Messages are forwarded with clean embeds showing the original author and source
- **Permission Control**: Only users with "Manage Channels" permission can create or modify bindings
- **Easy Management**: Simple commands to create, list, and remove channel bindings

## Commands

### Creating a Channel Binding
```
!disshare <target_guild_id> <target_channel_id> [true]
```
- `target_guild_id`: The ID of the target server
- `target_channel_id`: The ID of the target channel
- `true`: (Optional) Set to "true" to create a two-way binding

Example:
```
!disshare 123456789012345678 987654321098765432 true
```
This creates a two-way binding between the current channel and the specified target channel.

### Listing Channel Bindings
```
!listbindings
```
Shows all channel bindings for the current server, including whether they are one-way or two-way bindings.

### Removing Channel Bindings
```
!removebinding [channel_id]
```
- `channel_id`: (Optional) The ID of the channel to remove bindings for. If not provided, removes bindings for the current channel.

Example:
```
!removebinding 123456789012345678
```

## How to Get Channel and Server IDs
To use DisShare, you'll need to know the IDs of the target servers and channels:

1. Enable Developer Mode in Discord (User Settings > Advanced > Developer Mode)
2. Right-click on a server icon and select "Copy ID" to get the server ID
3. Right-click on a channel and select "Copy ID" to get the channel ID

## Binding Types

### One-Way Binding
Messages flow in one direction only (from source to target). This is useful for announcement channels where you want to broadcast messages to multiple servers.

### Two-Way Binding
Messages flow in both directions. This creates a true bridge between channels, allowing conversations to span across servers.

## Requirements
- The bot must be present in both the source and target servers
- The bot needs "Read Messages" and "Send Messages" permissions in all bound channels
- Users need "Manage Channels" permission to create or modify bindings

## Changelog

### Version 1.0.0
- Initial release
- Basic channel binding functionality
- Support for one-way and two-way bindings
- Commands: !disshare, !listbindings, !removebinding

## Troubleshooting

### Common Issues
- **Binding not working**: Ensure the bot has proper permissions in both channels
- **Can't find server/channel**: Verify the IDs are correct and the bot is in the target server
- **Messages not forwarding**: Check if the bot has "Read Messages" and "Send Messages" permissions

### Getting Help
If you encounter issues not covered here, please contact the server administrators.
