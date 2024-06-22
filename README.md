# Autonomous-driving_2d_object_detection
경기도 자율주행센터에서 진행한 2d 객체 탐지 공모전

경희대학교 공과대학 산업경영공학과 2023 추계학술제 장려상 수상
<br/>
경기도 자율주행센터 데이터분석 경진대회 은상 수상

## 문제 정의
자율주행 기술 발전으로 도로 상황을 실시간으로 모니터링하고 위험 상황을 빠르고 정확하게 식별하는 것이 중요

## 접근 방법 
기존 객체탐지 모델 대비 소형 객체 탐지 성능 향상을 목표로 진행
### 1. 실험을 통한 앵커박스 크기 최적화
- K-means clustering을 사용하여 IOU 최적화
- 바운딩 박스의 크기 분포를 분석하여 각 클러스터 중심을 실제 데이터의 대표적인 바운딩 박스 크기로 설정함

![image](https://github.com/muk-jjang/Autonomous-driving_2d_object_detection/assets/122384236/a062d6d0-83d6-47a1-8681-e3d3f9ef1428)

### 2. 데이터 증강을 통한 데이터 불균형 해소
- VerticalFlip, Mosaic, GridDistortion 등의 데이터증강 기법을 사용하여 일반화 성능을 올림
![image](https://github.com/muk-jjang/Autonomous-driving_2d_object_detection/assets/122384236/e13ca870-960f-4676-9344-c469f472f44b)

### 3. 소형 객체 탐지에 좋은 성능을 보이는 HIC-YOLO 모델 도입
- 소형 객체탐지에 좋은 성능을 보이는 HIC-YOLO 모델 도입
  
![image](https://github.com/muk-jjang/Autonomous-driving_2d_object_detection/assets/122384236/e488bf4b-2043-4c8c-bd16-682130b9ae36)

---
## 전체 프로세스
![image](https://github.com/muk-jjang/Autonomous-driving_2d_object_detection/assets/122384236/02428ed9-07c0-4647-bf0a-e221f84fe626)

## Experiment
![image](https://github.com/muk-jjang/Autonomous-driving_2d_object_detection/assets/122384236/ce05e6b1-7036-4eb7-8693-4d2676586adf)



