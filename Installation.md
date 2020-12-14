# L'installation de PowerShell Linux (debian 10 - VM) : 
---
1. **Télécharger du répertoire clés GPG de Microsoft**
- wget https://packages.microsoft.com/config/debian/10/packages-microsoft-prod.deb
</ul>

2. **Insérer le répertoire clés GPG de Microsoft**
- sudo dpkg -i packages-microsoft-prod.deb
</ul>

3. **Mettre à jour la lise des produits**
- sudo apt-get update 

4. **Installer PowerShell**
- sudo apt-install -y powershell

5. **Lancer Powershell**
- pwsh
---




