# StudyDS

## 자료구조
### <자료의 정의>
관찰이나 측정을 통해 발생한 값으로 컴퓨터에 입력 및 저장이 가능하여야 하며 처리한 결과는 정보로 활용된다</br>
### <자료구조의 정의>
컴퓨터 내부에서 형성된 자료와 자료의 논리적 관계이다</br>
선언문으로 준비하는 기본 자료구조, 기본 자료구조에서 파생된 파생 자료구조, 프로그래밍으로 구현하여야 하는 사용자 정의 자료구조로 분류</br>

기본 자료구조 -> 숫자(정수, 실수), 문자</br>
파생 자료구조 -> 문자열, 배열, 구조체, 포인터</br>
사용자 정의 자료구조(선형, 비선형)</br>
선형 -> 연결 리스트, 스택, 큐</br>
비선형 -> 트리 그래프</br>

### [선형구조] 자료가 분기 없이 일렬로 나열된 구조</br>
연결 리스트, 스택, 큐, 배열, 테이블의 레코드</br>

### [비선형구조] 분기를 허용하는 구조로 자료가 계층, 그물망 모양을 나타냄</br>
트리, 그래프</br>

## 자료에 대한 기본 작업</br>
* 초기화: 자료를 생성할 때 특정 값으로 설정</br>
* 소멸: 자료가 사용했던 기억장소를 다른 목적으로 재사용할 수 있게 점유를 해제함</br>
* 조회: 자료구조 또는 데이터베이스에서 조건에 맞는 자료원소</br>또는 튜플들을 찾아 가져와서 이를 출력장치에 나타냄</br>
* 순회: 자료구조에서 모든 원소를 한번만 방문하면서 전체 자료를 처리</br>
* 삽입: 자료구조에 새로운 원소 삽입</br>
* 삭제: 자료구조에서 기존의 원소 삭제, 기억장소가 유지된다는 점에서 소멸과 차이가 있음</br>
* 탐색: 자료구조에서 목표 원소 또는 탐색 키를 갖고 있는 자료를 찾는 작업</br>
* 정렬: 자료구조에서 자료 원소를 순서대로 나열하는 작업</br>
* 합병: 두 개 이상의 자료 집합을 하나로 합치는 과정</br>

## 알고리즘
### <알고리즘의 정의>
문제를 해결하기 위하여 입력된 자료를 토대로 원하는 결과를 만들어 내기 위한 규칙의 집합</br>
여러 단계의 유한 집합으로 구성되는데 많은 연산이 필요함</br>

### 알고리즘 충족 요건
* 유한성: 언젠가는 종료되어야 함</br>
* 명확성: 각 단계별로 무엇을 해야 하는지 구체적으로 표현하여야 함</br>
* 입력: 처리를 위하여 0개 이상 필요함</br>
* 출력: 1개 이상의 출력을 얻기 위해 알고리즘은 존재함</br>
* 효과성: 효과적인 방법으로 결과를 만들어야 함</br>

### ✨유클리드 호제법(최대공약수 구하기)✨를 통해 살펴 본 충족 요건
(ㄱ): m = 264, n = 72, r = 48 (r <- m % n) ---> 명확, 입력 </br> 
(ㄴ): m = 72, n = 48, r = 24 ( m <- n, n <- r, r <- m % n) ---> 명확, 효과 </br>
(ㄴ): m = 48, n = 24, r = 0 ( m <- n, n <- r, r <- m % n) ---> 명확, 효과 </br>
(ㄹ): r = 0 이면 반복 종료 (최대공약수는 n값) ---> 명확, 유한 </br>
(ㅁ): 최대공약수 24 출력 ---> 명확, 출력</br>
 
### 알고리즘 분석 기준
작업 시간: (수행 시간) 시간복잡도로 정량적 평가 </br>
기억장소 사용량: (주기억장치 사용량) 공간복잡도로 정량적 평가 </br>
단순성: (수행 과정의 단순성) 정성적 평가 </br>
* 정량적 평가: 몇 분 몇 초로 정확하게 측정 가능 </br>
* 정성적 평가: 숫자로 나타낼 순 있지만 정확하게 측정 X </br>

