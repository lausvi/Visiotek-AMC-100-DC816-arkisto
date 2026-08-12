# 📝 Visiotek AMC-100 DC816 -arkisto

![kone](https://github.com/lausvi/Visiotek-AMC-100-DC816-arkisto/blob/main/kuvat/AMC100_etupaneeli_pieni.jpeg)

Kerään tänne ym. laitteeseen liittyviä havaintojani, kuvia ja tulevaisuudessa toivottavasti myös levyimageja, jos sellaisia saan käsiini lisää.

# Historiaa ja taustoja

<br />

> Suomen suosituin alkuaikojen koulutietokone oli kielistudioita valmistaneen Auditekin AMC-100, jota myytiin ulkomaillekin. AMC-100:t pystyi myös kytkemään lähiverkoksi.
>
_Ville-Matias Heikkilä @ https://skrolli.fi/2014/06/60-vuotta-suomalaisia-tietokoneita/)_

<br />

1970-luvulla perustettu turkulainen kielistudiolaitteiden valmistaja Auditek Oy alkoi 1980-luvun alussa kehitellä atk-järjestelmiä perinteisten kielistudioitten laajentamiseksi. Tästä syntyi AMC-100 opetustietokone vuonna 1982 (Z80-prosessorilla, CP/M-käyttöjärjestelmällä ja mustavalkografiikalla). Koneesta julkaistiin useampia malleja, ehkä tavallisimpana suoraan kalusteisiin sijoitettu luokkamalli. Toinen turkulainen äänetoistolaitteita valmistava yritys, Teleste, osti Auditekista ensin vuonna 1977 40% osuuden ja myöhemmin Auditekista tuli Telesten tytäryhtiö.
<br /><br />
Auditekin perustaja Jarkko Metsätähti perusti vuonna 1984 uuden yrityksen, Visiotek Oy:n, jolle Teleste myi atk-opetuslaitetoiminnot, koska Teleste ei halunnut itse osallistua kilpailuun tietokoneiden valmistuksessa. AMC-tietokoneiden piirilevyjen syövytyksen hoiti alihankintana Salora, jonka logo esiintyy monissa tietokoneen piirilevyistä. Vuosien 1984–1989 välillä koneeseen tuli tarjolle uusia prosessorikortteja, 5,25" lerppuasema muuttui 3,5" korppuasemaksi ja käyttöjärjestelmä CP/M:stä MS-DOS:ksi. Myöhempiä malleja olivat mm. AMC-100/8, AMC-100/16, AMC-100/XT, AMC-100/AT.

_Kts. "Visiotek AMC-100 - Tiatokone Suamen Turust" (Tapani Joelsson) @ Skrolli 2024.2 (https://skrolli.fi/2024.2.anttila.pdf, s. 38 alk)_

<br />

# 🪛 Rauta

<br />
Ulkoisesti kone on suuri, n. 50cm leveä, 42cm syvä ja 13cm korkea. Painava. Koneessa on kahden 5.25" asemapaikan lisäksi virtalähde sekä korttikehikko johon koneen CPU- ja muut piirilevykortit asetetaan. Koneessa on sisäärakennettu kaiutin. <br />

🖼️ [Kone sisältä](https://github.com/lausvi/Visiotek-AMC-100-DC816-arkisto/blob/main/kuvat/AMC100_sisus.jpg)

<br />

**Levykeasemat**
+ 2x 5.25" lerppuasemat: Mitsubishi M4853-342M (04/1985) "Mini Flexible Disk Drive" - 80 tracks, 96 tracks/inch, 2 sides.
+ tarra A0-aseman etupaneelissa: "Kaksipuolinen kaksoistiheys 720 K DSDD"
+ A0-asema: DS0, B1-asema DS1 (suora kaapeli)
+ jumpperit: HS, IU, MM, A-asemassa kantaan asennettuna 150ohm terminaattori (16-pin DIP)
+ ohjainpiiri: TMS2793NL ("IBM compatible in single mode (FM) and double-density mode (MFM)" -datasheet)

**CPU**
+ NEC D70116D-8 (=NEC V30, eli 8086-yhteensopiva) @ 8Mhz)

**ROM**
+ paikat neljälle ROM-piirille (2x LO, 2x HI)
+ tässä koneessa 2x M2764-2FI (tarrojen tekstissä ROM:in checksum)

**RAM**
+ Koneen sisällä viirtalähteen kannessa tussilla kirjoitettu 128 -> muistin määrä?
+ Piirit 16x TMM4164AP-15 -> täsmäisi 128k:n

**Piirilevyt ja niiden backplane**
+ 5 korttipaikkaa ja kehikko, tässä koneessa kolme korttia asennettuna:
  - Peripheral Interface Card 8450. Test-jumpperin tarkoitus?
  - CPU Card 8416B
  - AMC-100 Junior 8437B (mikä tämän tarkoitus? Z80 CPU + 2x M2764 EPROM, tarrojen teksti ei täsmää checksumeihin. Videolähtö tällä kortilla)
  - 🖼️ [Kuvia piirilevyistä](https://github.com/lausvi/Visiotek-AMC-100-DC816-arkisto/tree/main/kuvat/PCB)
+ liitin: Perlos CO64FS-C1E-0,8/5 - backplanessa ja CPU-kortilla kaksi liitintä, muissa vain yksi

**Virtalähde**
+ Boschert XL60-3601R/4601R - 110/220V 108W - date 8611
+ jumpperikaapeli 110/220V asennoille virtalähteen sisällä
+ lähdöt backplanen liittimen tekstien perusteella: GND, +5V, +12V, -5V, -12V
+ yksi säädettävä trimmeri, jolle reikä virtalähteen suojapellissä. Arvaus: +5V jännitesäätö? Tässä koneessa sinetöity liimatipalla.
+ elkot: 2x 220/200V, 2x 220/16V SL, 2x 2200/16 pun. SXC, 1000/25 pun SXC, 220/25 RX, 2x 100/25 RX, 470/63, 470/35 pun SXC, 4,7/100 SL, 1/100 SL
+ virtaliittimessä takapaneelissa linjafiltteri (Feller AG 8843.N2.130), lisäksi virtalähteessä 3x RIFA 4700pf Y-konkat
+ virtakytkin ja -merkkivalo etupaneelin vasemmassa yläkulmassa
+ 🖼️ [Kuvia virtalähteestä](https://github.com/lausvi/Visiotek-AMC-100-DC816-arkisto/tree/main/kuvat/PCB)

**Kaiutin**
+ 10ohm 0,5W pienoiskaiutin koneen sisällä
+ backplanessa vapaa kytkemätön liitin SPEAKER, ehkä linjalähtö koska sis.kaiuttimen signaali tulee muualta?

**Liitännät**
+ 🖼️ [Takapaneeli](https://github.com/lausvi/Visiotek-AMC-100-DC816-arkisto/blob/main/kuvat/AMC100_takapaneeli.jpg)
+ VIDEO1 (komposiittivideo monitorille, koaksiaaliliitin)
+ RF (analog.tv-viritin televisiolle, koaksiaaliliitin) - Alpsin viritin kotelon takaosassa
+ SERIAL 1 ("med" - mitä tarkoittaa?) - D25 naaras, musta
+ SERIAL 2 - D25 naaras, valkoinen
+ PARALLEL - D25 uros
+ KEYBOARD - D25 uros
+ EXT (tässä koneessa vain tyhjä, 5-pin DIN-liittimen näköinen aukko kotelossa - mille tarkoitettu?)
+ takapaneelin kuvassa maininta neljästä lisäliittiimestä: R, G, B, Sync - ilmeisesti siis malliin oli optio RGB-lähdölle? Backplanessa nähtävillä vapaa 5-pinninen liitin VIDEO, jossa signaalit ehkä tarjolla?

**Näppäimistö**
+ QWERTY, ääkköset, F1-F15 funktionäppäimet, nuolinäppäimet ylös-alas välilyönnin vasemmalla puolella, oikealla vasen-oikea. YES- ja NO-näppäimet alimman rivin laidoissa.
+ piirilevy KEYBOARD DECODER 8438A. Ohjainpiiri NEC D80C39C + ROM M2764
+ piirilevyllä myös juotospisteet EAR ja MIC, eli ilmeisesti mahdollisuus tuoda kielistudiokäytössä myös kuulokemikrofonin linjat näppäimistön kautta
+ kiinteä johto näppäimistön päässä (9-johdinta: GND, GND, T0, CLK, DAT, STR, RST, BRK, +5), 25-pinninen D-liitin tietokoneen päässä
+ näppäimistö-reset näppäinyhdistelmällä PRINT RESET + CALL RESET
+ Ulkoiset mitat: 35cm leveä, 20cm syvä, n. 5cm korkea.
+ 🖼️ [Kuvia näppäimistöstä](https://github.com/lausvi/Visiotek-AMC-100-DC816-arkisto/tree/main/kuvat/näppäimistö)

<br />

# 💾 Softa

![boot](https://github.com/lausvi/Visiotek-AMC-100-DC816-arkisto/blob/main/kuvat/boot_screenshot.png)

Tällä hetkellä ainoan levykkeeni (Sukol + Brainware Kieli-Welho näyteversio) perusteella: 60k CP/M ver 2.2, muitakin?

<br />

![softa](https://github.com/lausvi/Visiotek-AMC-100-DC816-arkisto/blob/main/kuvat/kieli-welho_screenshot.png)

🎮 Katso "läpipeluuvideo": <https://archive.org/details/amc-100-kieliwelho>

<br />

# ❔Kysymyksiä

+ Miten mallimerkintä "AMC-100 DC" ja "DC816" pitäisi tulkita?
+ Miten avauslainauksessa mainittu lähiverkko oli rakennettu?
+ Tässä kuvatussa laitteessa on sekä Z80 että 8086-prosessori, onko ensimmäinen yhteensopivuutena vanhempien vain CP/M-mallien softille, vai miksi molemmat?
