# ODIN-workshop: Fra krav til kjørte tester (versjon 3)

Nov 11, 2026 · @Ummear Khan

I denne workshopen går du fra en kravspesifikasjon til kjørte tester med Claude i Cowork, og lager dine egne skills og en agent underveis. Hver oppgave gjør du først med vanlige meldinger (prompts) til Claude. Deretter ber du Claude gjøre det du nettopp gjorde om til en skill eller agent, slik at du kan gjenta det med én kommando neste gang. Til slutt prøver du skillsene og agenten på et nytt krav.

Når du er ferdig, har du dette i Claude:

- to skills du har laget selv: `lag-testcaser` og `kjor-tester`
- en agent du har laget selv: `tenor-testdata`
- testcaser for alle kravene
- testdata fra Tenor for kundeinformasjonen
- en rapport fra testkjøringen
- en GIF-film av kjøringen (valgfritt)

Skriv meldingene til Claude akkurat slik de står i rammene nedenfor. Du kan gjerne endre dem når du har fått det til å virke én gang.

## Før du starter

Sjekk at dette er på plass før workshopen. Det tar ca. 5 minutter.

- [ ] Claude-appen på PC eller Mac, med Cowork.
- [ ] Skills er slått på i Claude. Du trenger ingen skills på forhånd, for du lager dem selv.
- [ ] Google Chrome med utvidelsen Claude in Chrome, koblet til Claude-appen.
- [ ] MinID, BankID eller en annen ID-porten-innlogging. Du trenger den for å logge inn i Tenor testdatasøk.
- [ ] Innloggingen til saucedemo.com: brukernavn `standard_user`, passord `secret_sauce`. Passordet taster du alltid inn selv. Claude gjør det ikke for deg.

Start en ny oppgave (+ New) i Cowork før steg 1, og bruk den samme oppgaven til og med steg 4. Da husker Claude det dere har gjort i de forrige stegene.

## Steg 1: Les kravspesifikasjonen (ca. 5 min)

Claude åpner kravspesifikasjonen på GitHub i Chrome og lister kravene.

1. Gå først selv inn på https://github.com/ummeark/ODIN. Naviger deg til [kravspesifikasjon.md](https://github.com/ummeark/ODIN/blob/main/kravspesifikasjon.md) og trykk på Code. Du vil se krav nummerert som KRAV-01 frem til og med KRAV-09.
2. Gå til Claude og skriv:

   ```
   Gå inn på https://github.com/ummeark/ODIN. Naviger deg til kravspesifikasjon.md. List det du ser der.
   ```
3. Hvis Claude in Chrome ber om tilgang til github.com, godkjenner du det.
4. Kontroller svaret: Du skal se 9 krav (KRAV-01 til KRAV-09) fordelt på innlogging, handlekurv, kundeinformasjon og oversikt.

## Steg 2: Lag testcaser (ca. 10 min)

Claude lager testcaser med «handling» og «forventet resultat» for hvert krav, og legger dem på en artifaktside.

1. Skriv til Claude:

   ```
   Jeg ønsker testcaser med teststeg inkludert "handling" og "forventet resultat". Testcasene skal dekke hvert av kravene og listes pent opp både her i Cowork og på en artifaktside. Lag maks 10–15 testcaser.
   ```
2. Åpne artifaktsiden som dukker opp. Den har testcasene gruppert under hvert krav.
3. Velg to testcaser og kontroller dem selv:
   - Følger forventet resultat av kravteksten, og ikke av hvordan butikken oppfører seg i dag?
   - Finner du testcasene for grensene i KRAV-07: 3, 4 og 5 siffer, og 4 tegn der ett ikke er et siffer?
4. Se etter merknader om uklarheter i kravene. Noter én du er enig i og én du er uenig i.

## Steg 2b: Lag en skill for testcaser (ca. 5 min)

Nå gjør du det Claude nettopp gjorde om til en skill, slik at du kan lage testcaser fra en hvilken som helst kravspesifikasjon.

1. Skriv til Claude:

   ```
   Lag en skill av det vi nettopp gjorde, slik at jeg kan lage testcaser med teststeg fra en vilkårlig kravspesifikasjon. Kall den lag-testcaser.
   ```
2. Claude viser et kort med forslaget til skill. Les gjennom det før du lagrer:
   - Sier beskrivelsen når skillen skal brukes?
   - Er testteknikkene med, som grenseverdier, ett ugyldig felt om gangen og negative tester?
   - Sier den at forventet resultat skal følge av kravet?
3. Mangler noe, skriv det til Claude og be om et nytt forslag. Trykk Lagre når du er fornøyd.

## Steg 3: Lag testdata fra Tenor (ca. 15 min)

Claude henter syntetiske personer fra Tenor testdatasøk og lager testdata for KRAV-07 (postnummer).

1. Skriv til Claude:

   ```
   Åpne Tenor testdatasøk i Chrome, slik at jeg kan logge inn.
   ```
2. Du blir sendt til ID-porten. Logg inn selv med MinID eller BankID, og skriv til Claude når du er inne.
3. Skriv til Claude:

   ```
   Jeg ønsker å generere testdata basert på Tenor for testcasene til KRAV-07. Vis dem på en ny artifaktside.
   ```
4. Åpne artifaktsiden og kontroller:
   - Gyldige postnummer kommer uendret fra Tenor. Ugyldige er laget ved å endre et Tenor-postnummer, og siden viser hvordan.
   - Tegn som ikke er siffer er merket, og antall tegn vises.
   - Finner du et postnummer med null foran? Hvorfor er det en nyttig felle?

## Steg 3b: Lag en agent for testdata fra Tenor (ca. 5 min)

