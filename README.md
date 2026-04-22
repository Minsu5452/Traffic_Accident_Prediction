# Traffic Accident Prediction

실시간 날씨 데이터를 기반으로 충남, 대전, 세종 지역의 1시간 이내 교통사고 확률을 예측한 개인 프로젝트입니다. 기상 데이터와 교통사고 이력을 연결하기 위해 역지오코딩 로직도 직접 구현했습니다.

## Snapshot

| Item | Detail |
| --- | --- |
| Type | Competition project |
| Period | 2023 |
| Team | Individual |
| Task | 지역별 단기 교통사고 발생 확률 예측 |
| Region | 충남, 대전, 세종 |
| Key work | 기상청 데이터 분석, 역지오코딩 구현, 예측 모델링 |

## Work Summary

- 날씨 변수와 사고 발생 간의 상관관계를 먼저 분석했습니다.
- 좌표를 행정구역으로 변환하는 역지오코딩 모듈을 직접 만들었습니다.
- 지역, 시간, 날씨 조합을 기반으로 단기 사고 확률 예측 모델을 구성했습니다.

## Repository Layout

- `기상청 날씨 데이터와 교통사고 데이터 간의 상관관계 분석_국민대민쑤팀.ipynb`: EDA
- `실시간 날씨 데이터를 기반으로 충남·대전·세종 각 지역별 1시간 이내 교통사고확률 예측모델_국민대민쑤팀.ipynb`: 모델링 노트북
- `역지오코딩_Code_자체제작/`: 자체 제작 geocoding 실험
- `traffic_accident_prediction.pkl`: 저장된 모델
- `【붙임 2】 데이터 분석 최종결과 보고서_국민대민쑤팀.pdf`: 제출 보고서
