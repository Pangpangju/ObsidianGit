타이머 장치가 수 밀리 초마다 인터럽트를 발생시키도록 함.

인터럽트가 발생하면 수행 중인 프로세스는 중단되고 미리 구성된 운영체제의 ==인터럽트 핸들러(interrupt handler)==가 실행된다.
그 후에는 OS가 CPU 제어권을 다시 얻음.

OS는 하드웨어에게 타이머 인터럽트가 발생했을 때 실행해야 할 코드를 알려주어야 한다.
(부팅될 때 함)

하드웨어는 인터럽트가 발생하였을 때 실행 중이던 프로그램의 상태를 저장하여 나중에 return-from-trap 명령어가 프로그램을 다시 시작할 수 있도록 해야함.