1. Skriv til Claude:

   ```
   Lag en agent for å generere testdata fra Tenor, og spør meg om hvilket krav det skal genereres for. Kall den tenor-testdata.
   ```
2. Les gjennom forslaget før du lagrer:
   - Spør agenten hvilket krav det gjelder?
   - Sier den at du skal logge inn i ID-porten selv, og at Claude aldri gjør det?
   - Beskriver den hvordan ugyldige verdier lages fra Tenor-verdier?
3. Be om endringer hvis noe mangler, og trykk Lagre. Du kan for eksempel be om en egen del om innlogging i Tenor, der agenten ber deg logge inn med BankID.

## Steg 4: Kjør testene mot saucedemo.com (ca. 15 min)

Claude kjører testcasene for KRAV-07 med testdataene fra Tenor, og lager en rapport.

1. Skriv til Claude:

   ```
   Utfør testcasene for KRAV-07 med testdataene for KRAV-07, og kjør dem mot https://www.saucedemo.com. Vis tydelig i nettleseren hvilken test som kjøres, ta opp kjøringen som GIF, og vis resultatene på en artifaktside.
   ```
2. Claude åpner saucedemo.com og ber deg logge inn. Skriv `standard_user` og `secret_sauce` selv, trykk Login, og svar «Ferdig» til Claude.
3. Følg med i Chrome-fanen. Ikke klikk i fanen mens testene kjører.
4. Åpne rapportsiden når Claude er ferdig. Klikk på en feilet test og sammenlign forventet og faktisk resultat.
5. Noen tester vil feile. Det er meningen, og det er det vi skal diskutere i steg 6.
6. Vil du ha en film av kjøringen, be Claude lagre GIF-en.

## Steg 4b: Lag en skill for testkjøring (ca. 5 min)

1. Skriv til Claude:

   ```
   Lag en skill av testkjøringen vi nettopp gjorde, slik at jeg kan kjøre testcaser med testdata mot et system og få en rapport. Kall den kjor-tester.
   ```
2. Les gjennom forslaget før du lagrer:
   - Sier den at Claude aldri taster inn passord, og at du logger inn selv?
   - Vises det i nettleseren hvilken test som kjøres, med banner og markering?
   - Sier den hvordan bestått og feilet vurderes, og at forventet resultat aldri endres?
   - Beskriver den hva rapportsiden skal inneholde?
3. Be om endringer hvis noe mangler, og trykk Lagre. Du kan for eksempel be om en blå ramme rundt komponenten som brukes på siden, slik at det er lett å følge med på det som skjer i testen.

## Steg 5: Prøv skillsene og agenten på KRAV-05 (ca. 15 min)

Nå bruker du de to skillsene og agenten du har laget, i en ny oppgave der Claude ikke husker noe fra stegene før. Da ser du om de inneholder alt som trengs.

1. Start en ny oppgave i Cowork (+ New).
2. Skriv `/lag-testcaser` og be om testcaser for KRAV-05 i kravspesifikasjon.md på https://github.com/ummeark/ODIN.
3. Skriv `/tenor-testdata` og velg KRAV-05 når Claude spør. Logg inn i ID-porten hvis Claude ber om det.
4. Skriv `/kjor-tester` og be om å kjøre KRAV-05 mot https://www.saucedemo.com. Logg inn i saucedemo selv når Claude ber om det.
5. Hvordan synes du dette gikk?
   - Kjørte skillsene og agenten helt som forventet?
   - Måtte du forklare noe på nytt som skillen eller agenten burde visst?
6. Forbedre én av skillsene: Skriv hva som manglet, og be Claude foreslå en oppdatert versjon. Du kan for eksempel be om at skillen skal rydde opp etter seg og lukke faner og nettlesere den har brukt.

## Steg 6: Se på resultatet og diskuter (ca. 10 min)

Snakk med sidemannen om spørsmålene nedenfor. Noter svarene til felles oppsummering.

1. Hvilke feil fant testene, og hvilket krav brytes?
2. Er du enig i vurderingen av hver feil? Finnes det en test som burde vært vurdert annerledes?
3. Hvilke uklarheter i kravene må avklares med den som eier kravene?
4. Hva tok Claude med i skillsene som du ikke hadde tenkt på, og hva manglet?
5. Hva er forskjellen på å jobbe med prompts og å jobbe med skills?
6. Hvor sjekket du selv det Claude laget, og hvor stolte du på det uten å sjekke?
7. Hvilke skills ville du laget for et ekte prosjekt hos en kunde?

## Hvis noe går galt

| Det som skjer | Gjør dette |
| --- | --- |
| Claude får ikke kontakt med Chrome | Sjekk at Claude in Chrome-utvidelsen er på og koblet til appen. Skriv «prøv igjen» til Claude. |
| Claude ber om tilgang til et nettsted | Godkjenn github.com, testdata.skatteetaten.no og saucedemo.com. |
| Claude viser ikke noe kort for skillen | Skriv «vis forslaget til skill som et kort jeg kan lagre». |
| Skillen du laget finnes ikke når du skriver `/` | Sjekk at du trykket Lagre på kortet. Start en ny oppgave, så lastes skillsene på nytt. |
| Tenor viser ID-porten igjen | Innloggingen har gått ut. Logg inn på nytt og si fra til Claude. |
| Saucedemo viser innloggingssiden midt i kjøringen | Innloggingen går ut etter ca. 10 minutter. Logg inn på nytt og be Claude fortsette der den slapp. |
| Claude stopper uten svar | Skriv «fortsett». Kommer det ikke i gang, be Claude kjøre de gjenstående datasettene. |
| Du klikket i Chrome-fanen under kjøringen | Si fra til Claude hvilket datasett som kjørte, og be den kjøre det på nytt. |

## 
