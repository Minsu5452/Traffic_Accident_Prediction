# Traffic Accident Prediction

> 2023년 지역 치안 안전 데이터 분석 공모전에서 진행한 날씨 기반 교통사고 발생 확률 예측 프로젝트입니다.

## Overview

| Field | Details |
| --- | --- |
| Competition | 2023년 지역 치안 안전 데이터 분석 공모전 |
| Period | 2023.01.20 - 2023.02.15 |
| Host / Organizer | 경찰대학 |
| Result | Preliminary elimination |
| Team | Individual |
| Region | Chungnam, Daejeon, Sejong |
| Task | 충남, 대전, 세종 지역의 1시간 이내 교통사고 발생 확률 예측 |

## Approach

- 기상청 ASOS 관측 데이터와 경찰청 교통사고 데이터를 결합했습니다.
- 교통사고 좌표를 가장 가까운 기상 관측소 기준으로 매핑했습니다.
- 시간 단위 날씨 데이터에 사고 발생 여부를 라벨링했습니다.
- LightGBM, CatBoost 기반 분류 모델과 앙상블을 사용해 사고 발생 여부와 확률을 예측했습니다.
- SHAP 기반 중요도 분석으로 기상 요소와 사고 발생 간의 관계를 해석했습니다.

## Repository Layout

```text
.
|-- docs/
|   |-- final_report_redacted.pdf
|   `-- final_report_summary.md
|-- notebooks/
|   |-- 01_weather_accident_correlation_analysis.ipynb
|   `-- 02_hourly_accident_risk_prediction.ipynb
|-- requirements.txt
`-- traffic_accident_prediction.pkl
```

## Run

Install notebook dependencies:

```bash
pip install -r requirements.txt
```

Place the competition and external weather data under `data/`, then run the notebooks in order.

## Repository Scope

Competition data and generated outputs are excluded from the public repository.

The original submission report is kept locally. This repository includes a contact-redacted PDF version and a short report summary.

Reverse geocoding experiments are not included yet because the public scope is still undecided.
