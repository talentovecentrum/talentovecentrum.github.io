# SEO balík – Talentové centrum

## Pripravené v exporte

- `index.html`: dokument je označený ako slovenský (`lang="sk"`), má absolútny self-referencing canonical, Open Graph dáta a JSON-LD organizácie.
- `robots.txt`: stránka je povolená pre vyhľadávače.
- `site.webmanifest`: základné identifikačné údaje webu.
- `.nojekyll`: GitHub Pages bude publikovať súbory bez Jekyll spracovania.

## Doména je nastavená

SEO súbory sú pripravené pre `https://talentovecentrum.sk/`:

- `CNAME` nastavuje custom doménu v GitHub Pages.
- `index.html` obsahuje správne `og:url` a Schema.org URL.
- `robots.txt` odkazuje na finálny sitemap.
- `sitemap.xml` obsahuje jedinú indexovateľnú URL stránky.

Canonical, Open Graph URL, robots.txt a sitemap.xml používajú jednotne `https://talentovecentrum.sk/`.

## Po publikovaní

1. V GitHub Pages nastavte custom doménu a v DNS dokončite jej overenie/HTTPS.
2. Otvorte `https://talentovecentrum.sk/robots.txt` a `https://talentovecentrum.sk/sitemap.xml` a skontrolujte odpoveď 200.
3. Pridajte web ako Domain property do Google Search Console a odošlite `/sitemap.xml`.
4. V Search Console použite Kontrolu URL pre domovskú stránku a požiadajte o indexovanie.

## Auditové poznámky

- Ide o jednostránkový web; preto má sitemap práve jednu URL.
- Navigácia a viacero CTA v exporte zatiaľ vedú na `./index.html` namiesto sekčných kotiev. Nezhoršuje to indexáciu domovskej stránky, ale používanie kotiev (`#talent`, `#dotaznik`, `#kontakt`) by zlepšilo prechádzanie obsahu používateľom.
- Formulár je pôvodne Framer formulár. Export obsahuje honeypot, minimálny čas vyplnenia a limit opakovaného odoslania; po nasadení je však potrebné overiť odoslanie a ochranu doplniť na serveri/formulárovej službe (napr. Cloudflare Turnstile).
