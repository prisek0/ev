# ev.priseko.de

Serves the Tesla Fleet API partner public key for Home Assistant at
`/.well-known/appspecific/com.tesla.3p.public-key.pem`.

Static GitHub Pages site, nothing else. `.nojekyll` is required — without it
GitHub's Jekyll pass strips dot-directories and the key 404s.

**The key belongs to Home Assistant.** The Tesla Fleet integration generates
its own EC key pair and keeps the private half in HA's storage; this repo only
hosts the public half, which HA displays during setup. Do not replace it with a
locally generated key — Tesla compares what is served here against the key HA
holds, and a mismatch fails setup with "Der in deiner Domain gehostete
öffentliche Schlüssel passt nicht zum erwarteten Schlüssel".

If HA is ever reinstalled or the integration re-added from scratch, it may
generate a new pair; re-copy the public key it shows into this repo.
