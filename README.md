# project-RH-avec-excel
# Mini Projet RH avec Excel  Ce projet montre comment utiliser Excel pour automatiser certains calculs RH .  🎯 Objectif : pratiquer et démontrer mes compétences en Excel appliquées à un cas réel RH.
# 📊 Mini Projet RH avec Excel

## 🎯 Objectif du projet
Ce projet a pour but de montrer comment utiliser **Excel** pour automatiser certains calculs liés à la gestion des ressources humaines (RH).  
Il s’agit d’un **mini-projet pédagogique** qui illustre l’application de formules Excel dans un cas concret de suivi des employés.

---

## 📝 Contenu du fichier Excel
Le fichier contient une liste fictive d’employés avec les colonnes suivantes :

- **Nom et Prénom**
- **Date de naissance**
- **Date d’embauche**
- **Date de dernière absence**

À partir de ces données, plusieurs calculs automatisés sont réalisés :

1. **Âge de l’employé** (en années entières)  
   ```excel
   =DATEDIF(DateNaissance, AUJOURDHUI(), "y")
=DATEDIF(DateEmbauche, AUJOURDHUI(), "y") & " an(s), " & DATEDIF(DateEmbauche, AUJOURDHUI(), "ym") & " mois"


Date de fin d’année en cours (31/12/AAAA)

=DATE(ANNEE(AUJOURDHUI()),12,31)


Première date du mois prochain

=FIN.MOIS(AUJOURDHUI(),0)+1


Titre mensuel (Mois + Année) à partir de la date d’embauche

=TEXTE(DateEmbauche;"mmmm aaaa")


Nombre de jours depuis la dernière absence

=AUJOURDHUI() - DerniereAbsence


Numéro de semaine de la date d’embauche

=NO.SEMAINE(DateEmbauche;2)


Nom de sauvegarde automatique (BackupName)

="Backup_" & TEXTE(AUJOURDHUI();"aaaa-mm-jj")
