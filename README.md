# Pitwall Compact

A local proxy for Claude Code's API traffic that compacts long conversations with a local model through Ollama, so long sessions send fewer tokens. Claude Code keeps the whole conversation on screen; only what goes to the API changes. On any problem a request passes through untouched. It listens on 127.0.0.1 only.

## Install

The Pitwall installer sets it up when you choose it (`--compact` / `-Compact`, or its box in the full-screen installer) and keeps it updated:

```bash
curl -fsSL https://github.com/ParendumOU/pitwall-bootstrap/releases/latest/download/install.sh | bash -s -- --compact
```

```powershell
& ([scriptblock]::Create((irm https://github.com/ParendumOU/pitwall-bootstrap/releases/latest/download/install.ps1))) -Compact
```

By hand: download `pitwall-compact-<version>.tar.gz` from a release, check it against `SHA256SUMS`, unpack it, run `python3 pitwall_compact.py` (Python 3.8 or newer, standard library only) and point Claude Code at it with `python3 configure.py http://127.0.0.1:8887`.

## More

Website: https://pitwall.parendum.com

License: MIT (see [LICENSE](LICENSE)). Each release includes its full source.