### [시간복잡도] 데이터 수 증가에 따라 수행 시간을 가늠할 수 있는 O 표현식
O(1) 상수형. 데이터 수에 관계 없음 ---> 해시 테이블  </br>
O(log2 n) 로그형. 데이터 수에 따라 조금씩 증가함 ---> 이분 검색 </br>
O(n) 선형. 데이터 수에 따라 산술급수적으로 증가함 ---> 트리 운행 </br>
O(n･log2 n) 선형로그형. 로그형과 선형의 곱 ---> 퀵 정렬 </br>
O(n2) 평방형. 데이터 수에 따라 기하급수적으로 증가함 ---> 삽입 정렬 </br>
O(n3) 입방형. 평방형보다 더 기하급수적으로 증가함 ---> 3차원 처리 </br>
O(2n) 지수형. 입방형보다 더 기하급수적으로 증가함 ---> 하노이 타워 </br>
O(n!) 계승형. 지수형보다 더 기하급수적으로 증가함 ---> 순열 </br>

### [공간복잡도] 데이터 수에 따라 주기억장치 사용량을 가늠할 수 있는 O 표현식 </br>
예를 들어, 공간복잡도가 O(n), 데이터 타입은 4byte 정수일 때, 데이터 수가 100개면 주기억장치는 400byte, 1000개면 4000byte가 필요함 </br>

## 프로그램과 순서도
### 프로그램 정의
컴퓨터로부터 원하는 결과를 얻거나 기능 수행을 하도록 프로그램 언어를 사용하여 짜놓은 명령들의 집합 </br>

소규모의 프로그램을 작성하는 단계는 </br>
[문제 분석] -> [입출력 설계] -> [순서도 작성] -> [코딩] -> [오류수정] -> [테스트] -> [유지보수] </br>

[문제 분석] </br>
: 컴퓨터로 수행하여야 할 일이 무엇인지 파악하여 필요하면 문서화한다 </br>
[입출력 설계] </br>
: 입력할 데이터의 종류와 입력 양식, 입력 장치를 결정하고, 출력에 대해서도 종류와 내용 및 출력 양식, 출력장치를 결정하고 문서화한다 </br>
[상세 설계] </br>
: 데이터를 입력하여 원하는 정보를 얻기 위한 처리 방법과 순서를 약속된 기호를 사용하여 그림으로 그리거나 기술한다 상세 설계도 또는 순서도가 작성됨 </br>
[코딩] </br>
: 원하는 결과가 출력되도록 프로그래밍 언어를 사용하여 만들어진 절차에 따라 명령들을 작성한다 </br>
[오류 수정] </br>
: 코딩이 완료되면 컴파일을 하게 되고, 이 때 프로그래밍 언어의 규칙에 어긋나는 부분은 오류가 발생한다 오류의 원인을 찾아내 수정하는 작업인 디버깅을 한다 </br>
[테스트] </br>
: 디버깅이 끝나면 결과가 정확하게 나오는지 테스트한다 이 과정은 입출력의 종류가 많을 수록 시간과 비용이 50%를 초과한다 </br>
[유지보수] </br>
: 테스트가 끝나면 실제 사용을 하게 되고 입출력 내용이 변경되는 경우에 코드를 수정하여 사용한다 </br>

## 시스템 구축 과정
[사용자 환경] -> [시스템 정의] -> [요구 분석] -> [구조 설계] -> [상세 설계] -> [코딩] </br>
-> [디버깅] -> [단위 시험] -> [통합 시험] -> [시스템 시험] -> [인수 시험] ->  [설치 시험] </br>
[사용자 환경]</br>
: 업무 수행자, 업무 환경 등 정의 </br>
[시스템 정의]</br>
: 컴퓨터로 수행해야 할 업무가 무엇인지 정의 </br>
[요구 분석]</br>
: 부서별, 업무담당자별 시스템에 입력하고 출력하여야 할 내용을 구체적으로 파악한다 </br>
[구조 설계]</br>
: 시스템의 전체적인 구조를 설계 </br>
[상세 설계]</br>
: 업무 담당자가 컴퓨터로 처리할 일이 코드로 구현되도록 설계</br>
[코딩]</br>
: 상세 설계안에 따라 프로그래밍 언어를 사용하여 작성한다 </br>
[디버깅]</br>
: 작성한 코드에 문법적인 오류가 있으면 수정한다 </br>
[단위 시험] </br>
: 원시 코드를 오픈 시킨 상태에서 모든 논리적인 경로에 대하여 검사를 수행하는 화이트박스 테스트✔️ 방식을 사용 </br>
[통합 시험] </br>
: 내부 구조나 작동 원리를 모르는 상태에서 사용자의 요구대로 각 기능들이 정확하게 작동하는지 입증하는 블랙박스 테스트✔️ 방식으로 동작 검사 </br>
[시스템 시험] </br>
: 잘 실행되고 있는지를 확인하는 기능적 테스트와 처리 능력, 복구 및 재시동 능력, 보안 능력 등 비기능적 테스트로 나누어 실시한다 </br>
[인수 시험] </br>
: 시스템을 사용자에게 배포하여 실제 사용할 수 있는지를 검증하며 비기능적 특성에 대한 확신을 얻는 작업이다 </br>
[설치 시험] </br>
: 고객에게 배포하여 문제가 없는지, 수정 보완할 점이 무엇인지 테스트한다 </br>

