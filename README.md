# Greutatea mea — Telegram Mini App

Aplicație dintr-un singur fișier (`index.html`, fără build și fără dependențe) pentru monitorizarea zilnică a greutății.

## Funcții
- Adăugare/editare/ștergere cântărire zilnică (cu dată și notiță), butoane ±0.1
- Grafic al evoluției (7z / 30z / 3 luni / 1 an / tot) cu medie mobilă 7 zile și linie de obiectiv; tooltip la atingere
- Obiectiv: greutate țintă, start, dată țintă opțională → progres %, estimare dată atingere, ritm necesar/săptămână
- Statistici: total schimbat, medie 7 zile, min/max, ritm săptămânal, zile consecutive, IMC
- kg / lb, temă automată din Telegram, feedback haptic, export CSV (clipboard)
- Date salvate în **Telegram CloudStorage** (sincronizate între dispozitive, împărțite pe luni din cauza limitei de 4096 caractere/cheie); în afara Telegram se folosește `localStorage`

## Publicare
Telegram cere HTTPS. Încarcă `index.html` la oricine servește static (GitHub Pages, Netlify, Vercel, Cloudflare Pages). Pentru test local:

```bash
python3 -m http.server 8765
cloudflared tunnel --url http://localhost:8765   # dă un URL https
```

## Conectare la bot
1. În [@BotFather](https://t.me/BotFather): `/newbot` (dacă nu ai deja un bot).
2. `/mybots` → botul tău → **Bot Settings → Menu Button → Configure menu button** → trimite URL-ul https și un titlu (ex. „Greutate”).
3. Opțional, Mini App direct link: `/newapp` și alege botul → primești `t.me/<bot>/<app>`.

Deschide botul și apasă butonul de meniu.
