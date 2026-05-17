# GJR-GARCH와 분류 모델 기반 하이브리드 프레임워크를 활용한 KOSPI 200 지수의 동적 Value-at-Risk 조정

<img width="1920" height="2712" alt="GJRGARCH와 분류 모델 기반 하이브리드 프레임워크를 활용한 KOSPI 200 지수의_260517_181423_0" src="https://github.com/user-attachments/assets/d82fd48a-2664-42e1-ba61-2b021ed96b75" />



## Project Overview
GARCH 모델과 같은 전통적인 통계 모델은 비선형성 포착에 어려움이 있어 정확한 주식시장 리스크 추정량 산출에 한계가 있다. 본 연구는 시계열 예측 모델로부터 산출한 변동성 예측값과 분류 모델(기계학습, 강화학습)을 결합한 하이브리드 프레임워크를 제안한다. GJR-GARCH 모델로부터 산출한 VaR 추정량에 기초하여 위험 수준을 분류 모델로 예측하고, 그 결과에 따라 VaR 추정량을 동적으로 조정한다. YahooFinance와 KRX 데이터 마켓에서 수집한 2009년부터 2026년까지의 KOSPI 200 데이터로 본 프레임워크를 실험한 결과, 모든 분류 모델에서 조정된 VaR 적용 후 VaR 초과 비율이 이론적 초과 비율과 부합함을 Kupiec 검정으로 확인하였다. 이는 VaR 추정을 분류 문제로 재정의한 접근이 주식시장 리스크 추정에서 실증적 활용 가능성을 가짐을 시사한다.

**Keyword: 분류 · GJR-GARCH · 변동성 · Value-at-Risk · 한국주식 · 금융 리스크.**

## Contributors
- 김성택, (16890) 경기도 용인시 수지구 죽전로 152, 단국대학교 통계데이터사이언스학과, 학사과정. E-mail:dunkykim@dankook.ac.kr
- 도현석, (16890) 경기도 용인시 수지구 죽전로 152, 단국대학교 통계데이터사이언스학과, 학사과정. E-mail:32231447d@dankook.ac.kr
- 이찬재, (16890) 경기도 용인시 수지구 죽전로 152, 단국대학교 통계데이터사이언스학과, 학사과정. E-mail:32213591@dankook.ac.kr
- 정시훈, (16890) 경기도 용인시 수지구 죽전로 152, 단국대학교 통계데이터사이언스학과, 학사과정. E-mail:32231447d@dankook.ac.kr
- 조민영, 교신저자: (16890) 경기도 용인시 수지구 죽전로 152, 단국대학교 통계데이터사이언스학과, 조교수. E-mail:myjo@dankook.ac.kr



## file structure 

```text
project/
├─ data/
│  ├─ raw/          # 원본 데이터
│  └─ processed/    # 전처리 데이터
│
├─ notebooks/       # 주피터 실험용 코드
│  ├─ sharing/      # 기본 공용 코드 ex) data 수집 및 전처리
│  ├─ modeling/      # 모델링 개인/기능 실험
│  └─ experiments/   # 실험 진행 기능 실험
│
├─ src/             # 메인 소스코드(최종 실험용 코드 정리본)
├─ figures/         # 시각화 자료
├─ results/         # 실험 결과 저장
├─ README.md        
```

