## 무작위로 K개의 수 뽑기
![image](https://github.com/NAJJUU/1day-1study/assets/122864238/e71a57e4-8ea8-40bf-ad21-82b9cdb438c3)

### 내가 푼 풀이(오답1)
주어진 배열에서 중복된 수를 제거한 배열을 반환해야해서 중복을 허용하지 않는 set을 이용해서 중복을 제거해 준 후 다시 list로 바꾸어주었다.        

![image](https://github.com/NAJJUU/1day-1study/assets/122864238/abee8274-b626-4b2a-a03e-07b019677ce3)
 

### 내가 푼 풀이(오답2)
오답1에서 오류가 나는 이유가 반환되는 answer array의 길이가 k보다 큰 경우의 수를 생각해주지 못해서라고 생각하여 answer의 길이가 k보다 클 경우 index번호가 k부터 시작되는 요소는 삭제가 되도록 했다.

![image](https://github.com/NAJJUU/1day-1study/assets/122864238/59a1b06f-79db-4d33-9d07-68187e0a90c1)

#### 오답1, 오답2 둘 다 k개만 출력되어야한다는 생각에 첫번째 for문에서 범위를 arr.length로 지정했어야하는데 k로 지정해버림

### 내가 푼 풀이(오답3)
for문의 범위를 arr.length로 변경하고 set의 size가 k개가 되면 더이상 추가되지 못하도록 if문을 이용하여 for문을 중지했다.

![image](https://github.com/NAJJUU/1day-1study/assets/122864238/623aacfa-8097-4124-acac-cb7d16a6a0e3)

### 내가 푼 풀이(오답4)
set은 중복도 허용하지 않을뿐더러 순서도 보장하지 않기때문에 문제의 예시만 생각하고 set을 list로 변경 후 오름차순으로 정렬 후 -1을 k에 맞춰 추가해주었다.
#### ※ HashSet은 저장순서를 유지하지 않으므로 저장순서를 유지하려면 LinkedHashSet을 사용해야한다.

![image](https://github.com/NAJJUU/1day-1study/assets/122864238/eb6f2d21-097e-4b17-b288-6a89c24586e0)


### 내가 푼 풀이(정답1)
예시에는 오름차순으로 배열이 정렬되어있었지만 실제 파라미터로 입력된 배열은 그렇지 않을수도 있기 때문에 for문을 통해 요소를 하나하나 확인하며 set에 포함되어있지 않으면 answer에 추가해주고 set에 포함되어 있으면 추가해주지 않았다.      
그렇게 한 후 answer의 개수가 k개가 되면 더이상 추가되지 않도록하였고, k개보다 적으면 k에 맞춰 -1이 추가되록 했다.

![image](https://github.com/NAJJUU/1day-1study/assets/122864238/121bfe7a-0ae0-409c-aa9f-ccc2dd7b4ef8)


### 내가 푼 풀이(정답2)
contains method를 이용하여 list나 set의 요소 유무를 확인할 수 있다면 set을 사용하지 않고 list만으로도 확인하고 answer에 없는 요소를 추가할 수 있어서 set부분의 코드는 뺐다.

![image](https://github.com/NAJJUU/1day-1study/assets/122864238/97a6de23-c2c4-47cb-86ab-d52920324187)


### ※ 런타임에러 나는 이유
- 반복문이 무한으로 돌 때
- 문법이 틀렸을 때

### Collection 인터페이스를 기반으로 구현한 클래스에는 List와 Set이 있다.
- List 클래스는 선형 자료구조를 구현한 클래스
- Set은 비선형 자료를 구현한 클래스이다.

#### [List vs ArrayList]
List는 인터페이스이고 ArrayList는 이 List를 구현한 클래스로 ArrayList, LinkedList 둘 다 List 인터페이스를 구현했기 때문에 
List로 선언을 한 경우 인스턴스를 ArrayList로 받을 수 있고 LinkedList로 받을 수 있다.          
하지만 ArrayList로 선언한 경우는 ArrayList의 인스턴스를 만들어야 하므로 ArrayList로 받아야한다.       
-> LinkedList로는 ArrayList를 인스턴스를 만들 수 없기 때문입니다.


### <LinkedHashSet 사용한 풀이>
LinkedHashSet은 중복을 허용하지는 않지만 순서는 보장해준다.

![image](https://github.com/NAJJUU/1day-1study/assets/122864238/18df322e-4d49-4438-9bd5-6800c94295cb)
















