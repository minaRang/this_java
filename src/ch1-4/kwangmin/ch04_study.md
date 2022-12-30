### 4. 조건문과 반복문
#### 조건문
```
if
if(조건식){
    조건식이 true일 경우 실행
}

if - else
if(조건식){
    조건식이 true일 경우 실행
}elsf{
    조건식이 false일 경우 실행
}

else-if
if(조건식){
    조건식이 true일 경우 실행
}else if(조건식){
    if의 조건식이 false이고 else if의 조건식이 true일 때 실행
}else{
    모든 조건이 false일 경우 실행
}

중첩 if
if(조건식1){
  if(조건식2){
      조건식1이 true이고 조건식2가 true일 때 실행
  }else{
      조건식1이 true이고 조건식2가 false일 때 실행
  }
}

swith문

switch(변수){
  case(값1):
    변수의 값이 값1과 같은 경우 실행
    break;
}
```

#### 반복문
```
for
for(변수 초기화식; 조건식; 증감식){
    조건식이 true일 경우 실행
}

while
while(조건식){
    실행문
    증감식
}

do-while
do구문을 실행한 후 while문에서 조건식에 false일 경우 해당 do-while 구문 종료 while문의 조건식에서 true일 경우 다시 do-while실행
do{
    실행문;
}
while(조건식);

continue
for(변수 초기화식; 조건식; 증감식){
  if(조건식1){
      continue;
      조건식1에 true일 경우 아래의 1이 출력되지 않고 다시 for반복문으로 돌아간다.
  }
  System.out.println(1);
}
```
