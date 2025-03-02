# Leiðbeiningar fyrir Áslaugu

* **Bold** = kóðinn hjá tölvunni
* *Italic* = takkar
* Normal = lausn/það sem þú átt að skrifa

### Búa til notendur og setja í rétta hópa
#### Búa til notanda:
* sudo adduser [nafn] - þú setur nafnið á nýa notenda í stað [nafn]
* **New password:** pass.123 - skrá lykilorð
* **Retype new password:** pass.123 - endurtaka lykilorð
* **Full Name [ ]:** [fornafn] [eftirnafn] - skrá fullt nafn
* **Room Number [ ]:** - má slepa með því að smella á enter takkann
* **Work Phone [ ]:** - má slepa með því að smella á enter takkann
* **Home Phone [ ]:** - má slepa með því að smella á enter takkann
* **Other [ ]:** - má slepa með því að smella á enter takkann
* **Is the information correct? [Y/n]** Y - stórt Y fyrir já

#### Skrá í hópa:
* sudo pico /etc/group - opnar text editor
* **allir:x:1010:**aslaug,bjorn,bryndis,elin,ellert,elsa,erla,erlendur,[nafn] - skrá í réttan hóp (allir hópurinn)
* **forritun:x:1011:**aslaug,bjorn,bryndis,elin,ellert,[nafn] - skrá í réttan hóp (forritun hópurinn)
* **markadsmal:x:1012:**aslaug,elsa,erla,erlendur,[nafn] - skrá í réttan hóp (markadsmal hópurinn)
* *[control] takki + X* - (til að fara út ú pico)
* *[enter] takki*
* id - sínir id hjá notanda
* ls -l - sínir lista
* sudo xhange -d 0 [nafn] - lætur notanda þurfa að endur gera lykilorð

### Virkjað aðganga Erlendar og Erlu.
* sudo passwd -u erla - *til að opna aðgang fyrir **Erlu***
* sudo passwd -u erlendur - *til að opna aðgang fyrir **Erlend***
* sudo grep erla cat /etc/shadow - *til að gá hvort skipunin virkaði fyrir **Erlu***
* sudo grep erlendur cat /etc/shadow - *til að gá hvort skipunin virkaði fyrir **Erlend***
#### mynd:
* Læst - Þú checkar hvort það sé ! (ef það er ! þá er læst):
<img width="1068" alt="Screenshot 2025-02-28 at 10 11 59" src="https://github.com/user-attachments/assets/4a82059a-5d1c-4d7e-88d2-1c94f37b639b" />

* Opið:
<img width="1064" alt="Screenshot 2025-02-28 at 10 12 49" src="https://github.com/user-attachments/assets/19806d6f-9253-4130-b03b-e9dc32eccaff" />
