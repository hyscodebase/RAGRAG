# Week 02 Notes

## Summary

- Vector Database는 단순 ANN 검색기보다 넓은 개념이며 저장, CRUD, 메타데이터 필터링, 질의 인터페이스를 함께 다룸
- RAG 품질은 임베딩만이 아니라 어떤 인덱스를 쓰고 어떤 방식으로 질의하는지에도 크게 좌우됨
- Indexing은 검색 속도를 위한 사전 준비 단계이고, Querying은 질문에 맞는 후보를 실제로 찾는 단계임
- Dense Search만으로 부족한 경우 Sparse Search와 Hybrid Search가 큰 도움이 됨
- Vector DB 선택은 성능만이 아니라 운영 방식, 필터링, 하이브리드 지원, 관리 편의성까지 같이 봐야 함

## Key Concepts

- Vector Index:
- Vector Database:
- ANN:
- IVF:
- HNSW:
- Quantization:
- Sparse Search:
- Dense Search:
- Hybrid Search:
- Metadata Filter:

## Questions

- 현재 내가 만들려는 RAG는 Dense Search만으로 충분한가
- 문서 수가 커졌을 때 어떤 인덱스가 더 유리할까
- 정확도와 지연 시간 중 무엇을 우선해야 하는가
- 메타데이터 필터링이 꼭 필요한 데이터인가
- Pinecone 같은 managed 서비스와 self-hosted DB 중 어느 쪽이 더 맞는가

## Next Action

- `practice/week02.ipynb`를 읽고 인덱싱과 질의 흐름을 정리
- `practice/mit_lab.ipynb`로 MIT 문서를 직접 임베딩하고 검색 실습 진행
- `practice/chunking_rag.ipynb`와 연결해서 청킹 결과가 검색 단계에 어떤 영향을 주는지 생각
- 3주차에서 실제 임베딩과 벡터 저장소를 붙여 similarity search 실습 진행
