# linux-cli-command
내가 매일 까먹어서 만드는 리눅스 명령어
### linux filesystem
- 시스템 제어
  - 서비스 목록 확인(unit file, state)
``` linux
# systemctl list-unit-files
```
  - 서비스 목록 확인(UNIT, LOAD, ACTIVE, SUB, DESCRIPTION) 패턴예시(--type=service --state=active)
``` linux
# systemctl list-units [PATTERN...]
```
  - 서비스 시작 | 종료 | 재시작 | 활성화 | 비활성화 | 갱신
``` linux
# systemctl start | stop | restart | enable | disable | reload [서비스명]
```


### alias command(잘 안됨, 알아보자)
``` linux
# vim ~/.bashrc
```
add below on .bashrc
```
alias running_services='systemctl list-units  --type=service  --state=running'
```
then you can use running_services command
