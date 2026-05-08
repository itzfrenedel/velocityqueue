# 🚀 VelocityQueue
 
Advanced Velocity queue plugin for Minecraft servers, featuring **NORMAL** and **PULL_ONLY** modes — built for events, streams, tournaments, and any controlled access scenario.
 
---
 
## ✨ Features
 
- Full queue system managed directly on the Velocity proxy
- **NORMAL** mode — players automatically connect when they reach position #1
- **PULL_ONLY** mode — only staff decides who gets in using `/pull`
- Position displayed in the **action bar** in real time
- **Throttled connections** to prevent network spikes and backend freezes
- `/pull` command to connect N players or a specific player
- Hot config reload with `/queue reload`
- Automatic update checker on startup
---
 
## 📋 Commands
 
| Command | Description |
|---------|-------------|
| `/pull <count> [server]` | Pull N players from the queue to the server |
| `/pull <player>` | Pull a specific player from any queue |
| `/pull list [server]` | Display queue status |
| `/queue reload` | Reload the configuration without restarting |
| `/queue version` | Display the plugin version |
 
---
 
## 🔐 Permissions
 
| Permission | Description |
|------------|-------------|
| `queue.use` | Required to join the queue — give this to all players |
| `queue.admin` | Access to `/pull` and `/queue reload` commands |
| `queue.priority` | Bypasses the queue and PULL_ONLY mode, connects instantly |
| `queue.bypass` | Super admin — ignores the entire queue system |
 
---
 
## ⚙️ Configuration
 
```yaml
# VelocityQueue — config.yml
 
servers:
  event:
    mode: PULL_ONLY   # Staff controls who gets in
  survival:
    mode: NORMAL      # Auto-connect when reaching position #1
 
pull:
  connect-per-second: 5   # Number of connections per second (throttle)
 
messages:
  queue-position: "&eYou are &6#%position% &ein the queue for &6%server%&e."
  queue-joined: "&aYou joined the queue for &6%server%&a. Position: &6#%position%"
  pull-success: "&aYou have been pulled from the queue and are connecting to &6%server%&a."
  no-permission: "&cYou don't have permission to do this."
```
 
---
 
## 📦 Installation
 
1. Download the `.jar` from the **Releases** tab
2. Drop it into the `plugins/` folder of your **Velocity** server
3. Restart Velocity — `config.yml` will be generated automatically
4. Configure your servers in `plugins/velocityqueue/config.yml`
5. Restart or run `/queue reload`
> ✅ No plugin needed on Paper/Spigot — everything runs on the proxy.
 
---
 
## 📌 Requirements
 
- Velocity 3.x
- Java 17+
---
 
## 🧠 Contributing
 
- Drop a ⭐ if the plugin is useful to you
- Suggest features or report bugs via **Issues**
- Follow the repo to stay up to date with new **Releases**
---
 
## 📧 Contact
 
For any question, idea or collaboration:
frenedel@color-group.fr
 
---
 
## ❤️ Credits
 
Plugin developed by **FreneDel**  
Minecraft/Velocity developer — building proxy tools to improve server management and community experiences.
