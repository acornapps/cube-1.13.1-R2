---
title: "청지윈 Installation"
excerpt: ""
permalink: /docs/ko/2/
redirect_from:
  - /theme-setup/
toc: false
toc_sticky: false
---

---
## 사전 준비 사항

설치 전 아래와 같은 프로그램들이 미리 설치 되어 있어야 하며 설치 되어 있지 않을 경우 에러 메시지가 발생한다.

1) Docker 다운로드 후 설치 (필수)

[https://store.docker.com/editions/community/docker-ce-desktop-mac](https://store.docker.com/editions/community/docker-ce-desktop-mac)

2) Vagrant 다운로드 후 설치 (virtualbox를 이용한 로컬 테스트 환경 구축시)

[https://www.vagrantup.com/downloads.html](https://www.vagrantup.com/downloads.html)

3) VirtualBox 다운로드 (5.1.x version) (VirtualBox를 이용한 로컬 테스트 환경 구축시)

[https://www.virtualbox.org/wiki/Download_Old_Builds_5_1](https://www.virtualbox.org/wiki/Download_Old_Builds_5_1)

4) SSH private key & public key 생성 및 유저 등록 (필수)

* SSH키는 Cube가 생성한 server instance에 접속하기 위해 사용한다.

* SSH key경로는 'cube.yaml 파일'의 키 경로 항목에 지정한다. 이에 대한 자세한 내용은 각 설치 환경에 대한 문서를 참조한다.

* 새로운 키 생성은 아래를 참조한다. 기존 키 사용과 마찬가지로 생성한 키는 'cube.yaml' 파일에 지정해야 한다.

```
# ssh-keygen -f /path/to/private_file -t rsa -N ''
Generating public/private rsa key pair.
Your identification has been saved in /path/to/file.
Your public key has been saved in /path/to/file.pub.
The key fingerprint is:
SHA256:D5aprMbBbJFUPo7gKgLFXH8WGHsXCpm8HCKSQXO8gDE cloud@Clouds-MacBook-Pro.local
The key's randomart image is:
+---[RSA 2048]----+
|E*...o+=. . |
|+=+ooo*o o . |
| .*o.+=o= . |
| o oooo= + |
|. .o... S |
|.. =. o o |
|+ o .o . |
|o o. |
| .. |
+----[SHA256]-----+
# ssh-copy-id -i /path/to/id_rsa.pub {user_id}@ip
# ssh-add /path/to/id_rsa
```

5) kubectl 다운로드 (옵션)

[https://kubernetes.io/docs/tasks/tools/install-kubectl](https://kubernetes.io/docs/tasks/tools/install-kubectl)

####
