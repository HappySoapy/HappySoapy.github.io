---
layout: post
title:  화성시 최적 시내버스 노선 제시
date:   2020-07-14 10:05:55 +0300
image:  /assets/images/blog/bus.png
author: yelim
tags:   Team Projects
---

## Summary

### Subject : 화성시내 인구와 이동 형태를 고려해 관내 시내버스에 대한 노선 신설 또는 기존 노선의 개선 제안
### Data : 
### ㆍTripChain.csv : 2018년 7월 승차일 기준 1-4일의 버스 카드태깅 정보
### ㆍstations_table.csv : 17-18년 기준, 경기도 버스 정류장에 대한 정보
### ㆍtl_scco_emd.geojson : 화성시의 읍면동 정보
### ㆍsk_emd_od.csv : 2018년 7월 1-4일의 행정동별 이동 인구수 정보
### ㆍtl_scco_emd.csv : 화성시의 읍면동 정보
### ㆍh_100m_cell_flow.geojson : 2018년 특정일 기준. 100m x 100m 그리드에 시간별 유동인구 정보
### ㆍh_100m_cell_pop.geojson : 2019년 기준. 100m x 100m 그리드에 거주인구 정보
### ㆍmoc_link_2018.geojson : 2018년 기준 화성시 도로 네트워크 링크 정보
### ㆍroutestation.csv : 2018년 기준 버스 노선 기/종점 정보
### ML Algorithms : Kmeans++
### Tool : Python
