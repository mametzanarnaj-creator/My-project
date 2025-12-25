C4Context
    title "System Architecture: Next.js + Go"
    Person(user, "User", "Web Browser арқылы кіреді")
    
    System_Boundary(c1, "Cloud Infrastructure") {
        Container(web, "Frontend App", "Next.js", "Пайдаланушы интерфейсі")
        Container(api, "Backend API", "Go", "Бизнес логика мен API")
        ContainerDb(db, "Database", "PostgreSQL", "Мәліметтерді сақтау")
    }

    Rel(user, web, "Кіру", "HTTPS")
    Rel(web, api, "Сұраныс жіберу", "JSON/REST")
    Rel(api, db, "Оқу/Жазу", "SQL")
