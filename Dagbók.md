# Dagbók

* **Bold** = kóðinn hjá tölvuni
* Normal = svör

### Möppur:
Búið til möppu GÖGN á skráarkerfis rótina (/) og svo möppurnar Sameign, Forritun og Markadsmal í GÖGN.
### #1 Lausn - Búa til GOGN möppuna: 
* cd /
* ls 
* sudo mkdir GOGN
* ls 
* ls -l /
* cd /
* sudo chown ubuntu GOGN
* ls -l

### #2 Lausn - Búa til möppurnar Sameign, Forritun og Markadsmal í GÖGN möppuna:
* cd GOGN
* mkdir Sameign
* ls (gá hvort það virkaði)
* mkdir Forritun
* mkdir Markadsmal 
* ls (gá hvort það virkaði)
### Notendur:
Búðu til notendurna og tryggið að þegar notendurnir eru búnir til að:
Fullt nafn sé skráð á þá,
Lausn: …
Þeir séu settir í viðeigandi hópa,
Lausn: …
Þeir fái bash skelina,
Lausn: …
Heimasvæði hvers notanda séu möppurnar Vinna og Leikir ásamt vísun (e. link) á möppurnar sem eru í GÖGN möppunni,
Lausn: …
Notendur þurfi að breyta um lykilorð þegar þeir skrá sig inn í fyrsta skipti.
Lausn: …
### #3 Lausn: 
#### Áslaug:
* sudo adduser aslaug
* **New password:** pass.123
* **Retype new password:** pass.123
* **Full Name [ ]:** Áslaug Hauksdóttir
* **Room Number [ ]:** 205
* **Work Phone [ ]:**
* **Home Phone [ ]:**
* **Other [ ]:**
* **Is the information correct? [Y/n]** Y
#### Björn:
* sudo adduser bjorn
* **New password:** pass.123
* **Retype new password:** pass.123
* **Full Name [ ]:** Björn Jóhannsson
* **Room Number [ ]:** 205
* **Work Phone [ ]:**
* **Home Phone [ ]:**
* **Other [ ]:**
* **Is the information correct? [Y/n]** Y
* (endur taka fyrir alla notendur)

### Hópar:
### #4 Lausn - Búið til hópana (e.group) sem nefndir eru í töflunni hér að ofan: 
* :/GOGN$ sudo groupadd allir
* :/GOGN$ sudo groupadd forritun
* :/GOGN$ sudo groupadd markadsmal
* tail -12 /etc/group
* Sudo pico /etc/group
* allir:x:1010:aslaug,bjorn,bryndis,elin,ellert,elsa,erla,erlendur
* forritun:x:1011:aslaug,bjorn,bryndis,elin,ellert
* markadsmal:x:1012:aslaug,elsa,erla,erlendur
* [control] + [X] (til að fara út ú pico)
* [enter]
* id
* ls -l
* sudo chgrp allir Sameign
* sudo chgrp forritun Forritun
* sudo chgrp markadsmal Markadsmal
* ls -l
* chmod o-rx Forritun (lokar á aðgang fyrir aðilla sem eru ekki í Forritun möppuni)
* chmod o-rx Markadsmal (lokar á aðgang fyrir aðilla sem eru ekki í Markadsmal möppuni)
* chmod o-rx Sameign (lokar á aðgang fyrir aðilla sem eru ekki í Sameign möppuni)
* ls -l

### #5 lausn - skipun sem lætur alla endur gera password í fyrsta skypti sem maður logar in:
* sudo tail /etc/passwd
* sudo xhange -d 0 aslaug
* sudo xhange -d 0 bjorn
* sudo xhange -d 0 bryndis
* sudo xhange -d 0 elin
* sudo xhange -d 0 ellert
* sudo xhange -d 0 elsa
* sudo xhange -d 0 erla
* sudo xhange -d 0 erlendur

### #6 lausn - gefa Áslaugu sudo réttindi:
* sudo usermod -aG sudo aslaug
* groups aslaug
* **aslaug : aslaug sudo users allir forritun markadsmal**

### #7 lausn - læsa fyrir Erlu og Erlend:
* sudo passwd -l erla
* sudo passwd -l erlendur
* sudo grep erla cat /etc/shadow
* sudo grep erlendur cat /etc/shadow

### #8 lausn - setja möppurnar Vinna og Leikir í heimasvæði hvers notanda, ásamt vísun á möppurnar sem eru í GÖGN möppunni
* sudo mkdir /home/aslaug/Vinna /home/aslaug/Leikir
* sudo ln -s /GOGN /home/aslaug/GOGN
* sudo chown -h aslaug:aslaug /home/aslaug/GOGN
* sudo chown aslaug:aslaug /home/aslaug/Vinna /home/aslaug/Leikir
* sudo chmod 700 /home/aslaug/Vinna /home/aslaug/Leikir
* sudo ls -l /home/aslaug
