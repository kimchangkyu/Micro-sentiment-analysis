# Micro-sentiment-analysis

- CountVectorizer, TfidfVectorizer, N그램  등 다양한 인코딩 방법을 활용한 관객 평점 감성 분석 프로젝트

1. 인코딩 방법
  - CountVectorizer : 문서 집합에서 단어 토큰을 생성하고 각 단어의 수를 세어 BOW 인코딩 벡터를 만든다.
    - 1. 문서를 토큰 리스트로 변환한다.
    - 2. 각 문서에서 토큰의 출현 빈도를 센다.
    - 3. 각 문서를 BOW 인코딩 벡터로 변환한다.
  - TfidfVectorizer
    - TF-IDF(Term Frequency – Inverse Document Frequency) 인코딩은 단어를 갯수 그대로 카운트하지 않고 모든 문서에 공통적으로 들어있는 단어의 경우 문서 구별 능력이 떨어진다고 보아 가중치를 축소하는 방법
    - 문서  d (document)와 단어  t  에 대해 다음과 같이 계산
      - tf-idf(d,t)=tf(d,t)⋅idf(t)
      - tf(d,t) : term frequency. 특정한 단어의 빈도수
      - idf(t)  : inverse document frequency. 특정한 단어가 들어 있는 문서의 수에 반비례하는 수
  - N그램
    - N그램은 단어장 생성에 사용할 토큰의 크기를 결정
    - 모노그램(monogram)은 토큰 하나만 단어로 사용
    - 바이그램(bigram)은 두 개의 연결된 토큰을 하나의 단어로 사용
    
2. 나이브 베이즈 분류 모형
  - 다항 분류를 위해 MultinomialNB을 사용
