# Implement-FMCW-radar-3D-FFT-signal-processing-and-zero-padded-angle-estimation



1. FMCW Radar System Design & Multi-Stage FFT Estimation Pipeline

•	개요: 77GHz FMCW 레이더 시스템의 물리 모델링부터 최종 파라미터(거리, 속도, 각도) 추정까지의 전 과정을 아우르는 종합 신호 처리 파이프라인 스크립트입니다.

•	주요 내용:
o	대역폭(Bandwidth), 펄스 지속 시간(Chirp Duration) 등 송수신 안테나 파라미터와 타겟의 운동 상태를 반영하여 3차원 복소수 ADC Raw Data를 직접 설계 및 생성합니다.
o	Range-Doppler 2D FFT를 통해 거리와 속도를 우선 추출하고, 공간 축으로 FFT를 하여 최종 방위각(Angle)까지 도출해 내는 전체 데이터 흐름(Pipeline)을 유기적으로 완성합니다.




2. FMCW Radar AoA Estimation: Zero-Padding vs No-Padding Analysis

• 개요: 안테나 각도 추정 성능을 극대화하기 위한 제로 패딩(Zero-Padding)의 유무에 따른 차이를 집중적으로 분석·비교하는 실험용 스크립트입니다.

•	주요 내용:
o	N=4개의 물리적 안테나 배열 환경에서, 14.5°와 같이 격자 눈금 사이에 위치한 타겟을 마주했을 때 발생하는 각도 추정 오차 문제를 다룹니다.
o	제로 패딩을 통해 샘플 수를 N=64로 interpolation했을 때, 각도 추정 오차가 얼마나 감소하는지 수치 데이터와 비교 그래프를 통해 검증합니다.
