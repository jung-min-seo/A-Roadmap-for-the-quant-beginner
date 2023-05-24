# 퀀트 자동 거래 시스템 초보자를 위한 조언

## 들어가기에 앞서

이 글은 퀀트 혹은 시스템 트레이딩 비전공자이며 업계 경험이 없는 개인의 조언이다. 그로 인한 선입관, 편견을 고려하여 읽으시기 바란다. 

## 오버엔지니어링을 항상 경계하길 바란다.

* 무슨 언어가 좋은가? C? C++? Python?
  * 이 질문을 해야 할 상황이라면 Python을 추천한다.
  * 신기술을 학습하는 데에 소요되는 시간이 가장 적을 것이다.
  * 사용할 수 있는 라이브러리가 매우 풍부한 것도 장점이다.

* 거래시스템을 만들고 싶은데 어디서 시작을 해야할지 어떻게 나아가야할지 막막하다.
  * 국내 주식, 선물 등은 사고 파는 것을 위해 구현해야 할 것(로그인, 데이터 수집 등)이 초보에게는 너무 많고 복잡하다.
  * 가상화폐는 데이터를 무료로 제공해주며 RestAPI와 Websocket을 거의 기본으로 지원하여 국내 주식 거래 시스템보다 구현이 비교적 쉽다.
  * [파이썬을 이용한 비트코인 자동매매 (개정판)](https://wikidocs.net/book/1665)을 추천한다. 

* 책을 더 추천해 달라.
  * 한국어로 작성된 제대로 된 책이나 글은 매우 드물다. 
  * 인터넷에 있는 영어로 써진 퀀트에 대한 글은 해당 분야의 단어만 읽을 수 있어도 비교적 수월하게 읽을 수 있을 것이다. 더도말고 그정도까지만 노력하자.

* 데이터는 꼭 틱 단위를 이용해야 하는가?
  * 코딩에도 아직 익숙하지 못한 상황이라면 여기저기서 들어보니 틱 기반으로 하면 좋다더라 라는 말에만 사로잡혀서 본인의 코딩 실력 및 저장 비용 등 다른 것들은 고려 못하고 첫 목표부터 너무 거창한것 보다는 기본적으로 제공 해주는 수준의 분봉 데이터를 이용하기를 추천한다.
  * 고려할게 많은 프로그램을 만드려고 하다가 완성전에 포기하는 경우가 너무 많다.
  * 최대한 단순한 프로그램을 완성 후 차츰 원하시는 방향으로 개선해 나가는 것을 추천한다.

* 데이터를 모으다가 보니 중간에 빠진 데이터가 있다.
  * 데이터 빠지는건 유료 데이터 사는게 아니면 늘상 있는 일이다(심지어 유료도 싼건 빠진다).
  * 일부 데이터가 없다고 해서 제대로 돌아가지 않을 전략은 위험하다.
  * 반대로 일부 데이터가 없더라도 돌아가는데 문제 없을 전략을 추구하시기 바란다.

* 백테스팅 라이브러리는 어떤 것이 좋은가?
  * 아주 간단한 수준의 라이브러리라고 하더라도 직접 만드는 것을 추천한다.
  * 해당 라이브러리에서 백테스트 할 수 있는 전략'만' 생각하다보면 상상력이 제약된다.

* 우상향 하는 그래프가 그려졌다면 높은 확률로 버그로 인한 것이다. 다시 한번 잘 살펴보자.

* 돈 내고 쓰라고 하는 라이브러리가 본인의 필요에 딱 맞아 떨어질 가능성은 높지 않다.

* 정신건강을 위해 되도록 긴 시간을 기반으로 전략을 짜시는 것을 추천한다.
  * 짧은 시간을 기반으로 할 수록 같은 종목이지만 증권사 혹은 코인 거래소의 데이터가 조금만 달라도 다른 결과를 낼 가능성이 높다.
  * 시간이 짧아지면 그에 따라 데이터가 비례해서 거대해지고 단순히 보관하거나 다루는 것도 어려워진다.

* VPS(Amazon, vultr, digitalocean 등)을 꼭 사용해야 하는가?
  * 집에서 거래 시스템을 운용해보면 생각보다 단전과 네트워크 오류가 발생한다는 것을 알게 될 것이다.
  * 위 일은 겪지 않는 편이 정신건강에 좋다. 아무리 소액이라도 인프라 관련 오류로 잃으면 매우 힘들다.
  * 필요치 않은 관리 포인트를 늘려서 사고가 발생할 확률을 늘리지 말기 바란다.
  * 술 1,2번 마실 돈이면 시작을 위한 VPS 사양은 충분히 지불 할 수 있다. 

* Amazon이나 vultr 같은 곳도 오류로 인해서 꺼지는 것을 보았다. 그걸 어떻게 믿고 쓰는가?
  * 돈을 냈다는 것을 책임을 전가할 수 있다는 것이다. 
  * 관리가 미숙한 스스로를 자책하다 트레이딩을 포기하는 것 보다는 업체를 원망하는 것이 트레이딩 자체를 포기할 확률이 적다.
  * 업체는 당신이 자고 있는 시간에도 시스템을 감시하고 있다.

## 추천 블로그
  * [그대안의 작은호수](https://smallake.kr/) : 한국어로 수준 높은 퀀트에 대한 글을 접할 수 있는 귀한 블로그.

Copyright 2023. by Jungmin Seo. All rights reserved.
