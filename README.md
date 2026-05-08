# VirtualMotionInference Component (AI & Processing Layer)

NNE(Neural Network Engine)를 사용하여 ONNX 모델을 구동하고 제스처를 실시간으로 인식하는 두뇌 역할을 합니다.

## 주요 기능
- **NNE 기반 ONNX 추론**: 언리얼 5 공식 AI 엔진을 통해 ONNX 모델을 최적화된 성능으로 구동합니다.
- **슬라이딩 윈도우 관리**: 360프레임(30프레임 분량)의 데이터를 유지하며 실시간 분석을 수행합니다.
- **확률 기반 인식**: Softmax 연산을 통해 제스처 인식 확률을 계산하고 커트라인 초과 시 이벤트를 발생시킵니다.

## 사용 방법
1. 액터에 `VirtualMotionInferenceComponent`를 추가합니다.
2. `Pretrained Model Data` 항목에 ONNX 모델 에셋을 할당합니다.
3. `ReceiveMotionData` 함수를 호출하여 리시버로부터 받은 데이터를 입력합니다.


---

# VirtualMotionInference Component (AI & Processing Layer)

This component acts as the "brain," using the NNE (Neural Network Engine) to run ONNX models and recognize gestures in real-time.

## Key Features
- **NNE-Based ONNX Inference**: Runs ONNX models with optimized performance via the official Unreal Engine 5 AI engine.
- **Sliding Window Management**: Maintains a buffer of 360 frames (approx. 30 frames worth) for real-time analysis.
- **Probability-Based Recognition**: Calculates gesture recognition probability via Softmax and triggers events when the threshold is met.

## How to Use
1. Add the `VirtualMotionInferenceComponent` to your Actor.
2. Assign your ONNX model asset to the `Pretrained Model Data` field.
3. Call the `ReceiveMotionData` function to input data received from the Receiver.
