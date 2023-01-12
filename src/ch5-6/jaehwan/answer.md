   ### ✔️ 광민
1. 기본형과 참조형 타입에 대해 설명해주세요.
   - 기본형: 실제 데이터 값을 저장하는 타입
   - 참조형: 객체의 주소를 참조하는 타입
2. 싱글톤에 대해 설명해주세요.
   생성자가 아닌 정적 메소드를 통하여 객체를 생성하는 방식
3. 오버로딩과 오버라이딩에 대해 설명해주세요.
   - 오버로딩: 메소드명이 같으며 파라미터의 타입 또는 개수가 다른 것
   - 오버라이딩: 상위 클래스로부터 상속받은 메소드를 재정의 하는 것. 메소드명, 파라미터, 리턴값이 모두 같아야 함
4. public, protected, default, private에 대해 설명해주세요.
   - protected: 같은 패키지 혹은 자식 객만 사용 가능
   - default: 같은 패키지에서만 사용 가능
   - private: 객체 내부에서만 사용 가능
5. 인스턴스 멤버와 정적 멤버에 대해 설명해주세요.
   - 인스턴스 맴버: 객체에 소속된 맴버로써 객체가 생성된 후 사용할 수 있다.
   - 정적 맴버: 클래스가 로딩되며 메소드 영역에 할당될 때 정적맴버들이 같이 관리되기 때문에 객체 생성없이 쓸 수 있다.


***
### ✔️ 재환
1. 메모리 영역에 대해 설명하세요. 
   - 메소드 영역: 바이트코드 파일을 읽은 내용이 저장되는 영역, 클래스가 클래스로더를 통해 로딩된 후 해당영역에 할당된다.
   - 힙 영역: 객체가 생성되는 영역
   - 스택 영역: 메소드를 호출할 때마다 프레임이 생성되는 영역
2. 생성자에 대해 설명하세요. 
   - new 연산자를 통해 인스턴스를 생성할 때 호출되며 가장 먼저 실행되는 것
3. 정적 맴버에 대해 설명하세요. 
4. 접근 제한자에 대해 설명하세요. 
5. 싱글톤 패턴에 대해 설명하세요. 

***
### ✔️ 지훈
1. 객체는 메모리상 어디에 생성되는가, 또 어떻게 메모리를 해제하는가 
2. Call by value 와 Call by Reference 차이, 자바의 call by reference
3. 자바에서 파라미터로 객체를 넘기는 것은 Call by Reference인가
4. 객체지향의 특징 중 캡슐화와 은닉성에 대해 설명하시오.

***
### ✔️ 지우
1. nullPointerException은 언제 발생하는지 설명해주세요.
2. 배열 변수를 선언한 시점과 값을 대입하는 시점이 다를 시 
값을 대입하는 법을 설명해주세요.
3. 캡슐화에 대해 설명해주세요.
4. 라이브러리 클래스와 실행 클래스에 대해 설명해주세요.
5. getter와 setter에 대해 설명해주세요.
***
### ✔️ 미나
1. JVM의 메모리 영역에 대해 설명해주세요.
2. String 객체 생성시, new연산자를 쓰면 같은 문자열이더라도 서로 다른 번지를 가진다.
    <br> 이떄 equals를 사용하여 비교하면 true가 나오는데, 그렇게 나올 수 있는 이유는?
3. static 키워드에 대해 설명해주세요.
4. this 키워드에 대해 설명해주세요.