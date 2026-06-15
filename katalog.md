## 1. Funkční požadavky
Funkční požadavky definují, co má systém dělat, jaké funkce nabízí uživatelům a jak se má chovat v konkrétních situacích.

### 1.1 Správa a zobrazení menu
* **FR-01: Zobrazení denního menu** – Systém musí pro každý všední den (pondělí až pátek) zobrazit nabídku přesně 3 obědů.
* **FR-02: Detail oběda** – U každého z 3 obědů musí být zobrazeny následující informace:
  * Označení jídla (např. Oběd 1, Oběd 2, Oběd 3).
  * Přesné datum, kdy bylo jídlo podáváno.
  * Reálná fotografie/obrázek daného oběda.
* **FR-03: Historie menu** – Uživatelé musí mít možnost procházet menu z předchozích dnů (archiv).

### 1.2 Hodnocení a zpětná vazba
* **FR-04: Rychlé hodnocení (Palce)** – Uživatel musí mít možnost udělit každému obědu hodnocení "palec nahoru" (pozitivní) nebo "palec dolů" (negativní).
* **FR-05: Změna/Zrušení hodnocení** – Uživatel musí mít možnost své již udělené hodnocení (palec) změnit nebo zrušit.
* **FR-06: Slovní komentáře** – Uživatel musí mít možnost přidat k libovolnému obědu textový komentář (nepovinné rozšíření k palcům).
* **FR-07: Agregované výsledky** – Systém musí u každého obědu zobrazovat celkový počet palců nahoru a dolů pro všechny uživatele (např. v procentech nebo absolutním číslem).

### 1.3 Administrace a správa obsahu (Pro správce/jídelnu)
* **FR-08: Nahrávání menu a fotografií** – Administrátor (nebo pověřená osoba) musí mít rozhraní pro zadání textu jídla, data a nahrání reálné fotografie oběda.
* **FR-09: Moderování komentářů** – Administrátor musí mít možnost smazat komentáře, které porušují pravidla slušného chování.

---

## 2. Nefunkční požadavky (Non-functional Requirements)
Nefunkční požadavky definují vlastnosti systému, jako je výkon, bezpečnost, spolehlivost a uživatelské rozhraní.

### 2.1 Výkon a dostupnost (Performance & Availability)
* **NFR-01: Dostupnost systému** – Systém by měl být dostupný 24/7 s minimální dostupností 98 % v průběhu školního roku.
* **NFR-02: Rychlost odezvy** – Načtení denního menu včetně obrázků nesmí na běžném mobilním připojení (4G/5G) trvat déle než 2 sekundy.
* **NFR-03: Optimalizace obrázků** – Nahrané fotografie obědů musí systém automaticky komprimovat a optimalizovat pro web, aby se šetřily mobilní data studentů.

### 2.2 Kompatibilita a responzivita (Usability & Compatibility)
* **NFR-04: Mobile-First Design** – Uživatelské rozhraní musí být plně responzivní. Primárním cílovým zařízením je chytrý telefon (studenti hodnotí přímo v jídelně).
* **NFR-05: Podpora prohlížečů** – Aplikace musí správně fungovat ve všech moderních webových prohlížečích (Chrome, Safari, Firefox, Edge).

### 2.3 Bezpečnost a ochrana dat (Security)
* **NFR-06: Omezení vícenásobného hlasování** – Systém musí technicky zajistit, aby jeden uživatel nemohl u jednoho obědu kliknout na palec tisíckrát a zkreslit tak výsledky (např. pomocí vazby na školní Google/Microsoft účet, cookies, nebo IP adresu).
* **NFR-07: Bezpečný protokol** – Veškerá komunikace mezi uživatelem a serverem musí být šifrována pomocí protoklu HTTPS.
* **NFR-08: Ochrana osobních údajů** – Komentáře mohou být anonymní, nebo vázané na školní přezdívku. Systém nesmí veřejně zobrazovat citlivé osobní údaje uživatelů bez jejich souhlasu (v souladu s GDPR).

### 2.4 Udržitelnost a rozšiřitelnost (Maintainability)
* **NFR-09: Čitelnost kódu** – Zdrojový kód systému musí být dokumentovaný a verzovaný v repozitáři (např. GitHub/GitLab), aby na něm mohli v budoucnu pracovat další studenti SPŠ a VOŠ Liberec v rámci ročníkových projektů.