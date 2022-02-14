---
layout: post
title: 데이콘 구내식당 식수 예측 AI 경진대회
date: 2021-06-03
image: /assets/images/post3/gunae.png
author: yelim
---

<p>&nbsp;</p>
<p>&nbsp;</p>
<div><span style="font-size: 20pt;"><strong><span style="color: #3598db;">Summary</span></strong></span>
<p>&nbsp;</p>
<p style="padding-left: 40px;"><span><strong>Subject</strong> : 구내식당의 요일별 점심, 저녁 식수 예측</span></p>
<p style="padding-left: 40px;"><span><strong>Evaluation</strong> : MAE</span></p>
<p style="padding-left: 40px;"><span><strong>Tool</strong> : Python</span></p>
<p style="padding-left: 40px;"><span><strong>ML</strong> : XGBoost, LGBM Regressor</span></p>
<p style="padding-left: 40px;"><span><strong>Data</strong> : 1822 lines with 11 columns + Weather of Jinju</span></p>
</div>
<p>&nbsp;</p>
<p>&nbsp;</p>
<div><span style="font-size: 20pt;"><strong><span style="color: #3598db;">Ideas</span></strong></span>
<p>&nbsp;</p>
<p style="padding-left: 40px;">
    <span>
        1. 주어진 데이터의 변수만으로는 예측 점수가 낮게 나왔다. 구내식당에서 식사를 하지 않는다는 것은 퇴근, 외근의 가능성은 제외하고 외식을 했다고 생각했다. 일반적으로 생각했을 때 비가 오는 날이나 폭염, 강추위 등으로 외식을 하기 힘들 때에는 구내 식당에서 식사를 할 확률이 더 높을 것이라고 판단해 날씨 변수도 추가했다.  
    </span>
</p>

<p style="padding-left: 40px;">
    <span>
        2. XGBoost와 LGBM Regressor를 점심, 저녁에 각각 훈련시키려고 했으나 점수가 잘 나오지 않아 앙상블을 시도해봤더니 점수가 오르는 것을 확인할 수 있었다.  
    </span>
</p>

</div>
<p>&nbsp;</p>
<p>&nbsp;</p>
<p style="text-align:center"><span style="font-size: 20pt;"><strong><span style="color: #3598db;">Result</span></strong></span></p>
<p style="text-align:center;"><img src="/assets/images/post3/gunae_score.png" alt="result" style="width:90%;" /></p>
<p>&nbsp;</p>
<p>&nbsp;</p>
<p><span style="color: #3598db; font-size: 20pt;"><strong>Codes</strong></span></p>
<iframe src='https://nbviewer.org/github/HappySoapy/happysoapy.github.io/blob/main/_posts/post3/gunae_pred.ipynb' width='100%' height='1200px'>