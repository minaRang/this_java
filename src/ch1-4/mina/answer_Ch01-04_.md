- 자유롭게 문제 제출해주시면 됩니다
### ✔️ 미나
1. jdk와 jre차이 
   - JRE (Java Runtime Environment)
     - 자바 실행 환경의 약자로, 자바로 만들어진 프로그램을 실행시키는데 필요한 라이브러리들과 각종 API,
      그리고 JVM이 포함되어 있다.
     - JVM + 자바 클래스 라이브러리
     - 컴파일 된 자바 프로그렘을 실행하는데 필요한 패키지
   - JDK (Java Development Kit)
     - 자바 개발키트의 약자, 개발자들이 자바로 개발하는 데 사용 됨. 개발 시 필요한 라이브러리들과 
       javac, javadoc 등의 개발 도구들도 포함되어 있고, 개발을 하려면 당연히 실행도 시켜줘야 하기때문에
       JRE도 포함되어 있음.
     - 다시 말해 자바 프로그램을 실행, 컴파일, 개발하는 도구로 JRE와 JVM을 모두 포함하는 키트.
     - JDK가 포함하고 있는 것들 
       - javac : 자바 컴파일러(자바 소스를 바이트코드로 변환)
       - java : 자바 프로그램 실행기 (JVM을 실행시켜 자바 프로그램 실행)
       - javadoc : 자바 소스로부터 HTML형식의 API document 생성
       - jar : 자바 클래스 파일을 압축한 자바 아카이브 파일(.jar) 생성 및 관리
       - jdb : 자바 응용프로그램 실행 중 오류를 찾는데 사용하는 디버거
       - 등등...
       

2. 컴파일과 빌드 차이
   - 컴파일(Compile)
     - 하나의 언어를 다른 언어로 바꾸는 것.
     - Java에서는 Compiler가 소스코드를 JVM이 이해할 수 있는 바이트코드로 바꾸는 과정을 의미.
     - 컴파일을 통해 바이트 코드 형태의 .class 파일이 생성된다.
   - 빌드(Build)
     - 소스코드(개발자가 고급 언어로 작성한 것) 파일을 실행가능한 SW 산출물로 만드는 일련의 과정.
     - .class파일들과 resources 파일들을 지정된 위치에 옮기고 실행할 수 있게 하는 프로세스를 포함.
     - 빌드는 컴파일을 포함하며 추가로 실행할 수 있는 환경을 제공함
   - Run
     - 컴퓨터가 이해하지 못하는 소스코드를 이해할 수 있는 기계어로 바꿔 하드웨어 OS에 맞게 실행하는 것.
     - .class파일을 JVM의 Class Loader가 메모리에 올리고, 필요한 클래스들을 로딩하고 <br>
        JIT(Just-In-Time) Compiler가 메모리 상에 있는 바이트 코드를 기게어로 변경하여 실행
     

3. JVM 역할
   - Java는 OS에 종속적이지 않다는 특징을 가지고 있는데, OS에 종속받지 않고 실행되기 위해선 OS위에서 Javac 실행시킬 수 있는<br>
     도구가 필요함. -> JVM
   - OS에 종속받지 않고 CPU가 Java를 인식, 실행할 수 있게하는 가상 컴퓨터.
   - JVM이 인식할 수 있는 파일 -> Java bytecode(*.class)
   - bytecode?
     - VM에서 돌아가는 실행 프로그램을 위한 이진 표현법.
     - java bytecode는 JVM이 이해할 수 있는 언어로 변환된 자바 소스코드.
     - 자바 컴파일러에 의해 변환된 코드의 명령어 크기가 1바이트이기 때문에 자바 바이트 코드로 불리움
     - 바이트 코드는 다시 실시간 번역기 또는 JIT 컴파일러에 의해 바이너리 코드로 변환된다.
     - 즉 CPU가 이해하는 언어는 바이너리 코드, VM이 이해하는 코드는 바이트 코드.
   - JIT 컴파일러?
     - JIT 컴파일(Just-in-time Compliation)또는 동적 번역(dynamic translation)
     - 프로그램을 실제 실행하는 시점에 기계어로 번역하는 컴파일러.<br>
     

4. primitive type이란?
   - 미리 정의되어 제공되는 데이터 타입. 원시타입이라고도 함.
   - 기본값이 있기 때문에 Null 허용하지 않음.
   - Stack에 실제 값을 저장함.(Reference Type의 경우 Heap에 저장)
     - Reference Type은 stack에는 참조값만 있고, 실제 값은 Heap에 저장
     - 값을 필요로 할 때마다 언박싱 과정을 거쳐야 하므로 접근 속도가 느려짐
     - 따라서 이러한 이유로 reference type보다 primitive type이 접근속도가 빠름.
   - 값을 저장할 수 있는 범위가 있기때문에 벗어나면 컴파일 에러남.
     - reference type과 비교해서 사용하는 메모리양이 압도적으로 낮기때문에 primitive type이 효율적일 수 있음.
   - 제네릭에서 사용 불가
   - 성능과 메모리에 장점이 있는 원시타입을 먼저 고려해보고, Null을 다루거나 제네릭에서 사용되어야 할 경우 참조타입을 사용하자.
   
