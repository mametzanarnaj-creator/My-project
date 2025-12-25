flowchart LR
    Code[Commit Code] --> Test[Unit Test & Linter]
    Test --> Security[Security Scan: Snyk/Trivy]
    Security --> Build[Docker Build]
    Build --> Push[Push to Registry]
    Push --> Deploy[Deploy to Staging/Prod]
