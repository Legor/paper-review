# FaceNet: A Unified Embedding for Face Recognition and Clustering [[pdf]](https://arxiv.org/abs/1503.03832)
* Author
	* Florian Schroff (Google)
	* Dmitry Kalenichenko (Google)
	* James Philbin (Google)
* Title of Conference(Journal)
	* CVPR 2015

	
## Abstract
* Implementing face verification and recognition efficiently at scale presents serious challenges to current approaches.
<br>➤ 크기에 맞게 효율적으로 얼굴 확인 및 인식을 구현하는 것은 현재의 접근법으로 보았을 때 상당히 도전적인 과제이다.
* In this paper, we present *FaceNet*, that directly learns a mapping from face images to a compact Euclidean space where distances directly correspond to a measure of face similarity.
<br>➤ 이 논문에서 우리는 *FaceNet*을 소개할 것이다. *FaceNet*은 유클리디안 공간에 얼굴 이미지를 매핑되는 좌표를 학습시키고, 매핑된 좌표들의 거리는 얼굴의 유사도를 의미하게 된다.
* Our method uses a deep CNN trained to directly optimize the embedding itself, rather than an intermediate bottleneck layer as in previous deep learning approaches.
<br>➤ 우리는 이전 연구처럼 중간에 bottleneck layer를 사용하기 보다 직접적으로 embedding layer를 최적화하도록 CNN을 학습시켰다.
* On the widely used *Labeled Faces in the Wild (LFW)* dataset and *YouTube Faces* DB, our system achieves a accuracy better than the previous best published result.
<br>➤ 우리의 시스템은 *LFW* dataset과 *YouTube Faces* DB에 대해서 이전 최고 기록보다 더 나은 정확도를 얻었다.


## 1. Introduction
* In this paper we present a unified system for ➤ 우리는 아래의 task를 위한 통합 시스템을 제안한다.
	1. face verification (is this the same person) <br>➤ 같은 사람인가?
	2. face recognition (who is this person) <br>➤ 이 사람은 누구인가?
	3. face clustering (find common people among these faces) <br>➤ 공통된 사람을 찾아라(묶어라)

	![facenet](https://user-images.githubusercontent.com/15166794/35256631-0fd0f62a-0038-11e8-85e4-67dd005ab981.png)

* The network(CNN) is trained such that the squared L2 distances in the embedding space directly correspond to face similarity: faces of the same person have small distances and faces of distinct people have large distances.
<br>➤ 네트워크는 embedding space에서 squared L2 distance가 얼굴 유사도에 대응하도록 학습된다. 같은 사람의 얼굴의 경우 거리가 작고 다른 사람은 큰 거리를 갖는다.

* Once this embedding has been produced, ➤ 한번 embedding이 학습되고 나면,
	1. face verification simply involves thresholding the distance between the two embeddings <br>➤ face verification은 distance에 대한 thresholding을 통해 해결할 수 있다.
	2. face recognition becomes a k-NN classification problem <br>➤ face recognition은 k-NN 분류 문제로 풀 수 있다.
	3. face clustering can be achieved using off-the-shelf techniques such as k-means or agglomerative clustering <br>➤ face clustering은 거리 k-means 같은 off-the-shelf 테크닉을 사용하여 풀 수 있다.

* Previous face recognition approaches based on deep networks take an intermediate bottleneck layer as a representation.
<br>➤ 이전에 deep networks 기반의 face recognition 연구는 representation(embeddings)로 중간에 있는 bottleneck layer를 사용했다.
* The downsides of this approach are its indirectness and its inefficiency. ➤ 이런 접근의 단점은 비직접성(간접성)과 비효율성이다.
	* one has to hope that the bottleneck representation generalizes well to new faces
	<br>➤ 새로운 얼굴에 대해서 bottleneck representation이 잘 일반화하여 판단해야 한다. (새로운 얼굴을 잘 인식하지 못 할 가능성이 크다.)
	* representation size per face is usually very large (1000s of dimensions)
	<br>➤ 얼굴에 대한 representation size가 보통 너무 크다.
	
* Incontrast, *FaceNet* directly trains its output to be a compct 128-D embedding using a triplet based loss function based on LMNN.
<br>➤ 반면, *FaceNet*은 LMNN에서의 triplet기반의 loss function을 사용하여 직접적으로 output이 128-D embedding이 되도록 학습을 시킨다.
* Our triplets consist of two matching face thumbnails and a non-matching face thumbnail and the loss aims to separate the positive pair from the negative by a distance margin.
<br>➤ triplets은 2개의 matching face와 1개의 non-matching face로 구성되고 loss는 positive pair를 negative로부터 거리 상으로 떼어내는 것을 목적으로 한다.

* Choosing which triplets to use turns out to be very important for achieving good performance and, inspired by curriculum learning, we present a novel online negative exemplar mining strategy which ensures consistently increasing difficulty of triplets as the network trains.
<br>➤ triplets을 선정하는 것이 좋은 성능을 얻는데 있어서 매우 중요하다. 우리는 curriculum learning에서 영감을 받아 네트워크 학습에 있어서 triplet의 어려움을 지속적으로 증가시키는 새로운 online negative exemplar mining strategy을 제시한다.


## 2. Related Work
* ...


## 3. Method
* 

### 3.1. Triplet Loss


### 3.2. Triplet Selection


### 3.3. Deep Convolutional Networks