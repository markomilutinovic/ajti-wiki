# SAP GUI 8.00 — Instalacija

## Preduslovi

Skinuti instalacioni paket `SAPGui 8.00 install.zip` sa deljene lokacije. Paket sadrži:

- `SAP_GUI_for_Windows_8.00_Comp._1_\` — glavni GUI installer
- `gui800_06_1-80006341.exe` — patch/kompilacija
- `SAPUILandscape.xml` i `SAPUILandscapeGlobal.xml` — konfiguracioni fajlovi konekcija

---

## Korak 1 — Instalacija SAP GUI

1. Otpakovati `SAPGui 8.00 install.zip`.
2. Pokrenuti:
   ```
   SAPGui 8.00 install\SAP_GUI_for_Windows_8.00_Comp._1_\PRES1\GUI\Windows\Win32\SapGuiSetup.exe
   ```
3. Otvoriće se **SAP Front End Installer**. Kliknuti **Next**.
4. Na ekranu za odabir komponenti ostaviti podrazumevani izbor i kliknuti **Next**.  
   Ukoliko neka komponenta ne može da se označi — zanemariti i nastaviti.
5. Kliknuti **Next** do kraja instalacije.

## Korak 2 — Instalacija patch-a

1. Pokrenuti:
   ```
   SAPGui 8.00 install\gui800_06_1-80006341.exe
   ```
2. Kliknuti **Next** do kraja instalacije.

## Korak 3 — Kopiranje konfiguracionih fajlova

### Slučaj A — Pre prvog pokretanja SAP Logon-a (preporučeno)

Kopirati `SAPUILandscape.xml` i `SAPUILandscapeGlobal.xml` na Desktop pre nego što se SAP Logon prvi put pokrene. SAP će ih automatski preuzeti pri prvom pokretanju.

### Slučaj B — SAP Logon je već pokrenut

Ručno kopirati oba fajla u:
```
C:\Users\%username%\AppData\Roaming\SAP\Common\
```

## Korak 4 — Podešavanje makroa u Word-u i Excel-u

SAP koristi VBA skripte za integraciju sa Office-om. Neophodno je omogućiti makroe u oba programa.

**U Microsoft Word-u:**

1. `File` → `Options` → `Trust Center` → `Trust Center Settings` → `Macro Settings`
2. Izabrati: **Enable all macros**
3. Čekirati: **Trust access to the VBA project object model**
4. Kliknuti **OK**.

**U Microsoft Excel-u:**

1. `File` → `Options` → `Trust Center` → `Trust Center Settings` → `Macro Settings`
2. Izabrati: **Enable VBA macros**
3. Čekirati: **Enable Excel 4.0 macros when VBA macros are enabled**
4. Čekirati: **Trust access to the VBA project object model**
5. Kliknuti **OK**.

## Korak 5 — Podešavanje jezika i izgleda

Po završetku instalacije podesiti jezik i vizuelni izgled prema uputstvu:  
[SAP GUI — Podešavanje jezika i izgleda](SAP-GUI-Jezik-i-Izgled.md)

---

Za sva nejasnoća obratiti se na: **sapbc@beograd.gov.rs**
