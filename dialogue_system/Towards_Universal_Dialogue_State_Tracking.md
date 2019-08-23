# Towards Universal Dialogue State Tracking


## Abstract

* Dialogue State Tracking란 Dialogue System에 있어서 매우 중요한 파트로서, **매 대화 턴 별로 유저의 목표(goal)에 대한 가능성을 예측하는 문제**임
* 하지만 대부분의 최근 어프로치들은 넓은 범위의 대화 도메인으로 인해 아래의 한계 및 어려움이 있음
  * Ontology의 슬롯 값이 동적으로 변하는 환경에서 잘 작동하지 않음
  * 슬롯의 개수에 비례해서 모델 파라미터 크기가 커짐
  * Hand-crafted Lexicon Feature를 기반으로 함
* 이런 문제들을 해결하기위해, **우리는 Universal Dialogue State Tracker인 StateNet을 제안**함
* StateNet은 특징 및 Contribution은 다음과 같음
  * 모든 슬롯에 대해 파라미터를 공유하기 때문에 슬롯의 개수에 대해 모델 크기가 독립적임
  * Lexicon Feature (explicit semantic dictionaries) 대신에 Pre-trained Word Vector를 사용함
  *  Dialogue State Tracking 분야의 대표적인 데이터셋인 DSTC2와 WOZ에 대해서 state-of-the-art 성능을 보임
  * 또한 실험 결과를 통해 위에 언급한 한계점들을 극복했다는 것을 보여줌



## 1. Introduction

