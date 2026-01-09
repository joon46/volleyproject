|    컬럼명          |    타입          |          설명                 | <br>
| 시즌 (Season) |	Object / Int  |	해당 경기 시즌 (예: 2023-2024) |	수치형 변환 <br>
| 세트득실률 | Float | 팀의 총 득세트 / 실세트 비율   | <br>
| 공격_성공률 | Float | 팀 전체 공격 시도 대비 성공률 | <br>
| 	 |  | 	 | <br>

<br>


A[KOVO Crawling Data] --> B{Data Preprocessing} <br>
    B --> C[One-hot Encoding: Team] <br>
    B --> D[Numeric Scaling: Season/Streak] <br>
    C & D --> E[Feature Selection: Correlation > 0.7] <br>
    E --> F[Linear Regression Model] <br>
    F --> G[Predicted Points / Ranking] <br>

    
