# crafty controller - *craftycontroller.home.arpa*
- used to manage a minecraft 26.1.2 server
- can handle 10 concurrent players
- plugins:
	- GeyserMC - allows players to play on the same server with different versions of the game (Java/Bedrock)
	- PaperMC - enables a more stable and secure Minecraft server
# epic games
- automatically claims Epic's weekly free games
- WIP
# local game sync
- DIY project to sync game saves across multiple devices on a local network
- intended for games with simple save files, such as emulated games, minecraft worlds, etc
- WIP
```
            On System Start Workflow - local game sync

                              ┌───────┐
                              │ Start │
                              └───┬───┘
                                  │
                                  ▼
                  ┌─────────────────────────────┐
                  │ Find and store local /      │
                  │ network saves               │
                  └───────┬───────────┬─────────┘
                          │           │
                          │           │
                          ▼           ▼

                 Network save    Network save
                     older           newer
                          │           │
                          ▼           ▼

            ┌──────────────────┐   ┌──────────────────┐
            │ Push local save  │   │ Backup local     │
            │ to network       │   │ save             │
            └────────┬─────────┘   └────────┬─────────┘
                     │                      │
                     ▼                      ▼

            ┌──────────────────┐   ┌──────────────────┐
            │ Make a backup of │   │ Pull network     │
            │ the network save │   │ save to local    │
            └────────┬─────────┘   │ folder           │
                     │             └────────┬─────────┘
                     │                      │
                     ▼                      ▼

                 Backups > 5 ?         Backups > 5 ?
                       │                    │
                  Yes ─┘                    └─ Yes
                       │                    │
                       ▼                    ▼

            ┌──────────────────┐   ┌──────────────────┐
            │ Delete oldest    │   │ Delete oldest    │
            │ backup           │   │ backup           │
            └──────────────────┘   └──────────────────┘
```	
