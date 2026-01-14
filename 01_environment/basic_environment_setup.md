# 리눅스 실습 정리 (환경 설정)

## 실습 환경

* OS: CentOS (Red Hat 계열)
* 계정: root
* 네트워크 관리: NetworkManager 사용

---

## 호스트네임 변경

```bash
hostnamectl set-hostname Client2
```

* 서버 식별용으로 호스트네임 변경
* 여러 서버 사용할 때 구분하기 위함

---

## 네트워크 설정 (GUI)

```bash
nm-connection-editor &
```

* NetworkManager GUI 실행
* IP, DNS 설정 확인/수정 용도
* 초기 세팅이나 테스트 환경에서 사용

---

## 네트워크 연결 확인

```bash
nmcli connection up ens33
```

* ens33 인터페이스 활성화

```bash
systemctl restart NetworkManager
```

* 네트워크 설정 변경 후 적용

---

## 시스템 종료

```bash
init 0
```

* 시스템 종료 명령어
* 요즘은 poweroff / shutdown 명령을 더 많이 사용

---

## 리눅스 배포판 계열 정리

### Red Hat 계열

* RHEL
* CentOS Stream
* Fedora
* Rocky Linux
* Amazon Linux
* Oracle Linux

→ 서버 환경에서 많이 사용
→ yum / dnf 패키지 매니저

---

### Debian 계열

* Debian
* Ubuntu
* Kali Linux

→ 커뮤니티 기반
→ apt 패키지 매니저

---

## 메모

* 리눅스 환경 구성 단계에서 자주 사용하는 명령어 위주 정리
* 서버 세팅 시 네트워크 설정과 호스트네임 변경이 기본 작업
* 이후 사용자/권한, 디스크, 프로세스 관리 실습 예정
