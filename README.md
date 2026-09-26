<div align="center">

## 박재현 · Jaehyun Park

**경제학·역사학 × AI 시스템** — 서강대학교 경제학·역사학 · AI 서비스 기획 / 데이터 분석

[![Email](https://img.shields.io/badge/jhp3822n@sogang.ac.kr-Email-B6002B?style=flat-square&logo=maildotru&logoColor=white)](mailto:jhp3822n@sogang.ac.kr)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=flat-square&logo=langchain&logoColor=white)
![Hugging Face](https://img.shields.io/badge/Hugging_Face-FFD21E?style=flat-square&logo=huggingface&logoColor=black)

</div>

> 모호한 질문을 측정 가능한 형태로 바꾸고, 그 답을 직접 구현해 확인합니다.
> 경제학의 인과추론 방법론과 LLM 에이전트 구현을 함께 씁니다.

### 일하는 방식

- **숫자는 코드가 계산하고, LLM은 설명만 합니다.** 근거가 부족하면 답하지 않는 게이트를 먼저 설계합니다. → `3EYEXAI` · `on-prem-rag-service`
- **남들이 버리는 변수를 다시 봅니다.** 원-핫 대상이던 우편번호를 소득 데이터 결합 키로 바꿨습니다. → `churn-guard`
- **가설이 틀려도 그대로 기록합니다.** 비유의·반대 방향 결과도 결론으로 남깁니다. → `EnvEcon_MarineDebris_DID_2025` · `dolmen-maritime-risk-analysis` · `saez-vs-ai-economist`

---

### 📌 대표 프로젝트

<table>
<tr>
<td width="50%" valign="top">

#### [Churn Guard](https://github.com/PJH720/churn-guard)
<sub>고객 이탈 예측·리텐션 전략 · AI@Sogang 2기 3인 팀 **PM** · Demo Day 현직자 심사</sub>

모두가 버리는 `Zip Code`(고유값 1,652개)를 **미국 인구통계국 ACS 소득 데이터 결합 키**로 재해석.
- 결합률 **99.94%** · 소득 대비 통신비 부담률 이탈군 1.08% vs 유지군 0.87% (**t=11.72**)
- 소득만으로는 이탈률이 평평(27.5/26.6/26.7/26.3%)하지만 **약정 형태와 교차**하면 저소득 × 무약정 **44.4%** vs 저소득 × 2년 약정 **1.9%**
- 리텐션 액션 3종 + 손익 추정: 방어율 50% 가정 시 연 **$27K~30K**

`LightGBM` `SHAP` `pandas` `ACS Census`

</td>
<td width="50%" valign="top">

#### [TSFM-Portfolio_Optimizer](https://github.com/PJH720/TSFM-Portfolio_Optimizer)
<sub>시계열 파운데이션 모델 기반 동적 포트폴리오 · 단독 · 패스트캠퍼스 Hugging Face 미니 프로젝트</sub>

**Chronos-2**(거시 공변량 11개) + **TimesFM 1.0** 제로샷 앙상블로 기대수익률 μ를 예측하고,
**Markowitz QP**(`cvxpy`, 섹터 ≤30% · 종목 ≤25% · 롱온리)로 가중치를 산출해 **Gradio** 대시보드로 제공.
- Kaggle S&P 500 + yfinance + FRED 자동 데이터 파이프라인
- Walk-forward 백테스트(10종목, 12회 리밸런싱): **Sharpe 1.598** vs 균등가중 0.164

`Chronos-2` `TimesFM` `cvxpy` `Gradio`

</td>
</tr>
<tr>
<td width="50%" valign="top">

#### [on-prem-rag-service](https://github.com/PJH720/on-prem-rag-service)
<sub>사내 온보딩 RAG 챗봇 · 2026 AX 실무 해커톤 제출물 · [라이브 데모](https://on-prem-rag-service.vercel.app)</sub>

기본 추론은 **사내 GPU 서버(sglang)**, 외부 API는 사용자가 키를 넣을 때만 쓰는 선택 옵션 — 애플리케이션 코드는 동일.
- **문서 단위 RBAC 사전 필터**: 비인가 문서는 검색 후보에 아예 적재되지 않음
- 근거 점수 미달 시 LLM 호출 전에 거부하는 **grounding gate**, 권한 위장 쿼리 정제
- 검색·RBAC 테스트 **26/26 통과**

`Next.js` `LangChain.js (LCEL)` `BM25` `sglang`

</td>
<td width="50%" valign="top">

#### [saez-vs-ai-economist](https://github.com/PJH720/saez-vs-ai-economist)
<sub>논문 주장 검증 · AI@Sogang 강화학습 스터디 발표 (2026-08-13)</sub>

"The AI Economist가 Saez 대비 16% 우수"라는 주장이 **무엇에 의존하는지**를
저자들의 원본 코드(`salesforce/ai-economist`, 무수정)로 검증. 16% 재현이 아니라 가정을 분리한 **실험 5건**을 설계·실행.
- 같은 4개 정책을 사회후생함수 7개로 다시 채점하면 **승자가 3번 바뀜**
- 평균 소득이 같아도 분포 모양만 바꾸면 Saez 세율이 역진적 ↔ 누진적으로 뒤집힘

`Python` `optimal taxation` `welfare economics`

</td>
</tr>
<tr>
<td width="50%" valign="top">

#### [EnvEcon_MarineDebris_DID_2025](https://github.com/PJH720/EnvEcon_MarineDebris_DID_2025)
<sub>해양 쓰레기 정책 효과 분석 · 환경경제학(ECO3005) 2025-2 · 2인 팀 제1저자</sub>

과테말라 Motagua 강 유역의 플라스틱 차단 정책(2019-10-31)을 **Sentinel-2 위성영상 + MARIDA**로 학습한 U-Net의 해양 잔해 비율로 평가, 이중차분(DID) 적용 (2016-07 ~ 2020-12, N=359).
- β₃ = −0.095, p = 0.64 — **통계적으로 유의하지 않음**
- 정책 후 대조군 관측이 2건뿐인 식별 한계를 명시하고, 이벤트 스터디·고정효과 설계를 후속 과제로 제시

`Sentinel-2` `U-Net` `DID` `STATA`

</td>
<td width="50%" valign="top">

#### [dolmen-maritime-risk-analysis](https://github.com/PJH720/dolmen-maritime-risk-analysis)
<sub>공간통계 · 경제학 × 역사학 복수전공 관점</sub>

"고인돌이 무덤이라면, 거친 바다에 면한 해안일수록 많을 것"이라는 **반증 가능한 가설**을 영산강 유역 공간 데이터로 검정.
- 예측과 **반대 방향**: 가장 거친 바다 인접 셀에는 고인돌의 6.9%뿐
- 파고와 **역U자 관계** — 중간 두 분위에 **87.7%** 집중 (정점 0.684 m)

`GeoPandas` `spatial regression`

</td>
</tr>
<tr>
<td width="50%" valign="top">

#### [krx-vol-drag-screener](https://github.com/PJH720/krx-vol-drag-screener)
<sub>변동성 드래그 스크리너 · GitHub Actions CI</sub>

이토 보정항 ½σ²로 **산술 기대수익률 μ와 실제 복리 성장률 g의 괴리**를 KOSPI·KOSDAQ 전 종목 횡단면으로 순위화.
- 필터 통과 1,106종목 중 **20.7%**가 μ > 0 이지만 g < 0 — 기대수익률은 양수인데 원금이 줄어든 상태

`Python` `Itô calculus` `CI`

</td>
<td width="50%" valign="top">

#### [VoiceVault](https://github.com/PJH720/VoiceVault)
<sub>로컬 음성 지식 비서 · 오픈소스 데스크톱 앱</sub>

온디바이스 **Whisper** 전사 → 로컬 LLM 요약·자동 분류 → **Obsidian** 마크다운 내보내기. 클라우드·계정 없이 동작
(RAG 검색은 Electrobun 런타임 전환 후 재구현 중).
전사 정확도보다 **"사용자가 지금 무엇을 보고 있는지 모른다"**는 점이 더 큰 병목이었고, 이것이 XR에 관심을 갖게 된 출발점.

`whisper.cpp` `llama.cpp` `Bun` `TypeScript`

</td>
</tr>
</table>

---

### 🔒 비공개 작업

**3EYEXAI** — 투자 리서치를 위한 Computation-First Glass Box XAI `v0.1.0-mvp`

블랙박스형 AI 주식 해설을 **감사 가능한 리서치 리포트**로 바꿉니다. 원칙은 하나 — *AI는 숫자를 계산하거나, 만들어내거나, 반올림하거나, 매매를 권하지 않는다.*

```
OHLCV 데이터 → Freshness 게이트 → 결정론적 Python 계산 → Evidence Ledger(content-addressed JSON 스냅샷)
            → LLM은 ledger 토큰만 번역 → Numeric Fidelity · Wording Safety · Traceability 게이트 → React UI
```

- 모든 수치·주장이 ledger JSON 경로로 역추적되며, 스냅샷 변조 시 digest 검증 실패
- 선택적 LangGraph 어댑터, 외부 데이터 장애 시 결정론적 샘플로 폴백
- GitHub CI 통과 (Python 3.11 · 3.12) — 코드는 비공개, 요청 시 데모 가능

---

### 🛠 기술

**인과추론·계량** DID · 공간데이터(GeoPandas) · 최적화(cvxpy, Markowitz QP) · 시계열 파운데이션 모델(Chronos, TimesFM)
**LLM/에이전트** LangChain · LangChain.js(LCEL) · LangGraph · RAG(Hybrid Search, Reranking) · 로컬 LLM(sglang, llama.cpp) · Whisper
**언어·도구** Python · SQL · TypeScript · Git · Docker

<sub>**자격** NVIDIA DLI *Building LLM Applications with Prompt Engineering* (2025.08) · K-Digital Training AI 부트캠프 840시간 수료 (2026.06) · JLPT N1</sub>
