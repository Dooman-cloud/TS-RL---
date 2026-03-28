
# TS_RL_proj

## 1. Project Overview
본 프로젝트는 2026 춘계 학회 포스터 논문을 위한 연구 프로젝트입니다.
주요 목표는 GARCH 모델링을 통한 VaR + DDQN classification이며, 
참고 논문인 **"Bridging Econometrics and AI VaR Estimation via"**의 데이터 수집, 전처리, 모델링, 실험 및 결과 정리를 체계적으로 수행 및 활용하는 것을 목적으로 합니다.

## 2. Team Roles
- **PM 현석**  
 Git/GitHub 구조 관리, 브랜치/merge 관리, 코드 검수, 실험 진행 보조, 레퍼런스 논문 활용 방안

- **Modeling 찬재**  
  ML 모델 구조 설계 및 구현, backtest 설계 , 레퍼런스 논문 활용 방안

- **Modeling 시훈**  
  ML 모델 구조 설계 및 구현, backtest 설계 

- **Experiment 성택**  
  변수선택, 실험 실행, DDQN 이론 숙지, 성능 결과 정리


## 3. Project file structure 

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

## 4.Branch strategy
```text
-main : 안정 버전, 검수 완료 코드만 반영
-feat/model-1 : 모델링 담당 1번 작업 브랜치 (찬재)
-feat/model-2 : 모델링 담당 2번 작업 브랜치 (시훈)
-feat/experiment : 실험 진행 담당 브랜치 (성택)
-feat/pm-setup : 구조 관리/ 공통 정리 브랜치 (현석)
-integration/model : 모델 브랜치 통합용

**main 브랜치는 직접 push 금지, 개인 브랜치를 통한 작업 push만**
**main 반영전 팀원 최소 2명 이상 검수후 merge**
**modeling은 대략적 코드 구조를 맞춰 개인작업 후 integration 브랜치에 merge한 후 main 브랜치로 merge 하기**
**main 반영될시 개인 브랜치에 주기적으로 pull하기**
```
## 5.commit 규칙

1) 기능 단위로 자주 commit 하기

2) 아래의 commit 메세지 규칙을 따르기
예시 :
`(추가) 파일이름 or 작업이름 : 데이터 전처리 후 시각화 추가`
`(수정) 파일이름 or 작업이름 : VaR변수 임계점 조정 -1 => -1.5`
`(생성) 파일이름 or 작업이름 : ANN,SVM 모델링 코드`

## 6. 파일명 규칙

1) 공용 파일 및 sharing 파일 
<01.data_collection> 과 같이 0x 번호 기반

2) modeling 파일 / experiments 파일
역할 , 작업 기반 이름 사용
`model_svm.ipynb`
`ex_boruta.ipynb `
`data_GARCH_VAR.ipynb`
이런 형식으로 진행
