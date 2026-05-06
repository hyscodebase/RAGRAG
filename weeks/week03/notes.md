# Week 03 Notes

## Summary

- 고급 RAG는 모델 자체를 바꾸는 일보다 retrieval 실패 원인을 나누고 그에 맞는 검색 전략을 붙이는 일에 가깝다
- baseline dense retrieval이 먼저 있어야 query rewrite, hybrid retrieval, reranking의 효과를 제대로 비교할 수 있다
- query transform 계열은 recall을 높이는 데 유리하고, reranking은 precision을 높이는 데 유리하다
- metadata filtering과 구조적 retrieval은 관련 없는 후보를 초기에 줄여 검색 안정성을 높인다
- 모든 고급 방식은 정확도만이 아니라 latency, cost, 운영 복잡도까지 같이 봐야 한다

## Key Concepts

- Baseline Dense Retrieval: 임베딩 유사도만으로 top-k 문서를 찾는 가장 단순한 검색 흐름
- Metadata Filter: 권한, 날짜, 문서 유형 같은 조건으로 검색 대상을 제한하는 방식
- Hybrid Retrieval: sparse search와 dense search를 함께 써서 키워드 일치와 의미 일치를 동시에 잡는 방식
- Query Rewrite: 사용자 질문을 검색 친화적인 표현으로 다시 쓰는 방식
- Multi-Query Retrieval: 하나의 질문에서 여러 질의를 만들어 검색 recall을 높이는 방식
- HyDE: 가상의 답변 문서를 먼저 만든 뒤 그 문서를 검색용 표현으로 활용하는 방식
- Parent-Child Retrieval: 작은 청크로 찾고, 실제로는 더 큰 상위 문맥을 가져오는 방식
- Reranking: 1차 검색 후보를 더 정교한 모델이나 점수 기준으로 다시 정렬하는 단계
- Context Compression: 검색된 문맥 중 필요한 부분만 압축해 LLM에 전달하는 방식

## What To Study

- dense retrieval만으로 놓치는 질문 유형이 무엇인지 확인
- exact keyword가 중요한 문서에서는 hybrid retrieval이 왜 유리한지 이해
- 질문 표현이 애매할 때 query rewrite나 multi-query가 어떤 도움을 주는지 비교
- top-k 후보는 맞는데 순서가 아쉬운 경우 reranking이 왜 필요한지 파악
- 작은 청크와 큰 문맥 사이 균형을 맞추는 parent-child retrieval 감각 익히기

## Questions

- 현재 데이터에서는 recall 부족이 더 큰가, precision 부족이 더 큰가
- retrieval 실패 원인이 청킹인지 임베딩인지 질의 표현인지 구분할 수 있는가
- 메타데이터 필터가 없으면 노이즈가 크게 늘어나는 데이터인가
- reranker를 붙일 만큼 1차 검색 후보 품질이 충분한가
- 응답 속도 예산 안에서 몇 단계까지 검색을 추가할 수 있는가

## Next Action

- 기본 similarity search 결과를 먼저 저장
- metadata filter, hybrid retrieval, multi-query 중 1~2개만 골라 전후 비교
- reranking 적용 전후 top-k 순위 변화를 기록
- 4주차 파이프라인 구성 때 실제로 유지할 기법만 추려 반영
