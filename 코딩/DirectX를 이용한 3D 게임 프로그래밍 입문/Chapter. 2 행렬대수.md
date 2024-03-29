

# 전치행렬
행렬의 전치(Transpose)는 행렬의 행과 열들을 맞바꾼것이다.
$m \times n$ 행렬의 전치는 $n \times n$ 행렬이 된다.

행렬 $A$ 의 전치행렬을 $A^T$라 표기한다.
# 단위 행렬
단위행렬은 정방행렬(square matrix)의 주대각(main diagonal) 성분이
전부 1이고 나머지는 0인 행렬이다.
$\begin{bmatrix}1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 1\end{bmatrix}$, $\begin{bmatrix}1 & 0 \\ 0 & 1\end{bmatrix}$
같은 행렬들이다.
단위 행렬은 항등원 역할을 하기 때문에
$$AI = B , IB = B$$
인 성질을 가지고 있다.

# 행렬식(Determinant)
행렬식은 기하적으로 표현하자면 한 행렬이 단위벡터로 이루어진 넓이 혹은 부피의 증감을 나타내는 값이다.
==크라메르 법칙(Cramer's rule)==을 이용해서 1차 연립방정식을 푸는 데에도 쓰인다.
$det A \neq 0$ 일때에만 A는 역행렬을 갖기 때문에 역행렬의 존재여부 판단할 때에도 사용한다.

# 소행렬(Minor Matrix)
$n \times n$ 행렬 A가 주어졌을 때 그 소행렬 $\overline{A_{ij}}$ 는 $A$의 i번째 행과 j번째 열을 삭제해서 나온 $(n-1)\times(n-1)$ 행렬이다

$A = \begin{bmatrix}A_{11} & A_{12} & A_{13} \\ A_{21} & A_{22} & A_{23} \\ A_{31} & A_{32} & A_{33}\end{bmatrix}$ 일 때

$\overline{A_{11}} = \begin{bmatrix} A_{22} & A_{23} \\ A_{32} & A_{33} \end{bmatrix}$  이다

소행렬을 사용하여 행렬식을 재귀적으로 정의할 수가 있다.
$4\times4$ 행렬은 $3\times3$행렬의 행렬식으로,
$3\times3$ 행렬은 $2\times2$ 행렬의 행렬식으로, .....

그러므로 A의 행렬식:
$$detA = \sum_{j=1} ^{n}A_{1j}(-1)^{1+j}det\overline{A}_{1j}$$
# 딸림행렬
일단 여인수(Cofactor)행렬에 대한 정의가 필요하다.
$A$가 $n\times n$ 행렬이라고 할 때
$C_{ij} = (-1)^{i+j}det\overline{A}_{ij}$를  $A_{ij}$의 여인수라고 부른다.

그리고 $A$의 각 성분의 $C_{ij}$를 계산해서 해당 $ij$번쨰 위치에 배치한 행렬 $C_A$을 A의 여인수행렬이라고 부른다.

그리고 $C_A$의 전치행렬을 A의 딸림행렬이라고 부른다.
$A^* = C_A^T$
# 역행렬
1. 역행렬은 정방행렬에만 있다.
2. 행렬 $M$의 역은 $M^{-1}$로 표기한다.
3. 모든 정방행렬에 역행렬이 있지 않음
	1. 역행렬이 있는 행렬은 가역행렬.
	2. 역행렬이 없는 행렬은 특이행렬.
4. 역행렬이 존재하면 그 역행렬은 고유하다.
5.  행렬에 역행렬 곱하면 단위행렬이 나온다.
	1. $MM^{-1} = I$ 이다

딸림행렬과 행렬식을 이용해서 역행렬을 구할 수 있다.
$A^{-1} = \frac{A^*}{detA}$

또한 다음이 성립한다.
$(AB)^{-1} = B^{-1}A^{-1}$
