
***
### ✔️ 광민

1. 추상클래스에 대해 설명해주세요.
   - 추상클래스란
     - p.324 클래스들의 공통적인 필드나 메소드를 추출해서 선언한 클래스
     - 완성되지 않은 메서드가 존재하는 '미완성 설계도'
     - 인스턴스 생성 불가능(new 연산자 불가능)
     - extends 뒤에만 올 수 있음
     - 클래스 선언에 abstract 키워드 붙이면 추상 클래스 선언이 됨.
     - 필드, 메서드 선언 가능하고 생성자도 있어야 함.
     
2. 인터페이스에 대해 설명해주세요.
   - 인터페이스란
     - 다형성 구현에 주된 기술로 이용 됨.
     - interface 키워드 사용. default, public 사용
     - 구현 객체는 여러 개의 인터페이스 implement 가능 
     - 다른 인터페이스 상속 가능 
     - 모든 멤버변수는 public static final

3. 추상메소드, 정적메소드, 디폴트메소드의 차이에 대해 설명해주세요.
   - 추상메소드
     - 구현 클래스가 재정의해야하는 public 추상 메소드
     - 리턴 타입, 메서드명, 매개변수만 기술하고 중괄호를 붙이지 않는 메서드.
     - public abstract 붙이지 않아도 컴파일 과정에서 자동으로 붙음
   - 디폴트 메서드
     - 인터페이스를 구현할 때마다 메서드를 모두 구현해야하기 때문에
        이를 보완하기 위한 기능
     - 완전한 실행 코드를 가진 메서드. 추상 메서드와 다르게 실행부가 있다.
     - default 키워드가 리턴 타입 앞에 붙음
   - 정적 메서드
     - 추상 메서드와 디폴트 메서드는 구현 객체가 필요하지만 정적 메서드는
        구현 객체가 없어도 인터페이스만으로 호출 가능.
     - 선언 방법은 정적 메서드와 동일하나, public을 생략하더라도 컴파일 과정에서 자동으로 붙는다
     

4. 다형성에 대해 설명해주세요.
   - 사용 방법은 동일하지만 실행 결과가 다양하게 나오는 성질. 
   - 자동 타입 변환과 메서드 오버라이딩이 필요
   - 하나의 객체가 여러가지 타입을 가질 수 있는 것.
   - 자바에서는 부모 클래스 타입의 참조 변수로 자식 클래스 타입의 인스턴스를 참조할 수 있도록 하여 구현
***
### ✔️ 재환

1. final 클래스와 메소드에 대해 설명하세요.
   - 클래스의 경우 해당 키워드가 붙으면 상속 불가능.
   - 메서드의 경우 자식 클래스에서 재정의 못함
2. 다형성에 대해 설명하세요.
   - 앞에서 설명
3. 추상 클래스에 대해 설명하세요.
   - 앞에서 설명 
4. 인터페이스의 특징에 대해 설명하세요.
   - 앞에서 설명 

***
### ✔️ 지훈
1. 다형성에 대해 설명하시오
   - 앞에서 설명
 
2. 부모 클래스가 매개변수를 갖는 생성자만 존재할 경우, 자식 클래스의 생성자를 구현하는 방법에 대해 설명하시오
   - 모든 객체는 생성자를 호출해야만 생성됨. 부모 객체도 예외는 아님.
     - 부모 객체의 생성자는 어디서 호출? -> 부모 생성자는 자식 생성자의 맨 첫 줄에 숨겨져있는 super()에 의해 호출됨
     - super()는 컴파일 과정에서 자동 추가됨. 이는 부모의 기본 생성자 호출.
     - 이때 부모 클래스에 기본생성자 없으면 자식 생성자 선언에서 컴파일 오류 발생
   - 부모 클래스에 기본 생성자 없고 매개변수를 갖는 생성자만 있다면, super(매개값..);을 직접 작성해야함.
     - 해당 super(매개값..)은 부모 생성자를 호출하는 것.

