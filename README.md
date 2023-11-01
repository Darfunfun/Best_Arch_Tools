# Best Arch Tools

## Desktop
* Dock : Latte Dock, PopOS Dock ?
* **Desktop Environnement : Plasma**
* Tiling : i3 ? Awesome ? dwm / xmonad ?
* **Windows Manager : KWin**
* File Manager : Dolphin ! vifm ? Nautilus ?
* Applications Finder : KRunner ? Albert, Ulauncher, Synapse, Gnome Do, Cerebro, Launchy ? Rofi

## Games
* **Games : **
  * **Steam**
  * **Lutris**
  * **FSR**
  * **Proton GE** -> 
```sh
# make temp working directory
mkdir /tmp/proton-ge-custom
cd /tmp/proton-ge-custom

# download  tarball 
curl -sLOJ $(curl -s https://api.github.com/repos/GloriousEggroll/proton-ge-custom/releases/latest | grep browser_download_url | cut -d\" -f4 | egrep .tar.gz)

# download checksum 
curl -sLOJ $(curl -s https://api.github.com/repos/GloriousEggroll/proton-ge-custom/releases/latest | grep browser_download_url | cut -d\" -f4 | egrep .sha512sum) 

# check tarball with checksum
sha512sum -c *.sha512sum
# if result is ok, continue

# make steam directory if it does not exist
mkdir -p ~/.steam/root/compatibilitytools.d

# extract proton tarball to steam directory
tar -xf GE-Proton*.tar.gz -C ~/.steam/root/compatibilitytools.d/
echo "All done :)"
```
* Drivers NVIDIA : 

## Useful Tools
* Screenshot : sudo pacman -S flameshot, scrot ?
* Clipboard : Klipper, Parcellite, CopyQ, Clipit, Gpaste, xclip
* **Password Manager : keepassxc**
* **Scanner : sudo pacman -S simple-scan**
* Text Editor : Kate
* **Disks manager : partitionmanager**

## Organisation :
sudo snap install superproductivity
wget -O - https://raw.githubusercontent.com/laurent22/joplin/dev/Joplin_install_and_update.sh | bash

## Misc
* Virtualization : VirtualBox ? KVM ?

## Emoji
* sudo pacman -S noto-fonts-emoji
* sudo nano /etc/fonts/local.conf

<?xml version="1.0"?>
<!DOCTYPE fontconfig SYSTEM "fonts.dtd">
<fontconfig>
 <alias>
   <family>sans-serif</family>
   <prefer>
     <family>Noto Sans</family>
     <family>Noto Color Emoji</family>
     <family>Noto Emoji</family>
     <family>DejaVu Sans</family>
   </prefer> 
 </alias>

 <alias>
   <family>serif</family>
   <prefer>
     <family>Noto Serif</family>
     <family>Noto Color Emoji</family>
     <family>Noto Emoji</family>
     <family>DejaVu Serif</family>
   </prefer>
 </alias>

 <alias>
  <family>monospace</family>
  <prefer>
    <family>Noto Mono</family>
    <family>Noto Color Emoji</family>
    <family>Noto Emoji</family>
   </prefer>
 </alias>
</fontconfig>


## Quelques bonus :
- Musique : mpd + ncmpcpp / mocp
- Vidéo : mpv + yt-dlp
- Images : sxiv
- Gestionnaire de paquets pour Pacman avec accès à l'AUR : paru
- LaTeX : texlive-most + texlive-lang + pandoc
- Compilateur TeX : XeTeX
- Couteau suisse pour les scripts : dmenu / fzf
- Visualiseur de documents : zathura (backend MuPDF) 
Langages de programmation favoris : POSIX Shell / Bash / Emacs Lisp / Haskell


# Ricing
## Wallpaper :
 * Simple : https://www.wallpaperflare.com/ , blueprint wallpaper game boy SP , https://yandex.com/images/search?text=double%20screen%20%20wallpaper , https://w.wallhaven.cc/full/k9/wallhaven-k9m76m.png , 
 * DualScreen : https://www.dualmonitorbackgrounds.com/ , https://www.reddit.com/r/pcmasterrace/comments/70zfpj/300_legendary_dual_monitor_wallpapers_for_your/ , https://www.reddit.com/r/pcmasterrace/comments/4cdvsr/over_2200_glorious_dual_monitor_wallpapers_all/ , https://www.reddit.com/r/multiwall/ , https://www.setaswall.com/dual-monitor-wallpapers/6/ , https://4kwallpapers.com/dual-monitor-hd-wallpapers/ , 
 * Animé : https://github.com/GhostNaN/mpvpaper


## Docks 
- Latte
Pour personaliser Latte -> `Click droit` ->  `Modifier un tableau de bord` (**et non** "Configurer Latte")
Plugin indicator : 
-> https://store.kde.org/p/1994299

  - Exporter la conf
	- /home/zizou/.config/latte/templates/
	- /home/zizou/Ma disposition.layout.latte


- Docky
- Plank
- XFCE Panel
- AWN


## Supervision
### Conky
- Minimalis 10/10 : https://www.pling.com/p/1112273 -> Install .ttf en double cliquant, placer .conf dans `.config/conky`, lancer la commande `conky -c ~/.config/conky/conky.conf`
- Mirach with custom color : https://store.kde.org/p/1851356/
- A tester ? -> https://www.ubuntupit.com/best-conky-themes-for-linux/


## Terminal
- Gnome
  - De mémoire, le meilleur
- Alacritty 
  -Bof, pas de click droit possible
- XFCE
  - Moche
- Konsole
  - Moche
- Kitty
  - A tester

## Shell
- Fish
Ergonomie +++


## Barre
- Layan (interessante)
- Extensions pour bar : Blur My Shell, Just Perfection, Freon, Clipboard indicator, User Theme, Aylur's Widgets -> https://i.redd.it/gnome-do-i-wanna-know-v0-ifwllc8x9nba1.png?s=cefa93a25753f7ead04d097d03715b34167955e8


## Spicetify (?) (Pour spotify)
Sleek, elementary 


## Autres
### OCS
Uilitaire pour installer desitems depuis pling !
- Telecharger https://www.opendesktop.org/p/1136805/
- sudo pacman -S qt5-base qt5-svg qt5-declarative qt5-quickcontrols
- sudo pacman -U /home/USER/Download/*.pkg.tar.xz


* * *

# **Parametres**
Note : Instaler des themes permet d'installer un pack de couleurs, de style plasma, de decorations de fenetres, d'icones, de pointeurs, etc
##### Comportement de l'espace de travail : 
- **Comportement général** :
	- Comportement visuel
		- Tout cocher
	- Cliquer sur les fichiers et les dossiers 
		- Les selectionne
- **Effets de bureau** :
	- Animation à l'ouverture / fermeture des fenetres
		- Choisir...
	- Focus
		- Reglage inactif
			- Force 10
	- Translucidité
		- Activée
- **Gestion des fenetres** :
	- **Sélécteur de tâches** :
		- Visualisation
			- MediumRounded
### **Apparence** :
*Themes : Glassy 5/10, Sweet 10/10*
- **Décorations de fenetres**
	- Sweet-dark et Glassy sont pas mal (ou autre (-> Breezemite pour Mams car possible d'avoir des boutons de fermeture enorme))
		- Edit (crayon)
			- Dessiner un cercle autour du bouton de fermeture
			- Tracer une bordure sur les fenetres agrandies et superposées
- **Pointeurs**
	- Brise
- **Icones** :
	- Layan 8/10 (+ barre du haut interessante)
	- Sweet 10/10
	- Numix-circle
		

