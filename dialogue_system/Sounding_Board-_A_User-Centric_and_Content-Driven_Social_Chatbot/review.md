#  

- Author
  - Tom Bocklisch, Joey Faulkner, Nick Pawlowski, and Alan Nichol
  - Rasa
- Title of Conference(Journal)
  - arXiv 2017
  - NIPS 2017 Conversational AI Workshop

- Key Points and My Comments
  - 역시 Task-oriented System
  - 논문이라기보단 System Description 느낌
  - 얘네가 추구하는 건 아주 높은 퀄리티보단 누구나 쉽고 편하게 쓸 수 있는 거 같음
  - 따라서 구조나 모듈이 심플하고 나이브함
  - 데이터의 포맷만 잘 맞춰서 준비하면 사용할 수 있음
  - Rasa NLU는 크게 NER과 Intent, 이 결과로 structured data를 얻음 (no vector representation)
    - NER, Intent 둘 다 사용자에 의한 도메인 커스터마이징 가능, 이 경우 해당 모듈을 새로 학습
      - 택시 챗봇을 만들 때, "booking_taxi" 같은 intent를 정의할 수 있음
  - Dialogue Handling(DM)을 옛날처럼 state machine 기반으로 하는 건 더이상 ㄴㄴ. 넘나 복잡함
    - 강화학습(RL)을 하기엔 데이터도 많이 필요하고 policy 정의가 힘듬. 비전문가도 쉽고 편하게 쓰기 위해선 더욱 심플한 구조가 필요
    - state는 다른 Task-oriented 챗봇처럼 slot-value 형태
    - action은 slots, previous utternaces, results of previous action을 기반으로 모델이 결정
    - action은 다시 state에 영향을 줌. action은 "SlotSet", "AllSlotsReset", "Restarted" 등의 "list of event" 형태로 주어짐
  - NLG는 잘 설명이 안되어있는데, 다른 Rasa 자료를 찾아보면 DM(Rasa Core)로부터 structured data를 받고 이를 unstructured text data로 변환하는 작업을 함
    - 기본적으로 Rasa는 built-in templated based NLG로 되어있고, 이 역시 external HTTP server를 붙여서 외부 NLG를 사용한 커스터마이징이 가능