# BufferedReader와 BufferedWriter를 이용한 기초 알고리즘

## BufferedReader&BufferedWriter

- 문자 기반의 보조 스트림으로 버퍼를 이용해서 입출력의 효율을 높일 수 있도록 해주는 역할

## InputStreamReader와 OutputStreamWriter
- 문자 기반의 보조 스트림으로 바이트 기반 스트림을 문자 기반 스트림으로 연결시켜주는 역할

- A + B 의 합 구하기


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
		
		BufferedReader bf = new BufferedReader(new InputStreamReader(System.in));
		BufferedWriter bw = new BufferedWriter(new OutputStreamWriter(System.out));
		
		//StringTokenizer은 문자열을 우리가 지정한 구분자로 문자열을 쪼개주는 역할
		//쪼개어진 문자열을 토큰(Token)이라고 부름.
		StringTokenizer st;
		
		int num = Integer.parseInt(bf.readLine());
		
		for(int i=1; i<=num; i++) {
			st = new StringTokenizer(bf.readLine());
			
			//nextToken() : 다음의 토큰 발급
			int A = Integer.parseInt(st.nextToken()); //2
			int B = Integer.parseInt(st.nextToken()); //3
			
			bw.write(A + B + "\n"); //5
		}

        //flush() : 모든 내용 출력
		bw.flush(); 
	}
}
```