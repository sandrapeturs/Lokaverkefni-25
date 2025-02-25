# KEST1VL - Lokaverkefni (25%) - Haust 2024

- Verkefnið er hópverkefni (en má vinna sem einstaklingsverkefni), tveir nemendur saman í hóp.
- Verkefnið skal unnið með skipanalínu á báðum tölvum hópsins.

Haldið utan um verkefnið á GitHub. Annar hópmeðlimur býr til nýja lokaða geymslu (e. private repo) á GitHub og býður hópfélaga sínum og kennara til samstarfs (e. collaberation) á geymsluna. Skilið svo hlekk á geymsluna í skilahólfið á Innu.

## Virtualbox og Ubuntu

Hvor hópmeðlimur setur upp á tölvuna sína [Virtualbox](https://www.virtualbox.org), býr þar til sýndarvél og setur upp [Ubuntu Desktop](https://ubuntu.com/download/desktop) á sýndarvélinni.

Leiðbeiningar eru [hér](https://ubuntu.com/tutorials/how-to-run-ubuntu-desktop-on-a-virtual-machine-using-virtualbox). :warning: þið verðið að breyta sjálfgefna notendanafninu og lykilorðinu.

Þeir nemendur sem eru með Apple tölvu með M1/M2/M3/M4 örgjörvanum þurfa að nota [UTM](https://mac.getutm.app) í stað Virtualbox. Leiðbeiningar fyrir uppsetnigu á Ubuntu á UTM eru [hér](https://docs.getutm.app/guides/ubuntu/).

## Verkefnalýsing

Þið hafið verið fengin til að setja upp linux tölvur fyrir lítið sprotafyrirtæki sem er að hefja starfsemi. Hjá fyrirtækinu vinna í dag 8 starfsmenn.

### Starfsmannalisti

Nafn | Notendanafn | Hópar | Lykilorð
--- | --- | --- | ---
Áslaug Hauksdóttir | aslaug | allir, forritun, markadsmal | pass.123
Björn Jóhannsson | bjorn | allir, forritun | pass.123
Bryndís Samúelsdóttir | bryndis | allir, forritun | pass.123
Elín Sveinsdóttir | elin | allir, forritun | pass.123
Ellert Gestsson | ellert | allir, forritun | pass.123
Elsa Jónsdóttir | elsa | allir, markadsmal | pass.123
Erla Þorbjörnsdóttir | erla | allir, markadsmal | pass.123
Erlendur Jónsson | erlendur | allir, markadsmal | pass.123

### Hópar

- Búið til hópana (e. group) sem nefndir eru í töflunni hér að ofan.

### Möppur

- Búið til möppuna **GÖGN** á skráarkerfis rótina (/) og svo möppurnar **Sameign**, **Forritun** og **Markadsmal** í **GÖGN**.
- Stillið réttindin á möppunum þannig að 
  - þeir sem eru í *allir* hópnum hafi les og skrifréttindi ásamt keyrsluréttindum á **Sameign** möppuna, 
  - þeir sem eru í *forritun* hópnum hafi les og skrifréttindi ásamt keyrsluréttindum á **Forritun** möppuna 
  - þeir sem eru í *markadsmal* hópnum hafi les og skrifréttindi ásamt keyrsluréttindum á **Markadsmal** möppuna.
- Tryggið að aðrir en þeir sem eru í viðeigandi hópum hafi ekki aðgang að möppunum.

### Notendur

Búið til notendurna og tryggið að þegar notendurnir eru búnir til að:

- fullt nafn sé skráð á þá,
- þeir séu settir í viðeigandi hópa,
- þeir fái bash skelina,
- heimasvæði séu búin til fyrir þá,
- í heimasvæði hvers notanda séu möppurnar **Vinna** og **Leikir** ásamt vísun (e. link) á möppurnar sem eru í **GÖGN** möppunni,
- notendur þurfi að breyta um lykilorð þegar þeir skrá sig inn í fyrsta skipti.

Setjið lykilorð á alla notendur.

Erlendur og Erla hefja ekki störf alveg strax, tryggið því að ekki sé hægt að skrá sig inn sem þau með því að læsa þeirra aðgangi.

Áslaug þarf að geta notað sudo skipunina, aðrir notendur mega ekki nota sudo skipunina.

Áslaug vill fá zsh skelina í stað bash. Setjið upp [oh my zsh](https://ohmyz.sh) fyrir hana. <!-- Hún vill fá [agnoster](https://github.com/ohmyzsh/ohmyzsh/wiki/Themes#agnoster) þemað þannig að þið skuluð setja inn [powerline fontana](https://github.com/powerline/fonts). -->

Skrifið leiðbeiningar fyrir Áslaugu þar sem þið útskýrið hvernig á að búa til notendur og setja í rétta hópa ásamt því að útskýra hvernig hún getur virkjað aðganga Erlendar og Erlu.
<!--
Setjið upp ```git``` og setjið svo upp SSH lykla fyrir GitHub á Linux vélinni ykkar og tengið við GitHub reikninginn ykkar, sjá [hér](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent).
-->
## Skil verkefnisins

Skil verkefnisins fara fram með tvennum hætti:

1. Þið sýnið kennaranum helstu virkni.
2. Skýrsla á GitHub þar sem fram kemur:
   1. Dagbók, hver gerði hvað í verkefninu.
   2. Leiðbeiningarnar sem þið gerið fyrir Áslaugu.
   3. Skjáskot (e. screenshot) af **GÖGN** möpputrénu (keyrið ```sudo ls -alR``` skipunina í **GÖGN** möppunni).
   4. Skjáskot af passwd skránni (keyrið ```tail /etc/passwd``` skipunina).
   5. Skjáskot af shadow skránni (keyrið `sudo tail /etc/shadow` skipunina).
   6. Skjáskot af group skránni (keyrið ```tail -15 /etc/group``` skipunina).
   7. Skjáskot af `skel` möppunni (keyrið `ls -al /etc/skel` skipunina).
   8. Skjáskot af heimasvæði Áslaugar (verið logguð inn sem Áslaug og keyrið `ls -a` skipunina).
   <!-- 9. Skjáskot af **public** ssh lyklinum ykkar. -->