5. 변수 사용 범위에 따라, 각각 사용 위치에 따른 특징
    - 지역 변수(메서드, 생성자, 초기화 블록 내부)
      - 메서드 속에 선언하여 해당 메서드 속에서만 사용 가능한 변수
      - 메서드 호출 시 생성, 메서드 종료 시 소멸
      - 매개변수도 일종의 지역변수 임.
        - 매개변수는 호출 시 값이 넘어오기 때문에 초기화 필요없음.
      - 선언 외에 다시 사용하기 위해서는 반드시 초기화가 필요함.
    - 전역 변수(class영역에서 선언)
      - 함수 바깥에 선언하여 클래스 전역에서 사용 가능한 변수.
      - 클래스 변수, 인스턴스 변수
        - 클래스 변수
          - static 키워드를 가지고 필드에 선언(메모리의 static 영역 사용) 
          - 클래스가 메모리에 올라갈 때 생성됨
          - 초기화 순서
            - JVM 기본값 -> 명시적 초기값 -> 정적 초기화 블럭 -> 인스턴스 초기화 블럭 -> 생성자
        - 인스턴스 변수(멤버 변수)
          - 인스턴스가 생성되었을 때 생성됨, 참조하지 않으면 소멸(GC)
          - static 키워드 없이 필드에 선언(메모리의 heap영역 사용)
          - 초기화 순서
            - JVM 기본값 -> 명시적 초기값 -> 인스턴스 초기화 블럭 -> 생성자
***

### ✔️ 재환
1. JVM 의 특징을 설명하세요
   - 클래스 로더/런타임 데이터 영역/실행엔진 등으로 구성되어 있음.
     - 클래스 로더(Class Loader)
       - JVM내로 클래스 파일을 로드하고 링크를 통해 배치하는 작업을 수행하는 모듈.
       - 런타임시 동적으로 클래스를 로드하고 jar파일 내 저장된 클래스들을 JVM위에 탑재.
       - 즉, 클래스를 처음 참조시 해당 클래슬르 로드하고 링크하는 역할
     - 실행 엔진
       - 클래스를 실행시키는 역할.
       - 클래스 로더가 JVM내의 런타임 데이터 영역에 바이트 코드를 배치시키고, 이것은 실행 엔진에 의해 실행됨.
       - 인터프리터, JIT, GC로 구성됨
         - 인터프리터
           - 자바 바이트 코드를 명령어 단위로 읽어서 실행
           - 한줄 씩 수행하기 때문에 느림
         - JIT
           - 인터프리터의 느린 속도를 보완하기 위해 나온 방식.
           - 인터프리터 방식으로 실행하다가 적절한 시점에 JIT컴파일 방식으로 명령어 실행
           - 이후에는 인터프리팅하지 않고 기계어로 직접 실행
           - 매번 같은 코드를 실행하지 않고 캐싱하여 이후에는 바뀐 부분만 컴파일함.
           - JVM은 JIT방식과 인터프리터 방식을 혼합해서 사용.
         - GC
           - 더이상 사용되지 않는 인스턴스를 찾아 메모리에서 삭제
     - 런타임 데이터 영역 (Runtime Data Area)
       - 프로그램을 위해 OS에서 할당받은 메모리 공간.<br>
         (참고)
          1. https://doozi0316.tistory.com/entry/1%EC%A3%BC%EC%B0%A8-JVM%EC%9D%80-%EB%AC%B4%EC%97%87%EC%9D%B4%EB%A9%B0-%EC%9E%90%EB%B0%94-%EC%BD%94%EB%93%9C%EB%8A%94-%EC%96%B4%EB%96%BB%EA%B2%8C-%EC%8B%A4%ED%96%89%ED%95%98%EB%8A%94-%EA%B2%83%EC%9D%B8%EA%B0%80)
          2. https://code-lab1.tistory.com/92 
   - 플랫폼에 종속적임.
   

2. 자동 타입 변환이 무엇인지 설명하세요
   - 두 데이터 타입이 자동으로 변환이 이루어지는 것.(컴파일러가 처리해줌)
   - 자바에서는 데이터의 손실을 최소화하거나 방지하기 위해 범위가 작은 데이터 값을 더 큰 데이터 타입으로 할당하는 경우에만 동작
   - byte -> short -> int -> long -> float -> double
   - type promotion
   - 정수는 실수로 자동 형변환 가능 -> 정수는 실제 값을 저장하지만 실수는 지수부와 가수부를 따로 나눠 작성하기 때문에
     바이트 크기보다 더 많은 값을 표현 가능.
   - 논리형은 형변환 규칙에서 제외.
   - 명시적 형변환(type casting)은 범위가 큰 타입의 값을 작은 타입으로 할당하기 위해 사용(자동 X)


