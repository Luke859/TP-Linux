
# **Mise en place d'une VM (Machine Virtuel)**


### **Qu'est ce qu'une VM :**

Une **machine virtuelle** ou **VM** est un environnement entièrement virtualisé qui fonctionne sur une machine physique. Elle exécute son propre système d’exploitation (OS) et bénéficie des mêmes équipement qu’une machine physique : CPU, mémoire RAM, disque dur et carte réseau. Plusieurs machines virtuelles avec des OS différents peuvent coexister sur le même serveur physique : Linux, MacOS, Windows…

---
</br>

## **1- L'installation de la VM**


-Pour la mise en place de la VM, nous allons utiliser VMWare :

- Qui ce presente ainsi :

![](Image/VMWare.PNG)

Nous allons premièrement créer une nouvelle machine avec l'ISO suivant qui est Debian 11 sous Linux.

---

### **Qu'est ce que Debian ?**

Debian  (Debian GNU/Linux) est un système d’exploitation Linux composée exclusivement de logiciels libres.

![](Image/debian.jpeg)

---

Nous utilisons Debian 11 puisque c'est la version la plus récente de Debian.

</br>
Ici pour télécharger l'ISO -> https://lecrabeinfo.net/telecharger/debian-11-x64

Une fois tout cela installé, il faudra lancer la machine virtuel et suivre les étapes une par une.

## **Etape n°1**

- Donner un nom à votre machine : 

![](Image/etape1.PNG)

## **Etape n°2**

- Le domaine sera vide, appuyer sur **continuer** :

![](Image/etape2.PNG)

## **Etape n°3**

- Il faudra créer un mot de passe pour la machine et répéter cette démarche 2 fois :

![](Image/etape3.PNG)

## **Etape n°4**

- Choississer **"utiliser un disque entier"** ci-dessous :

![](Image/etape4.PNG)

## **Etape n°5**

- Choisir **"tout dans une seule partition"** puis appuyez sur **entrer** :

![](Image/etape5.PNG)

## **Etape n°6**

- Choisit **"Terminer le partitionnement et appliquer les changements"** :

![](Image/etape6.PNG)

## **Etape n°7 et 8**

- Il faudra choisir "OUI" pour les 2 : 

![](Image/etape7.PNG)
![](Image/etape8.PNG)

## **Etape n°9**

- Il faudra choisir **"deb.debian.org"** donc celui qui est surligné : 

![](Image/etape9.PNG)

## **Etape n°10**

- Le mandataire HTTP sera vide, appuyez sur **continuer** :

![](Image/etape10.PNG)

## **Etape n°11**
- Il faudra dire **"non"** à cette étape 

## **Etape n°12**

- Une étape importante, puisqu'il faudra décocher les 2 premiers logiciels en **appuyant sur la barre "espace"** puis appuyez sur entrer :

![](Image/etape12.PNG)

## **Etape n°13**

- Choisir **"oui"** pour l'installation de GRUB puis appuyez sur entrer :

![](Image/etape13.PNG)

## **Etape n°14**

- Choisir "/dev/sda" puis appuyer sur entrer :

![](Image/etape14.PNG)

## **Etape finale**
- Installation finit !!!

![](Image/etapeFinal.PNG)

---

</br>

# **2- Mise en place d'une clé SSH**

**1- Pour la mise en place de la clé SSH, il faudra ce rendre dans notre VM que l'on a créer précédamment :**

</br>

- La VM allumée, vous aurez une console où il vous demandera votre identifiant et votre mot de passe.

- Il faudra ce rendre à la **racine** de la console pour pouvoir installer les composants pour la clé SSH, en fesant "**su**" puis inscrire votre mot de passe.

- On peut voir sur notre image en rouge qu nous sommes bien à la racine "**root**".

![](Image/debut.png)

</br>

**2- Nous pouvons mainteant installer les composants nécessaires :**

</br>

- Premièrement nous installons "sudo", sudo va nous permettre d'installer la clé SSH car elle nous permet de lancer une commande en tant qu'administrateur, ou en tant qu'autre utilisateur.

- La Commande : 

```
apt install sudo
```

- Installation de la commande SSH avec :

```
sudo apt install openssh-server
```

![](Image/install.png)

<br>

**3- Lancer un ping du poste client vers la VM**

</br>

- Pour trouver l'adresse IP de votre machine il faut taper dans votre console "**ip a**"(orange) cela donnera votre adresse IP (en vert)

![](Image/ip.png)

- Sur votre pc windows (poste client) aller dans votre "**invite de commandes**" tapez "**ping[ip de votre serveur]**" (en vert).

- Si vous avez une réponse alors la connection à été établit.

![](Image/ping.png)

<br>

**4- La connection avec la clé SSH**

<br>

- Dans l'invite de commandes (windows) tapez "**ssh [nom utilisateur]@[ip de votre serveur]**" pour vous connecter à la clé SSH. 
- Il demandera votre mot de passe entrez le et vous êtes connecté à votre machine.

![](Image/ssh.png)