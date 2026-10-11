# NumeroLogIA

Numerologie pitagoreică și chaldeană, cu analiză a ciclurilor, compatibilitate și un oracol IA opțional care rulează pe modelul tău local.

**Live:** https://chiuta.github.io/NumeroLogIA/

![Captura de ecran](screenshot.png)

## Ce este

NumeroLogIA calculează un „portret” numerologic pornind de la numele complet de la naștere, data nașterii și, opțional, ora nașterii. Aplicația folosește numerologia pitagoreică (cu opțiune chaldeană), păstrează numerele maestru 11/22/33 și marchează datoriile karmice 13/14/16/19; calculele sunt afișate pas cu pas. Aplicația precizează explicit că numerologia este un sistem simbolic tradițional, oferit pentru reflecție personală și explorare culturală, nu o știință.

## Funcții

- Interfață în 7 limbi: engleză, română, italiană, spaniolă, franceză, portugheză, catalană.
- Comutator de sistem **Pythagoras / Chaldean**; temă deschisă/închisă (butonul ◐); **⎙** pentru tipărire / salvare PDF.
- File: **Profil**, **Cicluri**, **Grila nașterii**, **Calculator nume**, **Compatibilitate**, **Universal & Referință**, **BaZi**, **Bioritm**, **IA**, **Salvate**.
- Butoane în Profil: **Dezvăluie portretul**, **Salvează portretul**, **Copiază link partajabil**, **Exemplu**, **Raport PDF**.
- Calculator de valoare numerică pentru orice nume sau cuvânt, defalcat literă cu literă (vocale și consoane), în ambele sisteme, și compararea a două nume (nume de scenă, după căsătorie, pseudonime).
- Compatibilitate între două persoane (Drumul Vieții, Expresia, Dorința Sufletului).
- Numerele universale ale zilei și o referință completă a numerelor.
- **Portrete salvate** în browser.
- **Oracol IA** (opțional): sinteză de portret, ghidaj pentru azi, interpretare de compatibilitate și întrebări libere, trimise către un model lingvistic la o adresă pe care o setezi tu (implicit Ollama local). Poate lista modele instalate și descărca modele prin Ollama.

## Manual de utilizare

1. Alege limba din lista de limbi și sistemul (Pythagoras sau Chaldean).
2. În „Profil”, introdu numele complet de la naștere (diacriticele sunt normalizate), data nașterii și, dacă vrei, ora; apasă **Dezvăluie portretul** (Enter în câmpuri face același lucru). **Exemplu** completează date demonstrative.
3. Parcurge filele Cicluri, Grila nașterii, BaZi și Bioritm pentru restul analizei.
4. Pentru un cuvânt oarecare, folosește „Calculator nume”; pentru două persoane, „Compatibilitate”.
5. **Salvează portretul** îl păstrează în fila „Salvate”; **Copiază link partajabil** pune în link numele, data, ora, limba și sistemul.
6. **Raport PDF** sau **⎙** deschid dialogul de tipărire al browserului, de unde poți salva PDF.
7. Pentru fila IA: instalează Ollama (sau alt server compatibil OpenAI), pornește un model, deschide „Setări”, verifică adresa (implicit `http://localhost:11434/v1`) și modelul, apasă salvare / test, apoi alege o acțiune. Dacă pagina este servită de pe un site, aplicația indică pornirea Ollama cu `OLLAMA_ORIGINS=*` pentru a permite conexiunea din browser.

## Avertisment

Conținut informativ/de divertisment, fără validare științifică: numerologia, BaZi, astrologia și bioritmul sunt sisteme simbolice tradiționale sau populare, nu științe, și nu oferă predicții sau sfaturi medicale, financiare ori juridice. Aplicația afișează o „Notă onestă" în subsol; textele generate de IA pot fi greșite sau inventate.

## Confidențialitate și rețea

- **Stocare locală (localStorage):** `numerologie_saved_v1` (portretele salvate), chei `num_pref_*` (limbă, sistem, temă) și `num_ai_*` (adresa, modelul și, dacă o introduci, cheia API a oracolului IA, stocată necriptat; aplicația afișează acum un avertisment vizibil sub câmpul „Cheie API” din Setările IA, în toate cele 7 limbi).
- **Rețea:** calculele numerologice nu fac cereri. Singurele cereri posibile sunt cele din fila IA, doar când apeși o acțiune IA (sau listare/descărcare de modele), către adresa configurată de tine, implicit `http://localhost:11434` (Ollama pe calculatorul tău). Dacă setezi o adresă la distanță, numele, datele și întrebările tale ajung la acel server. Aplicația nu include chei, analytics sau telemetrie și nu încarcă resurse de la terți; o politică CSP (`default-src 'none'`, `connect-src http: https:`) limitează paginii orice altă încărcare.
- Linkul partajabil conține în partea de după `#` numele și data introduse (hash-ul se actualizează la fiecare calcul, deci apare și în bara de adrese/istoricul browserului, dar nu este trimis niciunui server); mesajul de confirmare la copiere spune acum explicit că linkul conține numele și data nașterii; partajează-l conștient.

## Rulare locală / offline

Descarcă `index.html` și deschide-l în browser; numerologia funcționează fără internet. Oracolul IA are nevoie de un server de modele local (de exemplu Ollama) sau de o adresă la alegerea ta.

## Licență

Licență: nedeclarată de autor; toate drepturile rezervate până la o declarație contrară. Contact: alexio@trom.tf

License: not declared by the author; all rights reserved until stated otherwise. Contact: alexio@trom.tf

Aceeași declarație apare în antetul HTML și în subsolul aplicației (RO + EN). Nu există fișier LICENSE: alegerea unei licențe aparține autorului.

## Audit

Audit: 2026-10-10 — verificat cu Playwright și axe-core (toate filele, ambele teme); verificat în cod: un singur `fetch` (fila IA, la acțiune, către adresa configurată); numele din linkul `#n=` și din câmpuri, testat cu `<img onerror>`, nu se execută (escape). Corectate: etichete lipsă la câmpurile de dată/oră, contrast în tema luminoasă, nume accesibil la glisorul de bioritm.

## Autor

Alexio — Alexandru-Ionuț Chiuță. Contact: alexio@trom.tf

## English summary

NumeroLogIA is a single-file numerology tool (Pythagorean and Chaldean systems, master numbers, cycles, birth grid, name calculator, compatibility, BaZi, biorhythm) in 7 languages, with saved portraits in localStorage. An optional AI tab talks only to an endpoint you configure (default: local Ollama at localhost:11434); with a remote endpoint your inputs would be sent there. No telemetry or third-party resources. License: not declared by the author; all rights reserved until stated otherwise (contact: alexio@trom.tf).

Runda 3 (2026-10-11): declarație explicită de licență nedeclarată (antet, subsol, README); adăugat CSP; tema esoterică și stocarea cheii API rămân decizii ale autorului.
