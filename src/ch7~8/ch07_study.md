### 상속
#### 상속 개념
- 상속이란 하위 클래스에게 물려주는 것을 의미한다.
- 부모 클래스에서 private 접근 제한을 갖는 필드와 메소드는 대상에서 제외되며 부모 클래스와 자식 클래스가 다른 패키지에 존재한다면 default 접근 제한을 갖는 필드 메소드도 제외된다.
- 상속을 이용하게 된다면 클래스 A를 상속받는 B와 C는 A필드의 메소드를 수정시 B와 C를 수정하지 않아도 수정된 A의 필드와 메소드를 사용할 수 있다.
```
public class A{
  int field1;
  void method1(){}
}

public class B extends A{
  int field2;
  void method2(){}
}
```
