# vpn-education
vpn-education
1) Generate PASSWORD_HASH for wg-easy:
docker run --rm -it ghcr.io/wg-easy/wg-easy wgpw "YOUR_PASSWORD"

2) RF admin panel with QR generation:
- file: `wg-one/docker-compose.yml`
- run: `docker compose -f wg-one/docker-compose.yml up -d`
- open: `http://RF_SERVER_IP:51822`
- in UI click "New Client" and show QR for phone WireGuard app

3) Current uplink chain (already configured):
- `xray-client/*` on RF -> `xray-server/*` on US
- phone connects to RF wg-easy endpoint (`WG_HOST=91.188.215.79`, UDP 51823)

