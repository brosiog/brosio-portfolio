# logical map

```
┌─────────────────────────────────────────────────────────┐
│ Remote Tailscale Network Devices (Phone, Laptop)        |
└────────────────────┬────────────────────────────────────┘
┌────────────────────▼────────────────────────────────────┐
│  UniFi Network (VLANs, Firewall)                        │
└────────────────────┬────────────────────────────────────┘
                     │
┌────────────────────▼────────────────────────────────────┐
│ Subnet Router (Tailscale)                               │
└────────────────────┬────────────────────────────────────┘
                     │
┌────────────────────▼────────────────────────────────────┐
│  Infrastructure Layer                                   |
|  ├─Reverse Proxy (Caddy)                                |  
|  ├─DNS, Local Resolution (Dnsmasq)                      |  
│  └─DNS, Filtering (AdGuard Home)                        |  
└────────────────────┬────────────────────────────────────┘
                     │
┌────────────────────▼────────────────────────────────────┐
│  Application Layer                                      │
│  ├─ Files (Jellyfin, Samba)                             │
│  ├─ Apps (Crafty Controller, OpenWebUI, Ollama)         │
│  └─ Planned (Openclaw, Epic Games, Game Sync, Wazuh)    │
└─────────────────────────────────────────────────────────┘

```

