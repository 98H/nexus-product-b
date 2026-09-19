# Deployment & Operations Guide: Product B

## 🚀 Live Access & URLs
- **Live Public Access URL:** [/preview/prod-product-b-eff20b/](/preview/prod-product-b-eff20b/)
- **Internal Port:** `0`
- **Runtime Engine:** `python_preview`
- **Deployment Status:** `DEPLOYED / ACTIVE`
- **Timestamp:** `2026-09-19T21:12:19.041589+00:00`

## 🛠️ Management & Service Control
### Launch Command
```bash
python3 app.py --port 0
```

### Health Check Probe
```bash
curl -I http://127.0.0.1:0/
```

### Systemd Service Template
```ini
[Unit]
Description=Product B Service
After=network.target

[Service]
Type=simple
WorkingDirectory=/tmp/pytest-of-root/pytest-0/test_multi_product_execution_s0/workspaces/prod-product-b-eff20b
ExecStart=/usr/bin/python3 /tmp/pytest-of-root/pytest-0/test_multi_product_execution_s0/workspaces/prod-product-b-eff20b/app.py
Restart=always
RestartSec=3

[Install]
WantedBy=multi-user.target
```

## 🔒 Production Security Protocols
- HTTP-only reverse proxy via Nexus Gateway.
- Dedicated port allocation with zero port conflict.
