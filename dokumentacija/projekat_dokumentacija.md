# ScriptShare

<br>

## Sadržaj
1. [Uvod](#1-uvod)
    - [1.1. Rezime](#11-rezime)
    - [1.2. Namena dokumenta i ciljne grupe](#12-namena-dokumenta-i-ciljne-grupe)
2. [Opis problema i inovativna rešenja](#2-opis-problema)
3. [Kategorije korisnika](#3-kategorije-korisnika)
    - [3.1. Gost](#31-gost)
    - [3.2. Student](#32-student)
    - [3.3. Moderator](#33-moderator)
    - [3.4. Administrator](#34-administrator)
4. [Opis proizvoda](#4-opis-proizvoda)
    - [4.1. Pregled arhitekture sistema](#41-pregled-arhitekture-sistema)
    - [4.2. Pregled karakteristika](#42-pregled-karakteristika)
5. [Funkcionalni zahtevi](#5-funkcionalni-zahtevi)
    - [5.1. Autentifikacija i upravljanje nalogom](#51-autentifikacija-i-upravljanje-nalogom)
        - [5.1.1. Registracija](#511-registracija)
        - [5.1.2. Prijavljivanje](#512-prijavljivanje)
        - [5.1.3. Upravljanje profilom](#513-upravljanje-profilom)
        - [5.1.4. Resetovanje lozinke](#514-resetovanje-lozinke)
    - [5.2. Funkcionalnosti za goste](#52-funkcionalnosti-za-goste)
        - [5.2.1. Pretraga materijala](#521-pretraga-materijala)
        - [5.2.2. Pregled materijala](#522-pregled-materijala)
    - [5.3. Funkcionalnosti za studente](#53-funkcionalnosti-za-studente)
        - [5.3.1. Otpremanje materijala](#531-otpremanje-materijala)
        - [5.3.2. Preuzimanje materijala](#532-preuzimanje-materijala)
        - [5.3.3. Interakcija (Komentarisanje i ocenjivanje)](#533-interakcija-komentarisanje-i-ocenjivanje)
        - [5.3.4. Lista omiljenih](#534-lista-omiljenih)
        - [5.3.5. Gamifikacija (Bodovi i bedževi)](#535-gamifikacija-bodovi-i-bedževi)
        - [5.3.6. Bounty sistem](#536-bounty-sistem)
    - [5.4. Funkcionalnosti za moderatore i administratore](#54-funkcionalnosti-za-moderatore-i-administratore)
        - [5.4.1. Odobravanje materijala](#541-odobravanje-materijala)
        - [5.4.2. Brisanje sadržaja](#542-brisanje-sadržaja)
        - [5.4.3. Upravljanje korisnicima](#543-upravljanje-korisnicima)
        - [5.4.4. Dodela verifikovanog statusa](#544-dodela-verifikovanog-statusa)
6. [Pretpostavke i ograničenja](#6-pretpostavke-i-ograničenja)
7. [Kvalitet](#7-kvalitet)
8. [Nefunkcionalni zahtevi](#8-nefunkcionalni-zahtevi)
    - [8.1. Sistemski zahtevi](#81-sistemski-zahtevi)
    - [8.2. Performanse i dostupnost](#82-performanse-i-dostupnost)
9. [Zahtevi za korisničkom dokumentacijom](#9-zahtevi-za-korisničkom-dokumentacijom)
    - [9.1. Uputstva za korišćenje sajta](#91-uputstva-za-korišćenje-sajta)
    - [9.2. Označavanje](#92-označavanje)
10. [Plan i prioriteti](#10-plan-i-prioriteti)

---
<br>

## 1. Uvod

### 1.1 Rezime
Projekat ScriptShare je deo praktične nastave predmeta Principi softverskog inžinjerstva. Aplikacija je namenjena studentima za jednostavnu razmenu materijala kao što su skripte, beleške, zbirke zadataka i prethodni ispiti.

### 1.2 Namena dokumenta i ciljne grupe
Tekst koji sledi definiše namenu aplikacije, zahteve i funkcionalnosti koje ona upotrebljava i pruža, namenjen je svim članovima tima.

<br><br>

## 2. Opis problema i inovativna rešenja
Ova aplikacija stupa u pomoć studentima i omogućava im da na jednom mestu imaju brz, jednostavan i pouzdan pristup materijalima za učenje.

U tu svrhu razvija se aplikacija **ScriptShare**, koja predstavlja centralizovano mesto namenjeno studentima za razmenu i organizaciju nastavnih materijala. Korisnici sistema imaju mogućnost da pregledaju dostupne skripte, ispitne rokove iz ranijih godina, zbirke zadataka, laboratorijske vežbe i druge korisne materijale vezane za određene predmete.

Pored osnovnog problema rasutosti materijala, ScriptShare rešava i problem **motivacije korisnika** i **pouzdanosti sadržaja**. 

ScriptShare uvodi inovativne mehanizme koji rešavaju neaktivnost korisnika i nepouzdanost sadržaja:
* **Sistem potražnje (Bounty)**: Umesto da korisnici čekaju da neko postavi materijal, oni aktivno mogu da zahtevaju specifične dokumente, stimulišući druge korisnike nagradama u vidu bodova.
* **Gamifikacija**: Integracija bodovnog sistema direktno podstiče kvantitet i kvalitet doprinosa, pretvarajući deljenje znanja u interaktivno iskustvo.
* **Aktivna provera kvaliteta**: Uz pomoć vizuelnog isticanja verifikovanog sadržaja, korisnik odmah zna koji je materijal prošao proveru.

Registrovani korisnici, pored pregleda sadržaja, mogu da postavljaju nove materijale, preuzimaju postojeće dokumente, ocenjuju njihovu korisnost i ostavljaju komentare kako bi pomogli drugim studentima pri izboru odgovarajućih resursa. Sistem omogućava kategorizaciju materijala po fakultetu, smeru, godini studija i predmetu, čime se značajno olakšava pretraga i pristup željenim dokumentima.

Moderator sistema brine o ažurnosti i kvalitetu sadržaja, ima mogućnost dodavanja, izmene i brisanja materijala, kao i odobravanja novih objava korisnika. Administrator vodi računa o upravljanju korisničkim nalozima, autorizaciji i dodeli korisničkih privilegija.

Na početnoj strani aplikacije nalaze se najnovije i najpopularnije skripte, obaveštenja o aktuelnim ispitnim rokovima, kao i preporučeni materijali koji mogu biti od značaja studentima.

<br><br>

## 3. Kategorije korisnika
Aplikacija podržava više tipova korisnika: goste, studente, moderatore i administratore.

### 3.1. Gost
Posetilac sajta koji nema nalog. Gost sajta ima mogućnost da pregleda sadržaj, kao i mogućnost registracije.

### 3.2. Student
Student je registrovani korisnik koji prilikom prijavljivanja dobija mogućnost postavljanja materijala, preuzimanja materijala, komentarisanja, ocenjivanja kao i čuvanja omiljenih materijala.

### 3.3. Moderator
Korisnik zadužen za ispravnost materijala. Njegov fokus je da proverava pristigle materijale, dodeljivanje verifikovanog statusa i održavanju reda u komentarima. Nema ovlašćenja nad korisničkim nalozima u smislu promene privilegija.

### 3.4. Administrator
Korisnik zadužen za sistemsku administraciju. Upravlja korisničkim nalozima (banovanje, dodela uloga) i ima pun pristup bazi podataka. On nadgleda rad moderatora i zadužen je za tehničko održavanje platforme.

<br><br>

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
* korisničkim nalozima (korisničko ime, mejl, lozinka, ime, prezime, fakultet, smer)
* nastavnim materijalima (skripte, zbirke zadataka, kolokvijumi, ispiti iz prethodnih rokova)
* komentarima i ocenama materijala
* predmetima, godinama studija i kategorijama
* statistici preuzimanja i popularnosti dokumenata

Studenti imaju mogućnost da postavljaju nove materijale, pregledaju i preuzimaju postojeće, dok moderator upravlja sadržajem i proverava ispravnost objavljenih dokumenata. Administrator upravlja korisničkim privilegijama i celokupnim sistemom.

Ovakva arhitektura omogućava centralizovano, sigurno i efikasno skladištenje akademskih materijala dostupnih studentima u svakom trenutku.

### 4.2. Pregled karakteristika
| Korist za korisnika | Karakteristika koja je obezbeđuje |
| :--- | :--- |
| Brz pristup materijalima | Optimizovana pretraga i hijerarhijska kategorizacija |
| Motivacija za doprinos | Bodovni sistem i rangiranje (bedževi) |
| Poverenje u sadržaj | Verifikovan status dodeljen od strane moderatora |
| Nabavka retkih skripti | Sistem potražnje (Bounty) koji nagrađuje specifična otpremanja materijala |
| Pouzdanost i kvalitet sadržaja | Moderator vrši proveru, izmenu i brisanje neodgovarajućih materijala |
| Platformska nezavisnost | Odzivan (responsive) web dizajn dostupan na svim uređajima |

<br><br>

## 5. Funkcionalni zahtevi
U ovom odeljku definišu se osnovne funkcije koje sistem treba da obezbedi različitim kategorijama korisnika radi efikasne razmene akademskog sadržaja.

<br>

### 5.1. Autentifikacija i upravljanje nalogom
Ova grupa funkcija osigurava bezbednost sistema i personalizaciju korisničkog iskustva. Pristup privatnim podacima i interaktivnim funkcijama strogo je ograničen na autorizovane korisnike.


#### 5.1.1. Registracija
Ukoliko korisnik nema svoj nalog, može ga kreirati unošenjem ličnih (korisničko ime i lozinka) i akademskih podataka (ime, prezime, fakultet, smer, mejl). Ovi podaci se upisuju u bazu podataka, čime korisnik dobija status studenta i mogućnost pristupa naprednim funkcijama sistema.

#### 5.1.2. Prijavljivanje
Registrovani korisnici, moderatori i administratori se autorizuju unošenjem korisničkog imena i lozinke. Ovi kredencijali moraju da se poklope sa postojećim podacima u bazi. Nakon potvrđene autorizacije, sistem dodeljuje odgovarajuće privilegije u skladu sa ulogom korisnika.

#### 5.1.3. Upravljanje profilom
Autorizovani korisnik može da pristupi interfejsu za pregled i izmenu svojih podataka. Ovo obuhvata promenu lozinke, ažuriranje akademskih informacija i uvid u istoriju sopstvenih objavljenih materijala.

#### 5.1.4. Resetovanje lozinke
Sistem omogućava korisnicima koji su izgubili pristupne podatke da samostalno pokrenu proces resetovanja lozinke. Unosom registrovane mejl adrese, korisnik dobija automatski generisan privremeni link putem kojeg može postaviti novu lozinku.

<br>

### 5.2. Funkcionalnosti za goste

#### 5.2.1. Pretraga materijala
Sistem omogućava gostima pretragu baze podataka putem ključnih reči. Pretraga se može filtrirati prema fakultetu, smeru ili predmetu kako bi se brzo pronašli relevantni dokumenti.

#### 5.2.2. Pregled materijala
Gosti mogu pregledati osnovne informacije o dostupnim skriptama i materijalima (naslov, opis, autor i ocena), ali nemaju mogućnost preuzimanja fajlova ili uvida u komentare dok se ne registruju.

<br>

### 5.3. Funkcionalnosti za studente
Studenti su primarna kategorija korisnika kojima je omogućena puna interakcija sa sadržajem i drugim članovima platforme.

#### 5.3.1. Otpremanje materijala
Studenti mogu dodavati nove materijale (skripte, beleške, ispitne rokove) putem generisanih formi. Prilikom unosa, obavezno je definisati kategoriju i predmet. Svaki postavljeni fajl se šalje na proveru pre nego što postane vidljiv ostalim korisnicima.

#### 5.3.2. Preuzimanje materijala
Autorizovani studenti imaju neograničenu mogućnost preuzimanja dostupnih materijala iz baze podataka na svoj lokalni uređaj.

#### 5.3.3. Interakcija (Komentarisanje i ocenjivanje)
Korisnici mogu ocenjivati korisnost materijala i ostavljati tekstualne komentare. Ove akcije se beleže u bazi i direktno utiču na rangiranje i vidljivost materijala na početnoj strani.

#### 5.3.4. Lista omiljenih
Sistem nudi mogućnost čuvanja određenih materijala u privatnu listu omiljenih. Time se studentu omogućava brz pristup često korišćenim dokumentima bez ponovne pretrage.

#### 5.3.5. Gamifikacija (Bodovi i bedževi)
Sistem prati korisnost doprinosa svakog studenta. Autori čiji materijali dobijaju visoke ocene ili veliki broj preuzimanja automatski akumuliraju poene. Ovi poeni vode do osvajanja bedževa koji se prikazuju na profilu korisnika, čime se gradi reputacija unutar zajednice i motiviše deljenje proverenog sadržaja. Korisnici sakupljaju bodove kroz aktivnosti:
* Otpremanje materijala: 10 bodova.
* Visoka ocena: Dodatni bodovi ukoliko materijal dobije prosečnu ocenu iznad 4.5.
* Bedževi: Vizuelne ikonice na profilu (npr. *Donator* za 10 otpremljenih fajlova, *Ekspert* ukoliko najmanje 5 materijala koje je otpremio jedan korisnik imaju verifikovan status).

#### 5.3.6. Bounty sistem
Ukoliko traženi dokument ne postoji u bazi, student može objaviti javni zahtev (potražnju). Korisnik koji odgovori na zahtev i prvi postavi adekvatan materijal dobija bonus od 50 bodova i specijalan bedž, čime se stimuliše širenje baze podataka za retke predmete.

Student ne može da odgovori na zahtev ukoliko ga je on objavio.

<br>

### 5.4. Funkcionalnosti za moderatore i administratore
Ove funkcionalnosti su namenjene održavanju kvaliteta, reda i tehničke ispravnosti sistema ScriptShare.

#### 5.4.1. Odobravanje materijala
Moderatori imaju pristup interfejsu koji omogućava pregled svih novopristiglih dokumenata. Oni mogu potvrditi objavu materijala, zatražiti izmenu ili ga trajno ukloniti ukoliko ne ispunjava akademske standarde. Tek nakon njegove potvrde, materijal postaje vidljiv svima.

#### 5.4.2. Brisanje sadržaja
U cilju održavanja kvaliteta moderatori mogu vršiti uklanjanje neadekvatnih komentara ili materijala koji krše pravila (npr. uvredljiv sadržaj ili spam). Svako brisanje se automatski reflektuje u bazi podataka i na korisničkom interfejsu.

#### 5.4.3. Upravljanje korisnicima
Administrator sistema poseduje ekskluzivna prava za dodeljivanje moderatorskih privilegija, blokiranje ili brisanje korisničkih naloga i rešavanje tehničkih problema.

#### 5.4.4. Dodela verifikovanog statusa
Moderatori imaju opciju za dodelu oznake "Verifikovan" materijalima koji su prošli proveru relevantnosti i tačnosti (npr. zvanični ispitni rokovi). Ovi materijali dobijaju vizuelni identifikator (bedž poverenja) i prioritet u rezultatima pretrage.

<br><br>

## 6. Pretpostavke i ograničenja
Prilikom razvoja sistema potrebno je težiti jedinstvenom i intuitivnom dizajnu koji olakšava navigaciju kroz akademske materijale. Neophodno je strogo voditi računa o bezbednosti autorizacionih podataka kako bi se sprečio neovlašćeni pristup privatnim informacijama korisnika.

* **Validnost profila:** Pretpostavlja se da korisnici unose tačne akademske podatke radi pravilne organizacije baze.
* **Tehnička ograničenja:** Maksimalna veličina otpremljenog fajla je **50MB**.
* **Formati:** Podržani su isključivo standardni formati (PDF, DOCX, PPTX, JPG, PNG, MD, TXT).
* **Sigurnost baze:** Lozinke se čuvaju isključivo u enkriptovanom (hashing) formatu; administrator nema uvid u lozinke u čistom tekstu.
* **Internet veza:** Aplikacija ne podržava offline rad; za pristup je neophodna aktivna internet konekcija.

<br><br>

## 7. Kvalitet
Sve definisane funkcionalnosti sistema moraju biti podvrgnute testiranju metodom crne kutije. Poseban fokus biće stavljen na:
* **Performanse:** Testiranje brzine odziva servera i kapaciteta baze podataka pri  pristupu velikog broja korisnika.
* **Otpornost na greške:** Validacija svih korisničkih unosa kako bi se sprečili padovi sistema.
* **Bezbednost:** Implementacija zaštite od malicioznih napada, sa posebnim naglaskom na sprečavanje SQL injekcija, čime se osigurava integritet baze podataka.

<br><br>

## 8. Nefunkcionalni zahtevi

### 8.1. Sistemski zahtevi
Za funkcionisanje sistema neophodno je da serversko okruženje podržava PHP servis i MySQL bazu podataka. Korisnički interfejs treba da bude raspoloživ za većinu poznatih internet pretraživača.

### 8.2. Ostali zahtevi
Sistem mora obezbediti visok stepen interaktivnosti i tečan rad korisničkog interfejsa. Odziv sistema treba da bude optimizovan tako da korisniku pruži neometano iskustvo prilikom pretrage i pregleda materijala.

<br><br>

## 9. Zahtevi za korisničkom dokumentacijom

### 9.1. Uputstva za korišćenje sajta
Potrebno je izraditi detaljno uputstvo za studente (proces registracije i pravilnog otpremanja materijala) i namensko uputstvo za moderatore, koje definiše kriterijume i tehničke korake za odobravanje ili odbijanje sadržaja.

### 9.2. Označavanje
Svaka stranica aplikacije mora sadržati logotip platforme ScriptShare. Stranice sa materijalima moraju imati jasno istaknutu putanju (breadcrumb): **Fakultet > Smer > Godina > Predmet**. Na profilu korisnika moraju biti vidljivi osnovni identifikacioni podaci.

<br><br>

## 10. Plan i prioriteti
U prvoj fazi razvoja, fokus je na sledećim prioritetima:
* Implementacija sistema za autentifikaciju i autorizaciju.
* Razvoj modula za otpremanje i kategorizaciju materijala po fakultetima i predmetima.
* Osnovna pretraga i filtriranje sadržaja.
* Interfejs za moderatorsko odobravanje dokumenata.

U završnim fazama projekta, akcenat će biti stavljen na sistem gamifikacije, bounty mehanizam i verifikaciju materijala, čime će ScriptShare postati napredna i samoodrživa platforma.