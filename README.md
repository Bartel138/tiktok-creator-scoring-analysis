# 📊 Analyse et Scoring de Créateurs TikTok sur Excel (Bootcamp Bartel)

## 🎯 Objectif du Projet
Ce projet formalise une démarche analytique complète menée sous **Excel** pour exploiter des données brutes issues de web scraping sur TikTok. L'objectif est d'objectiver la performance des créateurs au-delà de la simple viralité brute, en évaluant l'engagement réel et qualitatif de leur communauté.

## ⚙️ Méthodologie & Pipeline Analytique sur Excel
1. **Importation & Gestion des Contraintes :** 
   - Correction de l'encodage (UTF-8) et ajustement manuel des séparateurs (virgules) pour structurer l'affichage.
   - Application d'un "Kill Switch" pour isoler et abandonner les datasets corrompus (ex: hashtags) au profit des sources fiables (`Trending_video`, `Liked_video`, `Author_video`).
2. **Nettoyage (*Data Cleaning*) :**
   - Suppression des lignes vides (raccourci `F5`) et dédoublonnage ciblé sur les clés primaires uniques (`ID Utilisateur` / `ID Vidéo`).
   - Normalisation des formats de texte et de chiffres pour sécuriser les calculs.
3. **Modèle de Scoring Multicritère (sur 100) :**
   Calcul d'un Score Composite Global via une formule pondérée combinant quatre indicateurs clés :
   - 👁️️ **Vues (40%)** : Portée et visibilité globale.
   - 🔄 **Partages (30%)** : Viralité active et recommandation organique.
   - ❤️ **J'aime (20%)** : Adhésion du public.
   - 💬 **Commentaires (10%)** : Engagement conversationnel.
   - *Normalisation :* Division des volumes par 1 000 000 pour obtenir un score lisible.
4. **Croisement Inter-Tables & Dataviz :**
   - Utilisation de `RECHERCHEV` sécurisées pour injecter les métadonnées de la table des auteurs (`Author_video`) dans les tendances.
   - Mises en forme conditionnelles (MFC) et graphiques en **Treemap** pour une lecture immédiate par la direction.
5. **Segmentation Stratégique :**
   - 🟢 **Score > 35 :** *À contacter* (Priorité opérationnelle).
   - 🟡 **Score entre 20 et 35 :** *À observer* (Profils en veille).
   - 🔴 **Score < 20 :** *À éviter*.

## 🛠️ Outils Utilisés
- **Microsoft Excel** (Importation CSV, RECHERCHEV, MFC, Formules de scoring, Treemap).
