# Relation Classification via Convolutional Deep Neural Network [[pdf]](http://www.aclweb.org/anthology/C14-1220)
* Author
	* Daojian Zeng (Chinese Academy of Sciences)
	* Kang Liu (Chinese Academy of Sciences)
	* Siwei Lai (Chinese Academy of Sciences)
	* Guangyou Zhou (Chinese Academy of Sciences)
	* Jun Zhao (Chinese Academy of Sciences)
* Title of Conference(Journal)
	* COLING 2014


## Abstract
* 이 분야의 state of the art는 확률적 머신러닝 기법이고 이는 feature 추출의 질이 성능을 좌지우지함
* Deep CNN을 사용하여 lexical & sentence level feature를 추출하려고 함
* 우리는 복잡한 전처리가 필요하지 않음
* 먼저 word embedding lookup table을 통해 word 토큰을 벡터로 변환함
* lexical level feature는 주어진 명사들(nouns)에 따라 추출됨
* sentence lebel feature는 CNN 학습과정 중에 추출됨
* 이렇게 추출한 두 feature를 softmax classifier를 통해서 마킹한 두 명사(entity) 간의 관계를 예측함
* state of the art보다 상당히 성능이 좋음


## Introduction
* 대부분 supervised learning을 함
* supervised learning은 크게 feature-based method와 kernel-based method가 있음
* feature-based method는 bag-of-words model 같은 거고 kernel-based method는 dependency parse tree 같은 거임
* 이런 방법은 효과적이지만 이런 모델 자체의 영향력이 너무 크고 보통 이런 feature나 kernel은 기존에 존재하는 NLP system에 의해 유도됨 -> 외부 NLP system에 의존적이다는 의미인듯
* 우리는 Deep CNN을 사용할 것임


## Related Work
* skip...

