# 컬럼의 내부 유형 변형으로 인한 B*Tree 인덱스를 사용 할 수 없는 경우

|            유형            | 결과 데이터 타입 |
| :------------------------: | :--------------: |
|       CHAR + NUMBER        |      NUMBER      |
|       DATE + NUMBER        |       DATE       |
|        DATE - DATE         |      NUMBER      |
|        TRUNC(DATE)         |       DATE       |
|     NVL(CHAR, NUMBER)      |       CHAR       |
|      NVL(NUMBER, NVL)      |      NUMBER      |
| DECODE(?, ?, CHAR, NUMBER) |       CHAR       |
| DECODE(?, ?, NUMBER, CHAR) |      NUMBER      |

