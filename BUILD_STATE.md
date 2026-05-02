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

1. Build private internal dashboard
   - Links to pool controller
   - Links to irrigation/controller devices
   - Status-only first
   - No public exposure

2. Add friendly names
   - Pool
   - Irrigation
   - Controller builder
   - Gateway Pi
   - Future LogicalLink devices

3. Later
   - Cloudflare contact/email relay
   - Public site polish
   - Favicon/logo
   - Mobile refinements
   - Better company copy

## Rules

- Public website must never expose private IPs or controller controls.
- Private dashboard is only accessible through Tailscale/VPN.
- Keep public marketing and private control separated.
- No port forwarding to controllers.
- No controller control from public website.