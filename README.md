# Vue 3 + Vite

This template should help get you started developing with Vue 3 in Vite. The template uses Vue 3 `<script setup>` SFCs, check out the [script setup docs](https://v3.vuejs.org/api/sfc-script-setup.html#sfc-script-setup) to learn more.

Learn more about IDE Support for Vue in the [Vue Docs Scaling up Guide](https://vuejs.org/guide/scaling-up/tooling.html#ide-support).

Uppgift: Skapa en dynamisk Vite-webbapplikation med Vue

Mål

Du ska skapa en dynamisk webbapplikation med Vue och Vite som verktyg. Du har möjlighet att

välja att implementera lösningen med antingen Options API eller Composition API.

Projektet utförs individuellt. Inlämningen sker genom en länk till ditt repo på GitHub (eller liknande).

Observera att sena inlämningar inte kommer att kunna få VG.

---

För Godkänd (G)

Följande krav ska uppfyllas:

1. Webbanrop

- Webbanrop görs och information från en eller flera webbtjänster visas i webbapplikationen.

- Undvik CORS-problem och använd helst HTTPS (för att applikationen ska fungera bra som

publicerad).

- Visa åtminstone tre värden (obs: sidan måste vara innehållsrik och fylla ett syfte).

- Använd inte Cities-tjänsten eller någon annan webbtjänst som tagits upp som exempel.

2. Vue-funktionalitet

- Textinterpolering ({{ och }}) används.

- Attributinterpolering (v-bind eller dess kortform) används (key-props relaterade till v-for räknas

inte).

- Villkorlig rendering (v-if) används.

- Listrendering (v-for) används.

- Händelser (v-on eller dess kortform) används.

- v-model (och värdet som matas in) används.

3. Vue Router

- Skapa en Single Page Application med minst två webbsidor med hjälp av Vue Router.

- Använd både router-link och router-view.

4. Komponenter

- Minst en icke-Vue-Router-.vue-komponent ska skapas (App.vue räknas inte).

- Minst en komponent ska ta emot och använda minst en prop (via props-nyckeln).

5. GitHub

- Källkoden för projektet publiceras på GitHub (eller liknande).

6. Skriftlig rapport

- En kortfattad rapport ska lämnas in där du beskriver och motiverar de tekniska val du gjort under

projektet.

- Rapporten ska också innehålla reflektioner över lärdomar och utmaningar.

- Syftet är att minimera risken för fusk och visa att du förstår de val du gjort, enstaka frågor kan även komma från mig som lärare.

- Rapporten lämnas in som en PDF eller Word-fil.

---

För Väl Godkänd (VG)

Utöver kraven för G ska följande uppfyllas:

1. Webbanrop

- Använd någonting annat än fetch (t.ex. Axios) för att göra webbanropen.

2. Vue-funktionalitet

- Minst en beräknad egenskap (computed) används.

- Minst en bevakare (watch) används.

- Alla props ska vara typsäkra.

- Minst ett custom event används (skickas och tas emot).

3. State Management

- Använd Pinia för att lagra och dela information mellan flera komponenter.

4. Vue Router

- Använd minst ett Vue Router-adressparametervärde.

5. Grafisk design och kodkvalitet

- Använd Bootstrap, Vuetify eller ett annat grafiskt ramverk.

- Det finns en ESLint-konfiguration för projektet, som alla filer följer.

- Det finns en Prettier-konfiguration för projektet, som alla filer följer.

6. Skriftlig rapport (utökat krav)

- Rapporten för VG ska vara mer detaljerad och innehålla en djupare teknisk genomgång av de

lösningar du implementerat.

- Beskriv också hur du hanterat mer avancerade krav som t.ex. state management med Pinia och

adressparametervärden med Vue Router.

---

Options API och Composition API

- Options API: Implementera funktionaliteten med data, methods, computed och andra relaterade

delar.

- Composition API: Implementera funktionaliteten med setup(), ref() och reactive().

Du väljer själv vilket API du vill använda. Om du vill, kan du även kombinera båda.

---

Inlämning och regler

1. Inlämning

- Projektet lämnas in med en länk till ditt repo på GitHub (eller liknande).

- Rapporten lämnas in som en separat PDF eller Word-fil och frågorna finner ni här

2. Viktigt

- Om laborationen inte lämnas in i tid kommer VG inte att kunna erhållas, oavsett om alla delar är

uppfyllda eller inte.
