# Prime Media — SFTP Upload

Uputstvo za spoljne saradnike koji šalju materijal (zvuk ili video) Vision Team-u preko SFTP-a.

!!! info "Pristupni podaci"
    **Host, port, korisničko ime i lozinku dostavlja Vision Team, odvojenim kanalom.**
    Nisu objavljeni na ovoj stranici. Ako ih nemate, javite se Vision Team-u.

---

## FileZilla — podešavanje

Preuzmite [FileZilla Client](https://filezilla-project.org/download.php?type=client) i instalirajte ga.

1. Otvorite **File → Site Manager → New Site**.
2. Popunite:
   - **Protocol:** SFTP - SSH File Transfer Protocol
   - **Host** i **Port:** onako kako ste dobili od Vision Team-a
   - **Logon Type:** Normal
   - **User** i **Password:** vaši podaci
3. Kliknite **Connect**.
4. Prvi put se pojavi prozor sa pitanjem o host key-u. Označite **Always trust this host** i potvrdite sa **OK**.

---

## Slanje fajlova

Posle prijave vidite samo `/` — to je vaš folder. Prevucite fajlove iz levog prozora (vaš računar) u desni (server).

- Ne možete izaći van svog foldera niti videti šta drugi saradnici šalju. Tako je i predviđeno.
- Za velike isporuke (preko 1 GB) preporučujemo jedan fajl: zip ili mkv.
- Kad se prenos završi, javite Vision Team-u.

---

## Greške

| Poruka | Razlog | Šta da uradite |
|---|---|---|
| Connection timed out | Server je nedostupan | Probajte alternativni host koji ste dobili. Ako ni on ne radi, javite Vision Team-u |
| Authentication failed | Pogrešno korisničko ime ili lozinka | Proverite podatke, vodite računa o malim i velikim slovima |
| Host key changed | Server je promenio identitet | **Stanite i javite Vision Team-u.** Može biti regularna izmena, ali i pokušaj napada |

---

## Bezbednost

Lozinka važi samo za vaš nalog. Ako posumnjate da je procurela, odmah javite Vision Team-u da je promeni.
