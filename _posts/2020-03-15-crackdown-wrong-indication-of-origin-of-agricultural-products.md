---
layout: post
title: 농산물 원산지 표시 단속 추천 서비스
date: 2020-03-15
image: /assets/images/blog/vegetables.jpg
author: yelim
---


<p>&nbsp;</p>
<p>&nbsp;</p>
<p>&nbsp;</p>
<p style="font-size:20pt; text-align:center; font-weight:bold">[Tableau Dashboard Page]</p>
<div class='tableauPlaceholder' id='viz1642704105594' style='position: relative'>
    <object class='tableauViz'  style='display:visible;'>
        <param name='host_url' value='https%3A%2F%2Fpublic.tableau.com%2F' /> 
        <param name='embed_code_version' value='3' /> 
        <param name='path' value='views&#47;CrackdownonWrongIndicationofOriginofAgriculturalProducts&#47;1?:language=ko-KR&amp;:embed=true&amp;publish=yes' /> 
        <param name='toolbar' value='yes' />
        <param name='animate_transition' value='yes' />
        <param name='display_static_image' value='yes' />
        <param name='display_spinner' value='yes' />
        <param name='display_overlay' value='yes' />
        <param name='display_count' value='yes' />
        <param name='language' value='ko-KR' />
        <param name='filter' value='publish=yes' />
    </object>
</div>                
<script type='text/javascript'>                    
    var divElement = document.getElementById('viz1642704105594');                    
    var vizElement = divElement.getElementsByTagName('object')[0];                    
        if ( divElement.offsetWidth > 800 ) { vizElement.style.minWidth='500px';vizElement.style.maxWidth='1110px';
        vizElement.style.width='100%';vizElement.style.minHeight='977px';vizElement.style.maxHeight='1177px';vizElement.style.height=(divElement.offsetWidth*0.75)+'px';} 
        else if ( divElement.offsetWidth > 500 ) { vizElement.style.width='100%';vizElement.style.height=(divElement.offsetWidth*0.75)+'px';} 
        else { vizElement.style.width='100%';vizElement.style.height='2677px';}                     
    var scriptElement = document.createElement('script');                    
    scriptElement.src = 'https://public.tableau.com/javascripts/api/viz_v1.js';                    
    vizElement.parentNode.insertBefore(scriptElement, vizElement);                
</script>


<p>&nbsp;</p>
<div class="post_head" style="margin-left: 20px; line-height: 1.5;"><span style="font-size: 36px; color: #2c82c9;"><strong>Introduce</strong></span></div>
<section class="post_info">
<p style="padding-left: 40px;"><strong><span style="font-size: 15pt;">Period of Project</span></strong><span style="font-size: 20px;">&nbsp;: 2020.03 - 2020.11</span></p>
<p style="line-height: 1; padding-left: 40px;"><span style="font-size: 15pt;"><strong>Subject</strong> : 원산지 표시 단속에서 단속될 확률이 높은 업체를 추천</span></p>
<p style="line-height: 1; padding-left: 40px;"><span style="font-size: 15pt;"><strong>Role</strong> : PM</span></p>
<p style="line-height: 1; padding-left: 40px;"><span style="font-size: 15pt;"><strong>ML</strong> : Random Forest, Ada Boost, XG Boost, Light GBM</span></p>
<p style="line-height: 1; padding-left: 40px;"><span style="font-size: 15pt;"><strong>DL</strong> : CNN, MLP, CNN_LSTM</span></p>
<p style="line-height: 1; padding-left: 40px;"><span style="font-size: 15pt;"><strong>Tools</strong> : QGIS, Python</span></p>
<p style="line-height: 1; padding-left: 40px;"><span style="font-size: 15pt;"><strong>Data :&nbsp;</strong>20 columns with 200,000 lines from 국립 농산물 품질 관리원</span></p>
<p style="line-height: 1; padding-left: 40px;">&nbsp;</p>
<p style="line-height: 1;">&nbsp;</p>
</section>
<p>&nbsp;</p>
<section>
<div class="post_head" style="line-height: 2; text-align: center;"><span style="font-size: 36px; color: #2c82c9;"><strong>Hypothesis</strong></span></div>
<p style="line-height: 1.5; text-align:center;"><span style="font-size: 15pt;">1. 여러 번 적발된 업체일 수록, 수입 물량이 많을 수록 적발될 가능성이 높을 것이다.&nbsp;</span></p>
<p style="line-height: 1.5; text-align:center;"><span style="font-size: 15pt;">2. 65세 이상 인구, 독거 노인 수, 기초 생활보장 수급권자 수, 외국인 인구가 많을 수록 적발될 가능성이 높을 것이다.&nbsp;</span></p>
<p style="line-height: 1.5; text-align:center;"><span style="font-size: 15pt;">3. 소득수준이 낮을 수록 적발될 가능성이 높을 것이다.&nbsp;</span></p>
<p style="line-height: 1.5; text-align:center;"><span style="font-size: 15pt;">4. 주변에 관공서가 많거나 모범 업체로 선정된 업체일 경우 적발될 가능성이 낮을 것이다.</span></p>

