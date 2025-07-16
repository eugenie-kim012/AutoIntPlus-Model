# AutoIntPlus-Model

https://www.notion.so/eugeniekim012/AutoInt-231bdaab6ba4806bb015c7b1cfce4cba?source=copy_link

성능비교를 위한 다양한 시도 (자세한 내역은 notion에 수록되어있음)

Baseline 파라미터

epochs=5
learning_rate= 0.0001
dropout= 0.4
batch_size = 2048
embed_dim= 16

### 🔍 실험 결과 비교 (AutoInt+)

| 실험명 | 변경 파라미터 | 변경값 | NDCG@10 | HitRate@10 | 비고 |
|--------|----------------|--------|---------|-------------|------|
| Baseline | - | - | **0.66205** | **0.63042** | 기본 설정 |
| A-1 | epochs | 5 → 10 | 0.66164 | 0.63032 | 성능 소폭 하락 |
| A-2 | epochs | 5 → 15 | - | - | A-1보다 낮아 진행 중단 |
| B-1 | learning_rate | 0.0001 → 0.001 | 0.66183 | 0.63052 | 미세한 향상 |
| C-1 | embed_dim | 16 → 32 | 0.66181 | 0.63060 | 유사 성능 |
| D-1 | dropout | 0.4 → 0.2 | **0.66216** | **0.63065** | 가장 우수한 성능 |

✅ D-1 실험에서 가장 좋은 성능을 보였으므로, 해당 설정을 새로운 baseline 후보로 고려할 수 있습니다.
