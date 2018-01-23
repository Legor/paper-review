# Relation Extraction: Perspective from Convolutional Neural Networks [[pdf]](http://www.cs.nyu.edu/~thien/pubs/vector15.pdf)
* Author
	* Thien Huu Nguyen (New York University)
	* Ralph Grishman (New York University)
* Title of Conference(Journal)
	* NAACL 2015


## Abstract
* In relation extraction, tranditional approach with complicated feature engineering has errors and it lead to errors of relation detection and classification.
<br>➤ 관계추출에서 전통적인 방법은 복잡한 feature engineering을 하기에 에러가 많고 때문에 detection과 classification에서 많은 문제를 야기한다.
* Advantage of our model: multiple window sizes for filters.
<br>➤ 필터의 윈도우 사이즈를 여러가지로 할 수 있다.
* using pre-trained word embeddings as initializer.
<br>➤ pre-trained 된 워드 임베딩 모델을 사용하고 있다.


## 1. Introduction
* Relation Extaction task can be divided into two steps:
	1. Detecting
	2. Classifying
<br>➤ 관계추출 문제는 관계를 찾아내는 단계와 이를 분류하는 단계, 두 가지로 나눌 수 있다.
* Difference between Relation Classification and Relation Extraction ➤ RC와 RE의 차이점
	* In classification, non-relation examples in the dataset are comparable to the other examples, so they can be treated as a usual relation class like 'Other' class.(balanced)
	<br>➤ RC에서는 non-relation인 데이터의 양이 relation인 데이터 양과 비슷하다.(balanced) 그래서 보통의 클래스처럼 이를 다룰 수 있다.
	* In Extraction, non-relation examples far exceeds the others.(unbalanced) So more challenging but more practical than relation classification.
	<br>➤ RE에서는 non-relation인 데이터의 양이 매우 많다.(unbalanced) 그래서 더 어렵고 쓸모가 있다.
* In the last decade, the relation extraction has been dominated by two methods, the feature-based method and kernel-based method.
<br>➤ 지금까지 relation extraction의 해법으로 feature-based와 kernel-based 두 가지 방법이 지배적이었다.
* The common characteristic of these methods is the leverage of a large body of linguistic analysis and knowledge resourses to transform relation mentions into some rich representation to be used by some statistical classifier such as SVM, MaxEnt.
<br>➤ 두 방법의 공통적인 특징은 relation mention을 통계적 분류기(SVM, MaxEnt)에서 사용할 수 있는 풍부한 표현으로 변환하기 위해서 *언어 분석 및 지식 자원의 많은 부분을 활용*한다는 것이다.
* So these models depend on a supervised NLP toolkit and suffer from a performance loss when they are applied to out-of-domain data.
<br>➤ 그래서 이 모델들은 학습된 NLP toolkit에 의존적이고 out-of-domain 데이터에 대해서 퍼포먼스 소실이 있다.
* We target an independent RE system that both avoids complicated feature engineering and minimizes the reliance on the supervised NLP modules.
<br>➤ 우리는 복잡한 feature engineering과 NLP module의 의존성을 최소화한 독립적인 RE 시스템을 목표로 하였다.
* there are two recent works on CNNs for relation classification (Liu et al., 2013) and (Zeng et al., 2014); however work on CNNs for relation extraction is not yet.
<br>➤ CNN을 통한 RC에 대해서는 최근 Liu와 Zeng의 연구가 발표된 바 있지만, RE는 아직 발표된 게 없다.


## 2. Related Work
* ...


## 3. Convolutional Neural Network for Relation Extraction
* ...











