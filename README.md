# ISO-IVIM — International Verification & Integrity Mechanism
## Standardisation for educational credentials using eDiscovery, verifiable credentials and decentralized trust

**Objectif :** créer une norme mondiale (ISO-IVIM) qui transforme le diplôme académique en une *preuve numérique vérifiable*, interopérable et défendable juridiquement, en combinant ISO 21001 (management éducatif), ISO 27050 (eDiscovery / forensics), ISO 8000 (qualité des données) et les standards W3C (Verifiable Credentials, DIDs) ainsi que C2PA pour la provenance des documents.

---

## Résumé exécutif

La mobilité étudiante et la numérisation des certificats créent un besoin urgent : garantir qu’un diplôme émis n’importe où dans le monde soit immédiatement vérifiable, infalsifiable et interprétable par des systèmes automatiques. ISO-IVIM propose une architecture technique, juridique et opérationnelle :

1. **Couche gestion** — conformité institutionnelle (ISO 21001) ;  
2. **Couche intégrité forensique** — cycle eDiscovery adapté à l’éducation (ISO 27050) ;  
3. **Couche interopérabilité** — schéma ISO 8000 + W3C Verifiable Credentials + DIDs + C2PA.

L’objectif opérationnel : que la preuve d’une compétence soit portable, vérifiable cryptographiquement et acceptable légalement.

---

## Pourquoi c’est nécessaire

- Vérifications manuelles = lentes, coûteuses, vulnérables à la fraude.  
- Faux diplômes et falsifications visuelles (IA générative) augmentent le risque systémique.  
- Les conventions bilatérales (ARM) ne suffisent pas : il faut un protocole technique multilatéral, neutre et auditable.

---

## Pilier conceptuel : appliquer l’EDRM (eDiscovery) à l’éducation

Le cycle EDRM se transpose au dossier étudiant. La table ci-dessous résume la correspondance.

| Phase EDRM | Interprétation eDiscovery | Implémentation ISO-IVIM | Bénéfice |
|---|---:|---|---|
| Governance | Politiques & rétention | ISO 21001 + règles de conservation des ESI étudiantes | Traçabilité et gestion de risque |
| Identification | Localiser ESI pertinentes | Définir "Preuves d’apprentissage" (notes, projets) | Clarté du périmètre probatoire |
| Preservation | Legal hold / WORM | Verrou cryptographique des dossiers validés (hash on-chain) | Immutabilité, prévention de la spoliation |
| Collection | Extraction forensique | API sécurisées d’export vers wallet étudiant | Récupérabilité en cas d’incident |
| Processing | Normalisation | ISO 8000, mapping des échelles, nettoyage | Machine-readable data |
| Review | Audit & validation | Smart contracts + réviseur humain (Registrar) | Automatisation + responsabilité |
| Analysis | Contexte & comparaisons | IA auditable (FACT-AUDIT) pour équivalence | Reconnaissance rapide et transparente |
| Production | Livraison des preuves | W3C Verifiable Credentials + PDF signé C2PA | Format universel, infalsifiable |
| Presentation | Vérification | Vérificateur consulte DID / registre public | Vérif instantanée, sans intermédiaire |

---

## Architecture technique — composants clés

- **DIDs / PKI** : chaque institution accréditée possède un DID. Les VCs sont signés par la clé privée de l’émetteur ; la clé publique est décodable via le DID.  
- **Verifiable Credentials (W3C)** : format standard d’émission des diplômes & micro-crédits (JSON-LD).  
- **C2PA** : attestation de provenance pour la représentation visuelle (PDF/image) — protège contre les deepfake diplomas.  
- **Blockchain / registre d’ancrage** : ancrage des empreintes (hashes) pour immuabilité et horodatage (publique ou consortium).  
- **ISO 8000 schemas** : dictionnaires de compétences / codes ISCED/ISCQ pour portabilité sémantique.  
- **IA auditable (FACT-AUDIT)** : agents pour comparer curriculum vs exigences locales (déceler « différence substantielle »).  
- **SlideChain** : provenance et versioning du contenu pédagogique (plans de cours, syllabus).

---

## Gouvernance et rôle des acteurs

- **Institutions** : émetteurs et custodians des preuves ; nécessité d’audits ISO 21001 et ISO 27050.  
- **Organismes d’accréditation** : trust anchors ; délivrent l’accréditation vérifiable (révocable on-chain).  
- **Étudiants** : titulaires des VCs dans leur wallet ; contrôle de divulgation (selective disclosure).  
- **Vérificateurs** : employeurs / universités d’accueil ; vérifient signatures et métadonnées via DID + registres.  
- **Instances internationales (UNESCO / ISO)** : adoption normative et cadre légal multilatéral.

---

## Confidentialité & conformité juridique

- Respect du principe de minimisation (GDPR) via divulgation sélective et ZKP.  
- Défendabilité judiciaire : les métadonnées et la chaîne de traçabilité permettent des audits forensiques conformes à ISO 27050.  
- Mécanisme de révocation / suspension géré par les autorités d’accréditation.

---

## Feuille de route (proposition)

**Phase 1 (1–2 ans)** : pilotes régionaux, adoption ISO 21001, formation auditeurs ISO 27050.  
**Phase 2 (3–5 ans)** : déploiement DIDs, intégration VC/C2PA dans SIS/LMS, standardisation ISO 8000 des cursus.  
**Phase 3 (5+ ans)** : adoption multilatérale, wallets étudiants universels, agents IA pour reconnaissance automatique.

---

## Cas d’usage (exemples rapides)

- Employeur vérifie en 3s l’authenticité d’un diplôme via VC présenté par le candidat.  
- Étudiant change d’université : ses micro-crédits sont transférés automatiquement, audités et acceptés si équivalence.  
- Enquête pour fraude académique : métadonnées et log forensics démontrent altération ou non-altération.

---

## Avantages attendus

- Réduction drastique des coûts et délais de vérification.  
- Meilleure résilience contre la fraude (internes et externes).  
- Portabilité sémantique mondiale des compétences.  
- Conformité juridique et auditabilité améliorée.

---

## Points d’attention / risques

- Adoption politique et souveraineté nationale.  
- Protection des données personnelles et exigences RGPD.  
- Gouvernance du registre (public vs consortium).  
- Formation et capacité d’audit des institutions (coûts initiaux).

---

## A propos & licence

**Auteur principal :** Bryan Ouellette — Independent Researcher  
**Licence :** Apache-2.0 (contrib libre & interopérable)  
**Contact / Contributions :** issues / PR sur ce dépôt GitHub

---
