# Jurnal de modificări — NumeroLogIA

## 2.0.1 — 2026-11-02 (reîmprospătare kit)

- Nou (kit): **Sincronizare între dispozitive** (`FFF.sync`) — în dialogul «Transparență» (clic pe versiune → Copie de siguranță): conectezi două dispozitive direct (WebRTC, cod/QR, fără server și fără cont) și își schimbă datele aplicației; cea mai recentă valoare câștigă, secretele (chei API, parole) nu se trimit, ștergerile nu se propagă. Aplicarea trece prin importul kitului (confirmare, chei permise, rollback).
- Nou (kit): **Istoric local — «mașina timpului»** (`FFF.history`) — instantanee automate ale datelor (IndexedDB, fără secrete), diferență față de starea curentă și restaurare reversibilă; «Șterge datele aplicației» șterge și istoricul.
- Module adăugate: `qr`, `p2p`, `sync`, `history` (+~140 KB). Versiunea aplicației nu se schimbă.

## 2.0.1 — 2026-10-27 (anterior: 2.0.0)

Doar texte, fără funcții noi.

- Notă „unealtă vs. curs” în partea de jos a aplicației (9 limbi), cu link reciproc către Numerologie.
- README: „Stare” și „Offline” (8 limbi) și secțiunea despre diferență.

Nu implementat:

- Unificarea aplicațiilor: NU s-a făcut (regulă: nu se fuzionează aplicații); doar explicație + linkuri reciproce.

Istoricul anterior (1.x–2.0.0) este în secțiunea „History” din README.md.
