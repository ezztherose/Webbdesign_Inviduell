# Lathund 

## Skapa cache i HTML5 med manifest
Lägg till:
```html
<html class="no-js" lang="sv" manifest="mySite.manifest">
```
Taggen ligger lokaliserad högst upp i html filen.

### Skapa filerna
Det behövs skapas två filer för att kunna använda sig av cachen. 
Dessa filer skapas följande:
- namn.appcache
- .htaccess

(i mitt fall finns redan en .htaccess-fil från boilerplaten)\
Om INTE en .htaccess fil existerar, gör föjlande:
- skapa .htaccess fil
- skriv i "AddType text/cache-manifest appcache"
- spara
Första steget är klart...  
nästa

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
