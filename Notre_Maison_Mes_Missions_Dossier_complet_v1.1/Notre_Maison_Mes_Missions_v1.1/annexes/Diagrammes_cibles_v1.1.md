# Diagrammes logiques proposés V1.0

## Navigation du portail
```mermaid
stateDiagram-v2
    [*] --> TASKS
    TASKS --> SECONDARY : ouvrir un volet
    SECONDARY --> TASKS : inactivité
    TASKS --> CAMERA_UNLOCKED : ouvrir caméra
    CAMERA_UNLOCKED --> TASKS : inactivité
    CAMERA_UNLOCKED --> CAMERA_LOCKED : verrouiller le maintien
    CAMERA_LOCKED --> TASKS : déverrouiller
    TASKS --> ADMIN : authentification autorisée
    ADMIN --> TASKS : inactivité et sauvegarde du brouillon
```

## Responsabilités et occurrences
```mermaid
erDiagram
    HOUSEHOLD ||--o{ PERSON : contient
    HOUSEHOLD ||--o{ TASK_LIST : contient
    TASK_LIST ||--o{ TASK_DEFINITION : organise
    TASK_DEFINITION ||--o{ OCCURRENCE : genere
    PERSON ||--o{ OCCURRENCE : responsable
    OCCURRENCE ||--o{ TASK_EVENT : trace
    OCCURRENCE ||--o{ REMINDER_JOB : rappelle
    DEVICE_SESSION ||--o{ DEVICE_LIST_BINDING : autorise
    TASK_LIST ||--o{ DEVICE_LIST_BINDING : associe
```

Le modèle JSON détaillé et les règles du cahier priment sur ces vues simplifiées. Les personnes qui valident restent distinctes des personnes responsables. Un report est un événement sur une occurrence ouverte ; une réalisation, un saut et une annulation sont des issues distinctes.
