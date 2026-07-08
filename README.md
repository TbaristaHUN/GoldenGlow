Golden Glow – Fodrászat & Kozmetika Weboldal

Egy modern, letisztult és reszponzív bemutató és online időpontfoglaló weboldal a debreceni Golden Glow szépségszalon számára. A projekt célja egy prémium felhasználói élményt nyújtó, gyors és regisztrációmentes foglalási folyamat biztosítása a vendégek számára, miközben minimalizálja az adminisztrációs terheket a szalon dolgozói számára. 

Projekt Célkitűzés & MVP Logika

A weboldal fejlesztése során az **MVP (Minimum Viable Product)** szemléletet követtem. Bonyolult háttérrendszerek (adatbázisok, felhasználói fiókok kezelése, GDPR-kockázatos jelszókezelés) helyett egy kliensoldali, API-vezérelt hibrid architektúrát alkalmaztam.

A foglalási folyamat logikája:
1. **Szolgáltatás kiválasztása:** A vendég az árlapon checkboxok segítségével összeválogatja a kívánt kezeléseket.
2. **Dinamikus kalkuláció:** A JavaScript (DOM) valós időben számolja a végösszeget és összesíti a kiválasztott elemeket.
3. **Regisztrációmentes checkout:** A vendég megadja a nevét és telefonszámát egy biztonságos, írásvédett (`readonly`) űrlapon.
4. **API Kommunikáció:** Az adatok megerősítése után a háttérben egy **Axios HTTP POST** kérés továbbítja az adatokat egy külső API szolgáltatónak, amely azonnali formázott e-mail értesítést küld a szalon munkatársainak.

Alkalmazott Technológiák

Frontend:
HTML5: Szemantikus struktúra, tiszta dokumentum-hierarchia és egyedi `data-` attribútumok az adatátvitelhez.
CSS3: Egyedi arculat design, flexbox elrendezések és médialekérdezések (`@media`) a teljes mobil-reszponzivitás érdekében.
Vanilla JavaScript: Kliensoldali üzleti logika, DOM manipuláció és eseménykezelés (`addEventListener`) - (fejlesztés alatt).

Hálózat és API:
Axios (CDN): Ígéret-alapú (Promise-based) HTTP-kliens a külső API-kkal való aszinkron kommunikációhoz (fejlesztés alatt).

---

Jelenlegi Fejlesztési Állapot (Elvégzett feladatok)

1. Oldalstruktúra és Navigáció
Elkészült a teljes moduláris felépítés: Főoldal (`index.html`), `szolgaltatasok.html`, bemutatkozó oldal (`rolunk.html`) és a dedikált foglalási felület (`form.html`).
Kialakításra került az egységes, reszponzív footer a közösségi média ikonokkal és linkekkel.

2. Arculati Konzisztencia (UI/UX)
Integrálásra kerültek a Google Fonts betűcsaládjai (*Cinzel* a prémium hatású főcímekhez, *Fira Sans* a jól olvasható form-szövegekhez).
A globális és lokális CSS stílusok szinkronizálásával a foglalási oldal is megkapta a szalonra jellemző arany arculatot (`rgb(245, 243, 160)`), text-shadow effektusokat és a letisztult kártya-alapú űrlap elrendezést.

3. Biztonságos Adatbekérés
Elkészült a foglalási űrlap kliensoldali validációja (`required` attribútumok).
A *Választott szakember* és *Választott szolgáltatás* mezők `readonly` védelmet kaptak, hogy a felhasználó ne tudjon manuálisan hibás adatot bevinni – ezeket a JS automatikusan fogja tölteni.

Ütemterv (Következő lépések)

Lokális Adatbázis felépítése (JS):** A fodrászati és kozmetikai szolgáltatások, árak és szakemberek strukturálása JavaScript objektumtömbökbe.
DOM és Form összekötés:** Checkbox eseményfigyelők lefejlesztése, amelyek automatikusan feltöltik a `readonly` input mezőket a kiválasztott elemekkel.
Végösszeg-kalkulátor:** Dinamikus matematikai logika implementálása a kiválasztott elemek árai alapján.
Axios POST integráció:** Az aszinkron HTTP kérés megírása az űrlap elküldéséhez és az e-mail API triggereléséhez.

Lokális futtatás

1. Klónozd a repót:
   git clone (https://github.com/TbaristaHUN/GoldenGlow.git)

<img width="1920" height="1243" alt="Képernyőfotó 2026-07-08 - 20 35 25" src="https://github.com/user-attachments/assets/ea22818c-62ce-47b6-a0f6-c55d48a81a31" />