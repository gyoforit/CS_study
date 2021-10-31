# CS_study_16회

## 1. [컴퓨터구조] Call by value/address/reference

> actual argument: 전달 인자
>
> formal argument: 매개 변수

함수가 호출될 때 매개변수에 인자를 어떤 방식으로 넣어줄 건지에 대한 세가지 방식입니다.

1. **Call by value**: 값이나 일반 변수를 호출된 함수에 전달하는 것입니다. 전달인자의 값은 매개 변수에 복사됩니다. 따라서 함수의 작동은 전달 인자의 값에 영향을 미치지 않습니다.

   ```c
   void swap(int a, int b)
   {
       int t=a; a=b; b=t;
   }
   int main()
   {
       int a=5, b=10;
       printf("Before swap: a=%d, b=%d", a, b);
       swap(a, b);
       printf("After swap: a=%d, b=%d", a, b);
   }
   ```

   ```
   Before swap: a=5, b=10
   After swap: a=5, b=10
   ```

   main()에서 정의된 변수 a, b는 swap() 함수의 a, b와 변수의 이름은 같지만 주소 값이 다릅니다.

2. **Call by address**: 변수의 주소값을 호출된 함수에 전달하는 것입니다. 전달인자는 매개 변수에 복사되지 않고, 전달 인자의 주소값이 매개 변수에 할당됩니다. 따라서 매개 변수에 대해 함수가 수행하는 작업은 인자 값에 영향을 줍니다.

   ```c
   void swap(int *x, int *y)
   {
       int t=*x; *x=*y; *y=t;
   }
   int main()
   {
       int a=5, b=10;
       printf("Before swap: a=%d, b=%d", a, b);
       swap(&a, &b);
       printf("After swap: a=%d, b=%d", a, b);
   }
   ```

   ```
   Before swap: a=5, b=10
   After swap: a=10, b=5
   ```

   main()에서 정의된 a, b는 swap()의 x, y와 변수의 이름은 다르지만 a와 x, b와 y는 각각 같은 메모리 주소를 가리키고 있습니다.

3. **Call by reference**: 기본 주소값을 호출된 함수에 전달하는 것입니다. 전달인자는 매개 변수에 복사되지 않으며 참조만 됩니다. 따라서 매개 변수에 대해 함수가 수행하는 작업은 인자 값에 영향을 줍니다.

   ```c
   void change(int b[ ])
   {
       b[0]=10; b[1]=20; b[2]=30;
   }
   int main()
   {
       int a[3]={5, 15, 25};
       printf("Before Change: %d, %d, %d", a[0], a[1], a[2]);
       change(a);
       printf("After Change: %d, %d, %d", a[0], a[1], a[2]);
   }
   ```

   ```
   Before Change: 5, 15, 25
   After Change: 10, 20, 30
   ```

   change()에서 정의된 b는 main()의 배열 a를 가리키고 있습니다. 변수의 이름은 다르지만, 둘은 동일한 메모리 주소를 가리키고 있습니다.