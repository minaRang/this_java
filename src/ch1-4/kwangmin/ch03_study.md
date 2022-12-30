### 3. 연산자
#### 연산자와 연산식
- 연산자의 우선 순위
- 대입 연산자, 부호, 비트, 논리를 제외한 연산자는 모두 왼쪽에서부터 연산을 시작한다.
#### 부호 연산자
- +피연산자 : 피연산자의 부호를 유지한다.
- -피연산자 : 피연산자의 부호를 변경한다.
```
int i = -100;
int result1 = -i; // 100
int result2 = +i; // -100
```
#### 증감 연산자
- ++피연산자 : 피연산자 앞에 붙었을 경우 다른 연산을 수행하기 전 피연산자의 값을 1증가시킨다.
- 피연산자++ : 다른 연산을 수행한 후에 피연산자의 값을 1증가시킨다.
```
int x = 10;
int y = 10;
int z; 

z = x++;
System.out.println("z= " + x);// 10출력
System.out.println("x= " + x);// 11출력
```
#### 논리 부정 연산자(!)
- !피연산자 : 연산의 값이 true라면 false로 false라면 true로 값을 바꾼다.
#### 비트 반전 연산자(~)
- 정수 타입(byte, long, int, short)에만 사용가능하며 2진수로 표현시 비트 값 0을 1로 1을 0으로 반전시킨다. 산출 값은 int로 반환되기 된다.
```
int v1 = 10; // 10
int v2 = ~v1; // -11
int v3 = ~v1 + 1; // -10

v1을 byte로 표현시 000000000000000000000001010이며
v2을 byte로 표현시 111111111111111111111110101이다.
```
#### 산술 연산자
- long을 제외한 정수 타입 연산은 int타입으로 산출되므로 byte byte3 = byte1 + byte2의 경우 컴파일 에러가 난다.
- 5 / 2 를 한 경우 double로 선언시에 2.5가 나오지 않으며 2.0이 저장된다. 그렇기에 2.5의 값을 얻기 위해서는 아래와 같은 방법을 사용해야 한다.
```
double result = (int1*1.0) / int2;
double result = (double) int1 / int2;
double result = int1 / (double)int2;
```
#### 오버플로우
- 산술 연산시 연산 후의 산출값이 산출 타입으로 표현할 수 없는 값이 나온 경우 오버플로우라고 한다.
- 그렇기에 아래와 같이 메소드를 활용하여 오버플로우를 탐지하는 것이 좋다.
```
public class CheckOverflowExample {
	public static void main(String[] args) {
		try {
			int result = safeAdd(2000000000, 2000000000);
			System.out.println(result);
		} catch(ArithmeticException e) { // 예외 처리 코드
			System.out.println("오버플로우가 발생하여 정확하게 계산할 수 없음");
		}
	}
	
	public static int safeAdd(int left, int right) {
		if(right > 0) {
			if(left > (Integer.MAX_VALUE - right)) { // 예외 발생 코드
				throw new ArithmeticException("오버플로우 발생");
			}
		} else { // right <= 0 일 경우
			if(left < (Integer.MIN_VALUE - right)) {
				throw new ArithmeticException("오버플로우 발생"); // 예외 발생 코드
			}
		}
		return left + right;
	}
}
```
- 정확한 계산시에는 부동소수점을 사용하지 않는다.
```
public class AccuracyExample1 {
	public static void main(String[] args) {
		int apple = 1;
		double pieceUnit = 0.1;
		int number = 7;
		
		double result = apple - number * pieceUnit;
		
		System.out.println(result);
	}
}
 
이 경우 출력값은 : 0.299999999999999이며 0.3이 아닌 근사치의 값을 산출한다. 그렇기 때문에 정수 연산으로 변경해서 아래와 같이 처리해야 한다.
public class AccuracyExample2 {
	public static void main(String[] args) {
		int apple = 1;
		
		int totalPieces= apple * 10;
		int number = 7;
		int temp = totalPieces - number;
		
		double result = temp / 10.0;
    
		System.out.println(result);
	}
}
```
