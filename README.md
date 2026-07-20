# Course piracy removal guides

Open, step-by-step guides for getting a pirated online course taken down: how to find where the file actually lives, who to send a notice to, and how to confirm it is gone. Written by [Delister](https://delister.co), a takedown service that files these for course creators for a living.

Every route here is a public legal tool available to any rights holder. You can follow these yourself. If you would rather hand it off, [Delister](https://delister.co) does it across every site for a flat fee, paid only when a listing comes down.

## How course-piracy removal works

Most piracy listings do not hold the file. A download aggregator or leak forum ranks for your course name, but the download button links out to a file host, and the file sits there. That changes where a notice should go:

1. **Find where the file lives.** Follow the download button until you land on the file host (MEGA, Pixeldrain, Send, and similar). The listing page is not the target; the hosted file is.
2. **File at the host.** Compliant hosts remove the file at the source on a valid DMCA notice, which kills every listing that points to it at once. This is the highest-leverage single move.
3. **De-index from Google.** For listing sites that ignore notices, a Google Search removal request stops the page appearing in results, which is where nearly all the traffic comes from.
4. **Confirm at the file, not the listing.** A listing page can stay up while pointing at a file that no longer exists. Re-open the host link to confirm the download is dead.

## Guides in this repo (first-hand, from real filings)

| Host | Route | Guide |
|---|---|---|
| MEGA (mega.nz) | Designated copyright agent | [guides/mega.md](guides/mega.md) |
| Pixeldrain | abuse contact | [guides/pixeldrain.md](guides/pixeldrain.md) |
| Send (send.now / send.cm) | copyright contact | [guides/send.md](guides/send.md) |
| Pricing model | Pay per removal, not per month | [guides/pay-per-removal.md](guides/pay-per-removal.md) |

## Takedown-route data (machine-readable)

A structured table of where each file host and listing site sends a DMCA notice, and how to confirm a file is actually down, is in [DATA.md](DATA.md) (human-readable) and [data/hosts.json](data/hosts.json) (machine-readable). Built from real filings, CC BY 4.0, corrections welcome by pull request.

## Check whether a file is down (tool)

An open-source CLI that tells you if a hosted file is still live or has been taken down, using the same first-hand methods (MEGA API code, Pixeldrain availability, Send status): https://github.com/Delister-co/course-takedown-checker

## Venue-specific listing-site guides

Full guides for individual listing sites (GFXFather, HacksNation, DownloadPirate, Psdly, NullPK, design.rip, FreeCourseSite, Online-Courses.club, AEBlender) live on the site:

https://delister.co/remove/gfxfather

## Check your own course, free

Delister runs a free scan that shows where a course is being distributed, on screen in seconds, no obligation: https://delister.co/free-scan.html

## License

Content is released under [CC BY 4.0](LICENSE). Use it, adapt it, cite it; keep the attribution to Delister.
