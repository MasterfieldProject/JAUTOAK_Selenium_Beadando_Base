### Selenium Beadandó feladat ###

Feladat a lenti két manuális funkcionális teszteset automatizálása Selenium WebDriver használatával Chrome böngészőben.
A tesztesetek a **Digital Bank** webalkalmazást tesztelik.
A feladat elkészítésénél az alábbi szempontokra figyeljetek:

* a feladatot a Selenium alkalmakon tanultak szerint egy-egy JUnit futtatható tesztként kell megvalósítani egy
  osztályban (DBankTest.java)
* a kódot megfelelő mértékben és minőségben, informatív módon kommentelnetek kell
* a Chrome-ban megjelenő HTTPS/SSL certificate probléma megoldására, meg kell adni egy Chrome opciót (
  --ignore-certificate-errors) a WebDriver
  inicializálásakor:

```
  ChromeOptions options = new ChromeOptions();
  options.addArguments("--ignore-certificate-errors");
  driver = new ChromeDriver(options);
  ```

A megoldáshoz szükségetek lesz egy profilra, amit magatoknak kell kézzel elkészíteni
a https://185.199.31.30:9443/bank/login oldalon.

### TC1 - GDPR nyilatkozat sikeres elfogadása

Lépések:

1. Navigálás: https://185.199.31.30:9443/bank/login
2. Ellenőrzés, hogy a sütik elfogadása ablakon megjelent a megfelelő szöveg és elfogadás gomb.
3. A sütik elfogadása.
4. Ellenőrzés, hogy a Login oldal beviteli mezői és gombja betöltődött.
5. Ellenőrzés, hogy a sütik elfogadása ablak látható-e még.

<hr>

### TC2 - Sikeres bejelentkezés érvényes adatok megadásával

Lépések:

1. Navigálás: https://185.199.31.30:8443/bank/login
2. Ellenőrzés, hogy a sütik elfogadása ablakon megjelent a megfelelő szöveg és elfogadás gomb.
3. A sütik elfogadása.
4. Ellenőrzés, hogy a Login oldal beviteli mezői és gombja betöltődött.
5. Érvényes, a rendszerben már regisztrált belépési adatok megadása.
6. Ellenőrzés, hogy a HomePage oldal betöltődött.

Jó munkát kívánunk!
