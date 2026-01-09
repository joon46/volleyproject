A[KOVO Crawling Data] --> B{Data Preprocessing} <br>
    B --> C[One-hot Encoding: Team] <br>
    B --> D[Numeric Scaling: Season/Streak] <br>
    C & D --> E[Feature Selection: Correlation > 0.7] <br>
    E --> F[Linear Regression Model] <br>
    F --> G[Predicted Points / Ranking] <br>
