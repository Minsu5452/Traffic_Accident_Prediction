# 🚦 Traffic Accident Prediction — 실시간 날씨 기반 교통사고 확률 예측

![Host](https://img.shields.io/badge/Host-경찰대학-navy)
![Competition](https://img.shields.io/badge/2023-지역%20치안%20안전%20데이터%20분석%20공모전-blue)
![Role](https://img.shields.io/badge/Role-개인-orange)
![Region](https://img.shields.io/badge/Region-충남%20·%20대전%20·%20세종-green)

> **경찰대학 주최 2023 지역 치안 안전 데이터 분석 공모전** · **실시간 날씨 데이터 기반 충남·대전·세종 지역별 1시간 이내 교통사고 확률 예측 모델**. 기상청 데이터 × 역지오코딩 자체 구현 결합.

---

## 🎯 Competition

- **공모전**: 2023년 지역 치안 안전 데이터 분석 공모전
- **주최**: 경찰대학
- **역할**: 개인 (국민대민쑤팀)
- **결과**: 예선 참여

## 🔍 Overview

- **배경**: 실시간 교통사고 위험도 예측은 순찰·구급 자원 배분과 정책 설계의 근간.
- **문제 정의**: 기상청 실시간 날씨 + 교통사고 이력 + 지리 데이터로 **1시간 이내 지역별 교통사고 확률** 예측.
- **범위**: 충남 · 대전 · 세종 3개 지역

## 🧠 Approach

### 주요 분석
1. **날씨 ↔ 교통사고 상관관계 분석** (기상청 ASOS 데이터)
2. **역지오코딩 자체 제작** — 좌표 → 행정구역 매핑 모듈
3. **실시간 확률 예측 모델**: 지역 × 시간대 × 날씨 조합 학습

### 파이프라인
```
기상청 ASOS 실시간 날씨 + 교통사고 이력
    │
    ▼  역지오코딩 (자체 구현)
지역(시/군/구) 매핑
    │
    ▼  Feature Engineering
시간대 · 날씨 · 지역 조합
    │
    ▼  예측 모델
1시간 내 교통사고 확률
```

## 📁 Structure

```
Traffic_Accident_Prediction/
├── 기상청 날씨 데이터와 교통사고 데이터 간의 상관관계 분석_국민대민쑤팀.ipynb
├── 실시간 날씨 데이터를 기반으로 충남·대전·세종 각 지역별 1시간 이내 교통사고확률 예측모델_국민대민쑤팀.ipynb
├── 역지오코딩_Code_자체제작/            # 자체 제작 역지오코딩 모듈
├── traffic_accident_prediction.pkl       # 학습된 모델
├── 【붙임 2】 데이터 분석 최종결과 보고서_국민대민쑤팀.pdf
└── README.md
```

## 🛠 Tech Stack

- Python · Pandas · scikit-learn · 기상청 ASOS API · 역지오코딩 (자체 구현) · Jupyter

---

> 🔗 Portfolio: [Minsu5452](https://github.com/Minsu5452)
