Sources
- [유니티 공식 문서]https://learn.unity.com/tutorial/introduction-to-the-vfx-graph-unity-2018-4-lts#
- [VFX Tutorial 유튜버]https://www.youtube.com/@GabrielAguiarProd

![[VFX_1.png]]
VFX 그래프는 약 4가지 블럭으로 이루어져 있다.

1. Spawn: 스폰할 때, 언제 스폰되는지, 얼마나 스폰될 지 정함
2. Initialize: 생존 시간, 어디 스폰되는지, 한번에 몇개 존재하는지 등
3. Behavior over time: 시간 지날수록 어떻게 변하는지
4. Quad Output: 렌더링 항목


![[VFX_2.png]]
1. [[System]]: 여러 Context들이 모여서 특정한 역할 수행하는 것
2. Context: 