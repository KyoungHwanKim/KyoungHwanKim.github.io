---
layout: post
author: "KyoungHwan Kim"
title:  "메타 휴리스틱 기법을 활용한 외판원 순회 문제 시뮬레이터 제작"
subtitle: "담금질 기법(Simulated Annealing)과 유전 알고리즘(Genetic Algorithm)"
type: "Algorithm, NP-Hard"
projects: true
text: true
portfolio: true
post-header: true
header-img: "img/card.jpg"
main-img: "thumbnail/metaheuristic-tsp.jpg"
team: "개인 프로젝트"
role-title: "개인 프로젝트"
role-specific: "Algorithm Develop"
platforms: "Python"
date: "2020.05 - 2020.08"
order: 4
---

![외판원 순회 문제를 해결하는 모습](img/simulated.gif)
###### 외판원 순회 문제를 해결하는 모습.

# Problems

외판원 순회 문제(TSP, Traveling Salesman Problem)는 컴퓨터 과학 분야에서 중요한 문제로 취급되어 왔습니다.

완전 탐색으로 이 문제를 해결한다면, 도시의 수가 N개일 때, N!이라는 경우의 수를 모두 탐색해야지 답을 도출해낼 수 있었습니다. 만약 도시의 수가 20개라면 2,432,902,008,176,640,000이라는 매우 큰 경우의 수가 되고, 컴퓨터가 해결할 수 없게 됩니다.

그래서 다항 시간 내에 답을 "근사"할 수 있는 메타 휴리스틱(Meta-Heuristic) 기법을 활용해 이 문제를 해결해보려고 했습니다.

# 담금질 기법 - Simulated Annealing

전역 최적화 문제에 대한 메타 휴리스틱 기법 중 하나입니다.



