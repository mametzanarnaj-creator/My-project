graph TD
    User((Пайдаланушы)) -- HTTPS --> FE[Frontend: Next.js]
    FE -- REST API --> BE[Backend: Go/Python]
    BE -- Query --> DB[(Database: PostgreSQL/Redis)]
    
    subgraph Infrastructure
        BE
        DB
    end
    
    subgraph Orchestration
        K8s[Kubernetes Cluster]
    end
