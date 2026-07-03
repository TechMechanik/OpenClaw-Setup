# TOOLS.md - Local Notes

Skills define _how_ tools work. This file is for _your_ specifics — the stuff that's unique to your setup.

## Homelab

### Unraid NAS

- Host: Unraid NAS (name TBD)
- Spec: i7-12700K, 64GB RAM, RTX 3060 12GB (used for Ollama inference — qwen3:14b)
- Services: arr stack, Immich, Jellyfin, Navidrome, Audiobookshelf, AzuraCast, Home Assistant, AMP, Vaultwarden, Syncthing
- Lightroom RAW share used by Lightroom Classic workflow

### Network

- UDM Pro, 10.0.x.0/24 scheme
- VLANs: Mgmt/1, Trusted/10, IoT/20, Servers/30, Work/40, Guest/50

### Gaming/Dev Desktop

- Spec: Ryzen 7800X3D, RX 9070 XT (16GB), 32GB DDR5, Samsung 32" Odyssey G8 OLED
- Planned: rebuild on Ubuntu 26.04 LTS (see memory/projects/linux-desktop-rebuild.md)

### Photography

- Camera: Sony A7 II
- Editing: Lightroom Classic on a refurbished M1 MacBook Pro
- Blog: self-hosted Ghost ("lumen" theme), auto EXIF injection per post

### Naming Convention

- Personal/homelab systems: IT-style, role-based names (LOTR/Middle-Earth theming retired)
- UUFFXBG systems: role-based names only, never themed — kept fully separate from personal naming

### Domains

- techmechanik.com — personal/professional brand
- nullpointlabs.net — homelab, via Cloudflare

## Messaging / Bot

- Telegram: Lyra (assistant's primary interface) — token/config TBD
- Eric's Telegram: @TechMechanik
- Eric's Signal: Techmechanik.16
- Eric's Discord: techmechanik

## Security

- Password manager: Bitwarden, self-hosted Vaultwarden container
- Auth: YubiKeys and passkeys preferred over passwords

## AI Providers

- Local: Ollama on Unraid (qwen3:14b, RTX 3060 12GB)
- Cloud: Anthropic API (alternative/fallback provider)
- Routing policy: TBD — decide based on task sensitivity/complexity (see memory/projects/openclaw-deployment.md)

## UUFFXBG (Volunteer)

- Google Workspace for Nonprofits — super admin
- Manages: Shared Drives, Google Groups, GCPW rollout, OU structure
- Also: cybersecurity workshops, OBS streaming for Sunday services, event sound

## Not Yet Filled In

- Specific SSH hostnames/IPs for Unraid, UDM Pro, and other hosts
- Camera locations (if home cameras are added later)
- TTS voice / speaker preferences (not in use yet)

---

Add whatever helps you do your job. This is your cheat sheet.
