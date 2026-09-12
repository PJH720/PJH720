## 박재현 (Jaehyun Park)

서강대학교 경제학·역사학 · AI 서비스 기획 / 데이터 분석
📧 jhp3822n@sogang.ac.kr

> 모호한 질문을 측정 가능한 형태로 바꾸고, 그 답을 직접 구현해 확인합니다.
> 경제학의 인과추론 방법론과 LLM 에이전트 구현을 함께 씁니다.

---

### 대표 프로젝트

#### [Churn Guard](https://github.com/PJH720/churn-guard) — 고객 이탈 예측·리텐션 전략
`AI@Sogang Sprout 2기 팀 프로젝트` · Demo Day 현업 심사

모두가 버리는 `Zip Code`를 원-핫 대상이 아니라 **공개 소득 데이터 조인키**로 재해석.
조인 성공률 **99.94%** → 이탈군 vs 잔존군 **t=11.72, p=4.76e-31**.
소득 단독으로는 이탈이 설명되지 않으나(27.5/26.6/26.7/26.3%), **계약형태와 교차**하면 44.4%~1.9%로 갈림.
저소득 × 월단위 계약 구간은 **46.75%** (기저 26.54%의 약 2배).
산출물을 리더보드 점수가 아닌 **"승인 가능한 리스크 3개 + 액션 3개"**로 정의 → 연 **≈$30K** 방어.
LightGBM ROC-AUC **0.8356**.

#### [saez-vs-ai-economist](https://github.com/PJH720/saez-vs-ai-economist) — 재현 연구
"The AI Economist가 Saez 대비 16% 우수"라는 주장이 **무엇에 의존하는지**를
저자들의 원본 코드로 검증. 가정을 분리한 **실험 5건**을 직접 설계·실행.

#### [VoiceVault](https://github.com/PJH720/VoiceVault) — 로컬 음성 지식 비서
로컬 **Whisper STT** 기반 프라이버시 보존형 파이프라인 (녹음→전사→요약→RAG 검색→Obsidian 내보내기).
전사 정확도보다 **"사용자가 지금 무엇을 보고 있는지 모른다"**는 점이 더 큰 병목이었고,
이것이 XR에 관심을 갖게 된 출발점.

#### [on-prem-rag-service](https://github.com/PJH720/on-prem-rag-service) — 온프레미스 RAG
외부 API 없이 사내망에서 동작. **문서 단위 RBAC** 설계 및 E2E 검증. 테스트 7/7 통과.

#### [krx-vol-drag-screener](https://github.com/PJH720/krx-vol-drag-screener) — 변동성 드래그 스크리너
이토 보정항(½σ²) 기반 국내 상장주 횡단면 스크리너. GitHub Actions CI.

#### [dolmen-maritime-risk-analysis](https://github.com/PJH720/dolmen-maritime-risk-analysis) — 공간통계
전남 고인돌 밀집과 고대 항해 위험도의 공간통계 분석. 경제학 × 역사학 복수전공 관점.

---

### 비공개 / 수업 산출물

**해양 폐기물 정책 인과분석** (2인 팀, 2025-2학기) — 지상 조사가 불가능한 과테말라 모타구아강 유역을
대상으로, Sentinel-2 위성영상 + MARIDA 라벨을 결합해 `Debris Ratio` 지표를 직접 설계.
구름 14.02% · 해양쓰레기 0.41%라는 관측 불균형을 지표 재정의로 처리하고,
유사 유역을 대조군으로 두어 정책 이전 추세의 평행성을 확인한 뒤 이중차분(DID) 적용.
지상 데이터 없이 위성만으로 정책 전후를 비교하는 분석 틀을 완성.

---

### 기술

**인과추론·계량** DID · 평행추세 확인 · 패널 데이터 설계 · 공간데이터(GeoPandas) · 시계열 파운데이션 모델(Chronos, TimesFM)
**LLM/에이전트** LangChain · LangGraph · RAG(Hybrid Search, Reranking) · 로컬 LLM · Whisper
**언어·도구** Python · SQL · TypeScript · Git · Docker

**자격** NVIDIA DLI *Building LLM Applications with Prompt Engineering* (2025.08) ·
K-Digital Training AI 부트캠프 840시간 수료 (2026.06) · JLPT N1
