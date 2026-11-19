# Galerie de la villa (monde VRChat « Le Volcan des Surfeurs »)

Ce dépôt contient les photos affichées dans les tableaux de la villa.
Le monde les télécharge tout seul : **pas besoin de réuploader le monde** pour changer ou ajouter des photos.

---

## Ce qu'il y a dans ce dépôt

| Fichier | À quoi il sert |
|---|---|
| `rod.jpg`, `rodavecrequin.jpg`, `rodenmoto.jpg`, `rodsaucisson.jpg` | Photos **par défaut** : celles que voient tous les joueurs qui ne sont pas dans la liste. |
| `liste.txt` | La liste des joueurs qui ont **leurs propres photos**. |
| `p/` | Les photos des joueurs : `p/001.jpg`, `p/002.jpg`, `p/003.jpg`… (300 emplacements, de 001 à 300). |

⚠️ Ne pas supprimer ni renommer les photos par défaut : le monde les cherche sous ces noms exacts.

---

## Les 5 tableaux de la villa (dans cet ordre)

1. **Buffet** (salle à manger) — cadre en largeur
2. **Salon** (grand tableau) — cadre en largeur
3. **Cheminée** — cadre en largeur
4. **Cinéma 1** — affiche en hauteur
5. **Cinéma 2** — affiche en hauteur

Les photos ne sont jamais déformées : si le format ne correspond pas, elles sont recadrées
(une photo en hauteur dans un cadre en largeur garde plutôt le haut, là où sont les visages).

---

## Ajouter les photos d'un joueur

Quand quelqu'un envoie ses photos à **photopourvrchat@gmail.com** avec son pseudo VRChat :

1. **Vérifier les photos** (elles seront visibles en ligne et dans le monde).
2. **Les préparer sur le PC** : format **JPG**, **2048 pixels maximum** de côté (sinon VRChat les refuse).
3. **Les renommer** avec les prochains numéros libres, en 3 chiffres : par exemple `005.jpg`, `006.jpg`, `007.jpg`.
4. **Les envoyer dans le dossier `p/`** : ouvrir le dossier `p` → *Add file* → *Upload files* → *Commit changes*.
5. **Ajouter une ligne dans `liste.txt`** (ouvrir le fichier → crayon ✏️ *Edit* → *Commit changes*) :

   ```
   SonPseudo: 0,5,6,7,0
   ```

   - un numéro par tableau, dans l'ordre ci-dessus (buffet, salon, cheminée, cinéma 1, cinéma 2) ;
   - `0` = ce tableau garde son image d'origine ;
   - le même numéro peut servir pour plusieurs tableaux.

6. Attendre **1 à 5 minutes** (mise à jour de GitHub Pages). Le joueur verra ses photos à sa prochaine entrée dans la villa.

### Bon à savoir

- Le pseudo doit être **exactement** le pseudo affiché dans VRChat (les majuscules ne comptent pas).
  Si le joueur change de pseudo, il faut changer sa ligne.
- Chaque joueur voit **ses** photos : deux joueurs dans la villa ne voient pas les mêmes tableaux.
- Les lignes qui commencent par `#` sont des commentaires (ignorées par le monde).
- Pour **changer** une photo : remplacer le fichier en gardant **le même nom**.
- Pour **retirer** un joueur : supprimer sa ligne dans `liste.txt` (il reverra les photos par défaut).

---

## Si une photo ne s'affiche pas

- Vérifier le nom exact du fichier (`p/005.jpg`, pas `p/5.jpg` ni `p/005.JPG`).
- Vérifier la taille (2048 pixels maximum) et le format (JPG).
- Ouvrir l'adresse dans un navigateur pour voir si elle répond :
  `https://flandrinrodolphe-oss.github.io/galerie-ile/p/005.jpg`
- Attendre quelques minutes après un envoi : GitHub Pages met un peu de temps à se mettre à jour.

---

## Réglages côté monde (déjà faits, pour mémoire)

- Adresse de base : `https://flandrinrodolphe-oss.github.io/galerie-ile/`
- Liste : `liste.txt` — Emplacements : `p/001.jpg` à `p/300.jpg`
- Les photos se chargent quand le joueur arrive à moins de 70 m de la villa (VRChat : une image toutes les 5 secondes).
- Pour plus de 300 emplacements ou d'autres tableaux, il faut modifier le monde (menu Unity
  *Radwolf → Ile Surf → Villa : galerie de photos (tableaux)*) puis le réuploader.
