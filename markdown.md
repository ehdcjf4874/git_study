# 마크다운 작성법
 1.마크다운에 관하여
===================
 1.1 마크다운이란?
-------------------
Markdwon은 텍스법트 기반의 마크업언어로 2004년 존그루버에 의해 만들어졌으며 쉽게 쓰고 읽을 수 있으며 HTML로 변한이 가능하다. 특수기호와 문자를 이용한 매우 간단한 구조의 문법을 사용하여 웹에서도 보다 빠르고 컨텐츠를 작성하고 보다 직관적으로 인식할 수 있다. 마크다운이 최근 각광받기 시작한 이유는 깃헙(https://github.com) 덕분이다. 깃헙의 저장소 Repository에 관한 정보를 기록하는 README.md는 깃헙을 사용하는 사람이라면 누구나 가장 먼저 접하게 되는 마크다운 문서였다. 마크다운을 통해서 설치방법, 소스코드 설명, 이슈 등을 간단하게 기록하고 가독성을 높일 수 있다는 강점이 부각되면서 점점 여러 곳으로 퍼져가게 된다.

 1.2 마크다운의 장단점
---------------------
### 1.2.1. 장점
```
1. 간결하다.
2. 별도의 도구없이 작성가능하다.
3. 다양한 형태로 변환이 가능하다.
4. 텍스트(Text)로 저장되기 때문에 용량이 적어 보관이 용이하다.
5. 텍스트파일이기 대문에 버전관리 시스템을 이용하여 변경이력을 관리할 수 있다.
6. 지원하는 프로그램과 플랫폼이 다양하다.
```
### 1.2.2. 단점
```
1. 표준이 없다.
2. 표준이 없기 때문에 도구에 따라서 변환방식이나 생성물이 다르다.
3. 모든 HTML 마크업을 대신하지 못한다.
```
 2.마크다운 사용법(문법)
=========================
```
일단 md파일로 만들어야 한다. ex>markdwon.md
주의할점은 문법기호를 쓰고 띄어쓰기를 한 뒤 글을 써야 한다. ex> # This is a H1
```
 2.1. 헤더
--------- 
* 큰제목: 문서 제목
```
This is an H1
=============
```
This is an H1
=============

* 작은제목:문서 부제목
```
This is an H2
-------------
```
This ia an H2
-------------

* 글머리: 1~6까지만 지원
```
# This is a H1
## This is a H2
### This is a H3
#### This is a H4
##### This is a H5
###### This is a H6
```

# This is a H1
## This is a H2
### This is a H3
#### This is a H4
##### This is a H5
###### This is a H6

 2.2. BlcokQuote
----------------
이메일에서 사용하는 ```>``` 블럭인용문자를 이용한다.
```
> This is a first blockqoute.
>	> This is a second blockqoute.
>	>	> This is a third blockqoute.
```
> This is a first blockqoute.
>	> This is a second blockqoute.
>	>	> This is a third blockqoute.

이 안에서는 다른 마크다운 요소를 포함할 수 있다.

> #### This is a H3
>	> * List
>	>	> code

 2.3. 목록
---------
### ● 순서있는 목록(번호)


순서있는 목록은 숫자와 점을 사용한다.

```
1. 첫번째
2. 두번째
3. 세번째
```
1. 첫번째
2. 두번째
3. 세번째

 **현재까지는 어떤 번호를 입력해도 순서는 내림차순으로 정의된다.**

```
1. 첫번째
3. 세번째
2. 두번째
```
1. 첫번째
2. 세번째
3. 두번째


### ● 순서없는 목록(글머리 기호:```*```,```+```,```-```지원)

```
* 빨강
	* 녹색
		* 파랑

+ 빨강
	+ 녹색
		+ 파랑

- 빨강
	- 녹색
		- 파랑
```

* 빨강
	* 녹색
		* 파랑

+ 빨강
	+ 녹색
		+ 파랑

- 빨강
	- 녹색
		- 파랑

혼합 해서 사용하는 것도 가능하다

```
* 1단계
	- 2단계
		+ 3단계
			+ 4단계
```

* 1단계
	- 2단계
		+ 3단계
			+ 4단계

		
 2.4. 코드
----------

4개의 공백 또는 하나의 탭으로 들여쓰기를 만나면 변환되기 시작하여 들여쓰지 않는 행을 만날때까지 변환이 계속된다.

### 2.4.1. 들여쓰기
```
This is a normal paragraph:

	This is a code block.

end code block.
```
실제로 적용해보면,

적용예:
* * *
This is a normal paragraph:

	This is a code block.

end code block.
* * *
> 한줄 띄어쓰지 않으면 인식이 제대로 안되는 문제가 발생합니다.

```
This is a normal paragraph:
	This is a code block.
end code block.
```
적용예:
* * *
This is a noraml paragraph:
	This is a code block.
end code block.
* * *
### 2.4.1 코드블럭
코드블럭은 다음과 같이 2가지 방식을 사용할 수 있습니다:
+ ```<pre><code>{code}</code></pre>``` 이용방식

```
<pre>
<code>
public class BootSpringBoot Application{
	public static void main(String[] args){
		System.out.println("Hello, Honeymon");
	}

}
</code>
</pre>
```

<pre>
<code>
public class BootSpringBoot Application{
	public static void main(String[] args){
		System.out.println("Hello, Honeymon");
	}
}
</code>
</pre>
+ 코드블럭코드("```")을 이용하는 방법
<pre>


```
public class BootSpringBootApplication{
	public static void main(String[] args){
		System.out.println("Hello, Honeymon");
	}
}
```


</pre>


```
public class BottStringBoot Application{
	public static void main(String[] args){
		System.out.println("Hello, Honeymon");
	}
}
```


 2.5.수평선 ``` <hr/> ```
--------------------------
아래줄은 모두 수평선을 만든다. 마크다운 문서를 미리보기로 출력할 때 페이지 나누기 용도로 많이 사용한다.
```
* * *

***

*****

- - -

-----------------------------------------

```

 + 적용 예

* * *

***

*****

- - -

-------------------------------




	

