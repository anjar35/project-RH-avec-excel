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
2.Ancienneté (en années et mois)
=DATEDIF(DateEmbauche, AUJOURDHUI(), "y") & " an(s), " & DATEDIF(DateEmbauche, AUJOURDHUI(), "ym") & " mois"
=DATEDIF(DateEmbauche, AUJOURDHUI(), "y") & " an(s), " & DATEDIF(DateEmbauche, AUJOURDHUI(), "ym") & " mois"
3.Date de fin d’année en cours (31/12/AAAA)

=DATE(ANNEE(AUJOURDHUI()),12,31)
4.Première date du mois prochain

=DATE(YEAR(TODAY()),MONTH(TODAY())+1,1)

5.Titre mensuel (Mois + Année) à partir de la date d’embauche

=TEXTE(DateEmbauche;"mmmm aaaa")

6.Nombre de jours depuis la dernière absence

=AUJOURDHUI() - DerniereAbsence

7.Numéro de semaine de la date d’embauche

=NO.SEMAINE(DateEmbauche;2)

8.Nom de sauvegarde automatique (BackupName)

="Backup_" & TEXTE(AUJOURDHUI();"aaaa-mm-jj")
