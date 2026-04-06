# Check Point Mobile VPN — Instalacija i podešavanje

## Preduslovi

Skinuti installer sa zvanične stranice:  
**https://www.checkpoint.com/quantum/remote-access-vpn/#downloads**

Ili koristiti MSI paket iz deljene lokacije: `E88.60_CheckPointVPN.msi`

---

## Instalacija

1. Pokrenuti installer (`E88.60_CheckPointVPN.msi` ili preuzeti exe).
2. Na uvodnom ekranu kliknuti **Next**.
3. Na ekranu **Client Products** izabrati **Check Point Mobile** → **Next**.
4. Pročitati i prihvatiti licencni ugovor (**I accept the terms in the license agreement**) → **Next**.
5. Ostaviti podrazumevanu putanju instalacije:
   ```
   C:\Program Files (x86)\CheckPoint\Endpoint Connect\
   ```
   Kliknuti **Install**.
6. Po završetku kliknuti **Finish**.

---

## Podešavanje VPN sajta (první put)

1. U sistemskom treju (donji desni ugao) kliknuti na strelicu nagore.
2. Pronaći ikonu katančića (Check Point), desni klik → **Connect to...**
3. Pojaviće se poruka: *"No site is configured. Would you like to configure a new site?"* — kliknuti **Yes**.
4. Otvoriće se **Site Wizard** → kliknuti **Next**.
5. Uneti podatke:
   - **Server address or Name:** `178.221.34.166`
   - Čekirati **Display name** i upisati: `GU Beograd`
6. Kliknuti **Next**.
7. Login opcija ostaje: **Username Password (Default)** → **Next**.
8. Poruka *"Site created successfully"* → kliknuti **Finish**.

---

## Rešenje problema na Windows 11 (24H2)

Ukoliko VPN ne radi ispravno na Windows 11 verziji 24H2, primeniti sledeće:

1. Ugasiti VPN klijent (desni klik na ikonu → **Shutdown Client**).
2. Otvoriti **Services** (`services.msc`) i stopirati obe usluge:
   - `Check Point Endpoint Client Watchdog`
   - `Check Point Endpoint Security VPN`
3. Otvoriti instalacionu putanju VPN klijenta:
   ```
   C:\Program Files (x86)\CheckPoint\Endpoint Security\Endpoint Connect\
   ```
   ili
   ```
   C:\Program Files (x86)\CheckPoint\Endpoint Connect\
   ```
4. Napraviti kopiju fajla `trac.defaults` (backup).
5. Otvoriti `trac.defaults` u Notepad++ ili drugom text editoru.
6. Pronaći parametar i promeniti vrednost:

   **Pre:**
   ```
   route_conflict_resolution_method STRING "delete_create" GLOBAL 1
   ```
   **Posle:**
   ```
   route_conflict_resolution_method STRING "modify" GLOBAL 1
   ```

7. Sačuvati fajl i zatvoriti editor.
8. U `services.msc` pokrenuti obe ranije stopovane usluge.
9. Konektovati se na VPN i proveriti da li radi.
10. Za svaki slučaj restartovati računar.