3. 추상클래스와 인터페이스의 차이에 대해 설명하시오
   - 둘 다 추상메서드 사용가능, 인스턴스화 불가능 
   - 키워드가 다름(extends, implements)
   - 사용가능한 변수
     - 추상클래스는 제한 없음
     - 인터페이스는 static final
   - 접근제어자
     - 추상클래스는 제한없음
     - 인터페이스는 public
   - 다중 상속 여부
     - 추상클래스 불가능
     - 인터페이스 가능
   - 사용처
     - 자신의 기능들을 하위 클래스로 확장 
     - 인터페이스에 정의된 메서드를 각 클래스 목적에 맞게 기능 구현 (인터페이스)

***
### ✔️ 지우
1. 상속에서 강제 타입 변환이 될 수 있는 경우는?
   - 자식타입이 부모타입으로 자동 변환된 후 다시 자식 타입으로 변환할 때

2. 추상클래스에 대해 설명해주세요.
   - 앞에서 기술

3. 봉인된 클래스에 대해 설명해 주세요
   - Java15부터 도입
   - 부모 클래스의 자식 클래스들을 명확하게 인지하는 목적 
   - 상속, 또는 구현할 클래스를 지정해두고 해당 클래스만 상속 혹은 구현을 허용 
   - sealed 키워드 사용
   - 상속/구현하는 클래스들은 final, non-sealed, sealed중 하나로 선언되어야 함.


4. 클래스 상속과 인터페이스 상속의 차이점은?
    - 앞에서 기술

5. 추상메소드에 대해 설명해주세요.
   - 앞에서 기술
***
### ✔️ 미나

1. instanceof 연산자와 지양하는 이유?
   - 같은 타입의 객체인지 확인하는 연산자.
   - 인스턴스의 타입 체크는 객체지향적인 코드에서 벗어남
   - 기능적으로는 문제가 없지만, 자주 사용하는것은 좋지 않음!
     - instanceof 연산자를 사용하는 코드는
      각 객체가 어떤것이고 어떤 결과를 리턴해야하는지 외부의 객체가 불필요하게 알 수있게 됨(캡슐화가 깨짐)
     - 상속받는 새로운 클래스가 있을 때, 해당 코드가 사용된부분에 또 추가해줘야함 
     - 다형성을 활용하자. 
2. 상속관계와 포함관계에 대해서 설명하기(is-a, has-a)
   - is-a 상속관계
     - 일반 클래스를 구체화하는 상황.
     - 하위 클래스가 상위 클래스에 종속
     - 유연성과 확장성이 떨어진다.
   - has-a 포함관계
     - 공통된 부분을 분리할 때, 상속보다 포함 관계로 클래스를 재사용하자
     - 상속으로 코드를 재사용하는 것과 구성으로 하는 것은 다르다. 
       - 구성으로 하면 객체의 내부는 공개되지 않고 인터페이스를 통해 코드를 재사용하기 때문에 구성에 대한 의존성을 인터페이스에 대한 의존성으로 변경하여 결합도 낮출수 있기 때문
   - Liskov Substitution Principle 리스코프 치환 원칙
     - 상위 타입의 객체를 하위 타입의 객체로 치환해도 프로그램이 정상 작동해야한다는 원칙.
     - 자식클래스가 부모클래스와 완전히 같은 것마냥 다뤄져야 함.
3. super, super()의 특징에 대해 설명하기
    - super
      - super는 자손 클래스에서 조상 클래스로부터 상속받은 멤버 참조하는데 사용되는 참조변수
      - 멤버변수와 지역변수 이름이 같을때, this를 붙여 구별하듯 상속받은 멤버와 자신의 멤버와 이름이 같을 때 supuer 붙여서 구별
      - 조상 클래스로부터 상속받은 멤버도 자손 클래스 자신의 멤버이므로 supuer대신 this 사용 가능(근본적으로 동일)
      - 그래도 조상클래스 멤버와 자손 클래스의 멤버가 중복 정의되어 서로 구별해야하는 경우에만 super 사용
      - 모든 인스턴스 메서드에는 자신이 속한 인스턴스의 주소가 지역변수로 저장되는데, 이것이 참조변수인 this와 super의 값이 됨.
    - super()
    - this()와 마찬가지로 super()역시 생성자.
    - super()는 조상 클래스의 생성자를 호출하는데 사용됨
    - Object클래스를 제외한 모든 클래스의 생성자 첫 줄에 생성자.this()또는 super()를 호출해야 함.
        - 그렇지 않으면 컴파일러가 자동적으로 super();를 생성자의 첫줄에 삽입.
    