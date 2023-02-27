## <프로그래머스> 문자열 내 p와 y의 개수

![image](https://user-images.githubusercontent.com/122864238/221536668-994607d1-4b85-4ae1-a506-50bc25e989c2.png)

- public char charAt(int index)       
Returns the char value at the specified index. An index ranges from 0 to length() - 1.        
The first char value of the sequence is at index 0, the next at index 1, and so on, as for array indexing.        
If the char value specified by the index is a surrogate, the surrogate value is returned.

만약 String s에 p나 P가 있을 경우 그 숫자를 더해줄 변수 int p를 만들어 주었고 String s에 y나 Y가 있을 경우 그 숫자를 더해줄 변수 int y를 만들어주었다.        
그리고 charAt() 메서드를 이용하여 String의 인덱스 번호별로 문자를 비교하여 p나 P일 경우 변수 p에 1씩 더해주고 y나 Y일 경우 변수 y에 1씩 더해주었다.        
그리고 그 둘을 비교하여 같다면 true를 다르다면 false를 반환하게 하였다.       
둘 다 p나 P, y나 Y를 가지고 있지 않을 경우 변수 p와 y는 0으로 변수의 값이 같아 true가 반환된다.