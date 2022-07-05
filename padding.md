## 구조체 패딩(padding) 현상
구조체는 구성원 중 가장 큰 데이터 타입을 기준하여 배수로 크기가 정해진다 </br>

```
struct temp1{
  char ch;
  int value;
  };
```
#### 가장 큰 데이터 타입은 int(4byte)이고 구성원이 2개 이므로 4 X 2 = 8byte 크기로 temp1 구조체가 준비된다 </br>
