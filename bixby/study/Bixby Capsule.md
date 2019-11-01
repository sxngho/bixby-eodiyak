# Bixby Capsule



* Capsule의 ID 종류

  * Example 

    * example 이라는 의미
    * Bixby Developer Center 또는 Bixby Develop들을 위한 Github에서 Example들을 다운로드 하면 이러한 이름으로 시작하는 캡슐 아이디를 가진 게 대부분이다.

    

  * Playground

    * playground 라는 이름으로 시작하는 캡슐 아이디를 쓰게 된다면,

      * 이 캡슐은 Bixby Developer Studio 개발 환경에서는 테스트하고 코딩하고 시뮬레이션하고 디버그 할 수 있다.
      * 하지만 Bixby Flatform Server의 Public Submission, Private Submission을 통해 단말에서 테스트 할 수 없다.
      * Public으로 외부 사용자들에게 실제로 노출시킬 수는 없다.

      

  * 사용자만의 Name Space

    * 개발자만의 특별한 Name Space를 사용하려면 Bixby Developer Center의 그 Name Space와 Capsule Name을 등록해야만 한다.
    * Bixby Studio 개발 환경에서 개발해서 이 내용을 Bixby Flatform의 Private Submission, Public Submission을 통해 Device Test도 진행하고 실제적으로 사용자에게 개발자의 Capsule과 서비스를 제공할 수 있다.

    

* Capsule의 ID 구성

  * Capsule ID는 Two Depth로 구성

    * 첫 번째는 Name Space라고 불리는 Team ID
    * 두 번째는 Capsule Name
    * 예 ) playground.burgershop

    

* 이러한 방식으로 Capsule ID 를 입력하여 새성하면 기본적인 폴더 구조**만**을 가진 Capsule이 생성된다.





---





# Bixby Capsule 구조



### 1. Modeling

*  Concepts
  * 발화 인식 및 발화 결과를 리턴할 때 필요한 값
  * 예 ) "햄버거 2개 주문해줘"
    햄버거 ->  FoodName,
    2 -> NumberOfFood
* Actions:
  * 캡슐이 사용자가 원하는 작업을 이해하도록 수행할 동작을 정의



### 2. Business Logic

- Javascript Code
  - 사용자가 원하는 작업을 실제 수행하는 코드
  - 이 단계에서 서비스 API를 연동



### 3.  UI/UX

- Bixby Views
  - 최종 결과를 사용자에게 보여주는 레이아웃 작업
- Dialog
  - 사용자에게 되묻거나 결과를 응답해주는 응답문을 생성



### 4. 트레이닝

- 발화 Training
  - Capsule이 잘 동작하도록, 처리할 수 있는 발화를 생성하고 자연어 트레이닝(NL Training)을 진행
- Debugging
  -  개발한 캡슐이 구현한대로 동작하는지 확인