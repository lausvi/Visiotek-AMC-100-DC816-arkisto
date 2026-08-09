# Visiotek-AMC-100-DC816-arkisto
Arkisto kuvia ja materiaalia suomalaisen 80-luvun opetustietokone Visiotek AMC-100:an liittyen

![kone](https://github.com/lausvi/Visiotek-AMC-100-DC816-arkisto/blob/main/kuvat/AMC100_front_web.jpeg)

> Suomen suosituin alkuaikojen koulutietokone oli kielistudioita valmistaneen Auditekin AMC-100, jota myytiin ulkomaillekin. AMC-100:t pystyi myös kytkemään lähiverkoksi. Toinen koulukäyttöön tarkoitettu CP/M-kone oli Pentti Hakalan suunnittelema Spectra eli Mikrospectra. (https://skrolli.fi/2014/06/60-vuotta-suomalaisia-tietokoneita/)

Kts. "Visiotek AMC-100 - Tiatokone Suamen Turust" (Tapani Joelsson) @ Skrolli 2024.2 (https://skrolli.fi/2024.2.anttila.pdf, s. 38 alk)  

# Rauta

**Levykeasemat** (5.25"): 2x Mitsubishi M4853-342M (04/1985)
+ tarra aseman etupaneelissa: "Kaksipuolinen kaksoistiheys 720 K DSDD"
+ 80 tracks/side, 2 sides, 96 tracks/inch?
+ A0-asema: DS0, B1-asema DS1 (suora kaapeli)
+ jumpperit: TODO
+ ohjain: TMS2793NL ("IBM compatible in single mode (FM) and double-density mode (MFM)" -datasheet)

**CPU**
+ NEC D70116D-8 (= V30 (8086) @ 8Mhz)

**ROM**
+ 2x M2764-2FI, paikat neljälle (2 LO, 2 HI) - tarrojen teksti = checksum

**Junior board**: Z80 CPU + 2x M2764 EPROM, tarrojen teksti ei täsmää checksumeihin

**RAM**
+ Virtalähteen kannessa tussilla kirjoitettu 128 - muistin määrä?
+ 16x TMM4164AP-15 -> täsmäisi 128k:n

**Piirilevyjen backplane**
+ 5x korttipaikkaa
+ liitin: Perlos CO64FS-C1E-0,8/5

**Virtalähde**
+ Boschert XL60-3601R/4601R - 110/220V 108W - date 8611
+ jumpperikaapeli 110/220V asennoille virtalähteen sisällä
+ elkot: 2x 220/200V, 2x 220/16V SL, 2x 2200/16 pun. SXC, 1000/25 pun SXC, 220/25 RX, 2x 100/25 RX, 470/63, 470/35 pun SXC, 4,7/100 SL, 1/100 SL
+ virtaliittimessä takapaneelissa filtterit, lisäksi virtalähteessä 3x RIFA 4700pf Y-konkat

**Kaiutin**
+ 10ohm 0,5W

**Näppäimistö**
+ reset = PRINT RESET + CALL RESET

# Softa

60k CP/M ver 2.2?
