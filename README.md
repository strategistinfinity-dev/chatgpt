# Car Wrap Calculator (Web)

A simple browser-based calculator for estimating car wrap material usage, labor, and pricing.

## Run locally

### Option 1: Python (quickest)

```bash
cd /workspace/chatgpt
python3 -m http.server 8000
```

Then open:

- http://127.0.0.1:8000/index.html

### Option 2: Open file directly

You can also open `index.html` directly in a browser by double-clicking it.

## How to check it works

1. Load the page and confirm you see **Car Wrap Calculator**.
2. Click **Calculate** with defaults and verify values are populated (not zero).
3. Change fields like `Vehicle type`, `Quantity`, and `Labor rate` and confirm totals update.
4. Click **Reset** and verify values return to defaults.

## CLI smoke check

Use this quick command to verify local serving and page availability:

```bash
cd /workspace/chatgpt
python3 -m http.server 8000 >/tmp/wrapcalc.log 2>&1 &
PID=$!
sleep 1
curl -I http://127.0.0.1:8000/index.html
kill $PID
```

Expected result: an HTTP status like `200 OK`.
