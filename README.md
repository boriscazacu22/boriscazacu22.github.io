# Greutatea mea — Telegram Mini App

Aplicație dintr-un singur fișier (`index.html`, fără build și fără dependențe) pentru monitorizarea zilnică a greutății.

## Funcții
- Adăugare/editare/ștergere cântărire zilnică (cu dată și notiță), butoane ±0.1
- Grafic al evoluției (7z / 30z / 3 luni / 1 an / tot) cu medie mobilă 7 zile și linie de obiectiv; tooltip la atingere
- Obiectiv: greutate țintă, start, dată țintă opțională → progres %, estimare dată atingere, ritm necesar/săptămână
- Statistici: total schimbat, medie 7 zile, min/max, ritm săptămânal, zile consecutive, IMC
- kg / lb, temă automată din Telegram, feedback haptic, salut cu numele din Telegram (sau setat manual)
- Import și export CSV (copiere, descărcare, fișier sau text lipit)
- Date salvate în **Telegram CloudStorage** (sincronizate între dispozitive, împărțite pe luni din cauza limitei de 4096 caractere/cheie); în afara Telegram se folosește `localStorage`