<p>&nbsp;</p>
<p>&nbsp;</p>
<p>&nbsp;</p>
<p style="text-align: center;"><strong><span style="font-size: 36px; color: #2c82c9;">Process of Analysis</span></strong></p>
<p style="text-align:center;"><img src="/assets/images/post2/process.png" alt="process" style="width:100%; border:2px solid gray; border-radius:20px" /></p>
<p>&nbsp;</p>
<p>&nbsp;</p>
<p style="padding-left: 20px;"><strong><span style="font-size: 36px; color: #2c82c9;">Summary</span></strong></p>
<p style="padding-left: 40px;"><strong><span style="font-size: 16pt; color: #843fa1;">지역추천&nbsp;</span></strong></p>
<p style="padding-left: 40px;"><span style="font-size: 15pt;">서울시를 100m*100m 그리드로 나누면 약 75000개가 추출됨.&nbsp;</span></p>
<p style="padding-left: 40px;"><span style="font-size: 15pt;">머신러닝과 딥러닝을 사용하여 단속이 될 확률이 높은 100개의 그리드를 선정.</span></p>
<p style="padding-left: 40px;"><span style="color: #843fa1; font-size: 16pt;"><strong>업체추천&nbsp;</strong></span></p>
<p style="padding-left: 40px;"><span style="font-size: 15pt;">선정된 100개의 그리드 내에 있는 업체들 중 우리가 정한 기준에 따라 업체 선정.</span></p>
<p style="padding-left: 40px;"><strong><span style="font-size: 15pt; color: #843fa1;">Machine Learning Ensemble</span></strong></p>
<p style="padding-left: 40px;"><span style="font-size: 15pt;">월별로 단속률이 다르다는 것을 밝혀내고 월별로 다른 머신러닝을 사용해 결과 도출.</span></p>
<p style="padding-left: 40px;">&nbsp;</p>
<p>&nbsp;</p>
<p style="padding-left: 20px;"><span style="color: #236fa1;"><strong><span style="font-size: 36px;">Result</span></strong></span></p>
<p style="padding-left: 40px;"><span style="font-size: 15pt;">추천한 100개의 업체 중 6개의 업체 단속 성공.</span></p>
<p>&nbsp;</p>
<p>&nbsp;</p>
<p style="padding-left: 20px;"><span style="color: #236fa1;"><strong><span style="font-size: 36px;">Opinion</span></strong></span></p>
<p style="padding-left: 40px;"><span style="font-size: 15pt;">데이터 분석 중에서도 Bright Analysis와 Dark Analysis가 있다면 이번 주제는 Dark Analysis에 속한다고 생각한다. 단속을 하는 입장에서 어떻게 해야 더 많이 단속할 수 있을까를 생각하며 분석해야했기 때문이다. 특사경 분들이 실제 단속 현장에서 실랑이가 많다고 들었는데, 속이는 수법도 교묘하다고 한다. 특히 일반인일 경우 육안으로 원산지를 판단하기 힘든데 이 때문에 경력이 많은 특사경들이 가야 한다고 한다.&nbsp;&nbsp;</span></p>
<p style="padding-left: 40px;"><span style="font-size: 15pt;">아쉬웠던 점은 지역 추천 시 시뮬레이션으로 22% 의 정확도를 보였지만 업체 추천을 했을 시 그 정확도가 떨어질 수 밖에 없었다는 것이다.</span></p>
<p style="padding-left: 40px;"><span style="font-size: 15pt;">또한 배달 서비스 업체 요기요를 크롤링 할 때 요기요 자체에 원산지 표시에 대한 <span style="color: #e03e2d;">기준이 정해져 있지 않은 것인지</span>, 모든 업체가 다 원산지 표시를 하지는 않았다는 점이다.</span></p>
<p style="padding-left: 40px;"><span style="font-size: 15pt;">이를 미루어 보았을 때 농산물 품질 관리원에서 이에 대한 기준을 명확히 하거나 이러한 업체를 단속하는 것도 좋을 것 같다는 생각을 했다.</span></p>
</section>
<p>&nbsp;</p>
<p>&nbsp;</p>
<p>&nbsp;</p>
<p style="text-align:center;"><img src="/assets/images/post2/report_img.jpg" alt="report" style="width:80%;" /></p>