주소에 데이터의 낮은 바이트(LSB : Least Significant Byte)를 저장하는 방식이다. 이 방식은 평소 사람이 숫자를 사용하는 선형 방식과 반대로 거꾸로 읽어야 한다. 

출처: [https://code-lab1.tistory.com/179](https://code-lab1.tistory.com/179) [코드 연구소:티스토리]

EXAMPLE

메모리에 `0x12345678` 를 저장하려 할 때

Little Endian 방식을 사용한다면 하위비트부터 저장하기 때문에

| 0x100 | 0x101 | 0x102 | 0x103 |
| :---: | :---: | :---: | :---: |
| 0x78  | 0x56  | 0x34  | 0x12  |

