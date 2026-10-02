# RAG Study Workspace

검색 기초에서 LangChain·벡터 검색·고급 RAG까지 이어지는 주차별 학습 작업 공간입니다. 노트북, 개념 노트, 예제 자료를 함께 관리합니다.

## 학습 지도

| 주차 | 자료 | 내용 |
|---|---|---|
| 1 | [week01](weeks/week01/README.md) | RAG 기초와 코사인 유사도 |
| 2 | [week02](weeks/week02/README.md) | 청킹, 벡터 DB 기초, LangChain 입문, MIT.pdf 검색 실습 |
| 3 | [week03](weeks/week03/README.md) | RAPTOR·Corrective·Modular RAG 예제 |
| 4~8 | `weeks/week04/` ~ `weeks/week08/` | 후속 학습용 폴더와 안내; 실습은 아직 빈 공간 |

전체 계획은 [학습 로드맵](docs/study-roadmap.md), 진행 상황은 [진행 기록](docs/progress-tracker.md)에서 확인합니다.

## 실행

노트북별 환경을 확인하고 필요한 패키지를 설치하세요. [requirements.txt](requirements.txt)는 기존 환경의 패키지 목록이며, 모든 노트북의 호환성을 보장하는 최소 의존성 파일은 아닙니다.

```bash
python3 -m venv .venv
source .venv/bin/activate
python -m pip install jupyterlab
jupyter lab
```

처음에는 `weeks/week01/practice/`의 기초 노트북, 이후 `weeks/week02/practice/langchain_basics_ko.ipynb` 순서로 읽습니다. LangChain 입문에는 외부 모델 호출 없이 공부하는 예제도 있습니다.

## 고급 실습 준비

3주차 예제는 LangChain·LangGraph·LlamaIndex와 외부 모델·검색 API를 사용합니다. OpenAI 또는 Tavily를 사용하는 셀은 해당 키와 인터넷 연결이 필요합니다. 원문 PDF 위치와 모델 설정을 확인한 뒤 실행하세요.

일부 3주차 노트북은 이전 import 경로와 작성자의 로컬 데이터 경로를 포함합니다. 최신 입문 노트북과 동일한 패키지 조합으로 모두 실행된다고 가정하지 마세요. 모델을 다운로드하는 MIT 검색 실습은 다운로드가 필요한 경우 인터넷 연결이 필요합니다.

## 자료 관리

각 주차의 `practice/`에는 실행 노트북, `data/`에는 입력 자료, `notes.md`에는 학습 정리를 둡니다. `resources/`는 공용 자료, `docs/`는 로드맵·진행 기록입니다. API 키는 환경변수로 관리하고 노트북·출력 파일에 남기지 않습니다.
