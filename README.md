# Lathund 

## Skapa cache i HTML5 med manifest
Lägg till följande rad för alla sidor som man vill ska vara cachade.
```html
<html class="no-js" lang="sv" manifest="site.appcache">
```
Taggen ligger lokaliserad högst upp i html filen.

### Skapa filerna
Det behövs skapas två filer för att kunna använda sig av cachen. 
Dessa filer skapas följande:
- .htaccess
- namn.appcache

(i mitt fall finns redan en .htaccess-fil från boilerplaten)\
Om INTE en .htaccess fil existerar, gör föjlande:
- skapa .htaccess fil
- skriv i "AddType text/cache-manifest appcache"
- spara
Första steget är klart...  
  
Skapa ny text-fil
- Ge den valfritt namn
- efter namn lägg till ".appcache"

---
***Innehåll .appcache***\
CACHE MANIFEST

#version (nummer)

  #Explicit cachade entiteter
  + index.html

  #Extra resurser till cachen
  + CACHE:\
    img/slider_1_resize.png

  #Filer som listas i denna del kan komma från nätverket om de inte befinner sig i cachen,\
  nätverket används inte annars om även om användaren är online.\
  Man kan "white" lista URL:er eller använda *, vilket tillåter alla URL:er.\
  De flesta sidor behöver *.
  + NETWORK:\
    *
---
Ovan är exemple, fyll ut efter egna sidor...

## EJ Fungerande för HTML5
Följande fungerar inte för HTML5:
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
