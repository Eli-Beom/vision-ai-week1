# vision-ai-week1
OpenCV를 활용한 이미지 전처리 및 시각화 수행

이 과제는 Hugging Face에서 제공하는 food101 이미지 데이터셋 중 "sushi" 클래스 이미지를 사용하여, OpenCV를 활용한 이미지 전처리 및 시각화를 수행하는 작업입니다. 특히 스시 이미지에서 빨간색 영역(예: 참치, 새우 등)을 감지하고 시각화하는 필터링 기법을 구현하는 것을 목표로 합니다.

# 📌 1주차 과제 - 스시 이미지 전처리 및 빨간색 영역 필터링

## 과제 개요

- Hugging Face `food101` 데이터셋을 활용해 "sushi" 클래스를 선택
- 상위 5장의 스시 이미지를 로컬로 저장
- OpenCV를 활용해 이미지에서 빨간색 영역을 감지하고 필터링
- 필터링된 결과를 시각적으로 확인

---

## 사용 기술 및 라이브러리

- Python 3.x
- [Hugging Face Datasets](https://huggingface.co/datasets/food101)
- OpenCV (`cv2`)
- NumPy
- Matplotlib

---

## 폴더 구조
<pre>
vision_ai_week1/
│
├── raw_sushi_samples/         # 스시 원본 이미지 저장 폴더
├── red_filtered_samples/      # 빨간색 필터링 결과 저장 폴더
├── vision_ai_week1.py         # 전체 실행 Python 스크립트
└── README.md                  # 현재 문서
</pre>

---

## 🚀 수행 절차

### 1. 데이터셋 불러오기
- `datasets` 라이브러리를 통해 `food101`의 `train` split 로드
- `sushi` 클래스에 해당하는 상위 5개의 이미지를 저장

### 2. 빨간색 감지 및 마스킹
- 이미지를 HSV 색상 공간으로 변환
- 빨간색을 나타내는 두 범위 `[0~10], [170~180]`을 마스크로 설정
- 마스크를 적용하여 빨간색 영역만 추출

### 3. 이미지 저장 및 시각화
- 빨간색 영역이 필터링된 이미지를 `red_filtered_samples`에 저장
- `matplotlib`를 이용해 원본과 필터링 이미지를 나란히 시각화

---

