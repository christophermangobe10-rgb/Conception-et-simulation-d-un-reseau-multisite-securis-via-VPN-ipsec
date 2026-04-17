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
Sanitization complete:  <br/>
<img src="https://i.imgur.com/K71yaM2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Observe the wiped disk:  <br/>
<img src="https://i.imgur.com/AeZkvFQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
