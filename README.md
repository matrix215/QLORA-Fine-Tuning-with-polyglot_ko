# Overeview

## Polyglot-ko란?

- Polyglot은 비영리 AI 연구단체인 EleutherAI에서 개발한 GPT-NeoX 기반의 multilingual pretrained 모델.
- 한국어 데이터로 사전학습된 Polyglot-ko모델은 TUNiB에서 수집한 1.2TB의 한국어 데이터를 다양한 방식의 전처리를 거쳐 가공한 뒤 사전학습시킴.
- Koalpaca모델의 백본 모델로 사용된다.

## QLoRA란?

![image](https://github.com/matrix215/QLORA-Fine-Tuning-with-polyglot_ko/assets/101815603/40f71bcc-70bd-4c00-a1b1-47acea346c8b)

- QLoRA(Quantized Low Rank Adapters)는 메모리 사용량을 크게 줄이는 효율적인 파인튜인 접근법으로, 전체 16비트 파인튜닝 성능을 유지하면서 단일 48GB GPU에서 650억 매개 변수 모델을 파인튜닝할 수 있다.
- 이는 frozen된 4비트 양자화 사전 훈련된 언어 모델을 통해 그레이디언트를 낮은 순위 어댑터(LoRA)로 역전파함으로써 가능해진다.

### 주요 방법들
### 4-bit NormalFloat
- Normally distributed data에 딱 맞는 quantization용 data type


### DoubleQuantization
- Quantization constants를 quantization함으로써 메모리 감소


### Paged Optimizer
- Optimizer를 paging하기
