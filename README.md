# CONFIGURATION-SERVEUR-WEB

Installons le serveur web avec la commande:
apt install apache2

Passer au repertoire apache2 avec la commande:
cd /etc/apache2

Copier le fichier de configuration (000-default.conf) au niveau de site-available avec la commande:
cp 000-default.conf habib.conf

Ouvrir le fichier habib.conf avec la commande :
nano habib.conf

Modifier le nom de la machine et le nom du domaine

Passer au répertoire var/www/html en utilisant la commande:
cd 

Supprimer toutes les informations se trouvant à l'intérieur avec la commande:
rm –rf index.html. 

Acceder au fichier index.html avec la commande :
nano index.html

Retourner au repertoir apache2 et aller au site available

Desactiver la configuration par defaut de 000-default.conf avec la commande :
a2dissite 000-default

Activer le site créer avec la commande: 
a2ensite habib.conf

Verifier si la syntaxe est correct et fonctionne avec la commande :
apachectl configtest

Redemarer le serveur avec la commande :
systemctl restart apache2

lancer de nouveau le srerveur avec la commande:
systemctl status apache2
