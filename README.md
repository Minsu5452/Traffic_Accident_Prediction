# Traffic Accident Prediction

> 2023년 지역 치안 안전 데이터 분석 공모전에서 진행한 날씨 기반 교통사고 발생 확률 예측 프로젝트입니다. 충남·대전·세종 지역을 대상으로 1시간 이내 사고 발생 여부와 확률을 예측했습니다.

## Overview

| 항목 | 내용 |
| --- | --- |
| 대회 | 2023년 지역 치안 안전 데이터 분석 공모전 |
| 기간 | 2023.01.20 ~ 2023.02.15 |
| 주최/주관 | 경찰대학 |
| 팀 구성 | 개인 |
| 결과 | 예선 탈락 |
| 분석 지역 | 충남, 대전, 세종 |
| 과제 | 1시간 이내 교통사고 발생 확률 예측 |

## Approach

- 기상청 ASOS 관측 데이터와 경찰청 교통사고 데이터를 결합했습니다.
- 교통사고 좌표를 가장 가까운 기상 관측소 기준으로 매핑했습니다.
- 시간 단위 날씨 데이터에 사고 발생 여부를 라벨링해 이진 분류 문제로 정의했습니다.
- LightGBM, CatBoost 기반 분류 모델과 voting ensemble 로 사고 발생 여부 및 확률을 예측했습니다.
- SHAP 기반 중요도 분석으로 기상 요소와 사고 발생 간의 관계를 해석했습니다.

## Reported Result

- F1 Score: 0.8577
- Accuracy: 0.7911

## Repository Structure

```text
.
├── notebooks/
│   ├── 01_weather_accident_correlation_analysis.ipynb
│   └── 02_hourly_accident_risk_prediction.ipynb
├── reports/
│   └── traffic_accident_prediction_report.pdf
├── requirements.txt
└── README.md
```

## Public Scope

이 저장소는 포트폴리오 공개용으로 정리한 버전입니다.

- 대회 제공 데이터, 외부 기상 데이터, 학습된 모델 파일은 포함하지 않았습니다.
- 노트북 출력 결과와 실행 메타데이터는 제거했습니다.
- 보고서 PDF는 개인정보(휴대폰·이메일)를 마스킹한 버전을 포함했습니다.
- 역지오코딩 사이드 작업은 공모전 본 솔루션과 별개라 제외했습니다.
- 실행하려면 대회 데이터와 외부 기상 데이터를 `data/` 경로에 별도로 배치해야 합니다.
