# ev.priseko.de

Serves the Tesla Fleet API partner public key for Home Assistant at
`/.well-known/appspecific/com.tesla.3p.public-key.pem`.

Static GitHub Pages site, nothing else. `.nojekyll` is required — without it
GitHub's Jekyll pass strips dot-directories and the key 404s.

The matching private key is NOT in this repo (`~/.tesla/fleet-private.pem`).
