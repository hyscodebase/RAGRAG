# Week 03 Embeddings And Vector Store

## Goal

문서를 임베딩으로 바꾸고 벡터 저장소에 넣어 baseline retrieval을 만든 뒤, 검색 품질을 높이는 고급 RAG 방식을 가볍게 비교합니다.

## Focus

- 임베딩 모델 선택과 chunk-to-vector 흐름 이해
- vector store 적재와 similarity search baseline 만들기
- metadata filtering으로 검색 범위 제어하기
- hybrid retrieval로 keyword match와 semantic match를 함께 쓰기
- query rewrite, multi-query, reranking의 역할 차이 이해
- recall, precision, latency 관점에서 각 기법의 tradeoff 정리

## Suggested Order

1. 기본 dense retrieval을 먼저 만들기
2. top-k 결과를 보고 실패 유형 기록하기
3. metadata filter 또는 hybrid retrieval 하나 붙여 보기
4. query rewrite 또는 multi-query로 recall 변화 확인하기
5. reranker를 마지막 단계에 붙여 순위 변화 비교하기

## Suggested Practice

- 임베딩 모델 하나 선택
- 문서 몇 개를 벡터화
- 간단한 similarity search 실행
- 같은 질의에 대해 filter, hybrid, rewrite, rerank를 순서대로 비교
- 어떤 기법이 어떤 실패를 줄였는지 `notes.md`에 기록

## Files

- `notes.md`

## Note

이번 주차는 고급 기법 이름을 많이 외우는 것보다, 검색 실패를 어떤 방식으로 줄일 수 있는지 감을 잡는 데 집중합니다.
