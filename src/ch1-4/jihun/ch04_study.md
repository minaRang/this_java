### CH 01. 조건문과 반복문
- 조건문
    - if
        - if, else if, else
    - case
        - switch(var), case value :, default :
- 반복문
    - for(int i=~~){ }
    - while(){ }
    - do { } while ();
    - break ⇒ 반복문 종료
        - 원래라면 현재 반복문만 종료함
        - 다만 레이블을 붙이면 모두 종료 가능
        
        <aside>
        💡 Outter: for(~~~){
          for(){
          break Outter;
         }
        }
        
        </aside>
        
    - continue ⇒ 아래를 수행하지 않고 위로 복귀