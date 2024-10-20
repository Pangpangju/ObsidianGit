# Fetch Stage(IF)
- PC(Program Counter)가 다음 실행될 instruction 의 주소를 듦
- PC에서 address가 instruction memory로 보내짐
- address에 있는 instruction 이 Instruction Register (IR)에 위치됨
- PC 가 PC+4 로 Update됨(다음 Instruction)

# Decode Stage(ID)
- 받아온 Instruction 이 Decode 되어 무슨 Action 을 취할지 판단됨.

# Execute Stage(EX)
- ALU 가 instruction 에 따른 operation 을 수행함
- 만약 Branch 나 Jump일 경우에는 target address 를 계산함
# Memory Access Stage (MEM)
- 만약 instruction 이 메모리를 참조하는 action 을 수행한다면 (lw/sw) 수행됨
# Write Back Stage (WB)
- 수행의 결과물이 destination register(instruction 에 명시되어있음)으로 전달됨(written back)
