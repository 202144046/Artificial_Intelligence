# 🇰🇷🆚🇰🇵 군복 이미지 기반 이진 분류 모델 개발 프로젝트

한국군(ROK)과 북한군(DPRK)의 군복 이미지를 분류하는 이진 분류 CNN 모델입니다.  
이미지 데이터를 기반으로 Convolutional Neural Network(CNN)를 학습하여  
두 클래스를 정확히 분류하는 것이 목표입니다.

---

## 🧪 사용 환경

- Python 3.x
- TensorFlow / Keras
- OpenCV
- NumPy, scikit-learn
- Google Colab 권장

---

## 📁 데이터 구조
<pre><code>/project/content/
│
├── datasets/
│   ├── rok/         ← 한국군 이미지 (훈련용)
│   └── dprk/        ← 북한군 이미지 (훈련용)
│
├── test/
│   ├── test_rok/    ← 한국군 테스트 이미지
│   └── test_dprk/   ← 북한군 테스트 이미지
</code></pre>

---

## 🗜️ 데이터 압축 해제 명령어 (Colab 기준)

```bash
# 훈련용 이미지 압축 해제
!unzip -o /content/rok.zip -d /content/datasets/rok/
!unzip -o /content/dprk.zip -d /content/datasets/dprk/

# 테스트 이미지 압축 해제
!unzip -o /content/test.zip -d /content/test/
```

---

## ⚙️ 실행 방법
1. 필요한 패키지를 설치하거나 Google Colab에서 환경 구성
2. datasets/rok, datasets/dprk, /content/test 폴더가 있는지 확인
3. main.py 또는 .ipynb 파일을 열어 순서대로 실행

---

## 🧠 모델 구조
• Conv2D × 4  
• Dense(256) + Dropout(0.4)  
• Optimizer : Adam  
• Loss : Binary Crossentropy  
• Metric : Accuracy  

---

## 📈 최종 성능
• 테스트 정확도 : 70.00%

---

## 📌 참고 사항
• 학습용 이미지 수가 적기 때문에 ImageDataGenerator를 활용하여 데이터 증강을 수행함  
• 더 많은 이미지와 Transfer Learning을 적용하면 성능 향상이 가능함  
