# UPDATE LOGG
## Fixade 
- Bilder: nerskalade från ca 5000x4000px till ca 400x200. Sparade som PNG för att hålla kvar kvaliten vid olika storlekar
- Prat om cache. Det bör finnas någon typ av cashe kontroll på sidan.
  Implementerade foljande:
  ```html
  <meta http-equiv="Cache-controll" content="no-store">
  ```

  Den vill dock ha en cashe, skall man lägga till:
  ```html
  <meta http-equiv="Cache-control" content="public">
  ```

  Följande är tagen från stackoverflow:
  ```html
  <meta http-equiv="Cache-control" content="public">
  ```
  Some information on the Cache-Control header is as follows

  HTTP 1.1. Allowed values = PUBLIC | PRIVATE | NO-CACHE | NO-STORE.

    - Public - may be cached in public shared caches.
    - Private - may only be cached in private cache.
    - No-Cache - may not be cached.
    - No-Store - may be cached but not archived.

    The directive CACHE-CONTROL:NO-CACHE indicates cached information should not be used and instead requests should be forwarded to the origin server. This directive has the same semantics as the PRAGMA:NO-CACHE.

    Clients SHOULD include both PRAGMA: NO-CACHE and CACHE-CONTROL: NO-CACHE when a no-cache request is sent to a server not known to be HTTP/1.1 compliant. Also see EXPIRES.

    Note: It may be better to specify cache commands in HTTP than in META statements, where they can influence more than the browser, but proxies and other intermediaries that may cache information.
- Lösningen set ut att vara att sätta in:
  ```html
  <meta http-equiv="Cache-control" content="public">
  ```
  Detta tar bort laddning so skall sker på sidan.


## Behöver fixas
- Bilder till mer korrekta storlekar
- Har resat upp onödiga bilder som skräpar runt
- Lagt till meta-tag med cach (Den ska fungera?)
- ```html
  <meta http-equiv="Cache-controll" content="no-store">
  ```
- Konstiga frågor:
  - Den föredrar "nex-gen format", JPEG 2000, JPEG XR och WebP... Dessa skall tydligen vara bättre komprimerade än PNG och JPEG. Skillnaden mellan dessa ligger runt 1-3KB. Ändras ett måste?
  - Render-blocking resources: Skall CSS/JS ändras? 


## Småfixar 2019-10-28

## 2019-10-27

### Eftermiddag
- Fixat till alla sidor, inga fel eller varningar på någon av dem.
- Nu behövs bara sociala medier hamna på bästa sätt i footern

### Förmiddag
- Index med sociala medier icon fixade
  Behöver finputsat lite mer, annars så är det bra
- About - Fixa design
  kladda upp layout samt skriv den simplelt
- Fixat contact sidan
  Den är responsiv och fungerar bra
- Fridykningssidan
  Den är skapad... men den har inget innehåll.
  Funderingar på hur jag skall desighna den på snyggaste sätt... Behöver lite insperation...

## Nytt 2019-10-26
- om följand kod inte fungerar, ta bort den
- ```html
  <figure>
      <a href=""><img src="./img/twitter.jpg" alt="twitter"></a>
    </figure>
    <figure>
      <a href=""><img src="./img/instagram.jpg" alt="Instagram"></a>
    </figure>
    ```

    denna kod finner man i footer längs ned på index sidan
- Annars finnns inga fel eller varnigar på hela index sidan...
  Uppdatera resterande sidor så att de uppfyller samma krav

## ReWork - Allt är omgjort
Dessa punkter är uppfyllda efter ny rework:
- Boilerplate 
- CSS-reset
- Mobile first
  
## About - Tillagd about sida 2019-10-22
- Logga tillagd
- About -> html, css 
- Skall det bara vara en enda css sida för alla sidor?

## Layout index 2019-10-22
- Fixat till "responsive" index page.
- Behöver fixa till en logga i index

## Fixa basic layout 2019-10-21
- Testing diffrent layouts for page, and trying out diffrent types of menus
- Found logo image
- Page will be about linux and diffrent types of distros vs win10 and mac OS?