```python
python3 -c 'import pty; pty.spawn("/bin/bash")'
```

```bash
control + z
# 로컬: 현재의 리버스쉘을 백그라운드 실행

stty raw -echo
# stty : 터미널 속성 제어 명령어
# raw : 키 입력을 가공하지 않고 있는 그대로(원시 상태) 터미널로 전달
#         → Ctrl+C, Ctrl+Z 등 특수키도 바로 쉘로 전달됨
# -echo : 입력한 키가 화면에 표시되지 않도록 끔
#         → 쉘이 제대로 입력받을 수 있도록 키 입력 출력 억제

fg
# 백그라운드(중단)된 프로세스를 포그라운드로 불러옴
# 쉘을 일시 중단(Ctrl+Z)한 뒤 다시 활성화하는 명령어

export TERM=xterm
# TERM 환경 변수 설정
# xterm은 일반적인 터미널 타입으로, 방향키 등 키보드 제어 정상 작동을 도와줌
# 올바른 터미널 타입 설정으로 쉘 내 키보드 입력 문제 해결

reset
# 터미널 초기화 명령어
# 터미널 화면이 깨지거나 이상해졌을 때 원래 상태로 복구
# 키 입력이나 화면 출력 문제 해결에 도움

python3 -c 'import pty; pty.spawn("/bin/bash")'
```
