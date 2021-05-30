## Spring Boot와 JPA로 재구현한 POS 프로그램 (ver.쇼핑몰) 

-> 해당 프로젝트를 기반으로 [자세한 내용은 이쪽](https://github.com/Slowth-KIM/univ-csProject/tree/main/DB%2BC_POS%20Implement)

### 1) POS 프로그램 DB 요구조건
<br>
<br>

1. 메뉴는 메뉴 Type과 메뉴 ID로 식별된다. 음료를 제외한 메뉴는 레시피가 존재한다.
    - 메뉴 타입은 음료, 식품, 생필품으로 고정되어 있다. 메뉴 타입 또한 메뉴타입아이디로 식별된다.

<br>

2. 직원은 직원 ID로 식별된다. 단, 한 직원은 하나의 업무만 맡을 수 있다.
    - 직원 타입은 캐셔, 매입자로 고정되어 있다. 직원타입 또한 직원타입아이디로 식별된다.

<br>

3. 거래처는 거래처ID로 식별된다. 주문할 수 있는 거래처는 고정되어 있으며, 삭제나 수정이 불가능하다. 

<br>

4. 테이블은 테이블 ID로 식별된다. status가 0이라면 빈 테이블이고, 1이라면, 현재 사용 중인 테이블을 나타내고 있는 것이다. 

<br>

5. 물품은 일정한 주기로 매입을 한다. 매입날짜, 매입처, 매입아이디, 물품ID로 식별한다. 


<br>
<br>
<br>
<br>



### 2) ER-D 및 IE

<br>
<br>

1. 해당 ER-D와 IE에서 

<br>
<br>


![ER-D](https://github.com/Slowth-KIM/univ-csProject/blob/main/DB%2BC_POS%20Implement/images/ER-D.png)


******************


<br>
<br>

![IE](https://github.com/Slowth-KIM/univ-csProject/blob/main/DB%2BC_POS%20Implement/images/IE.png)
