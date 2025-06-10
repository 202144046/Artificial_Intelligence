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
