# Sjekkliste for oppsett: ODIN-workshop 19. november

Gjør oppsettet før du kommer. Det tar ca. 15 minutter. I workshopen lager du egne skills og en agent i Claude Cowork, henter testdata fra Tenor testdatasøk og kjører tester i Chrome. Alt det krever at verktøyene er klare når vi starter.

## Sjekkliste

- [ ] Bærbar PC (Mac eller Windows) med strømlader
- [ ] Betalt Claude-abonnement (Pro, Max, Team eller Enterprise)
- [ ] Claude-appen installert, med Cowork tilgjengelig
- [ ] Skills slått på i Claude
- [ ] Google Chrome med utvidelsen Claude in Chrome, koblet til Claude-appen
- [ ] MinID, BankID eller annen ID-porten-innlogging som virker
- [ ] Du har klart å logge inn i Tenor testdatasøk én gang
- [ ] Testmeldingen til Claude virker (se nederst)

## 1. Claude-appen og Cowork

1. Last ned Claude-appen for Mac eller Windows fra [claude.ai/download](https://claude.ai/download), og logg inn med kontoen som har betalt abonnement.
2. Åpne appen og sjekk at du ser **Cowork**. Trykk **+ New** for å starte en oppgave, og skriv «Hei» for å se at Claude svarer.
3. Gå til innstillingene og sjekk at **Skills** er slått på. Du trenger ingen skills på forhånd, for du lager dem selv i workshopen.

Bruker du jobbkonto, kan det hende administratoren må slå på Cowork eller skills. Sjekk dette i god tid.

## 2. Chrome og Claude in Chrome

1. Installer [Google Chrome](https://www.google.com/chrome/) hvis du ikke har det.
2. Installer utvidelsen **Claude in Chrome** fra Chrome Utvidelser, og logg inn med den samme Claude-kontoen.
3. Fest utvidelsen til verktøylinjen, så er den lett å finne.
4. Sjekk i Claude-appen at Chrome er koblet til. Testmeldingen nederst viser om koblingen virker.

Underveis vil Claude be om tilgang til github.com, testdata.skatteetaten.no og saucedemo.com. Godkjenn dem når du blir spurt.

## 3. Innlogging i Tenor testdatasøk

Tenor er Skatteetatens søk etter syntetiske testpersoner. Du logger inn med ID-porten.

1. Gå til [testdata.skatteetaten.no](https://testdata.skatteetaten.no) i Chrome.
2. Logg inn med MinID, BankID eller en annen ID-porten-innlogging.
3. Sjekk at du kommer inn i søket. Går det ikke, gi beskjed til oss før workshopen.

I workshopen logger du alltid inn selv. Claude taster aldri inn passord eller BankID for deg. Det samme gjelder demo-nettbutikken saucedemo.com, der du får brukernavn og passord på workshopen.

## 4. Test at alt virker

Start en ny oppgave i Cowork (**+ New**) og skriv:

```
Åpne https://github.com/ummeark/ODIN i Chrome og fortell meg hvilke filer som ligger der.
```

Det virker hvis Chrome åpner en ny fane med GitHub-siden, og Claude lister filene, blant annet `kravspesifikasjon.md`. Ber Claude om tilgang til github.com, godkjenner du det.

## Hvis noe ikke virker

| Det som skjer | Gjør dette |
| --- | --- |
| Du finner ikke Cowork i appen | Sjekk at appen er oppdatert og at abonnementet er betalt. Jobbkonto: spør administratoren. |
| Claude får ikke kontakt med Chrome | Sjekk at utvidelsen er på og innlogget med samme konto. Start Chrome på nytt og skriv «prøv igjen» til Claude. |
| Du kommer ikke inn i Tenor | Sjekk at ID-porten-innloggingen virker på andre offentlige tjenester. Gi beskjed til oss hvis det fortsatt ikke går. |
| Skills er ikke tilgjengelig | Sjekk innstillingene i appen. Jobbkonto: spør administratoren. |

Får du det ikke til, ta kontakt med oss før workshopen, så hjelper vi deg. Kom gjerne 15 minutter tidlig hvis noe fortsatt mangler.
