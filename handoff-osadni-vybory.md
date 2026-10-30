# Handoff: srovnání směrnic o osadních výborech Kroměříže

## Cíl

Stránka pro kolegy ze zastupitelstva. Srovnává platnou **Směrnici č. 1/2025** (Pravidla pro fungování a financování osadních výborů, účinná od 1. 5. 2025) s návrhem **Směrnice č. 1/2026** (Osadní výbory města Kroměříže), který jde jako zpráva č. 31 na I. zasedání ZMK 3. 11. 2026.

## Stav

- Stránka je zveřejněná jako artefakt: https://claude.ai/artifact/VPPwfWUvmR8fvnqTfPju9U
  - Zatím je soukromá. Nasdílet ji kolegům musí uživatel přes menu Share.
  - Aktuální HTML získáš přes Artifact `action: "read"` s touto URL. Úpravy zveřejňuj na **stejnou URL** (parametr `url`), aby odkaz zůstal platný.
- Obsah stránky, shora dolů:
  1. hlavička se shrnutím;
  2. upozornění k porovnávanému znění;
  3. „Na co upozornit před hlasováním“, 7 zjištění seřazených podle závažnosti;
  4. „Všechny změny po článcích“, řádky s `data-type` = `nove` / `zmena` / `vypusteno` a JS filtrem;
  5. tabulka garantů;
  6. „Beze změny“ a „Co návrh zlepšuje“;
  7. „Otázky na předkladatele“;
  8. zdroje.
- Věcná kontrola proti oběma PDF je hotová. Nezávislý agent ověřil zhruba 60 údajů a našel 14 nepřesností. Ty jsou opravené (seznam níže), takže ji znovu nedělej.

## Co je potřeba udělat lokálně

1. **Vizuální styl „1. volby“.** Najdi stránku nebo podklady „1. volby“ ve složce `c:\Users\uzivatel\Dropbox\work\Volby 2026` a převezmi z nich vizuální styl: barvy, písma, rozvržení, prvky. Obsah stránky měň jen tam, kde to styl vyžaduje. Dodrž pravidla artefaktů (tokeny pro světlý i tmavý režim, šířka telefonu, skript filtru).
2. **Psaní a kontrola textu přes `/geeklife-publish`.** Skill je v `c:\Users\uzivatel\Dropbox\work\Weby\GeekLife`. Spusť ho nad textem stránky a uprav podle něj stylistiku a jazyk. **Věcný obsah neměň** (viz „Ověřená fakta“).
3. Zveřejni stránku znovu na stejnou URL a pošli uživateli odkaz.

## Zdrojové dokumenty

Uživatel je nahrál do cloudové session. Pokud je lokálně potřebuješ, požádej o ně:

- `Směrnice 2025_1_ Pravidla pro fungování a financování osadních výborů.pdf`
- `podklady-rada-zastupitelstvo.pdf`: zpráva č. 31 a návrh směrnice 1/2026

## Ověřená fakta, na kterých stránka stojí

- **Čl. 3 (volby).** Vypuštěno:
  - přihlašování kandidátů 1.–30. 9. volebního roku přes podatelnu nebo na veřejné schůzi (dosavadní odst. 6), včetně nominace jiného kandidáta;
  - výzva ve Zpravodaji, na webu a na výlepových plochách (dosavadní odst. 8);
  - tajné hlasování a aklamace (dosavadní odst. 9).

  Zůstává lhůta „v jednotlivých místních částech do čtyř měsíců od ustavujícího zasedání“ a dohled garanta. Mizí, kdo volbu pořádá a v jaké formě.
- **Čl. 3 odst. 7.** „Zvoleni za kandidáty na členy“. Jde o sladění s odst. 4: členy určuje zastupitelstvo, a to platilo i dosud.
- **Čl. 3 odst. 1.** Počet členů je lichý, 3–7.
- **Čl. 3 odst. 10.** Výbor „bude“ zrušen. Dosud „by mohl být“ zrušen.
- **Čl. 4.** Nové jsou:
  - pozvánka nejméně „3 dny“ předem, kopii dostane garant;
  - kvorum nadpoloviční většiny;
  - pravidla při střetu zájmů;
  - hlasování per rollam a on-line jednání, obojí s lhůtou „3 pracovní dny“ (rozpor s pozvánkou, kde jsou 3 dny).

  Vypadlo „zpravidla jednou měsíčně“.
- **Čl. 6.** Zápis se posílá do 14 dnů e-mailem garantovi, dosud šel přes podatelnu. Rezignace jde přes garanta.
- **Dosavadní čl. 7 (součinnost).** Vypuštěn celý. Šlo o „včasnou vzájemnou informovanost“ o stavebních záměrech a ochraně životního prostředí. Formuluj to jako vzájemnou informovanost, ne jako jednostrannou povinnost města.
- **Financování.** Mění se:
  - vypadly poštovní známky, ale položka 5161 Služby pošt zůstala;
  - u písm. f) přibylo „zejména“;
  - úvodní věta výčtu zní „na činnost osadních výborů takto:“;
  - čl. 9 odst. 1 nově předepisuje plánování výdajů s garantem a poznámku o účelu na zadní straně dokladu.

  Beze změny zůstává rezerva 148 000 Kč a vzorec 12 000 Kč + 10 Kč na obyvatele k 30. 9.
- **Garanti.** Mění se u 5 z 9 výborů:
  - Drahlov a Trávník: Holík → Vondráčková;
  - Hradisko a Postoupky: Kašík → Petřík;
  - Vážany: Kreml → Hebnar (ten je pak garantem tří výborů).

  U nových garantů chybí telefon.
- **Zrušovací ustanovení.** Ruší se 1/2025 „ve znění změny schválené Zastupitelstvem města Kroměříže usnesením č. ZMK/26/24/15 ze dne 18.06.2026“. Tuto změnu jsme neměli k dispozici a stránka na to upozorňuje.
- **Chyby v návrhu:**
  - překlep „OSADNÍCH VÝBORY“ na titulní straně;
  - v čl. 2 odst. 1 chybí slovo „zákona“ a vypadl § 94;
  - v čl. 4 odst. 6 je uveden Skype, který byl ukončen v květnu 2025.
- **Důvodová zpráva** uvádí doslova: „mění některé části stávající směrnice a to zejména čl. 3 … a čl. 4 …“. Další změny nezmiňuje.

## Čeho se vyvarovat (kontrola to už opravila)

- Nepsat, že návrh vypouští „celý“ postup voleb nebo že „financování zůstává stejné“.
- Neoznačovat zprávu č. 31 jako „bod č. 31“.
- Netvrdit jako fakt, že 3. 11. je ustavující zasedání. Dokument říká jen „I. zasedání“, proto stránka používá formulaci „pokud je…“.
- Netvrdit, že úřad podání „nebude evidovat“. Směrnice to neřeší.
- Citace nechávat doslovné.
