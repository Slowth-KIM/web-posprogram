## Spring Boot와 JPA로 재구현한 POS 프로그램 

-> 해당 프로젝트를 기반으로 [자세한 내용은 이쪽](https://github.com/Slowth-KIM/univ-csProject/tree/main/DB%2BC_POS%20Implement)

### 1) POS 프로그램 DB 요구조건
<br>
<br>

1. 메뉴는 메뉴 Type과 메뉴 ID로 식별된다. 음료를 제외한 메뉴는 레시피가 존재한다.
    - 메뉴 타입은 분식, 식사류, 음료, 김밥류로 고정되어 있다. 메뉴 타입 또한 메뉴타입아이디로 식별된다.

<br>

2. 직원은 직원 ID로 식별된다. 단, 한 직원은 하나의 업무만 맡을 수 있다. 홀직원만 각 테이블마다 고객에게 서비스를 제공한다.
    - 직원 타입은 홀, 주방, 매입자로 고정되어 있다. 직원타입 또한 직원타입아이디로 식별된다.

<br>

3.  고객은 정기적으로 단체로 주문하는 고객의 정보만 담는다. 그 외에 다른 손님이 주문할 경우에는 0으로 입력한다. 고객아이디로 식별된다.  

<br>

4. 거래처는 거래처ID로 식별된다. 주문할 수 있는 거래처는 고정되어 있으며, 삭제나 수정이 불가능하다. 

<br>

5. 테이블은 테이블 ID로 식별된다. status가 0이라면 빈 테이블이고, 1이라면, 현재 사용 중인 테이블을 나타내고 있는 것이다. 

<br>

6. 식재료는 일정한 주기로 매입을 한다. 매입날짜, 매입처, 매입아이디, 식재료ID로 식별한다. 

<br>

7. 영수증가격정보는 주문날짜와 주문아이디로 식별한다.

<br>

8. 영수증세부항목은 주문날짜와 주문아이디와 세부항목아이디로 식별한다.

<br>

9. 레시피는 메뉴타입, 메뉴아이디, 식재료아이디로 식별한다.

<br>

10. 재고는 주문날짜, 영수증번호, 식재료아이디로 식별한다.

<br>

11. 식재료는 식재로ID로 식별한다. 식재료는 고정되어있으며, 변경과 삭제와 수정이 불가능 하다. 
    - 대분류는 대분류 ID로 식별한다. 중분류는 중분류ID와 대분류ID로 식별한다. 

<br>
<br>
<br>
<br>



### 2) ER-D 및 IE
<br>
<br>


![ER-D](https://github.com/Slowth-KIM/univ-csProject/blob/main/DB%2BC_POS%20Implement/images/ER-D.png)


******************


<br>
<br>

![IE](https://github.com/Slowth-KIM/univ-csProject/blob/main/DB%2BC_POS%20Implement/images/IE.png)
