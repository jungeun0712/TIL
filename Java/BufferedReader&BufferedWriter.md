# BufferedReader와 BufferedWriter를 이용한 기초 알고리즘

## BufferedReader & BufferedWriter
- 문자 기반의 보조 스트림으로 버퍼를 이용해서 입출력의 효율을 높일 수 있도록 해주는 역할

## InputStreamReader & OutputStreamWriter
- 문자 기반의 보조 스트림으로 바이트 기반 스트림을 문자 기반 스트림으로 연결시켜주는 역할

- A + B 합 구하기

```java
import java.io.BufferedReader;
import java.io.BufferedWriter;
import java.io.IOException;
import java.io.InputStreamReader;
import java.io.OutputStreamWriter;
import java.util.Scanner;
import java.util.StringTokenizer;

public class test {
	public static void main(String[] args) throws IOException {
		Scanner input = new Scanner(System.in);
		int num = input.nextInt();
			
		for(int i=0; i<num; i++) {
			int A = input.nextInt();
			int B = input.nextInt();
			System.out.println(A + B);
		}
	}
}
```
- 꼭 예외처리 해주어야함!
```java
import java.io.BufferedReader;
import java.io.BufferedWriter;
import java.io.IOException;
import java.io.InputStreamReader;
import java.io.OutputStreamWriter;
import java.util.Scanner;
import java.util.StringTokenizer;

public class test {
	public static void main(String[] args) throws IOException {
		//입력
		BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
		//출력
		BufferedWriter bw = new BufferedWriter(new OutputStreamWriter(System.out));
		
		//StringTokenizer은 문자열을 우리가 지정한 구분자로 문자열을 쪼개주는 역할
		//쪼개어진 문자열을 토큰(Token)이라고 부름.
		StringTokenizer st;
		
		//테스트개수 받기
		int num = Integer.parseInt(bf.readLine());
		
		for(int i=1; i<=num; i++) {
			//입력받은 문자열을 ""공백으로 쪼개기
			st = new StringTokenizer(bf.readLine());
			
			//nextToken() : 다음의 토큰 발급
			//쪼개진 토큰 차례로 받기
			int A = Integer.parseInt(st.nextToken()); //2
			int B = Integer.parseInt(st.nextToken()); //3
			
			//한줄로 출력 \n : 한줄 띄기
			bw.write(A + B + "\n"); //5
		}

        //flush() : 모든 내용 출력
		bw.flush();
	}
}
```
