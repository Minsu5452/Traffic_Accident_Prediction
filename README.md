# 날씨 기반 교통사고 위험 예측

충남·대전·세종 지역의 교통사고와 기상 데이터를 결합해 1시간 이내 사고 발생 여부와 확률을 예측한 공모전 프로젝트입니다.

## 개요

| 항목 | 내용 |
| --- | --- |
| 대회 | 2023년 지역 치안 안전 데이터 분석 공모전 |
| 기간 | 2023.01.20 - 2023.02.15 |
| 주최 / 주관 | 경찰대학 / 경찰대학 |
| 결과 | 예선 탈락 |
| 지역 | 충남, 대전, 세종 |
| 과제 | 날씨 기반 교통사고 발생 확률 예측 |

## 접근

- 기상청 ASOS 관측 데이터와 경찰청 교통사고 데이터를 결합했습니다.
- 사고 좌표를 가까운 기상 관측소 기준으로 매핑했습니다.
- 시간 단위 날씨 데이터에 사고 발생 여부를 라벨링해 이진 분류 문제로 구성했습니다.
- LightGBM, CatBoost, voting ensemble을 사용했습니다.
- SHAP 기반 중요도 분석으로 기상 요소와 사고 발생 관계를 해석했습니다.

## 보고 지표

| 지표 | 값 |
| --- | --- |
| F1 Score | 0.8577 |
| Accuracy | 0.7911 |

## 저장소 구성

```text
.
├── docs/
│   └── final_report_redacted.pdf
├── notebooks/
│   ├── 01_weather_accident_correlation_analysis.ipynb
│   └── 02_hourly_accident_risk_prediction.ipynb
├── reports/
│   └── traffic_accident_prediction_report.pdf
└── requirements.txt
```

## 공개 범위

대회 원본 데이터, 외부 기상 데이터, 모델 파일, 개인정보가 포함된 원본 보고서는 포함하지 않았습니다. 공개 보고서는 마스킹된 버전입니다.
