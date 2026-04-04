# ScriptShare

<br>

## Sadržaj
1. [Uvod](#1-uvod)
    - [1.1 Rezime](#11-rezime)
    - [1.2 Namena dokumenta i ciljne grupe](#12-namena-dokumenta-i-ciljne-grupe)
2. [Opis problema](#2-opis-problema)
3. [Kategorije korisnika](#3-kategorije-korisnika)
    - [3.1 Gost](#31-gost)
    - [3.2 Student](#32-student)
    - [3.3 Moderator](#33-moderator)
    - [3.4 Administrator](#34-administrator)
4. [Opis proizvoda](#4-opis-proizvoda)
    - [4.1 Pregled arhitekture sistema](#41-pregled-arhitekture-sistema)
    - [4.2 Pregled karakteristika](#42-pregled-karakteristika)
---
<br>

## 1. Uvod

### 1.1 Rezime
Projekat ScriptShare je deo praktične nastave predmeta Principi softverskog inžinjerstva. Aplikacija je namenjena studentima za jednostavnu razmenu materijala kao što su skripte, beleške, zbirke zadataka i prethodni ispiti.

### 1.2 Namena dokumenta i ciljne grupe
Tekst koji sledi definiše namenu aplikacije, zahteve i funkcionalnosti koje ona upotrebljava i pruža, namenjen je svim članovima tima.

## 2. Opis problema
Ova aplikacija stupa u pomoć studentima i omogućava im da na jednom mestu imaju brz, jednostavan i pouzdan pristup materijalima za učenje, posebno u periodima kolokvijuma i ispita, kada je vreme od presudnog značaja. U praksi se materijali poput skripti, zbirki zadataka, rokova iz prethodnih godina i beleški često nalaze rasuti po različitim platformama, grupama na društvenim mrežama ili privatnim porukama, što otežava njihovo pronalaženje i korišćenje.

U tu svrhu razvija se aplikacija **ScriptShare**, koja predstavlja centralizovano mesto namenjeno studentima za razmenu i organizaciju nastavnih materijala. Korisnici sistema imaju mogućnost da pregledaju dostupne skripte, ispitne rokove iz ranijih godina, zbirke zadataka, laboratorijske vežbe i druge korisne materijale vezane za određene predmete.

Registrovani korisnici, pored pregleda sadržaja, mogu da postavljaju nove materijale, preuzimaju postojeće dokumente, ocenjuju njihovu korisnost i ostavljaju komentare kako bi pomogli drugim studentima pri izboru odgovarajućih resursa. Sistem omogućava kategorizaciju materijala po fakultetu, smeru, godini studija i predmetu, čime se značajno olakšava pretraga i pristup željenim dokumentima.

Moderator sistema brine o ažurnosti i kvalitetu sadržaja, ima mogućnost dodavanja, izmene i brisanja materijala, kao i odobravanja novih objava korisnika. Administrator vodi računa o upravljanju korisničkim nalozima, autorizaciji i dodeli korisničkih privilegija.

Na početnoj strani aplikacije nalaze se najnovije i najpopularnije skripte, obaveštenja o aktuelnim ispitnim rokovima, kao i preporučeni materijali koji mogu biti od značaja studentima.

## 3. Kategorije korisnika
Aplikacija podržava više tipova korisnika: goste, studente, moderatore i administratore.

### 3.1. Gost
Gost sajta ima mogućnost da pregleda sadržaj, kao i mogućnost registracije.

### 3.2. Student
Student je registrovani korisnik koji prilikom logovanja sa svojim ličnim i fakultetskim podacima dobija mogućnost postavljanja materijala, preuzimanja materijala, komentarisanja, ocenjivanja kao i čuvanja omiljenih materijala.

### 3.3. Moderator
Moderator je zadužen za održavanje integriteta platforme kroz proveru, odobravanje ili odbijanje postavljenih materijala. Njegova ključna uloga je da osigura kvalitet i relevantnost sadržaja, uz ovlašćenja da menja ili uklanja materijale koji ne ispunjavaju akademske standarde ili pravila korišćenja.

### 3.4. Administrator
Administrator vrši nadzor nad celokupnim radom sistema i upravlja korisničkim nalozima. Njegove privilegije uključuju dodelu i promenu korisničkih prava, upravljanje bazom podataka i kontrolu rada moderatora, čime obezbeđuje nesmetano funkcionisanje aplikacije na svim nivoima.


## 4. Opis proizvoda

### 4.1. Pregled arhitekture sistema
Sistem je zamišljen kao dinamička web aplikacija postavljena na web serveru koji podržava PHP tehnologiju, dok se za čuvanje i upravljanje podacima koristi MySQL baza podataka.

Aplikacija omogućava tri osnovna nivoa pristupa sistemu:
* Administrator
* Moderator
* Student (registrovani korisnik)

Pored registrovanih korisnika, sistem omogućava i gostujući pristup, gde korisnici mogu pregledati deo javno dostupnog sadržaja bez prijavljivanja.

Na serverskoj strani, aplikacija je realizovana korišćenjem PHP back-end logike, koja obrađuje zahteve korisnika, komunicira sa bazom podataka i generiše odgovarajući HTML/CSS/JavaScript interfejs koji se prikazuje korisniku putem web pregledača.

U MySQL bazi podataka čuvaju se informacije o:
* korisničkim nalozima (korisničko ime, lozinka, ime, prezime, fakultet, smer)
* nastavnim materijalima (skripte, zbirke zadataka, kolokvijumi, ispiti iz prethodnih rokova)
* komentarima i ocenama materijala
* predmetima, godinama studija i kategorijama
* statistici preuzimanja i popularnosti dokumenata

Studenti imaju mogućnost da postavljaju nove materijale, pregledaju i preuzimaju postojeće, dok moderator upravlja sadržajem i proverava ispravnost objavljenih dokumenata. Administrator upravlja korisničkim privilegijama i celokupnim sistemom.

Ovakva arhitektura omogućava centralizovano, sigurno i efikasno skladištenje akademskih materijala dostupnih studentima u svakom trenutku.

### 4.2. Pregled karakteristika
| Korist za korisnika | Karakteristika koja je obezbeđuje |
| :--- | :--- |
| Brz i jednostavan pristup svim materijalima za učenje | Sistem je neprekidno online i omogućava pristup sa bilo kog uređaja povezanog na internet |
| Centralizovano mesto za sve skripte i rokove | Svi materijali su organizovani po fakultetu, smeru, godini i predmetu |
| Jednostavna pretraga potrebnih dokumenata | Implementirana pretraga i filtriranje po kategorijama i nazivima predmeta |
| Mogućnost razmene znanja među studentima | Registrovani korisnici mogu postavljati, komentarisati i ocenjivati materijale |
| Sigurnost i poverljivost podataka | Pristup sistemu zaštićen je autentifikacijom i autorizacijom korisnika |
| Pouzdanost i kvalitet sadržaja | Moderator vrši proveru, izmenu i brisanje neodgovarajućih materijala |
| Pristup sa različitih platformi | Interfejs zasnovan na HTML-u, CSS-u, JavaScript-u i Django-u omogućava platformsku nezavisnost |
| Praćenje popularnosti materijala | Sistem vodi evidenciju broja pregleda i preuzimanja dokumenata |

<br>