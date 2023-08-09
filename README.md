<p>
아까 디자인 패턴이랑 소프트웨어 아키텍처 이야기 부연설명만 하자면
scope이 다름
<br>
아키텍처는 시스템적인 범위, 디자인 패턴은 객체 단위
<br>
그래서 어떠한 디자인 패턴을 적용했다고 해서 클린 아키텍처가 되진 않음. 반대도 마찬가지 
<br>
그랬을 때 소프트웨어 아키텍처가 디자인 패턴을 포함한다 라고 볼 수는 있음
</p>

<br>
<br>
아키텍처는 레이어 혹은 계층간의 상호 작용에 대해 코드에 집중함 
<br>
(model, view, service, port, adapter,etc)
<br>
(재사용성, 확장성 (Open-close 원칙)등 시스템적으로 발생할 수 있는 문제들을 해결)
<br>
<br>
디자인 패턴은 객체를 생성/관리하는 방법에 있어 정형화된 방법론을 말함
<br>
<br>
<br>
<br>

---

**상속 객체들을 다룰 때 나오는 게 팩토리 패턴**
- ex) 사용자는 병원에 전화를 걸 수 있음. 이 때, 사용자는 구글 OIDC사용자, apple OIDC사용자, 일반 사용자가 있음 

**단 하나만의 객체를 생성/관리할 때 나오는 게 싱글턴 패턴**
- ex) 공유되고(여러 부분에서 쓰일 수 있는 것) = 로깅같은 것들 

**다중관계 / 혹은 n개의 객체를 관리할 떄 나오는게 옵저버 패턴** 
- ex) 생성된 n개의 이벤트를 처리하기 위해서 사용될 수 있음

---
<p>
헥사고날 아키텍처는 클린 아키텍처를 따른다고 말할 수 있음<br>

클린 아키텍처에 대한 정의: 그림으로 대체<br>
<img width="870" alt="Screen Shot 2023-08-09 at 2 36 07 PM" src="https://github.com/S-hayeon/archive/assets/25574165/a7de3d89-9584-40c3-bb36-83fe373013f6">
<br>

핵심은 외부 시스템(계층)과 내부 시스템(계층)이 있다고 했을 때, 외부 시스템이 내부 시스템에 영향주지 않는것을 의미함<br>

</p>
<br>
<br>
<p>
핵사고날 아키텍처에 대한 간단 설명:<br>
포트와 어답터라는 계층이 있다고 했을 때, 외부로만 향하는 & 내부로만 향하는 포트/어답터가 존재하고<br><br>

각 usecase에 국한되어 개발됨. (외부시스템과 내부시스템의 분리)<br><br>

따라서, 단방향이기 때문에 시스템적으로 발생할 수 있는 문제를 최소화함<br><br>

포트는 인터페이스이며, 어답터는 인터페이스에 대한 구현체임. <br><br>

다만 usecase별로 정의를 해야하기 때문에 data flow가 엄격해서 고민을 하게 만들고, 단순 코드량(LOC)는 많아서 귀찮기는 함<br><br>

  <br>
<img width="800" alt="Screen Shot 2023-08-09 at 2 48 37 PM" src="https://github.com/S-hayeon/archive/assets/25574165/30bf6c27-dae3-433a-8d26-cd5ebffc34f5">
<img width="1253" alt="Screen Shot 2023-08-09 at 3 11 59 PM" src="https://github.com/S-hayeon/archive/assets/25574165/70c20d0f-1ef5-4347-ab80-45737ff4c313">

</p>
<br>
<p>
대신, 그렇기 떄문에 높은 응집도/낮은 결합도를 가져갈 수 있고,<br> 문제가 발생시 책임 소재에 대한 파악, 유지보수가 수월해짐</p>


[프론트 참고 레포](https://github.com/juanm4/hexagonal-architecture-frontend)<br>

[플러터 참고 레포](https://github.com/embraceitmobile/multi_module_hexagonal_mvi)
