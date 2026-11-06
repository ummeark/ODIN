# Kravspesifikasjon: Utsjekking i nettbutikken

System: https://www.saucedemo.com (passord for alle brukere: secret_sauce)

## Innlogging
KRAV-01  Brukernavn og passord er obligatoriske. Tomt felt gir en feilmelding som sier hvilket felt som mangler.
KRAV-02  En låst bruker (locked_out_user) skal ikke kunne logge inn, og skal få beskjed om at brukeren er låst.

## Handlekurv
KRAV-03  Kunden kan legge 1 til 6 ulike produkter i handlekurven. Antallet vises på handlekurv-ikonet.
KRAV-04  Kunden kan fjerne et produkt fra handlekurven før utsjekking.

## Kundeinformasjon
KRAV-05  Fornavn, etternavn og postnummer er obligatoriske. Tomt felt gir en feilmelding som sier hvilket felt som mangler.
KRAV-06  Fornavn og etternavn skal godta norske tegn (æøå), bindestrek og apostrof, og være mellom 1 og 50 tegn.
KRAV-07  Postnummer skal bestå av nøyaktig 4 siffer.

## Oversikt og bekreftelse
KRAV-08  Oversikten viser valgte produkter, varesum, skatt og totalsum. Totalsum = varesum + skatt, med to desimaler.
KRAV-09  Når bestillingen fullføres, vises en bekreftelse, og handlekurven tømmes.
