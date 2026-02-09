🛠 기술 스택
Language: Python 3.x
---Libraries---
Selenium, BeautifulSoup4: 웹 데이터 크롤링 및 스크래핑
Pandas, NumPy: 데이터 전처리 및 분석
Matplotlib, Seaborn: 데이터 시각화
Scikit-learn: 선형 회귀(Linear Regression) 모델 구축 및 평가


A[KOVO Crawling Data] --> B{Data Preprocessing} <br>
    B --> C[One-hot Encoding: Team] <br>
    B --> D[Numeric Scaling: Season/Streak] <br>
    C & D --> E[Feature Selection: Correlation > 0.7] <br>
    E --> F[Linear Regression Model] <br>
    F --> G[Predicted Points / Ranking] <br>

    
