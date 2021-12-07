# 운영 관리 솔루션

## 기능

1. 서버, 네트워크 등 하드웨어 장비 자산관리
2. 변경 이력 남기기
3. 서버 별 계정 리스트
4. 웹 로깅
5. 서버 접속 이력
6. 접속 KEY 관리
7. 웹 접속 계정
8. 서버 핸들링 명령어
9. 웹 설정 적용

---

## 만들고자 하는 것

```text
서버 운영 관리를 한번에 할 수 있는 웹 솔루션

서버의 OS 버전의 영향을 최소화 하도록 shell을 이용하거나 SSH를 이용하여 별도의 Client를 설치 하지 않아도 되도록
low level단의 개발을 하면 다양한 핸들링과 좋긴 하겠지만 혼자는 무리..

서버를 등록 하면 서버의 재원 정보를 등록 하고
서버 자동 스캔 기능 지정한 IP 대역을 스캐닝 하여 서버들 정보 리스트업 
서버의 생성된 계정 리스트 업
서버 계정 자동 생성, 삭제 
등록되지 않은 계정 생성시 알람 가능
서버 접속 이력 관리 root 및 설정한 계정으로 접속 시 알람
웹 접속, 수정 로깅하여 수정자 확인
알람 대상 등 셋팅 기능
커스텀 명령어 기능 # ansible을 사용하여 서버 생성후 적용할 서버 클릭 한뒤 명령어 실행 하면 해당 playbook 실행
서버 패스워드 관리 및 자동 변경
지정 시간대 계정 접속 시 알람 등등 
언제나 컬럼 추가 및 수정이 용이 하게 MSA ㄱㄱ

+ 서버 Cron 정보 및 커널 설정 정보 가져오기?

+ 모니터링 기능 # 워낙 해당 기능을 지원해 주는 opensource들이 많아서 이용하여 그래프 연동까지 하면 좋을꺼 같긴 하다
서버의 Listen중인 port, 프로세스 정보 확인 

+ 서버 접근 제어 # LDAP을 이용하여 다른 서버로 접근제어 관리 해주는 ??

이런 기능 다 만들면 만능 솔루션으로 팔아도 되겠다..
```

---

## 개발 영역

- WEB Front
- WEB Backend
- Control API
- Client install program

---

## Table schema

- Server # 서버의 유니크 값 관리
  
```sql
```

- hardware # 서버의 재원 정보
  
```sql
```

- history # 서버의 변경 이력 내용
  
```sql
```

- account # 서버별 계정 정보
  
```sql
```

- web-log # 웹 페이지 접속 등 사용 로그
  
```sql
```

- connection-log # 서버 접속 이력
  
```sql
```

- ssh-key # 서버 접속 키 정보
  
```sql
```

- command # 커스텀 명령어 관리
  
```sql
```

- web-account # 웹페이지 접속 정보
  
```sql
```

- setting # 알람 대상 모니터링 주기 등 설정 정보
  
```sql
```

---

## 하하

```text
누가 웹 Front만 해주면 좋겠다...
```
