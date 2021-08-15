# While문 알고리즘

- 데이터를 계속해서 입력을 받는중 입력받을 데이터를 보내지 않으면 NoSuchElementException을 발생시킬수 있다.
- 이것을 고려하여 Scanner이나 BufferedReader에서 조건을 주어야한다.

```java
import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;
import java.util.StringTokenizer;

public class test {
	public static void main(String[] args) throws IOException {
		//입력
		BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
		StringBuilder sb = new StringBuilder();
		StringTokenizer st;
		String str;
		
		while((str=br.readLine()) != null) {
			st = new StringTokenizer(str, " ");
			int num1 = Integer.parseInt(st.nextToken());
			int num2 = Integer.parseInt(st.nextToken());
			sb.append(num1+num2).append("\n");
		}
		System.out.println(sb);
	}
}
```
- String객체와 String객체를 더하는(+)행위는 메모리 할당과 메모리 해제를 발생시켜 더하는 연산이 많아진다면 성능이 좋지 않음.
- 그래서! StringBuilder를 사용!!
- StringBuilder는 새로운 객체를 생성하는게 아니라 기존의 데이터에 더하는 방식을 사용해서 속도가 빠르다
- StringBuilder에는 문자열을 더해주는 append()가 있다


```java
import java.util.Scanner;

public class test {
	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
		
		while(sc.hasNextInt()) {
			int num1 = sc.nextInt();
			int num2 = sc.nextInt();
			System.out.println(num1 + num2);
		}
		
		sc.close();
	}
}
```
- hasNextInt() : 정수가 아닌 값이 들어올때 false를 반환하여 반복문 종료.