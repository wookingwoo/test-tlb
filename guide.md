## 컴파일 방법

gcc -o test-tlb test-tlb.c

gcc -g -W -Wall -O2 -o test-tlb test-tlb.c





### [gcc 옵션]


1. -Wall 옵션 : 모든 모호한 코딩에 대해서 경고를 보내는 옵션

2. -W 옵션 : 합법적이지만 모호한 코딩에 대해서 경고를 보내는 옵션

3. -W -Wall 옵션 : 아주 사소한 모호성에 대해서도 경고가 발생

4. O2 옵션 : 최적화 레벨 2로 설정. (대부분의 최적화를 시도)

5. -E 옵션 : 전처리 과정의 결과를 화면에 보이는 옵션 

             (전처리과정 중 발생한 오류를 검증)
	     ※ enhanced Tip: --save-temps 옵션 
6. -S 옵션 : cc1으로 전처리된 파일을 어셈블리 파일로 컴파일까지만 수행하고 멈춘다. (*.s)

7. -c 옵션 : as에 의한 어셈블까지만 수행하고 링크는 수행하지 않는다.

8. -v 옵션 : gcc가 컴파일을 어떤 식으로 수행하는지를 화면에 출력한다.

9. --save-temps 옵션 : 컴파일 과정에서 생성되는 중간 파일인 전처리 파일(*.i)과 어셈블리 파일(*.s)을 지우지 않고, 현재 디렉토리에 저장한다. (오류 분석에 사용)


출처: https://jangpd007.tistory.com/220 [참 놀라운 세상]


## 실행 방법

```bash
for i in 4k 8k 16k 32k 64k 256k 512k 1M 2M 4M 6M 8M 16M 64M 128M 256M ; do echo -n "$i, "; ./test-tlb -r $i 64 ; done
```

Excel로 redirection

```bash
for i in 4k 8k 16k 32k 64k 256k 512k 1M 2M 4M 6M 8M 16M 64M 128M 256M ; do echo -n "$i, "; ./test-tlb -r $i 64 ; done > ss.xls
```