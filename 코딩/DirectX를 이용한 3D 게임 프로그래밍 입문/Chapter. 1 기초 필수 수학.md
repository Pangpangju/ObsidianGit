# 내적
내적의 정의
$$u\cdot v = u_xv_x + u_yv_y+u_zv_z$$
또한 내적은 $u\cdot v = ||u||v||\cos\theta$ 으로 나타낼 수 있다.



# 직교화(Orthogonalization):
벡터 집합 {$v_0,v_1, ... v_{n-1}$}의 n개의 모든 벡터가 단위 길이이고 서로 직교일때 그러한 벡터 집합을 **정규직교(Orthonormal)** 집합이라고 한다. 주어진 벡터 집합을 정규직교 벡터 집합으로 만드는 것을 직교화(Orthogonalization)라고 한다.
# 그람-슈미트 직교화
벡터 집합 {$v_0, v_1$} 를 직교화해서 정규직교 집합 {$w_0, w_1$} 을 얻는 과정을 살펴보자

$w_1 = v_1 - proj_{w_0} (v_1)$ (이때, $w_0 = v_0$)

$proj_a(b)$ 는 a에 대한 b의 직교투영 (정사영) 한 것이다
![[Pasted image 20240214185447.png]]
정규직교가 되려면 `모든 원소를 정규화해서` 단위길이로 만들면 정규직교 집합이 완성된다



또, 벡터 집합 {$v_0, v_1, v_2$} 를 직교화해서 정규직교 집합 {$w_0, w_1, w_2$} 을 얻는 과정을 살펴보자.

$w_1 = v_1 - proj_{w_0} (v_1)$ (이때, $w_0 = v_0$)
$w_2 = v_2 - proj_{w_0} (v_1) - proj_{w_1} (v_2)$
.
.
.


이때 {$v_0, v_1, v_2, ..., v_{n-1}$} 에 대해서는
 
$$w_i = v_i - \sum_{j=0} ^{i-1} proj_{w_j} (v_i)$$
를 사용한다.





# 외적
외적의 결과는 벡터이며 `3차원에서만` 적용된다.
두 벡터를 외적하면 두 벡터에 모두 직교하는 또다른 벡터가 나온다.

$$w = u \times v = (u_yv_z - u_zv_y, u_zv_x - u_xv_z, u_xv_y - u_yv_x) $$
# DirectX에서의 벡터연산
DirectX에서는 `XMVECTOR` 타입을 사용하여 벡터를 연산한다
```cpp
#include <DirectXMath.h>

using namespace DirectX;

int main() {
    // 벡터 생성
    XMVECTOR vec1 = XMVectorSet(1.0f, 2.0f, 3.0f, 0.0f);
    XMVECTOR vec2 = XMVectorSet(4.0f, 5.0f, 6.0f, 0.0f);

    // 벡터 덧셈
    XMVECTOR vecSum = XMVectorAdd(vec1, vec2);

    // 벡터 내적
    float dotProduct = XMVectorGetX(XMVector3Dot(vec1, vec2));

    // 벡터 정규화
    XMVECTOR normVec = XMVector3Normalize(vec1);

    return 0;
}

```
`XMVECTOR`는 SIMD 명령어를 활용하여 벡터 연산의 성능을 극대화한다.

