# AdGuard Home - *adguard.home.arpa*
- used to block
	- unnecessary telemetry
	- intrusive ads (especially on devices where a traditional adblocker cannot be installed)
	- untrustworthy websites
# Caddy 
- routes all incoming traffic to either 
	- AdGuard Home
	- Dnsmasq
- implemented at the request of my girlfriend, who did not appreciate AdGuard's tendency to break her favorite websites
# Dnsmasq
- handles DNS resolution
# Tailscale
- used for secure remote access to the local network 
- only trusted devices are allowed in the Tailnet
# VLANs and Subnets
- WIP