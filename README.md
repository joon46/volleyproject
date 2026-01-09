A[KOVO Crawling Data] --> B{Data Preprocessing}
    B --> C[One-hot Encoding: Team]
    B --> D[Numeric Scaling: Season/Streak]
    C & D --> E[Feature Selection: Correlation > 0.7]
    E --> F[Linear Regression Model]
    F --> G[Predicted Points / Ranking]
