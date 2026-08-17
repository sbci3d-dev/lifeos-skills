# Skill Engine Configuration

> Configuration centrale du moteur de compétences LifeOS
> Version : 1.0.0
> Dernière mise à jour : 2026-08-18

---

## Paramè²¹tres globaux

```yaml
engine:
  name: "LifeOS Skill Engine"
  version: "1.0.0"
  author: "Noureddine El Bounijmi"
  
validation:
  require_evidence: true
  min_evidence_count: 1
  evidence_types:
    - "livrable"
    - "url"
    - "rapport"
    - "github"
    - "client"
    - "etude_de_cas"
    - "kpi"
    - "resultat_financier"
    - "attestation"
  
scoring:
  factors:
    - name: "Knowledge"
      weight: 1.0
      scale: "0-5"
    - name: "Practice"
      weight: 1.0
      scale: "0-5"
    - name: "Experience"
      weight: 1.0
      scale: "0-5"
    - name: "Evidence"
      weight: 1.0
      scale: "0-5"
    - name: "Recency"
      weight: 1.0
      scale: "0-5"
    - name: "Results"
      weight: 1.0
      scale: "0-5"
  
  total_max: 30
  
levels:
  - range: "0-4"
    level: 0
    label: "Non é⁰valué²¹"
  - range: "5-8"
    level: 1
    label: "Initiation"
  - range: "9-12"
    level: 2
    label: "Fondations"
  - range: "13-16"
    level: 3
    label: "Opé²¹rationnel encadré²¹"
  - range: "17-21"
    level: 4
    label: "Autonome"
  - range: "22-26"
    level: 5
    label: "Avancé²¹"
  - range: "27-30"
    level: 6
    label: "Ré²¹fé²¹rent / maî²¹trise"

gap_status:
  green:
    symbol: "🟢"
    label: "Acquis"
    min_level: 4
    max_level: 6
    requirement: "Preuves ré⁰centes + ré⁰sultats observables"
  yellow:
    symbol: "🟡"
    label: "En cours"
    min_level: 3
    max_level: 3
    requirement: "Progression active documenté²¹e"
  orange:
    symbol: "🟠"
    label: "Insuffisant"
    min_level: 1
    max_level: 2
    requirement: "Niveau trop bas pour l'objectif"
  red:
    symbol: "🔴"
    label: "Manquant"
    min_level: 0
    max_level: 0
    requirement: "Aucune preuve exploitable"
```

---

## Domaines de compétences

