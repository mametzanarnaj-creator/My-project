graph LR
    A[Code Commit] --> B{GitHub Actions}
    B --> C[Linter & Unit Tests]
    C --> D[Security Scan: Snyk/Trivy]
    D --> E[Docker Build & Push]
    E --> F[Deploy to Staging]
    F --> G[Manual QA]
    G --> H[Production Release]
