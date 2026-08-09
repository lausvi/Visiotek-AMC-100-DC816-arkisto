# Visiotek AMC-100 DC816 Educational Computer -arkisto

![kone](https://github.com/lausvi/Visiotek-AMC-100-DC816-arkisto/blob/main/kuvat/AMC100_front_web.jpeg)

Kerään tänne ym. laitteeseen liittyviä havaintojani, kuvia ja tulevaisuudessa toivottavasti myös levyimageja, jos sellaisia saan käsiini.

# Historiaa ja taustoja

Turkulainen äänentoistolaitteiden valmistaja Telestestä syntyi kielistudioihin erikoistunut Auditek Oy, josta taas myöhemmin lähti liikkeelle opetustietokoneisiin erikoistunut Visiotek Oy. Tietokoneen piirilevyistä osan valmisti Salora, jonka logo näkyy piirilevyillä.

> Suomen suosituin alkuaikojen koulutietokone oli kielistudioita valmistaneen Auditekin AMC-100, jota myytiin ulkomaillekin. AMC-100:t pystyi myös kytkemään lähiverkoksi. Toinen koulukäyttöön tarkoitettu CP/M-kone oli Pentti Hakalan suunnittelema Spectra eli Mikrospectra. (Ville-Matias Heikkilä @ https://skrolli.fi/2014/06/60-vuotta-suomalaisia-tietokoneita/)

Kts. "Visiotek AMC-100 - Tiatokone Suamen Turust" (Tapani Joelsson) @ Skrolli 2024.2 (https://skrolli.fi/2024.2.anttila.pdf, s. 38 alk)

# Rauta

**Levykeasemat**
+ 2x 5.25" lerppuasemat: Mitsubishi M4853-342M (04/1985) "Mini Flexible Disk Drive" - 80 tracks, 96 tracks/inch, 2 sides.
+ tarra A0-aseman etupaneelissa: "Kaksipuolinen kaksoistiheys 720 K DSDD"
+ A0-asema: DS0, B1-asema DS1 (suora kaapeli)
+ jumpperit: HS, IU, MM, A-asemassa kantaan asennettuna 150ohm terminaattori (16-pin DIP)
+ ohjainpiiri: TMS2793NL ("IBM compatible in single mode (FM) and double-density mode (MFM)" -datasheet)

**CPU**
+ NEC D70116D-8 (= V30 (8086) @ 8Mhz)

**ROM**
+ paikat neljälle ROM-piirille (2x LO, 2x HI)
+ tässä koneessa 2x M2764-2FI (tarrojen tekstissä ROM:in checksum)

**RAM**
+ Koneen sisällä viirtalähteen kannessa tussilla kirjoitettu 128 -> muistin määrä?
+ Piirit 16x TMM4164AP-15 -> täsmäisi 128k:n

**Piirilevyjen backplane**
+ 5 korttipaikkaa, tässä koneessa kolme korttia asennettuna:
  - Peripheral Interface Card 8450
  - CPU Card 8416B
  - AMC-100 Junior 8437B (mikä tämän tarkoitus? Z80 CPU + 2x M2764 EPROM, tarrojen teksti ei täsmää checksumeihin. Videolähtö tällä kortilla)
+ liitin: Perlos CO64FS-C1E-0,8/5 - backplanessa ja CPU-kortilla kaksi liitintä, muissa vain yksi

**Virtalähde**
+ Boschert XL60-3601R/4601R - 110/220V 108W - date 8611
+ jumpperikaapeli 110/220V asennoille virtalähteen sisällä
+ lähdöt backplanen liittimen tekstien perusteella: GND, +5V, +12V, -5V, -12V
+ yksi säädettävä trimmeri, jolle reikä virtalähteen suojapellissä. Arvaus: +5V jännitesäätö? Tässä koneessa sinetöity liimatipalla.
+ elkot: 2x 220/200V, 2x 220/16V SL, 2x 2200/16 pun. SXC, 1000/25 pun SXC, 220/25 RX, 2x 100/25 RX, 470/63, 470/35 pun SXC, 4,7/100 SL, 1/100 SL
+ virtaliittimessä takapaneelissa linjafiltteri (Feller AG 8843.N2.130), lisäksi virtalähteessä 3x RIFA 4700pf Y-konkat

**Kaiutin**
+ 10ohm 0,5W
+ backplanessa vapaa kytkemätön liitin SPEAKER, ehkä linjalähtö?

**Liitännät**
+ VIDEO1 (komposiittivideo monitorille, koaksiaaliliitin)
+ RF (analog.tv-viritin televisiolle, koaksiaaliliitin) - Alpsin viritin kotelon takaosassa
+ SERIAL 1 ("med" - mitä tarkoittaa?) - D25 naaras, musta
+ SERIAL 2 - D25 naaras, valkoinen
+ PARALLEL - D25 uros
+ KEYBOARD - D25 uros
+ EXT (tässä koneessa vain tyhjä, 5-pin DIN-liittimen näköinen aukko kotelossa - mille tarkoitettu?)
+ takapaneelin tarrassa maininta neljästä lisäliittiimestä: R, G, B, Sync - optio RGB-lähdölle? Ei tässä koneessa asennettuna. Backplanessa nähtävillä vapaa 5-pinninen liitin VIDEO, jossa nämä ehkä tarjolla?

**Näppäimistö**
+ QWERTY, ääkköset, F1-F15 funktionäppäimet, nuolinäppäimet ylös-alas välilyönnin vasemmalla puolella, oikealla vasen-oikea. YES- ja NO-näppäimet alimman rivin laidoissa.
+ piirilevy KEYBOARD DECODER 8438A. Ohjainpiiri NEC D80C39C + ROM M2764
+ piirilevyllä myös juotospisteet EAR ja MIC, eli ilmeisesti mahdollisuus tuoda kielistudiokäytössä myös kuulokemikrofonin linjat näppäimistön kautta
+ kiinteä johto näppäimistön päässä (9-johdinta: GND, GND, T0, CLK, DAT, STR, RST, BRK, +5), 25-pinninen D-liitin tietokoneen päässä
+ näppäimistö-reset näppäinyhdistelmällä PRINT RESET + CALL RESET

# Softa

Tällä hetkellä ainoan levykkeeni (Sukol + Brainware Kieli-Welho näyteversio) perusteella: 60k CP/M ver 2.2, muitakin?

![boot](https://github.com/lausvi/Visiotek-AMC-100-DC816-arkisto/blob/main/kuvat/boot_screenshot_web.png)
