- 이걸 왜하냐, cpu가 여러 process를 수행하는데 모든 process 끝나고 다음거 실행하면 실행시간도 너무 오래걸리고 resource도 남아돔. 
- 그래서 datapath를 여러 단계로 쪼개고 동시에 수행될 수 있는 단계를 한꺼번에 수행하는거임.
## Stages of Pipeline
IF -> ID -> EX -> MEM -> WB

하지만 Pipeline을 할 때 [[Hazard]]라는 것이 발생함.