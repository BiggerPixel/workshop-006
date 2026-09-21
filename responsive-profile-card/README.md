# Gruppövning: ett responsivt profilkort

**Tid:** 20–30 minuter  
**Gruppstorlek:** 2–3 personer  
**Nivå:** Enkel

## Syfte

Vi utvecklar ett profilkort som redan har HTML, grundläggande CSS och Flexbox.
Kortet fungerar, men det anpassar sig ännu inte efter skärmens bredd eller användarens valda färgschema.

I övningen tränar vi på att:

- skapa och använda CSS-variabler;
- använda `max-width` och `min-width` i media queries;
- ändra en Flexbox-layout när utrymmet blir mindre;
- anpassa färger med `prefers-color-scheme`;
- kontrollera och förklara varför våra CSS-regler fungerar.

En CSS-variabel är ett namngivet värde som kan återanvändas i flera CSS-regler.
En media query är ett villkor som gör att viss CSS bara används i en särskild situation, till exempel när webbläsarfönstret är smalt.

## Start

Vi arbetar tillsammans i filerna [`index.html`](index.html) och [`main.css`](main.css).

Öppna `index.html` med Live Server.
Sidan ska från början visa ett enkelt profilkort med en avatar, en text och tre taggar.
Ändra inte HTML-koden under övningen. Allt arbete görs i `main.css`.

## Uppgift

### 1. Skapa CSS-variabler

Lägg till variabler i `:root` för tex:

- sidans bakgrundsfärg;
- kortets bakgrundsfärg;
- textfärg;
- accentfärg för taggarna;

Ge variablerna tydliga namn, exempelvis `--background` och `--foreground`.

Använd sedan variablerna med `var()`.
Lägg sidans bakgrund och textfärg i `body`, kortets bakgrund i `.profile` och accentfärgen i `.tags span`.

Kontroll: ändra värdet på en variabel. Alla CSS-egenskaper som använder variabeln ska ändras samtidigt.

### 2. Anpassa kortet för små skärmar

Lägg till en media query med `max-width: 600px`.

När fönstret är högst `600px` brett ska:

- profilkortets riktning ändras från rad till kolumn med `flex-direction`;
- innehållet centreras;
- texten centreras.

Kontroll: gör webbläsarfönstret smalare och bredare.
Layouten ska byta riktning när bredden passerar `600px`.

### 3. Lägg till mörkt färgschema

`prefers-color-scheme` läser vilket färgschema användaren har valt i operativsystemet eller webbläsaren.

Lägg till en media query för `prefers-color-scheme: dark`.
Ändra värdena för bakgrund, text och accent i `:root`. Återanvänd samma variabelnamn som tidigare.

```css
@media (prefers-color-scheme: dark) {
  :root {
    /* Ändra variablernas värden här. */
  }
}
```

Kontroll: byt till mörkt färgschema i webbläsaren eller operativsystemet.
Texten ska fortfarande vara tydlig mot bakgrunden.

## När vi är klara

Gruppen ska kunna visa att:

- färger hämtas från CSS-variabler;
- kortet byter riktning vid `600px`;
- färgerna ändras i mörkt färgschema;
