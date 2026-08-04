# Tokyo Yamathon — participant app prototype

A clickable, front-end-only prototype of the participant app for the Tokyo Yamathon Trek,
built for internal team review. Open `index.html` in any browser to walk through it.

## What it demonstrates

- **Sign in** — enter a bib number (or scan a team card), then confirm the matched team.
- **Which way are you trekking?** — Full and Half teams choose clockwise or counter-clockwise;
  Half-a-Half is clockwise only. The choice reorders the whole station track.
- **Track** — a scrollable list of all 30 Yamanote stations between the Tokyo TOKIA start and
  finish, with leg distances, an overall 0–30 progress meter, a QR check-in button, and a pacing
  panel (projected finish vs. the cutoff). Pressing "Scan station QR" simulates a check-in.
- **Notifications** — two separate streams, "My trek" (the team's own check-ins and milestones)
  and "Yamathon" (organizer broadcasts such as weather and logistics).
- **Completion** — a "finisher pass" confirming all 30 stations, with share and PDF actions.
  Deliberately *not* a certificate: official times and rankings are issued after the event.
- **Profile** — team identity, members, settings, and a **Safety** section with:
  - **Emergency help** — one tap to call or text IVG with the team and last location.
  - **Withdraw** — a dignified, reversible drop-out flow (reason → confirm → 10-minute undo →
    a warm "thank you for taking part" summary, recorded as withdrawn rather than completed).
- **Light / dark** — a toggle in the top-right corner.

## Scope and caveats

This is a **visual prototype only**. All data is hard-coded (team "Traveling Wilburys", bib 142),
nothing is saved, and nothing talks to a server. It exists so the team can click through the
experience and leave feedback before real development begins.

Planned production stack (not in this prototype): a Next.js PWA on Vercel, Supabase for data,
storage and auth, WebScorer for the registration roster, and QR + GPS geofence check-ins.

## Viewing

- **Locally:** open `index.html` in Chrome, Safari, or Edge.
- **Shared link:** hosted with GitHub Pages (see the repo's Pages settings for the URL).

Icons and styling render in a real browser. Some in-app preview panes strip inline SVG, so if
icons look missing, open the page in an actual browser tab.