3. 오버플로우/언더플로우가 무엇인지 설명하세요
   1. 오버플로우
      - 자료형 별 값의 최대 범위를 벗어나는 경우, 초과한 값을 버림처리하고 sign bit를 반전시켜 최소값으로 순환
   2. 언더플로우
      - 오버플로우의 반대 개념, 최소 범위보다 작은 수를 발생시키는 경우 발생하는 현상.
   오버플로우와 언더플로우가 발생한다고 해서 컴파일 에러나 런타임 에러가 발생하지 않으므로 <br>
   최대값 또는 최소값 범위를 고려하여 코드 작성해야 함. -> 계산이 처리되기 전에 자료형을 변경해주어야 함.
   

4. while 문과 do~while 문의 차이점에 대해 설명하세요
    - 조건을 만족하지 않았을 때, while문은 반복문을 한번도 실행하지 않지만 do-while문은 반복문을 적어도 한번 실행함. 
   
   1. 정수를 입력받으면 해당 정수가 짝수인지 홀수인지 판별하는 코드를 작성하세요
       ```java
       public static void main(String[] args) {
           Scanner sc = new Scanner(System.in);
           int num = sc.nextInt();
           boolean result = false;

           if(method(num)) System.out.println("홀수입니다");
           else System.out.println("짝수입니다");
           }
       
       public static boolean method(int num){
           if(num%2 == 1){
           return true;
           }
         return false;
       }
      ```

***

### ✔️ 광민
1. JVM의 동작 방식에 대해 서술해주세요.
   - 앞에서 기술
2. 강제 타입 변환과 자동 타입 변환을 설명해주세요.
   - 앞에서 기술
3. do~while과 switch문에 관하여 설명해주세요.
   - do-while
     - 앞에서 기술 
   - switch
     - if문은 조건식이 true, false밖에 없기 때문에 경우의 수가 많아질 수록 else if반복추가
     - switch문은 변수의 값에 따라 실행문이 결정되기 때문에 같은 기능의 if문보다 코드 간결해짐
     - switch문의 괄호에는 정수타입(byte, char, short, int, long), 문자열 타입(String)사용 가능
4. 오버플로우와 언더플로우의 차이점에 대해 서술해주세요.
   - 앞에서 기술
5. equals, contains, ==의 차이점을 서술해주세요.


***

### ✔️ 지훈
1. 자바 컴파일 과정에 대해 설명하시오.
   - 앞에서 기술
2. 자바는 모든 운영체제에서 실행 가능하다. 어떻게 이것이 가능한지 설명하시오. 그리고 컴파일 언어와 인터프리터 언어의 특징에 대해 설명하시오
   - 운영체제에서 실행 가능한 이유는 앞에서 기술
   - 컴파일 언어 VS 인터프리터 언어
     1. 컴파일 언어
        - 컴파일러는 고급 언어로 작성된 소스 코드를 저급 언어로 번역하는 프로그램.
        - 컴파일러 언어는 컴파일러를 통해 컴파일 타임에 전체 소스 코드를 한 번에 기계어로 변환후 실행파일을 만듦.
        - 컴파일 언어는 컴파일 단계와 실행 단계가 분리 되어 있음.
        - C, C++, C#, Java
     2. 인터프리터 언어
        - 프로그래밍 언어의 소스 코드를 바로 실행하는 프로그램
        - 컴파일 하지 않고, 소스 코드를 한 줄씩 읽어들여 실행.
        - 컴파일 과정이 없기 때문에 컴파일 시간은 소요되지 않으나 실행 파일이 별도 생성되지 않기 때문에 실행시마다 인터프리트 과정이 반복 수행되어<br>
        실행속도가 느림
        - Python, Javascript,Ruby
3. byte에서 char 형으로 형 변환 시, 자동 형 변환이 불가능한 이유에 대해 설명하시오
   - byte는 음수 포함, char는 음수 미포함 -> 형변환 불가 
4. int a = 32768;을 (short)a, (char)a으로 각각 강제 형변환할 경우, 발생하는 일에 대해 설명하시오
   1. short
      - overflow 
   2. char
      - 정상적으로 변환됨 (최대 범위 넘지 않음.)
5. if문과 switch ~ case문의 차이를 설명하시오.  
***

### ✔️ 지우
1.강제 타입 변환과 자동 타입 변환에 대해 작성하기 
    - 앞에서 기술
2. 다음 연산으로 실행되는 데이터 타입 작성하기
(1)-byte
   - int
(2)byte+byte
   - int
(3)int+long
   - long
3.정수를 입력받고, 7로 나누었을 때 나머지가 0이 아니면 "X"출력 후 반복, 0이면 "종료"출력 후 종료되는 반복문 코드 작성하기
```java
public static void main(String[]args){
        Scanner sc = new Scanner(System.in);
        int num = sc.nextInt();
        
        while(true){
            if(num  % 7 == 0 ){
                   System.out.print("종료");
                   break;
            }else System.out.println("X");
        }
}
```
4.2023년 1월 1일을 printf() 메서드를 이용하여 출력하는 코드 작성하기
```java
public static void main(String[]args){
    
        System.out.printf("%d년 %d월 %d일",2023,1,1);
        
}

```

5.++피연산자, 피연산자++ 설명하기
   1. 전위 연산자
      - ++가 연산되고 출력
   2. 후위 연산자
      - ++가 연산되기 전 출력하고 연산