```yaml
domains:
  career_os:
    name: "Career OS"
    description: "Compé²¹tences professionnelles principales"
    skills:
      - id: "hydraulique_irrigation"
        name: "Ingé²¹nierie hydraulique et irrigation"
        category: "career"
        monetization_potential: "high"
        target_revenue: 30000
        currency: "MAD"
        period: "month"
        
      - id: "excel_data"
        name: "Excel, modé²¹lisation et analyse de donné⁰es"
        category: "career"
        monetization_potential: "medium"
        target_revenue: 10000
        currency: "MAD"
        period: "month"
        
      - id: "gestion_projet"
        name: "Gestion de projet technique"
        category: "career"
        monetization_potential: "medium"
        target_revenue: 15000
        currency: "MAD"
        period: "month"
  
  business_os:
    name: "Business OS"
    description: "Compé²¹tences entrepreneuriales et business"
    skills:
      - id: "bioagroponics"
        name: "BioAgroponics et aquaponie"
        category: "business"
        monetization_potential: "high"
        target_revenue: 20000
        currency: "MAD"
        period: "month"
        
      - id: "consulting_b2b"
        name: "Conseil B2B et vente de services"
        category: "business"
        monetization_potential: "high"
        target_revenue: 30000
        currency: "MAD"
        period: "month"
        
      - id: "marketing_digital"
        name: "Marketing digital et contenus"
        category: "business"
        monetization_potential: "medium"
        target_revenue: 15000
        currency: "MAD"
        period: "month"
        
      - id: "produits_numeriques"
        name: "Produits numé²¹riques"
        category: "business"
        monetization_potential: "high"
        target_revenue: 25000
        currency: "MAD"
        period: "month"
  
  digital_systems_os:
    name: "Digital Systems OS"
    description: "Compé²¹tences techniques digitales"
    skills:
      - id: "wordpress"
        name: "Dé²¹veloppement Web : WordPress"
        category: "digital"
        monetization_potential: "medium"
        target_revenue: 10000
        currency: "MAD"
        period: "month"
        
      - id: "react_supabase"
        name: "Dé²¹veloppement Web : React, TypeScript et Supabase"
        category: "digital"
        monetization_potential: "high"
        target_revenue: 40000
        currency: "MAD"
        period: "month"
        
      - id: "n8n_automation"
        name: "Automatisation : n8n et inté⁰grations"
        category: "digital"
        monetization_potential: "medium"
        target_revenue: 15000
        currency: "MAD"
        period: "month"
  
  core_layer:
    name: "Core Layer"
    description: "Compé²¹tences transversales fondamentales"
    skills:
      - id: "ia_agricole"
        name: "Intelligence artificielle appliqué²¹e aux donné⁰es agricoles"
        category: "core"
        monetization_potential: "very_high"
        target_revenue: 40000
        currency: "MAD"
        period: "month"
        
      - id: "productivite_lifeos"
        name: "Productivit é⁰ syst é⁰mique et LifeOS"
        category: "core"
        monetization_potential: "medium"
        target_revenue: 10000
        currency: "MAD"
        period: "month"
```

---

## Objectifs financiers

```yaml
financial_targets:
  phase_1:
    name: "Phase 1 — Lancement"
    period: "90 jours"
    start_date: "2026-03-02"
    end_date: "2026-05-01"
    target_revenue: 11000
    currency: "MAD"
    period_type: "month"
    primary_focus:
      - "bioagroponics"
      - "produits_numeriques"
      - "marketing_digital"
  
  phase_2:
    name: "Phase 2 — Scaling"
    period: "12 mois"
    start_date: "2026-05-02"
    end_date: "2027-05-01"
    target_revenue: 50000
    currency: "MAD"
    period_type: "month"
    primary_focus:
      - "consulting_b2b"
      - "react_supabase"
      - "ia_agricole"
  
  total_potential:
    target_revenue: 115000
    currency: "MAD"
    period_type: "month"
    breakdown:
      hydraulique_irrigation: 30000
      bioagroponics: 20000
      excel_data: 10000
      ia_agricole: 40000
      n8n_automation: 15000
```

---

## Workflows de mise à⁰ jour

