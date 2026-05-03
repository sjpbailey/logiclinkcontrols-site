# LogicLinkControls Site — Build State

## Done

- Created public GitHub repo: `logiclinkcontrols-site`
- Added initial `index.html`
- Published with GitHub Pages
- Connected custom domain:
  - `https://logiclinkcontrols.com`
- DNS hosted at Cloudflare
- HTTPS enforced in GitHub Pages
- Public website is informational only
- No controller access exposed publicly
- Tailscale private access tested and working
- One Tailscale gateway Pi is used for private LAN access
- Pool/controller access works through private Tailscale route

## Current Architecture

### Public
- `logiclinkcontrols.com`
- Hosted on GitHub Pages
- DNS managed by Cloudflare
- Public site is marketing/info only

### Private
- iPhone → Tailscale → gateway Pi → LAN devices
- Controllers remain private on `192.168.1.x`
- No port forwarding
- No public control links

## Next

# LogicalLink Controls — Build State

## Current Status
- Public site live (GitHub Pages + domain)
- Private dashboard running on Pi (.7) via Tailscale
- Controllers reachable:
  - Pool Controller (.169)
  - LL4TR4AO8UI (.5)
  - LL8BO4AO16DI (.60)
  - LL4BO4UI (.61, .62)
- Sequent Microsystems review submitted

---

## Architecture
- Public site = informational only (no control)
- Private dashboard = control links (Tailscale only)
- Controllers = BACnet + Python backend + web UI
- Remote access = Tailscale VPN (no port forwarding)

---

## Next Steps (Short Term)
- Add “Controllers” section to public site
- Clean mobile layout (iPhone)
- Standardize controller ports (8099 / 8081)
- Improve dashboard labels

---

## Next Steps (Mid)
- Demo/read-only controller pages (public)
- Contact/email setup (Cloudflare later)
- Clean screenshots for presentation
- Prepare for Sequent follow-up

---

## Hardware Direction
- Using Sequent HAT stack
- Building BACnet-first controller platform
- Future:
  - Custom/OEM board
  - LogicalLink hardware spec (LL boards)

---

## Notes
- No public control endpoints
- Local-first control is required
- Remote = secure only (VPN)

## Rules

- Public website must never expose private IPs or controller controls.
- Private dashboard is only accessible through Tailscale/VPN.
- Keep public marketing and private control separated.
- No port forwarding to controllers.
- No controller control from public website.