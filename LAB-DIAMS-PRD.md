---
title: "Lab DIAMS — Landing Page App Store RH"
status: "🟡 En construction — v0.1"
created: "2026-05-16"
owner: "Arnaud (DAJM)"
stepsCompleted: []
---

# Lab DIAMS — PRD en construction

> Document vivant. Chaque session alimente ce fichier. Objectif : arriver au PRD complet avant de coder.
> À transmettre entre sessions pour ne perdre aucun contexte.

---

## 1. Contexte stratégique

### Qui est DAJM
Agence d'Arnaud, positionnée sur l'**attractivité RH augmentée par l'IA**.
Vision 2030 : agence de référence sur le carrefour communication de marque / stratégie RH / intelligence artificielle.
Document de référence : `DAJM-2030.md`

### Pourquoi ce projet
Le Lab DIAMS est le bras R&D de DAJM. Il développe des solutions IA pour les professionnels RH, recrutement et management. La landing page est la **vitrine de ce lab** — elle sert à :
1. Rendre la démarche IA de DAJM **tangible et crédible**
2. **Générer des leads qualifiés** (prospects qui ont déjà vu et essayé un outil)
3. Alimenter le pipeline commercial de DAJM sans prospection froide

### Lien avec DAJM 2030
Axe D (développement commercial à faible friction) + Axe A (marque employeur) du plan stratégique.
Les outils présentés dans le Lab couvrent les idées 003, 004, 005, 006, 007 du sandbox.

---

## 2. Concept produit

### Métaphore centrale : l'App Store pour les RH
Une landing page qui présente chaque outil Lab DIAMS comme une **"app"** :
- Icône + nom + tagline
- Badge de statut (Disponible / Beta / Bientôt)
- Note utilisateur (étoiles)
- 1 témoignage court
- CTA adapté au statut

Pas une page de présentation générique. Une interface qui montre qu'il se passe vraiment quelque chose.

### Ce que ça communique
> "On ne parle pas d'IA — on la construit. Et on vous laisse l'essayer."

---

## 3. Architecture des pages

### Page principale — la vitrine (App Store)
**Job unique** : faire cliquer sur une card. Elle ne convertit pas directement.

Structure :
- **Hero** : accroche forte sur la promesse + sous-titre clair sur la cible (RH, recrutement, management)
- **Filtres** : Recrutement / Marque employeur / Management / Candidat
- **Grid de cards** : 4-5 minimum au lancement (voir règle ci-dessous)
- **CTA global** : "Rejoindre les bêta-testeurs"
- **Footer** : lien vers dajm.fr + contact

⚠️ **Règle de lancement** : ne pas publier avec moins de 4-5 cards — le format App Store fait vide en dessous.

### Pages projet — la conversion (une par outil)
**Job** : convertir un visiteur curieux en lead qualifié ou bêta-testeur.

