# Self-Curator · Beta Landing

Passwort-geschuetzte Landing-Page fuer den Walking-MVP-Pilot (5 Creator + 3 Coaches).

- **Live:** https://noiion828-ui.github.io/self-curator-beta/
- **Passwort:** siehe persoenliche Einladungs-Mail (Hinweis: 1 Wort, Bezug zur H1)
- **Source-Landing:** `~/projects/self-curator/app/landing.html` (unverschluesselt, nicht deployen)

## Anti-Discovery-Schicht

- `<meta name="robots" content="noindex, nofollow, noarchive">`
- `robots.txt` blockt alle Crawler
- JS-Password-Gate (clientseitig, keine Sicherheit gegen Determined Attacker — bewusste Friction, kein Schutz sensibler Daten)

## Waitlist-Flow

1. User gibt Email ein
2. localStorage speichert Email (nur fuer Live-Counter)
3. `window.location.href = mailto:...` oeffnet User-Mail-Client mit pre-filled Body
4. Owner (`noiion828@gmail.com`) bekommt Mail, antwortet persoenlich

Keine Server-Infrastruktur noetig — funktioniert mit reinem GitHub-Pages-Hosting.

## Deploy

```bash
git push origin main
# GitHub Pages aktiviert sich auf main / root
```

## Roadmap

- [ ] Formspree-Endpoint falls Mailto-Fallback zu viel Drop-off
- [ ] Screenshot-OG-Image fuer Sharing
- [ ] A/B-Hero-Variante B aktivieren (Kommentar im HTML)
- [ ] Testimonial-Integration nach Pilot-Woche 2
