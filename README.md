# ESX Redzone

**The ultimate configurable FFA PvP zone for FiveM (ESX Legacy)**

---

## 🎬 Preview

[![Redzone Preview](https://img.youtube.com/vi/X5L4kkjyN80/0.jpg)](https://youtu.be/X5L4kkjyN80)  
[Watch the ESX Redzone preview on YouTube](https://youtu.be/X5L4kkjyN80)

---

## 📦 Download

[Download the latest release on GitHub](https://github.com/OnlyAlilSlow/ESX-RedZone/releases/tag/script)

---

## 🚀 Features

- **Configurable redzone area:** Location, radius, markers, blips, and respawn points
- **Bucket system:** Isolates all players in the redzone (no interaction with others)
- **Forced weapon with infinite ammo**
- **Kill rewards:** Money per kill, delivered when leaving or dying in the zone
- **Kill counter UI:** Tracks kills & potential cash reward
- **Respawn timer:** Teleports and revives at a random zone point after death
- **Killstreak announcements:** Milestones broadcast to all players in chat
- **Highly optimized, open-source, and easy to edit**

---

## 🧩 Dependencies

- [es_extended (ESX Legacy)](https://github.com/esx-framework/es_extended)
- [ox_lib](https://github.com/overextended/ox_lib)
- [ox_inventory](https://github.com/overextended/ox_inventory)
- [oxmysql](https://github.com/overextended/oxmysql)
- [esx_ambulancejob](https://github.com/esx-framework/esx_ambulancejob)

---

## 📥 Installation

1. **Download** the latest release from GitHub above.
2. **Extract** the `esx_redzone` folder to your server's `resources` directory.
3. **Add** `ensure esx_redzone` to your `server.cfg` **after all dependencies**.
4. **Edit** `config.lua` to set your redzone location, weapon, reward, etc.
5. **Restart your server.**

---

## ⚙️ Configuration

`config.lua` example:
```lua
Config = {}

Config.Zones = {
    Redzone = {
        center = vector3(-1474.455, -2716.211, 13.944),
        radius = 100.0,
        marker = {type=1, height=2.0, r=200, g=30, b=30, a=120},
        weapon = 'WEAPON_COMBATPISTOL',
        blip = {enabled = true, sprite = 161, color = 1, scale = 1.3, label = "Redzone"}
    }
}

Config.UseBucket = true -- true for FFA isolation
Config.RedzoneBucket = 5001
Config.KillReward = 50
Config.RespawnTime = 5
Config.ChatPrefix = "[Redzone] "
Config.KillstreakAnnounce = {5, 10, 15, 20, 25, 30, 40, 50}
Config.RespawnPoints = {
    vector3(-1411.407, -2806.361, 13.944),
    vector3(-1471.11, -2723.32, 13.94)
}
All options are explained in the config file comments.

💡 How It Works
Entering the redzone forces a weapon, gives infinite ammo, and puts the player into a private “bucket” for true FFA.

Players can only see/fight others in the redzone.

Kills are tracked; rewards are only given when the player dies or leaves the zone.

Killstreaks are announced in chat (5, 10, 15, etc).

Upon death, a respawn timer appears and the player is revived at a random zone point.

🛠️ Support & Contributions
Issues: Use the GitHub Issues tab.

PRs: Welcome!

Contact: Open a discussion or send a DM for help.

👤 Credits
Script by OnlyAlilSlow


---

**Let me know if you want any details added or changed!**  
You can also use this as your CFX post template.
