# Course-piracy takedown routes (data)

Where a pirated online course actually lives, and how to get it removed. First-hand routes and confirmation methods from real filings by [Delister](https://delister.co). Machine-readable version: [data/hosts.json](data/hosts.json). Licensed CC BY 4.0, so cite or reuse it with attribution. Corrections and new hosts welcome by pull request.

**Confirm a removal at the file, not the listing.** A listing page can stay up while pointing at a file that is already dead. Some ISPs also intercept piracy domains and serve a block page with HTTP 200, so a raw request can read "still live" when the site is unreachable or already down. On such a network, verify through a server-side text proxy (for example `https://r.jina.ai/<url>`) and resolve DNS over HTTPS rather than the local resolver.

## File hosts

| Host | Domains | DMCA route | How to confirm it is down | Typical response |
|---|---|---|---|---|
| MEGA | mega.nz | copyright@mega.io (designated agent) | MEGA API `POST g.api.mega.co.nz/cs?n=<handle>` body `[{"a":"f"}]` -> `-16` blocked, `-9` deleted, JSON = live | days |
| Pixeldrain | pixeldrain.com | abuse@pixeldrain.com (say "copyright infringement notice", links in body, no attachments) | `GET pixeldrain.com/api/file/<id>/info` -> `availability: unavailable_for_legal_reasons`; download returns HTTP 451 | first report reviewed by hand, then sender is whitelisted |
| Send | send.now, send.cm | copyright@send.now (plain-text, seven DMCA elements) | file URL shows "The file you were looking for" | days |
| Podaon SIA | gfxdrive.com | abuse@podaon.com (RIPE abuse contact; EU/DSA duties) | fetch via proxy (see note above) | unconfirmed |

## Listing sites

| Site | Domains | DMCA route | How to confirm it is down | Typical response |
|---|---|---|---|---|
| design.rip | design.rip | https://design.rip/dmca | listing returns HTTP 404 | days |
| Psdly | psdly.co.uk / .com / .io / .net (same site) | admin@psdly.com or the site's DMCA form | listing gone | slow / may not respond |

## Search and CDN layers

| Layer | Route | How to confirm | Notes |
|---|---|---|---|
| Google Search removal | https://dmca.google.com | Google Removals Dashboard, not a live-search spot-check | a URL with a settled counter-notice returns "Reinstated" and will not re-remove on a fresh notice |
| Cloudflare abuse | https://abuse.cloudflare.com/dmca | acknowledgment email with a case ID | forward-only: Cloudflare relays to the origin host and does not itself remove content |

## Not actionable by notice

| Case | Why |
|---|---|
| Torrents / magnet links | no host holds a file to notice; the content moves peer to peer. Notice-and-takedown does not apply. |

---

Want this done for you across every site a course turns up on, paid only when a listing actually comes down? That is what [Delister](https://delister.co) does, $79 per course on success.
