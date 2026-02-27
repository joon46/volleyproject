(팀프로젝트_테이블_크롤링.ipynb에서 웹크롤링 진행하고 그 결과를 파일에 저장)
(회귀모델.ipynb에서 이 크롤링한 데이터를 통해 데이터 전처리/시각화/머신러닝 작업 진행)<br>
##🛠 기술 스택
Language: Python 3.x <br>
---Libraries--- <br>
Selenium, BeautifulSoup4: 웹 데이터 크롤링 및 스크래핑 <br>
Pandas, NumPy: 데이터 전처리 및 분석 <br>
Matplotlib, Seaborn: 데이터 시각화 <br>
Scikit-learn: 선형 회귀(Linear Regression) 모델 구축 및 평가 <br>


graph TD

    subgraph "Data Acquisition"
        A[KOVO Official Website] --> B[Web Crawling]
        B -- "Python (Selenium, BS4)" --> C[Raw Data (CSV)]
    end

    subgraph "Data Processing"
        C --> D[Data Preprocessing]
        D -- "Pandas, NumPy" --> E[Refined Dataset]
    end

    subgraph "Machine Learning"
        E --> F[Linear Regression Model]
        F -- "Scikit-learn" --> G[Insights & R² Score]
    end


## 🛠 기술적 도전 및 해결 (Troubleshooting)

### 1. Selenium 수집 로직 재설계 (비정형 데이터 대응)
- **문제점**: KOVO 홈페이지의 동적 테이블과 매 시즌 변하는 경기 기록 방식(비정형 데이터 포함)으로 인해 기존 크롤링 방식에서 데이터 누락 및 에러 발생.
- **해결 방안**: 
  - 특정 요소(Element)가 로드될 때까지 기다리는 `WebDriverWait`를 도입하여 수집 안정성 강화.
  - 단순 텍스트 추출을 넘어, HTML 구조를 심층 분석하여 누락될 수 있는 세부 경기 지표(비정형 요소)까지 유연하게 파싱할 수 있도록 수집 로직 재설계.
- **결과**: 데이터 유실율 0% 달성 및 시즌별 상이한 데이터 구조에 대한 확장성 확보.

### 2. 데이터 학습 범위 최적화 (7개 팀 데이터 활용)
- 신규 창단팀(페퍼저축은행) 합류로 인한 리그 구조 변화를 반영하기 위해, 기존 6개 팀 기반 모델을 7개 팀 전체 데이터 기반으로 재학습시켜 예측 오차율을 대폭 개선하였습니다.