Structure par page :
1. **Problem statement** : le problème précis que l'outil résout (en langage DRH, pas en jargon tech)
2. **Solution** : comment l'outil fonctionne (démo visuelle, captures, gif)
3. **Use cases** : 2-3 cas concrets avec contexte
4. **Témoignages** : vrais retours bêta-testeurs (ou cas d'usage contextualisés au lancement)
5. **CTA primaire** : selon statut (voir modèle de conversion)
6. **CTA secondaire** : "Vous voulez qu'on l'adapte à votre contexte ? → Audit DAJM"

---

## 4. Modèle de conversion unifié

**Même parcours UX pour toutes les cards, peu importe le stade de l'outil.**

| Statut outil | Accès | Friction | CTA final |
|---|---|---|---|
| **Disponible** | Demo réelle après inscription (magic link ou email + mdp) | Quota : 1-2 productions puis blocage | "Contactez-nous pour accéder / obtenir une offre" |
| **Beta** | Accès limité après inscription | Même quota | Même CTA |
| **En développement** | Aucun accès | Formulaire d'expression d'intérêt | Notifié au lancement + suivi DAJM |

**Logique** : le visiteur vit le produit avant d'être converti. Le blocage post-quota est justifié — la valeur a été démontrée. DAJM entre en contact avec un prospect qui sait déjà ce que l'outil fait.

---

## 5. Mapping AARRR

| Étape | Où | Mécanique |
|---|---|---|
| **Acquisition** | Pages projet | SEO sur le problème RH ("comment rédiger une fiche de poste attractive") + partage LinkedIn d'une card |
| **Activation** | Page principale → page projet → demo | Premier essai de l'outil = activation |
| **Retention** | Email post-inscription | "Nouveau dans le Lab" à chaque outil ou mise à jour |
| **Referral** | Pages projet | Chaque page partageable + badge "testé par X DRH" |
| **Revenue** | Bas de chaque page projet | CTA "Audit DAJM" ou "accompagnement personnalisé" |

---

## 6. Décisions techniques actées

| Décision | Choix | Raison |
|---|---|---|
| **Hébergement** | Sous-domaine DAJM (`lab.dajm.fr`) | Lab = R&D interne, pas une marque autonome |
| **Technologie** | Code natif (HTML/CSS/JS ou framework léger) | Micro-interactions plus puissantes que Framer, déploiement plus rapide |
| **Site principal** | Reste sur Framer, lien depuis nav/footer vers lab.dajm.fr | Pas d'intégration Framer ↔ code natif (pas techniquement possible proprement) |
| **Backend** | Léger mais nécessaire pour les demos | Auth (magic link) + suivi quota par utilisateur × outil |
| **Outils sans demo** | Formulaire statique | Zéro backend nécessaire pour capturer l'intérêt |

**Backend à choisir** (décision ouverte) : Supabase ou PocketBase — à trancher selon préférence hébergement.

---

## 7. Outils du catalogue (draft)

À mapper sur les idées du sandbox. Statuts provisoires :

| # | Nom provisoire | Idée source | Statut envisagé | Catégorie |
|---|---|---|---|---|
| 1 | Générateur de fiches de poste attractives | Idée sandbox (score 6.8) | Beta | Recrutement |
| 2 | Diagnostiqueur marque employeur | Idée 004 (sandbox) | Bientôt | Marque employeur |
| 3 | Générateur de pistes marque employeur | Idée 003 (sandbox) | Bientôt | Marque employeur |
| 4 | CV Matcher | Ideas-data (score 6.2) | Bientôt | Candidat |
| 5 | Outil de mise au point stratégique commerciale | Idée 005 (sandbox) | Bientôt | Management |
| 6 | Agent de prospection personnalisée | Idée 006 (sandbox) | En développement | Recrutement |

---

## 8. Questions ouvertes

- [ ] Sous-domaine exact : `lab.dajm.fr` ou autre ?
- [ ] Noms définitifs des outils (actuellement provisoires)
- [ ] Témoignages au lancement : vrais bêta-testeurs ou cas d'usage contextualisés ?
- [ ] Choix backend demos : Supabase ou PocketBase ?
- [ ] Qui maintient la page quand un outil est ajouté ? (process de mise à jour)
- [ ] Identité visuelle : palette, typographie, ton — à aligner avec dajm.fr (corpus à fournir)
- [ ] CTA secondaire "Audit DAJM" : lien vers un formulaire ou vers une page dajm.fr existante ?

---

## 9. Ce qu'il reste à construire (prochaines étapes PRD)

- [ ] Personas détaillés (DRH PME, responsable recrutement, manager opérationnel)
- [ ] User journeys complets (du premier clic à la prise de contact)
- [ ] Wireframes des pages (principale + page projet type)
- [ ] Contenu des cards (noms définitifs, taglines, descriptions courtes)
- [ ] Spécifications fonctionnelles (auth, quota, états de l'interface)
- [ ] Spécifications non-fonctionnelles (performance, SEO, accessibilité)
- [ ] Corpus identité visuelle DAJM (à fournir par Arnaud)

---

## 10. Corpus stratégique à intégrer

*(À compléter par Arnaud — ces éléments alimenteront les sections Personas et Contenu)*

- [ ] Présentation de DAJM et de ses offres actuelles
- [ ] Cibles clients prioritaires (secteurs, tailles d'entreprise, interlocuteurs)
- [ ] Identité visuelle (couleurs, typo, ton éditorial)
- [ ] Exemples de missions passées ou en cours
- [ ] Témoignages clients existants
