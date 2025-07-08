# 🤖 Automation Lab: MCP 기반 자동화 어시스턴트 실험실

> 문헌정보학 기반 커뮤니티를 위한 AI 어시스턴트 실험 프로젝트  
> Gemini API + Python + Prompt Engineering + Firebase 구조 기반

---

## 🎯 Lab 목표

- 정보 요청을 자동 처리할 수 있는 **LLM 기반 자동화 어시스턴트(MCP 구조)** 설계
- **명령 분류 → 의도 해석 → 응답 생성** 흐름을 모듈화하고, Gemini API를 통해 실험 수행
- 향후 Yeobaek HUB 시스템에 통합 가능한 **기능 단위 실험 모듈** 확보

---

## 🧪 실험 구조

```plaintext
[사용자 입력]
      ↓
[명령 분류]
      ↓
[의도 분해] → [프롬프트 생성]
      ↓             ↓
 [문맥 구성 (MCP)] → [LLM 호출 (Gemini)]
      ↓
[응답 생성 및 출력]
```

---

## 🧱 실험 흐름 요약

| 단계 | 설명 | 주요 파일 |
|------|------|-----------|
| 1단계 | 명령 유형 분류 | `scripts/classifier.py` |
| 2단계 | 의미 기반 의도 분석 | `scripts/intent_parser.py` |
| 3단계 | 프롬프트 생성기 설계 | `scripts/prompt_generator.py` |
| 4단계 | Gemini API 연동 실험 | `scripts/gemini_runner.py` |
| 5단계 | 전체 흐름 통합 및 데모 | `app/main.py`, `demo.ipynb` |

---
## 🗂️ 폴더 구조

```
automation-lab/
├── prompts/               # 설계한 프롬프트 구조
│   ├── type_a_study.md
│   └── type_b_library.md
├── scripts/               # 실험 스크립트 (Python)
│   ├── classifier.py
│   ├── intent_parser.py
│   ├── prompt_generator.py
│   └── gemini_runner.py
├── app/                   # 전체 흐름 통합용 코드
│   └── main.py
├── docs/                  # 실험 흐름도 및 설명 자료
│   └── flowchart.drawio
├── results/               # 실험 결과 정리
│   ├── log_1.json
│   └── summary.md
├── experiment/            # 실험 내용 
├── demo.ipynb             # 실험 시나리오 통합 노트북
├── README.md              # 이 파일
└── requirements.txt       # 실행 환경
```

---
## ⚙️ 기술 스택

- **LLM 연동**: Gemini API (via Python)
- **프롬프트 설계**: 역할 기반 시스템 프롬프트 구조
- **백엔드 자동화**: Firebase Functions (예정)
- **시각화**: draw.io (실험 흐름도)
- **버전 관리 및 협업**: Git + GitHub PR 리뷰 기반

## 🧑‍💻 참여 인원 및 역할

| 이름 | 역할 | 주요 기여 |
|------|------|-----------|
| - | Front / Prompt | 프롬프트 구조 설계, Gemini 연동 실험 |
| - | Back | Firebase 연동 로직, 응답 후처리 설계 |
| - | Design | 인터페이스 기획 및 시나리오 문서화 |
| - | Data | 질의 유형 수집, 분류 스크립트 제작 |

---

## 📝 향후 발전 방향

- Firebase Functions 연계 자동 응답 시스템 구현
- 도서관 API 및 KDC 기반 추천 로직 연동
- 각 명령어 유형에 대한 성능 비교 및 테스트
- HUB 플랫폼 내 모듈로 통합하여 전체 시스템 구축

---

## 🔗 관련 링크

- [Gemini API 가이드](https://ai.google.dev/)
- [Arxiv: Prompt Engineering 논문](https://arxiv.org/abs/2107.13586)

---

> 여백 프로젝트의 실험은 ‘학문과 기술의 중간 지점’에서  
> 실질적인 문제 해결을 목표로 합니다.  
> 그 실마리를 이곳, Automation Lab에서 시작합니다.
