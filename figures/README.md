# 공개 UFUV 결과 그림

정성 비교용 두 PNG는 [UFUV 공개 데이터셋](https://huggingface.co/datasets/huihuixu/uterine_fibroid_ultrasound_video_segmentation)의 공식 test 영상에서 생성한 정성 비교 패널입니다. 데이터셋 페이지의 표시 라이선스는 **MIT**이며, 관련 논문은 [LGRNet, MICCAI 2024](https://papers.miccai.org/miccai-2024/460-Paper0813.html)입니다.

- 왼쪽: 공개 UFUV 초음파 프레임
- 가운데: 정답 mask를 녹색으로 표시
- 오른쪽: LGRNet Res2Net50 적응 실행의 예측 mask를 빨간색으로 표시

두 사례는 서로 다른 공개 test 비디오의 25번째 프레임입니다. 전체 성능을 대표하도록 무작위 추출한 그림은 아닙니다. 이 그림의 모델 실행은 `notes/2026-10-02-ufuv-baselines.md`의 **Res2Net50 적응 실행**이며, PVTv2 결과와 혼동하지 않습니다. 배포 파일에는 원본 비디오 ID와 환자 관련 메타데이터를 넣지 않았습니다.

`ufuv_public_per_video_dice.png`는 공개 UFUV test 17비디오의 LGRNet Res2Net50 적응 실행과 PVTv2 공개 설정 실행의 비디오별 Dice에서 만든 분포 그림입니다. 비디오 ID는 그림에 표시하지 않았고 두 실행의 학습 설정이 다르므로 통제 비교를 뜻하지 않습니다.
