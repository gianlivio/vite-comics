# Vue 3 + Vite

This template should help get you started developing with Vue 3 in Vite. The template uses Vue 3 `<script setup>` SFCs, check out the [script setup docs](https://v3.vuejs.org/api/sfc-script-setup.html#sfc-script-setup) to learn more.

## Recommended IDE Setup

- [VS Code](https://code.visualstudio.com/) + [Vue - Official](https://marketplace.visualstudio.com/items?itemName=Vue.volar) (previously Volar) and disable Vetur


1. Aprire terminale
2. Spostarsi nella cartella desiderata (cd nomecartella)
3. Creo progetto vite " "
4. Entro nella cartella creata (cd nome-repo)
5. "npm install"
6. "npm run dev"
7. Apriamo progetto con vsc
8. Publish to github (public!)
9. Istallare sass da terminale VSC digitando: npm add -D sass---verificare la presenza di sass su package.json
10. Resettare AppVue cancellando tutto e inserendo script (con export default {}) template e style (con lang="scss")
11. Cancellare style.css e creare una cartella style dentro src
12. Dentro la cartella style creare file general.scss (vi importerai le variables e mixins per formattare gli stili globali)
13. Dentro la cartella style creare la cartella partials
14. Dentro la cartella partials creare file _variables.scss e _mixin.scss
15. Su main.js cambiare il link del secondo import in './style/general.scss' per collegarlo al nuovo file
16. Effettuare css-reset( *{margin0padding0boxsizingborderbox}) su general.scss 
17. Su AppVue aggiungi un h1 hello per testare 
18. Sugeneral.scss prova un $primary-color: blue;
h1 {
    color: $primary-color;
} per testare il collegamento
ESERCIZIO INIZIO 
19. Sulla cartella components creo AppHeader.vue, AppMain.vue e Appfooter.vue
20. su ognuna imposto  
    script(export default {data() {return{}}}) template e style(scoped lang="scss")
21. Su AppVue importo tutti e 3 digitando es. <AppHeader /> in template e cliccando sul suggerimento. Comparirà un import... all'interno di script-->inserisci components: {AppHeader} dentro export default
22. crea le prime variabili in -variables.scss usando $, definisci tutte le variabili di colore, font, e altre costanti riutilizzabili.
23. crea mixinSCSS per riutilizzare pezzi di codice CSS.
24. Ogni volta che usi variables e mixin bisogna importarle con @use + percorso o @include