```yaml
update_workflows:
  after_project:
    name: "Mise à⁰ jour aprè²¹s projet"
    steps:
      - step: 1
        action: "describe_project"
        fields:
          - "context"
          - "role"
          - "duration"
          - "deliverables"
          - "tools"
          - "beneficiary"
      
      - step: 2
        action: "link_skills"
        description: "Lier le projet aux compe⁰tences mobilisé²¹es"
      
      - step: 3
        action: "add_evidence"
        target: "Registre des Preuves"
        format: "markdown_table_row"
      
      - step: 4
        action: "update_metrics"
        fields:
          - "Practice"
          - "Evidence"
          - "Recency"
          - "Results"
      
      - step: 5
        action: "recalculate_score"
        formula: "Knowledge + Practice + Experience + Evidence + Recency + Results"
      
      - step: 6
        action: "update_pipeline"
        target: "Skill → Project → Money"
        condition: "si projet cré⁰e offre exploitable"
  
  weekly_review:
    name: "Revue hebdomadaire des compe⁰tences"
    frequency: "weekly"
    day: "dimanche"
    steps:
      - step: 1
        action: "check_activity"
        description: "Vé²¹rifier les compe⁰tences utilisé⁰es cette semaine"
      
      - step: 2
        action: "update_recency"
        description: "Mettre à⁰ jour les dates de dernie⁺re utilisation"
      
      - step: 3
        action: "add_practice_hours"
        description: "Ajouter les heures de pratique de la semaine"
      
      - step: 4
        action: "review_evidence"
        description: "Ajouter les nouveaux livrables comme preuves"
  
  monthly_audit:
    name: "Audit mensuel des compe⁰tences"
    frequency: "monthly"
    day: 1
    steps:
      - step: 1
        action: "recalculate_all_scores"
        description: "Recalculer tous les scores avec les nouvelles preuves"
      
      - step: 2
        action: "update_gap_analysis"
        description: "Mettre à⁰ jour l'analyse des é⁰carts par rapport aux objectifs"
      
      - step: 3
        action: "prioritize_development"
        description: "Dé²¹finir les priorité²¹s de dé⁰veloppement pour le mois suivant"
      
      - step: 4
        action: "review_revenue"
        description: "Comparer les revenus gé⁰né²¹ré²¹s aux objectifs"
```

---

## Templates de preuve

```yaml
evidence_templates:
  project:
    required_fields:
      - "date"
      - "skill"
      - "project_name"
      - "deliverable_link"
      - "measured_result"
      - "revenue_or_value"
    optional_fields:
      - "client_name"
      - "duration_hours"
      - "tools_used"
      - "testimonial"
  
  product:
    required_fields:
      - "date"
      - "skill"
      - "product_name"
      - "product_url"
      - "price"
      - "sales_count"
      - "revenue"
    optional_fields:
      - "conversion_rate"
      - "customer_feedback"
      - "update_version"
  
  learning:
    required_fields:
      - "date"
      - "skill"
      - "course_or_resource"
      - "hours_spent"
      - "certificate_or_proof"
    optional_fields:
      - "key_takeaways"
      - "projects_enabled"
```

---

## Rè⁺gles de validation

```yaml
validation_rules:
  no_self_assessment_only: true
  min_evidence_per_skill: 1
  evidence_must_be_verifiable: true
  evidence_must_be_recent: true
  recency_threshold_days: 90
  
  accepted_evidence_types:
    - type: "github_repository"
      format: "https://github.com/{user}/{repo}"
      verification: "public_or_collaborator"
    
    - type: "live_website"
      format: "https://{domain}.{tld}"
      verification: "accessible"
    
    - type: "document"
      formats:
        - "pdf"
        - "xlsx"
        - "docx"
      verification: "downloadable_with_content"
    
    - type: "financial"
      formats:
        - "invoice"
        - "payment_proof"
        - "analytics_screenshot"
      verification: "redacted_sensitive_data"
    
    - type: "testimonial"
      formats:
        - "email"
        - "linkedin_message"
        - "video"
      verification: "identifiable_source"
```

---

## Inté²¹grations

```yaml
integrations:
  github:
    enabled: true
    repository: "sbci3d-dev/lifeos-skills"
    branch: "main"
    auto_commit: true
    
  google_drive:
    enabled: true
    folder: "LifeOS/Skills/Preuves"
    sync_frequency: "manual"
    
  hubspot:
    enabled: true
    purpose: "Tracking leads et clients consulting"
    
  google_calendar:
    enabled: true
    purpose: "Tracking heures de pratique par compe⁰tence"
    
  finance:
    enabled: true
    purpose: "Tracking revenus par source"
```

---

**Notes :**
- Ce fichier de configuration é⁰volue avec le systè²¹me
- Toute modification doit ê⁰tre commité²¹e sur GitHub
- Les objectif financiers sont ré⁰visé²¹s trimestriellement
- Les nouvelles compe⁰tences peuvent ê⁰tre ajouté⁰es à⁰ tout moment
