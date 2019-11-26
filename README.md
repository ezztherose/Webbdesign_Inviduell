# Inviduell uppgift

## Fixade 
- Bilder: nerskalade från ca 5000x4000px till ca 400x200. Sparade som PNG för att hålla kvar kvaliten vid olika storlekar

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