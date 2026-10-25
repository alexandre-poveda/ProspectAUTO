# ProspectAUTO 🚀

Plateforme métier & système automatisé de prospection intelligente pour commerces de proximité et établissements indépendants, couplé au moteur open-source [Harvey](https://github.com/ethanplusai/harvey).

---

## 🎯 Domaines d'Activité Répertoriés

1. **Micro-Crèches & Petite Enfance**
   - Formulaire complet de pré-inscription en ligne.
   - Présentation de la pédagogie, de l'équipe et de la journée type.
   - Galerie photo sécurisée et informations d'agrément PMI.
2. **Restaurants & Brasseries**
   - Carte & menus numériques optimisés smartphone (sans PDF lourd).
   - Module de réservation directe de table sans commissions tierces.
   - Intégration du flux Instagram en direct.
3. **Coiffeurs & Barbiers**
   - Prise de rendez-vous en ligne instantanée.
   - Tarifs clairs et galerie de réalisations grooming / coiffure.
   - Acquisition locale ciblée sur Google Maps.
4. **Petites Écoles & Établissements Privés**
   - Dossier de demande d'admission & portes ouvertes.
   - Calendrier des événements et valeurs éducatives (Montessori, bilingue, alternatives).

---

## 🤖 Intégration Harvey (Autonomous Outbound Sales)

ProspectAUTO tire parti de l'architecture d'**Harvey** (`ethanplusai/harvey`) :

- **Pas de frais d'API par token** : S'exécute directement sur l'abonnement Claude Code ou OpenAI Codex.
- **Recherche de cibles locales** : Scan des commerces et établissements sur Google Maps et annuaires par zone géographique.
- **Enrichissement & Décideurs** : Identification des coordonnées directes et analyse du site existant.
- **Emails sur-mesure** : Rédaction contextuelle valorisant les solutions métiers ci-dessus.
- **Validation Humaine Obligatoire (`require_approval: true`)** : Les emails attendent dans un pupitre de décision avant envoi.

---

## ⚙️ Configuration Harvey (`harvey.yaml`)

```yaml
agent:
  name: "ProspectAUTO Agent"
  user_name: "Alexandre Poveda"
  tone: "professionnel, bienveillant, concis"

safety:
  require_approval: true
  max_emails_per_day: 30
  kill_switch: false

target_niches:
  - name: "Micro-Crèches"
    query: "micro-creche"
  - name: "Restaurants"
    query: "restaurant bistrot"
  - name: "Barbiers & Coiffeurs"
    query: "barbier salon de coiffure"
  - name: "Petites Ecoles"
    query: "ecole privee alternative"
```

---

## 🌐 Lancement Local du Site

Ouvrez simplement le fichier `index.html` dans votre navigateur ou lancez un serveur local :

```bash
# Via npx serve ou python
npx serve .
# ou
python -m http.server 3000
```
