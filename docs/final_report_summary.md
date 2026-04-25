# Final Report Summary

## Project

- Title: 실시간 날씨 데이터를 이용한 충남, 대전, 세종 각 지역별 1시간 이내 교통사고 확률 예측 모델
- Competition: 2023년 지역 치안 안전 데이터 분석 공모전
- Host / Organizer: 경찰대학
- Participant: Individual

## Objective

The project analyzed whether weather conditions are associated with traffic accident occurrence and built a model that estimates near-term accident risk by region.

## Data Used

- Police event records filtered to traffic accident events
- KMA ASOS weather observations
- Weather station location metadata

## Key Method

Traffic accident coordinates were assigned to the nearest ASOS weather station using geographic distance. Hourly weather observations were then labeled with accident occurrence and used as binary classification data.

## Reported Result

- F1 score: 0.8577
- Accuracy: 0.7911

## Public Notes

The original submission report contains personal contact information. The public repository keeps a contact-redacted PDF version instead of the unredacted original.

Competition data and generated outputs are excluded.
