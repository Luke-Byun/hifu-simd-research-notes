# MRI 분할 기준선

- 기록 시기: 2026-09
- 상태: 기준선과 평가 범위 정리

## 질문

의료영상 사전학습 초기화와 LoRA 적응이 자궁근종 MRI 분할의 기준선으로 유용한가? 작은 병변과 큰 병변에서 모델의 거동은 어떻게 다른가?

## 설정

공개 UMD 자궁근종 MRI를 환자 단위로 train, validation, test에 나눴습니다. SAM3-LoRA와 MedSAM3 초기화 LoRA를 비교하고, 근종 mask의 pixel overlap과 병변 크기별 결과를 살펴봤습니다.

## 관찰

의료영상 초기화 모델을 후속 분석의 작업 기준선으로 선택했습니다. 크기별 분석에서는 가장 작은 병변군의 누락이 중요한 개선 대상이었습니다. 전체 pixel overlap만으로 이 문제를 설명하기 어려워 영상별 Dice와 병변별 Dice를 함께 보는 평가 형식을 정리했습니다.

## 해석

작은 병변 탐지와 큰 병변의 경계 품질은 서로 다른 오류 양상입니다. 다음 모델 비교에서는 pixel micro Dice, mean per-image Dice, mean matched-instance Dice를 함께 기록합니다.

## 다음 단계

작은 병변군의 recall과 전체 분할 성능을 같은 validation 설정에서 함께 추적합니다.
