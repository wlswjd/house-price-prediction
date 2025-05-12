# 🏠 서울시 부동산 가격 예측 프로젝트

본 프로젝트는 서울시 아파트 실거래가 데이터를 활용하여 향후 거래 가격을 예측하는 머신러닝 기반 모델을 구축하는 데 목적이 있습니다.

---

## 📁 디렉토리 구조

```
house-price-prediction/
├── data/
│   ├── raw/               # 원본 데이터 (train, test, 외부 데이터 등)
│   └── processed/         # 전처리된 데이터
├── notebooks/             # 분석 노트북 (EDA ~ 모델링 ~ 제출)
├── models/                # 저장된 모델 파일 (.pkl 등)
├── outputs/               # 제출 결과 파일
├── requirements.txt       # 프로젝트 실행을 위한 패키지 목록
└── README.md              # 프로젝트 설명 파일
```

---

## 📊 주요 진행 내용

### 1. 데이터 탐색 (EDA)
- 데이터의 기본 정보 및 결측치 확인
- 타겟값 분포 분석 및 로그 변환 시도
- 주요 범주형 변수 시각화
- 상관계수 히트맵 시각화

### 2. 전처리 및 피처 엔지니어링
- 결측치 처리 및 이상치 대응
- 범주형 변수 One-Hot Encoding
- 위도/경도 기반 클러스터링 (KMeans)
- 외부 데이터 (버스, 지하철) 병합 및 활용

### 3. 모델링
- RandomForest, LightGBM 등 다양한 모델 실험
- K-Fold 교차검증을 통한 RMSE 평가
- 최종 모델 저장 (.pkl 파일)

### 4. 예측 및 제출
- 테스트셋 예측 수행
- `sample_submission.csv` 포맷에 맞게 결과 저장
- outputs/submission.csv 생성

---

## 💻 사용된 주요 라이브러리
- `pandas`, `numpy`, `scikit-learn`, `matplotlib`, `seaborn`
- `lightgbm`, `joblib`

---

## 📌 실행 방법

```bash
# 필요한 패키지 설치
pip install -r requirements.txt

# 노트북 실행
jupyter notebook notebooks/01_EDA.ipynb
```

---

## 📬 문의
> 본 프로젝트는 FastCampus Kernel AI 부트캠프 과정 중 수행된 실습 과제입니다.
