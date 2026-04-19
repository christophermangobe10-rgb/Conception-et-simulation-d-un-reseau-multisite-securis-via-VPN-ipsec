<h1>Conception et simulation d'un reseau multisite securis via VPN ipsec site-to-site</h1>

 ### [Démonstration du projet](https://youtu.be/7eJexJVCqJo)

<h2>Description</h2>
Dans ce projet, nous avons ;
crée un tunnel vpn ipsec site-to-site entre deux sites,
realisé la segmentation reseau,
realisé le routage inter-vlans,
appliqué le principe de moindre privilege.
<br />


<h2>Languages and Utilities Used</h2>

- <b>bash</b> 

<h2>Environments Used </h2>

- <b>GNS3</b>
- <b>VMWare Workstation Pro</b>
- <b>WireShark</b>
- <b>Navigateur web (Firefox)</b> (21H2)




<h2>Program walk-through:</h2>

<p align="center">
Figure 16 - Interconnexion des réseaux locaux: <br/>
<img src="https://imgur.com/6Gb1fLO.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Figure 17 - Schéma réseau du site principal:  <br/>
<img src="https://imgur.com/J2SYBBB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Figure 18 - Schéma réseau du site distant: <br/>
<img src="https://imgur.com/grhYDXU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Figure 29 - Résumé des configurations effectuées sur le switch/l3 du site principale:  <br/>
<img src="https://imgur.com/AtudrwW.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Figure 49 : Résultats des configurations effectuées sur le switch/l3 du site distant:  <br/>
<img src="https://imgur.com/ojv8eTF.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Politique firewall site distant:  <br/>
<img src="https://imgur.com/GusB4fc.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Politique firewall site principale (VLAN Admins):  <br/>
<img src="https://imgur.com/JLcYksO.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://imgur.com/sOsMoKr.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://imgur.com/rEPMEYr.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Politique firewall site principale (VLAN Users):  <br/>
<img src="https://imgur.com/tZYJnau.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Politique firewall site principale (VLAN Servers):  <br/>
<img src="https://imgur.com/7N4DZE8.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Figure 61 - Configuration vpn ipsec tunnel phase 1 au site principale:  <br/>
<img src="https://imgur.com/GamCFN8.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Figure 62 - Configuration vpn ipsec tunnel phase 2 au site principale:  <br/>
<img src="https://imgur.com/0KAuQAA.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Figure 63 - Configuration vpn ipsec tunnel phase 1 au site distant:  <br/>
<img src="https://imgur.com/rVz1WYx.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Figure 64 - Configuration vpn ipsec tunnel phase 2 au site distant:  <br/>
<img src="https://imgur.com/PhDafqQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Figure 73 - Topologie du réseau sous GNS3:  <br/>
<img src="https://imgur.com/ADz8ZJY.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Figure 74 - teste de connectivité inter-vlans au site principale (PC-VLAN10-1):  <br/>
<img src="https://imgur.com/uDu1MzF.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Figure 75 - teste de connectivité inter-vlans au site principale (PC-VLAN20-1):  <br/>
<img src="https://imgur.com/PoGFwKa.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Figure 76 - teste de connectivité inter-vlans au site principale (Mon serveur):  <br/>
<img src="https://imgur.com/BUSNJvj.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Figure 77 - teste de connectivité inter-vlans au site distant (PC-VLAN100-1):  <br/>
<img src="https://imgur.com/3JIFTQc.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Figure 78 - teste de connectivité inter-vlans au site distant (PC-VLAN101-1):  <br/>
<img src="https://imgur.com/3UWnzXA.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Figure 79 - teste de connectivité Site distant vers le serveur/site principale (PC-VLAN100-1):  <br/>
<img src="https://imgur.com/jT5DH7o.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Figure 80 - teste de connectivité Site distant vers le serveur/site principale (PC-VLAN101-1):  <br/>
<img src="https://imgur.com/3HJNhCi.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Figure 81 - Confirmation de l'isolation de vlans distants par rapport vlans du site principale (PC-VLAN100-1):  <br/>
<img src="https://imgur.com/BxXSZmA.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Figure 82 - Confirmation de l'isolation de vlans distants par rapport vlans du site principale (PC-VLAN101-1):  <br/>
<img src="https://imgur.com/1MURpjm.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
Ce test vérifie que les utilisateurs du site distant ne peuvent pas "rebondir" sur d'autres segments du siège (Administration ou Postes utilisateurs) non déclarés dans la matrice de flux.<br />


<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
