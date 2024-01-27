---
title: "[System Cooler] DarkFlash Inf24 Pro"
date: 2023-11-08 23:00:00 +09:00
sitemap:
  changefreq: daily
  priority: 1
categories:
  - Hardware
  - Cooler
tags:
  - "#시스템팬"
  - "#쿨러"
  - "#데스크탑"
---

# 서론

마이크로닉스 m60 케이스를 구매해서 사용중이었는데, 해당 제품에 큰 소음이 처음에는 괜찮았지만, 갈수록 부담스럽게 느껴져서 교체를 해야겠다고 생각했다.

그리고 문뜩 AliExpress를 구경하다가 DarkFlash라는 유명한 회사의 팬이 보였다. INF24-Pro 팬이었는데, 120,140mm 시스템 팬 크기를 지원하는 m60 케이스와 찰떡인 120mm 팬이었다.

해당 제품의 경우 5V ARGB까지 지원하였기 때문에 해당 제품을 마음에 품고 있다가 구매하였다.

# 본론

### DarkFlash INF24-Pro - System Cooler Spec
- 크기: 120x120x25mm  
- 무게: 170g  
- 팬 속도: 800-1200 (10%) RPM  
- 소음: 18-30dBA  
- 풍량: 65CFM (최대)  
- 베어링: 유압 베어링  
- 전류: 0.15A  
- 수명: 100000 시간  
- 전원 공급 장치 인터페이스: PWM 4PIN + ARGB 3PIN

해당 제품에서 느낀 매력 포인트는 
1. 소음
2. 예쁜 디자인
이었다.
주 업무가 공부, Youtube, Netflix, KakaoTalk인 나에게는 성능은 그렇게 중요한 요소가 아니었다. 실제로 사용 중에 케이스를 열면 따뜻한 바람이 아니라 시원한 바람이 나온다...

<img src="/assets/img/2023-12-19-Change System Fan/Pasted image 20231219215428.png" width="70%" height="70%" title="4" alt="4">

해당 제품을 보면 매력적인 디자인임을 확인 할 수 있다. 그리고 케이스와 접촉되는 부분에 얇은 스펀지가 존재해서 유격으로 인해서 발생하는 소음도 잡아주도록 설계되었다.

해당 제품의 경우 5V A-RGB 선을 지원한다. 본체에서 5V 포트를 찾아보는 것보다 다나와에서 메인보드를 검색해서 5V ARGB 지원 여부를 확인하였다.
<img src="/assets/img/2023-12-19-Change System Fan/Pasted image 20231219215858.png" width="70%" height="70%" title="4" alt="4">
하지만 다나와에서 쓰인 것과는 다르게 ARGB 5V 3핀 헤더를 지원하지 않았고

한참을 5V 포트를 찾다가 지원하지 않는다는 리뷰를 확인할 수 있었다.

해서 빠르게 검색 후
<img src="/assets/img/2023-12-19-Change System Fan/Pasted image 20231219220121.png" width="70%" height="70%" title="4" alt="4">
darkFlash RC2 Hub를 구매하였다.

<img src="/assets/img/2023-12-19-Change System Fan/Pasted image 20231219221123.png" width="70%" height="70%" title="4" alt="4">
Input : ARGB port * 6, PWM port * 6, SATA 전원선, reset 선 ( rgb 변경용 )
output : mother board sync, PWM

을 지원하는 형식이다.

만약 본체에서 5V ARGB 포트를 지원한다면 6개의 선을 묶어서 하나로 내보내서 선정리에 용이하도록 하거나 리모컨을 사용해서 쉽게 RGB 조절이 가능하도록 도와주는 역할을 할 수 있고,

본체에서 5V ARGB 포트를 지원하지 않는다면, 6개의 선을 묶어서 SATA 전원선을 통해서 전원을 공급하고, 리모컨이나 reset 스위치를 통해서 RGB를 조절하도록 할 수 있다. ( 해당 경우에는 메인보드 RGB와 연동이 불가능하다.)

그래서 결론은 본체에서 5V ARGB를 지원하지 않는데 5V ARGB를 사용하고 싶거나 저처럼 잘못 구매하신 분들은 해당 제품 구매해서 해결 가능합니다.

하지만 국내에서는 리모컨을 찾을 수가 없고... Ali에서 구매하면 배송은 2~3일 정도 더 걸리지만 허브 하나 가격에 허브와 리모컨을 구매 할 수 있으니 Ali에서 팬 구매하실 때 같이 사시면 좋습니다...

그리고 팬 장착하고, 전원을 켰더니 팬이 엄청난 소음을 발생해서 찾아보니 BIOS 설정을 변경해주어야 된다고 한다.
<img src="/assets/img/2023-12-19-Change System Fan/Pasted image 20231219221218.png" width="70%" height="70%" title="4" alt="4">
그래서 
- CPU Fan Profile Standard -> Manual
- CPU Fan Min. Duty Cycle (%) 20 -> 0
- Chassis Fan 1 Q-Fan Control DC Mode -> PWM Mode
- Chassis Fan 1 Profile Standard -> Manual
- Chassis Fan 1 Max. Duty Cycle (%) 100 -> 90
으로 설정을 변경해주었다.

# 결론

<img src="/assets/img/2023-12-19-Change System Fan/Pasted image 20231219221437.png" width="70%" height="70%" title="4" alt="4">
<img src="/assets/img/2023-12-19-Change System Fan/Pasted image 20231219221446.png" width="70%" height="70%" title="4" alt="4">
해당 제품을 전면 흡기 후면 윗면 배기로 구성하여 사용중이고 소음도 없고, 좋다!