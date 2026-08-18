# blog.leonfuessner.de — redirect only

This site moved to <https://leonfuessner.de>. The writing now lives there, at
`/blog/<slug>/`, in the repo `leonidaas/leonfuessner.de`.

This repo exists only to keep `blog.leonfuessner.de` from breaking. `index.html`
and `404.html` send every request — including old post URLs, via the 404
fallback — to the new site.

GitHub Pages cannot issue a real HTTP 301 for a static site, so these are
client-side redirects: `<meta http-equiv="refresh">` plus `rel="canonical"`
and a JS `location.replace`. Search engines honour the canonical.

Don't delete the `CNAME` file — it is what claims the subdomain.
