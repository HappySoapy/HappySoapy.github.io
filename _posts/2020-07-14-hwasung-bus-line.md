---
layout: post
title: 화성시 최적 시내버스 노선 제시
date: 2020-07-14
image: /assets/images/blog/bus.png
author: yelim
---

<p style="margin-left: 80px; line-height: 1;"><span style="font-size: 30px;"><strong><span style="color: rgb(44, 130, 201);">Summary</span></strong></span></p>
<p style="margin-left: 80px; line-height: 1;"><span style="font-size: 16px;"><strong>Subject</strong> : 화성시 관내 시내버스에 대한 노선 신설 또는 기존 노선의 개선 제안</span></p>
<p style="margin-left: 80px; line-height: 1;"><span style="font-size: 16px;"><strong>Data</strong></span></p>
<p style="margin-left: 100px; line-height: 1;"><span style="font-size: 16px;">&lt;.csv&gt;</span></p>
<p style="margin-left: 100px; line-height: 1;"><span style="font-size: 16px;">버스카드 태깅 정보</span></p>
<p style="margin-left: 100px; line-height: 1;"><span style="font-size: 16px;">버스 정류장 정보</span></p>
<p style="margin-left: 100px; line-height: 1;"><span style="font-size: 16px;">행정동별 유동인구 정보</span></p>
<p style="margin-left: 100px; line-height: 1;"><span style="font-size: 16px;">&lt;.geojson&gt;</span></p>
<p style="margin-left: 100px; line-height: 1;"><span style="font-size: 16px;">화성시 읍면동</span></p>
<p style="margin-left: 100px; line-height: 1;"><span style="font-size: 16px;">100m x 100m 그리드 시간별 유동인구</span></p>
<p style="margin-left: 100px; line-height: 1;"><span style="font-size: 16px;">거주인구</span></p>
<p style="margin-left: 100px; line-height: 1;"><span style="font-size: 16px;">도로 네트워크 링크</span></p>
<p style="margin-left: 80px; line-height: 1;"><span style="font-size: 16px;"><strong>Tool&nbsp;</strong>: Python</span></p>
<p style="margin-left: 80px; line-height: 1;"><span style="font-size: 16px;"><strong>ML</strong> : KMeans++</span></p>
<p style="line-height: 1;"><span style="font-size: 16px;"><br></span></p>
<p style="line-height: 1;"><span style="font-size: 16px;"><br></span></p>
<p style="margin-left: 80px; line-height: 1;"><span style="font-size: 16px;"><strong><span style="color: rgb(44, 130, 201);">Key Points</span></strong></span></p>
<p style="margin-left: 100px; line-height: 1;"><span style="font-size: 16px;">1. 버스 노선 운행의 적합 여부를 확인하기 위해서는</span></p>
