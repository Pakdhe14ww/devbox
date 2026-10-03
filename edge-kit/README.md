# edge-kit — inti mesin

Modul yang dipakai runner pada `sync-views.yml`.

| Berkas | Fungsi |
|---|---|
| `relay_engine.py` | mesin utama — `python3 relay_engine.py "<tautan>"` |
| `profile_spoof.py` | profil perangkat per negara |
| `proxy_config.py` | parser konfigurasi proxy + profil perangkat |
| `proc_cleanup.py` | pembersihan proses ter-scope (tanpa kill by-name) |

Keluaran JSON: `{"ok": true, "final": "<tujuan>", "clicks": N, ...}`.
`relay_engine.py` membaca `proxies.txt` di direktori kerja (satu proxy per baris,
format `user:pass@host:port`); tanpa berkas itu koneksi langsung.
