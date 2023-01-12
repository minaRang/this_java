### 상속
#### 1. 상속 개념
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
#### 2. 클래스 상속
- 자바의 경우 다중 상속을 허용하지 않는다. extends 뒤에는 단 하나의 부모 클래스만 상속해야 한다.
```
// 부모 클래스
public class Cellphone {
	// 필드
	String model;
	String color;
	
	// 생성자
	
	// 메소드
	void powerOn() { System.out.println("전원을 켭니다."); }
	void powerOff() { System.out.println("전원을 끕니다."); }
	void bell() { System.out.println("벨이 울립니다."); }
	void sendVoice(String message) { System.out.println("자기: " + message); }
	void receiveVoice(String message) { System.out.println("상대방: " + message); }
	void hangUp() { System.out.println("전화를 끊습니다."); }
}

// 자식 클래스
public class DmbCellPhone extends Cellphone {
	// 필드
	int channel;
	
	// 생성자
	public DmbCellPhone(String model, String color, int channel) {
		this.model = model;
		this.color = color;
		this.channel = channel;
	}
	
	// 메소드
	void turnOnDmb() {
		System.out.println("채널 " + channel + "번 DMB 방송 수신을 시작합니다.");
	}
	void changeChannelDmb(int channel) {
		this.channel = channel;
		System.out.println("채널 " + channel + "번으로 바꿉니다.");
	}
	void turnOffDmb() {
		System.out.println("DMB 방송 수신을 멈춥니다.");
	}
}

public class DmbCellPhoneExample {

	public static void main(String[] args) {
		// DmbCellPhone 객체 생성
		DmbCellPhone dmbCellPhone = new DmbCellPhone("자바폰", "검정", 10);
		
		// CellPhone으로부터 상속받은 필드
		System.out.println("모델: " + dmbCellPhone.model);
		System.out.println("색상: " + dmbCellPhone.color);
		
		// DmbCellPhone의 필드
		System.out.println("채널: " + dmbCellPhone.channel);
		
		// CellPhone으로 부터 상속받은 메소드 호출
		dmbCellPhone.powerOn();
		dmbCellPhone.bell();
		dmbCellPhone.sendVoice("여보세요");
		dmbCellPhone.receiveVoice("안녕하세요! 저는 홍길동입니다.");
		dmbCellPhone.sendVoice("아~ 예 반갑습니다.");
		dmbCellPhone.hangUp();
		
		// DmbCellPhone의 메소드 호출
		dmbCellPhone.turnOnDmb();
		dmbCellPhone.changeChannelDmb(12);
		dmbCellPhone.turnOffDmb();
	}
}
```

#### 3. 부모 생성자 호출
- 모든 객체는 클래스의 생성자를 호출해야만 생성된다.
```
public DmbCellPhone(){
  super(); // 부모의 기본 생성자를 호출한다.
}

// super인자로 호출된 생성자
public CellPhone(){
}
```
- 직접 생성자를 호출하고 싶을시에 아래와 같이 사용할 수 있으며 super(매개값)은 매가값의 타입과 일치하지 않는 부모 생성자를 호출할 시에 컴파일 오류가 발생한다.
- 부모 클래스에 기본 생성자가 없고 매개 변수가 있는 생성자만 있다면 자식 생성자에서 반드시 부모 생성자 호출을 위해 super()를 선언해야 하며 자식 생성자 첫 줄에 위치해야 한다.
```
자식클래스(매개변수선언){
  spuer(매가값);
}
```
- 부모 클래스에서 기본 생성자가 존재하지 않을시
```
public class People{
	public String name;
	public People(Stinrg name){
		this.name = name;
	}
}

public class Student extends People{
	public int No;
	public Student(String name, int No){
		super(name); // 부모 생성자를 호출 한 것
		this.No = No;
	}
}
```
