# Studying-Deep-Learning
2026.01. Studying Deep-Learning
Q1.
업로드 예정

Q2.
MNIST Denoising
모델은 DnCNN 구조를 사용하였다.
DnCNN은 깨끗한 이미지를 직접 복원하는 대신, 입력 이미지에 포함된 노이즈 성분을 예측하고 이를 제거하는 잔차(residual) 학습 방식을 사용한다.
Optimizer로는 Adam과 AdamW를 모두 실험하였으며, 본 실험 조건에서는 AdamW의 weight decay 효과가 성능 향상으로 이어지지 않아 Adam을 최종적으로 선택하였다.
사용한 구조는 정확히 DnCNN 구조로, 총 8개의 convolution layer로 구성되며, 첫 번째 레이어는 Conv–ReLU 구조를 사용하고, 중간 6개 레이어는 Conv–BN–ReLU 구조를 반복적으로 사용하였다. 마지막 레이어는 활성화 함수 없이 Convolution 레이어만 사용하였다.
최종 점수값은 91.35점으로, 문제에서 고정하도록 주어진 값 외의 다른 값들도 더 fine tuning 하였다면 더 높은 점수를 얻을 수 있었을 것으로 보이나, 시간의 한계로 인해 더 테스트해보지 못하여 아쉬웠다.
