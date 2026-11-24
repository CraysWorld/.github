# CRAYS architecture overview

Web and mobile applications connect through CRAYS APIs and Core/BCC to the services responsible for commerce, hospitality, collaboration and personal intelligence.

~~~mermaid
flowchart TD
    UI["Web / mobile: Pro · Personal<br/>Member / Club · Work / SaaS"] --> API["CRAYS application APIs / GraphQL"]
    API --> Core["Core / BCC: identity, accounts,<br/>permissions and business rules"]
    Core --> Adapters["CRAYS BFFs and service adapters"]
    Adapters --> Services["Independent service APIs and runtimes"]
    Services --> Business["Plane · Vendure · Frappe / ERPNext · Qlo"]
    Services --> Collaboration["Nextcloud · Postiz"]
    Services --> Chuck["Chuck: personal intelligence"]
    Chuck -. "documented component relationship" .-> OpenClaw["OpenClaw agent components"]
    Core --> RDS["Core data: RDS PostgreSQL"]
    Services --> Data["Service-owned databases and file storage"]
    classDef crays fill:#fff1f2,stroke:#b42335,color:#202124;
    class API,Core,Adapters crays;
~~~

[Explore the architecture and service responsibilities](https://github.com/CraysWorld/crays-platform/blob/main/docs/architecture.md) · [Back to CRAYS](https://github.com/CraysWorld)
