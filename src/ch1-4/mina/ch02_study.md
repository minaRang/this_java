##Ch02. 변수

###2.1 변수 선언
컴퓨터 메모리(RAM)는 수많은 번지로 구성된 데이터 저장 공간.   
-> **변수**는 하나의 값을 저장할 수 있는 메모리 번지에 붙여진 이름.
- 변수의 초기화
  - 초기화되지 않은 변수는 아직 **메모리에 할당되지 않음**

###2.2 정수 타입
- 리터럴 : 코드에서 개발자가 직접 입력한 값.<br>

```java
public static void main(String[]args){
        int var1 = 0b1011; //2진수
        System.out.println(var1); //11출력 
}
```

- float, double
  - 이진 부동 소수점 연산
  - 넓은 범위의 수에 대해 **근사치**를 **빠르게** 연산(산출)하기 위해 설계됨
  - 정확한 계산이 아니라 빠른 계산! -> 돈계산 ㄴㄴ ! 
  - 은행이나 과학분야에서 쓰는 타입
    - int, long, BigDecimal
      - BigDecimal은 기본 데이터 타입이 아니라 불편, 실행속도가 느려짐
      - int, long 성능이 중요하고 소수점을 직접 계산 및 유지가 괜찮고 너무 큰수(18자리 이하)가 아니면 사용
  - double타입이 float보다 큰 실수 저장 가능하고 정밀도가 높다.
  - 컴파일러는 실수 리터럴을 기본적으로 double 타입으로 해석.
  - float쓰고싶으면 리터럴 뒤에 'f' 또는 'F'를 붙이자

###2.7 자동 타입 변환
- 자동 타입 변환 type promotion
  - 값의 허용 범위가 작은 타입이 허용 범위가 큰 타입으로 대입될 때 발생!
  - byte < short, char < int < long < float < double
  - 예외
    - byte타입은 char로 자동 변환 불가. char는 음수를 포함하지 않는데 byte는 포함하기 때문

###2.8 강제 타입 변환
- 강제 타입 변환 casting
  - 큰 허용 범위 타입은 작은 허용범위 타입으로 자동 변환 불가