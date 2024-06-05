Hazard는 pipelinging 을 할 때 pipeling의 단계 진행을 방해하는 요소이다. 

### Data Hazards:
- Data 사이에 의존성이 있는 경우일 때.
- EX) Instruction 2가 Instruction 1의 결과값을 사용하는 경우일 때.
- 해결방법:
	- Forwarding: 결과값을 다음 instruction으로 바로 넘겨줌
	- Stalling: Data 결과값 나올때까지 기다림
### Control Hazards:
- Branch instruction 때문에 생김. 다음 instruction 이 branch decision 에 따라 결정되기 때문.
- EX) Branch instruction 이 PC 값을 바꿔버림.
- 해결방법:
	- Branch Prediction(Branch 결과물 예측함)
### Structural Hazards:
- 2개 혹은 그 이상의 instructions가 같은 hardware resource 요구할때 생김.
- EX) 두개의 instruction 이 read/write하게 memory access 해야할 때
- 해결방법:
	- hardware duplication, 아니면 scheduling.