## 배열(Array)
### 배열 정의
같은 type의 자료를 연속된 공간에 저장하기 위해 준비하는 선형구조 </br>
![array](https://user-images.githubusercontent.com/80873447/177180233-49b14f65-eac6-4811-8f53-be988b1357ab.jpg)

### 배열의 장단점
[장점] </br>
1. 데이터 접근이 빠르다 (직접 접근) </br>
2. 기억장소를 효율적으로 사용할 수 있다 (데이터 저장을 위한 추가 공간 불필요) </br>

[단점] </br>
1. 특정 위치에 데이터 삽입/삭제 시, 자료의 이동이 많다 </br>
2. 배열 크기를 충분한 크기로 준비할 때, 사용하지 않는 공간은 낭비를 초래한다 </br>

## 구조체(Structure)
### 구조체 정의
타입이 다른 자료 원소를 하나로 묶은 자료형

```
<구조체 정의와 선언을 따로>✅

struct 이름{
  구성원1(필드1);
  구성원2(필드2);
  .
  .
  구성원n(필드n);
  };
  struct 이름 변수1, 변수2, ..., 변수n;
  
  struct book{
    char title[30];
    char writer[20];
    int value;
    char publisher[30];
    };
    struct book, book1, book2, book3;
    
    ```
<구조체 정의와 선언을 동시에>✅

struct 이름{
  구성원1(필드1);
  구성원2(필드2);
  .
  .
  구성원n(필드n);
  }변수1, 변수2, ..., 변수n;
  
  struct book{
    char title[30];
    char writer[20];
    int value;
    char publisher[30];
    }book1, book2, book3;
  
  
## 구조체 초기값 설정

[하나의 구조체 변수에 초기값 설정] </br>
struct book book1 = {"유물로 읽는 역사", "이덕일 외", 15000, "세종서적"}; </br>
-> book1.title은 "유물로 읽는 역사"라는 문자열을 가지게 된다 </br>

[구조체 배열에 초기값 설정] </br>
struct book books[] = { {"김병호의 문화체험", "김병호", 10000, "푸른숲"}, </br>
                        {"인류의 기원", "아서 니호프", 12000, "푸른숲"}, </br>
                        {"0교시 문학시간", "최지성", 14000, "나라말"}}; </br>
                        
-> book[1].title은 "인류의 기원"이라는 문자열을 가지게 된다 </br>
-> book[2].writer는 "최지성"이라는 문자열을 가지게 된다 </br>
```

## 중첩 구조체
구조체 멤버를 내포하고 있는 구조체을 중첩 구조체라고 한다 </br>

```
[중첩 구조체의 예]
struct personal_info{
  char name[20];
  char address[50];
  char tel_no[16];
  char e_mail[50];
  };
  
  struct book{
    char title[30];
    struct personal_info writer;
    int value;
    char publisher[30];
    }b1;
    
```
    
   
   
<img width="316" alt="구조형" src="https://user-images.githubusercontent.com/80873447/177263637-8c3ad910-841f-4ade-8053-dd7c5120b57d.png">

[사용 예] </br>
b1.title = "0교시 문학시간"; </br>
b1.writer.name = "이낭희"; </br>
b1.writer.address = "관악구 호암로 546"; </br>
b1.writer.tel_no = "872-4072"; </br>
b1.writer.e_mail = "mirim1@e-mirim.hs.kr"; </br>
b1.value = 14000; </br>
b1.publisher = "나라말"; </br>

## 구조체 패딩(Padding) 현상
구조체는 구성원 중 가장 큰 데이터 타입을 기준하여 배수로 크기가 정해진다</br>
struct temp1{ </br>
  char ch; </br>
  int vaule; </br>
  };
  
<img width="692" alt="패딩현상" src="https://user-images.githubusercontent.com/80873447/177321120-b284f74e-2fca-4800-8324-a6d9b11fa775.png">

가장 큰 데이터 타입은 int(4byte)고 구성원이 2개 이므로 4 X 2 = 8byte 크기로 temp1 구조체가 준비된다</br>
*sizeof(struct temp1)은 8* </br>

## 포인터 (Pointer)
### 포인터 정의
포인터 변수는 주소값을 갖는 변수이고 포인터는 주기억장치의 주소값이다 </br>
데이터를 간접 소유하게 되므로 한 번 이상의 접근으로 데이터를 조작할 수 있다 </br>

## 단순 포인터
포인터 변수에 데이터의 주소가 주어지고 한 번의 접근으로 데이터를 조작함 </br>

## 이중 포인터
이중 포인터 변수는 단순 포인터 변수의 주소를 갖는다 </br>
따라서 두 번 접근으로 데이터를 조작할 수 있다 </br>

*단순 포인터는 별(*)이 하나, 이중 포인터는 별(*)이 2개다 </br>

## 배열과 포인터
배열명은 배열의 시작 주소를 갖고 있으므로 포인터이다 </br>
그러나 배열명은 포인터 변수는 아니다 배열명에 주어지는 주소는 변경 불가능이다 </br>

[배열 선언]

int a[10] = {5, 10, 15, 20, 25};

#### 포인터 변수가 구조체 주소를 갖는 경우
```
#include<stdio.h> </br>
void main(void){ </br>
  struct node{ </br>
    char data;</br>
    struct node *link; </br>
    }a,b,c,*p; </br>
    
    p = &a; </br>
    a.data = 'A'; </br>
    a. link = &b; </br>
    b.data = 'B'; </br>
    b.link = &c; </br>
    c.dat = 'C'; </br>
    c. link = NULL; </br>
    }
 ```   
    
^: NULL 값에 해당하는 기호 명칭은 circumplex 또는 caret</br>

## 동적 메모리 할당
### 메모리 영역(C 프로그램)

CODE -> DATA -> BSS* -> STACK -> HEAP </br>
[CODE] 함수 실행코드 </br>
[DATA] 초기화된 전역변수 </br>
[BSS*] 초기화 안된 전역변수 </br>
[STACK] 지역변수(함수 호출하면 점유, 함수 정료되면 소멸) </br>
[HEAP] 동적할당(할당 함수 malloc(), calloc(), 소멸 함수 free()) </br>

CODE ~ STACK: 정적 할당 영역으로 컴파일 할 때 점유 할 메모리 크기가 결정됨 실행코드, 전역변수, 지역변수 </br>
HEAP: 실행 중에 함수를 사용하여 메모리 할당하고 해제하며 기본 제공 크기 이상의 할당이 가능함 </br> 

프로그램 실행 중에 필요에 따라 일정 크기의 메모리를 HEAP 영역에 할당하는 방법으로 C/C++에서는 사용 후 할당을 해제하여야 한다 </br>
STACK 영역의 공간이 부족할 땐 프로그램 실행이 중지되지만 HEAP 영역이 부족할 땐 다른 사용 가능한 공간을 확보하여 할당하여 준다 </br>
지역변수가 자리잡는 STACK 영역은 설정된 크기의 연속된 공간을 사용하므로 크기를 추가로 늘려 잡을 수 없지만 </br> 
HEAP 영역은 연속된 공간을 사용하지 않아도 되기 때문에 추가적으로 칠요한 공간만큼 다른 장소에 늘려 잡아 프로그램이 계속 실행되도록 한다 </br>

## 정적 메모리 할당
프로그램에서 선언된 지역 변수 할당에 해당되며, 실행 할 때 그 크기가 정해져 있고 STACK 영역을 사용한다 </br>
STACK 영역은 기본 제공 크기 이상을 요구하면 프로그램 실행이 중지된다 </br>

## 연결 리스트(Linked List)
### 연결 리스트 정의
기억공간에서 물리적으로 흩어져 있는 자료들을 논리적인 순서를 갖도록 링크를 사용하여 연결한 구조 </br>

### 배열과 연결 리스트 비교
### 구분            배열                        연결리스트 </br>
검색       |      데이터 검색 속도 빠름    |    데이터 검색 속도 느림 </br>
데이터 변경   |   데이터 추가/삭제 시 이동   |  데이터 추가/삭제 용이 </br>
기억 공간     |   정적 할당, 연속 공간     |    동적 할당, 불연속 공간 </br>
추가 기억 공간  |  추가 공간 없음       |       링크 필드 추가        </br>  

### 연결 리스트 종류

#### 단순 연결 리스트✏️
<img width="925" alt="단순 연결 리스트" src="https://user-images.githubusercontent.com/80873447/177343264-c4a2e569-5ed2-45ee-8f17-74d9bcee09f0.png">

#### 원형 연결 리스트✏️
<img width="1002" alt="원형 연결 리스트" src="https://user-images.githubusercontent.com/80873447/177343952-6f1123c0-9544-49d3-8463-d092f3cf587e.png">

#### 이중 연결 리스트✏️
<img width="943" alt="이중 연결 리스트" src="https://user-images.githubusercontent.com/80873447/177345819-9a28b44b-40ae-43d6-a359-2188b75329f6.png">

## 단순 연결 리스트 운용
### 노드 준비
노드는 연결 리스트를 구성하는 단위 요소로 최소 두 개의 필드를 가진다 </br>  
하나는 데이터, 다른 하나는 연결할 노드의 주소를 가져야 하므로 구조체로 준비 </br>  

// 문자를 갖기 위한 노드 준비 </br>  
```
struct node{
  char data;
  struct node *link;
  };
```

// 노드를 동적 할당 받아 head가 간접 소유 </br> 
```
struct node *head = (struct node*)malloc(sizeof(struct node));
```
<img width="269" alt="간접소유" src="https://user-images.githubusercontent.com/80873447/177347516-40b22f47-366e-47c5-bd72-24b9296e8cba.png">

### 노드 추가
// p가 간접 소유한 노드 다음에 새로운 노드 추가 </br> 
```
p -> link = (struct node*)malloc(sizeof(struct node));
```
<img width="626" alt="노드추가" src="https://user-images.githubusercontent.com/80873447/177561237-61f4aed3-6b70-488a-8128-b3afcc60c6e9.png">

// p는 다음 노드로 이동 </br>
```
p = p -> link;
```

<img width="623" alt="다음노드로이동" src="https://user-images.githubusercontent.com/80873447/177561273-c48b3ce2-b7fb-415c-9c07-f1708b578d0a.png">

### 노드 삽입
// p 다음에 노드 삽입 </br>

```
struct node *ins = (struct node*)malloc(sizeof(struct node));
ins -> data = 'O';
ins -> link = p -> link;
p -> link = ins;
```

### 노드 삭제
// p 다음에 노드 삭제 </br>
```
struct node *del = p -> link;
p -> link = del -> link;
free(del); 
```

## 스택
### 스택 정의
최근에 저장한 데이터를 먼저 사용하는 구조로 LIFO(Last In First Out) 구조라고 칭함 </br>

[스택 용어] </br>
* push(): 스택에 데이터를 삽입하는 작업 </br>
* pop(): 스택의 top에서 데이터를 꺼내는 작업 </br>
* overflow: limit을 벗어나면 발생 </br>
* limit: push할 수 있는 한계로 배열의 끝 </br>
* top: 데이터 상단 </br>
* base: 스택의 시작 위치로 가장 아래 쪽. 즉, 배열 인덱스 0 </br>
* underflow: base를 벗어나면 발생. 즉, 배열 인덱스 -1이하 </br>

## 큐
### 큐 정의
먼저 저장한 데이터를 먼저 사용하는 구조로 FIFO(First In First Out) 구조라고 칭함 </br>

[큐 용어] </br>
* add(): 데이터를 추가하는 작업 </br>
* delete(): 데이터를 꺼내 사용하는 직업 </br>
* rear: 가장 최근에 추가한 데이터를 지시하는 포인터 또는 인덱스 </br>
* font: 사용할 데이터를 지시하는 포인터 또는 인덱스 </br>
* overflow: 끝까지 add()된 경우, rear == SIZE -1일때 add()시도하면 에러발생 </br>
* underflow: 더 이상 꺼낼 수 없는 경우, font > rear 일 때 delete() 시도하면 에러발생 </br>

### 큐 종류
* Linear Queue --> 선형 큐 </br>
* Circular Queue --> 환형 큐 </br>
* DeQueue --> 데큐  </br>

[우선순위 큐] </br>

문제점: 우선순위가 낮은 큐는 삭제되지 않을 수 있다 </br>
개선책: 일정시간이 경과하면 우선순위가 높은 큐로 이동시켜준다 </br>

✔️(중요) 레벨 오더 운행의 방법에 대하여 말하고 코드를 작성하자

## 트리 운행
root에서 출발하여 모든 노드를 순회한다 </br>

<img width="400" alt="이진트리" src="https://user-images.githubusercontent.com/80873447/177673170-64bdb9bd-96fc-40c3-a601-486c51ee3113.png">

### 전위 운행(PreOrder Traversal) 
모든 노드에 대하여 다음 3가지 일을 차례로 수행한다 </br>

(1) 노드의 데이터를 출력한다 </br>
(2) 왼쪽 자노드가 있으면 전진한다 </br>
(3) 오른쪽 자노드가 있으면 전진한다 </br>

*[이진 트리 4위 전위 운행 결과] A-B-D-E-G-J-C-F-H-I* 

### 중위 운행(InOrder Traversal) 
모든 노드에 대하여 다음 3가지 일을 차례로 수행한다 </br>

(1) 왼쪽 자노드가 있으면 전진한다 </br>
(2) 노드의 데이터를 출력한다 </br>
(3) 오른쪽 자노드가 있으면 전진한다 </br>

*[이진 트리 4위 중위 운행 결과] D-B-G-J-E-A-C-H-F-I*


### 후위 운행(PostOrder Traversal)
모든 노드에 대하여 다음 3가지 일을 차례로 수행한다 </br>

(1) 왼쪽 자노드가 있으면 전진한다 </br>
(2) 오른쪽 자노드가 있으면 전진한다 </br>
(3) 노드의 데이터를 출력한다 </br>

*[이진 트리 4의 후위 운행 결과] D-J-G-E-B-H-I-F-C-A*

## 그래프
### 그래프 정의

[그래프 정의] </br>
자료를 갖고 있는 정점과 정점을 연결하는 간선으로 구성되는 자료구조로 전기회로 분석, 최단거리 탐색, </br>
컴퓨터 네트워크, 인공지능 등에 활용됨 </br>

[그래프 용어] </br>
* 인접: 정점과 정점 사이에 연결선이 있고 직접 접근이 가능한 경우 </br>
* 경로: 출발에서 목표 지점까지 정점들의 순서 </br>
        정점 사이는 -(무방향) 또는 ->(방향) 간선으로 표시 </br>
* 단순경로: 경로상의 모든 정점들이 다를 경우 (단, 출발과 목표 정점은 같을 수 있음) </br>
* 사이클: 출발과 목표 정점이 같은 simple path </br>
* 차수: 한 정점에 연결된 간선의 수 </br>
진입차수: 들어오는 간선 </br>
진출차수: 나가는 간선 </br>

## 그래프 종류
### [무방향 그래프]
간선은 방향성이 없으며 인접간에는 상호 접근이 가능하다 </br>

### [방향 그래프]
간선은 방향성이 있으며 방향을 따라 인접으로 접근이 가능하다 </br>

### [혼합 그래프]
간선은 방향성과 무방향성이 혼재한다 </br>

### [가중치 그래프]
간선에 가중치가 있는 그래프 </br>

### [완전 그래프]
그래프의 어떤 정점에 대하여 다른 모든 정점들이 인접한 그래프 </br>

### [신장 트리]
n개의 정점을 가지는 무방향 그래프에서 n개의 정점과 n-1개의 간선으로 구성된 트리 </br>

### [최소비용 신장트리]
무방향 가중치 그래프에서 간선들의 가중치 합이 최소인 트리 </br>
최단거리 네트워크 구축, 배관 설치, 도로 건설 등에 활용됨 </br>















