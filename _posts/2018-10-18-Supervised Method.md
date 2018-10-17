---

title: Supervised Method
key: 20181017
tags: Dimensionality Reduction

---

이 post는 고려대학교 산업경영공학과 DSBA연구실의 강필성 교수님의 Business-Analytics강의를 기반으로 작성되었습니다.

오늘은 차원축소(Dimensionality Reduction)에 대한 이야기를 해보겠습니다.

여기서 "차원"이란 독립변수를 의미합니다. 아래의 예시는 일명 iris 데이터 셋으로 iris라는 꽃의 종류를 분류하기 위한 데이터입니다. 

![ë°ì´í° ììì ëí ì´ë¯¸ì§ ê²ìê²°ê³¼](http://www.dbguide.net/publishing/img/dbguide/bigdata_technology/112_bigdata_02.gif)

즉 종속변수인 Species를 설명하기 위해 총 4개의 차원[Sepal.Length, Sepal.Width, Petal.Length, Petal.Width]이 존재합니다. 

따라서 "차원축소"란 종속변수를 설명하는 독립변수의 개수를 줄이겠다는 뜻입니다.

그렇다면 우리는 왜 굳이 "차원축소"를 하려고 하는 것일까요?

당연하게도 그 이유는 model의 성능을 높이기 위함입니다. 이 말을 다시 해석해보면 차원이 너무 많으면 model의 성능이 저하된다는 것을 의미합니다. 이런 현상을 일컬어 우리는 "차원의 저주"라고 부릅니다. 아래는 차원의 수에 따른 분류기의 성능을 보여주는 그래프입니다. 보시다시피 차원이 일정 수준 이상증가하게 되면 성능이 급격하게 저하되는 것을 알 수 있습니다. 

![img](https://cdn-images-1.medium.com/max/1600/1*ZuFOzQawXnw_CUnVpRDLgA.png)

이러한 현상은 왜 발생하는 것일까요?