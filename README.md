# 👋 Hi, I'm kyu-choi

### Systems · Embedded · Robotics · Web

C/C++ 시스템 프로그래밍과 MCU 제어부터 ROS 2 로봇, 웹 서비스까지 공부하고 있습니다.
하드웨어와 소프트웨어가 연결되는 과정을 직접 구현하고, 실습 결과와 배운 내용을 기록합니다.

---

## About Me

- 42 Gyeongsan에서 **C/C++ 기반 시스템 프로그래밍**을 학습하고 있습니다.
- **프로세스·스레드·IPC·소켓·HTTP**를 직접 다루며 시스템의 동작 원리를 익히고 있습니다.
- **NXP S32K144**의 레지스터를 설정하며 주변장치 제어와 **UART·SPI·CAN 통신**을 실습했습니다.
- **ROS 2·TurtleBot3·Nav2**를 웹 인터페이스와 연결하는 로봇 프로젝트를 진행했습니다.
- **React·TypeScript·Supabase** 기반 서비스와 **Capacitor**를 활용한 Android 앱 구성을 다루고 있습니다.
- 구현 과정, 디버깅 기록, 테스트 방법을 코드와 함께 남기는 것을 중요하게 생각합니다.

---

## Tech Stack

프로젝트와 실습에서 사용한 기술입니다.

| 분야 | 기술 |
| --- | --- |
| Languages | C, C++98, Python, JavaScript, TypeScript, HTML, CSS |
| Systems | Linux, Ubuntu, Makefile, Git, POSIX sockets, poll, pthread |
| Embedded | NXP S32K144, ARM Cortex-M4F, S32 Design Studio, GPIO, ADC, PWM, UART, SPI, CAN |
| Robotics & Vision | ROS 2, TurtleBot3, Nav2, Gazebo, OpenCV |
| Web & App | React, Vite, Tailwind CSS, FastAPI, Supabase, Capacitor |

---

## Featured Projects

### [Webserv](https://github.com/kyu-choi/42_webserver)

**C++98로 HTTP 요청 처리와 네트워크 I/O를 구현한 웹 서버 프로젝트**입니다.

- 단일 `poll()` 이벤트 루프에서 논블로킹 소켓과 CGI 파이프 처리
- HTTP 요청 파싱, 설정 파일 기반 라우팅, 정적 파일 및 오류 페이지 응답
- 파일 업로드·DELETE·리다이렉트·디렉터리 목록·chunked 요청 처리
- CGI 실행, 다중 포트 구성, 쿠키·세션 데모
- 통합 테스트, 동시 요청 테스트, Valgrind 점검 스크립트 포함

**Tech:** `C++98` `Linux` `TCP/IP` `HTTP` `poll` `CGI` `Makefile`

---

### [S32K144 Bare-Metal Study](https://github.com/kyu-choi/S32K144-study)

**NXP S32K144EVB-Q100 보드의 주변장치를 레지스터 수준에서 제어한 임베디드 실습 기록**입니다.

- GPIO, 시스템 클록, LPIT 타이머·인터럽트, eDMA 실습
- FTM PWM과 ADC를 연결한 LED 밝기 제어
- UART 명령 처리, SPI 송수신, 두 보드 간 CAN 통신
- ADC 값을 CAN으로 전송하고 수신 보드에서 PWM으로 출력하는 통합 실습
- 실제 보드 동작과 디버거의 레지스터·변수 확인 과정 기록

**Tech:** `C` `S32K144` `Bare-metal` `S32 Design Studio` `UART` `SPI` `CAN`

---

### [Physical AI Project](https://github.com/kyu-choi/Physical-Ai_project)

ROS 2 기반으로 **실제 TurtleBot3와 Gazebo/Nav2 시뮬레이션을 하나의 웹 인터페이스로 연결한 프로젝트**입니다.

- 실제 TurtleBot3 카메라 영상에 가상 오브젝트를 합성한 수동 조종·미션 모드
- Gazebo + Nav2 기반 자율주행 게임과 상태 머신
- FastAPI 웹 런처에서 모드 선택, 프로세스 실행·종료, ROS 2 topic/service 연동
- TF 기반 이동 거리, 주행 시간, 실패·복구 횟수를 CSV로 기록
- 동일 맵·seed 조건에서 Nav2 설정을 비교할 수 있는 벤치마크 구성

현재 벤치마크 CSV는 계측 확인용 샘플이며, 플래너별 성능 비교를 위한 반복 실험은 추가 과제입니다.

**Tech:** `Python` `ROS 2` `TurtleBot3` `Nav2` `Gazebo` `FastAPI`

---

### [Kyu Asset](https://github.com/kyu-choi/kyu_asset)

**자산·부채를 기록하고 순자산 변화를 확인하는 개인 자산 관리 서비스**입니다.

- 자산·부채 등록, 수정, 삭제와 순자산·부채비율 대시보드
- 자산 구성 차트, 순자산 스냅샷, 월별 변화 확인
- 주식 종목 검색과 가격 조회, 목표 비중 기반 리밸런싱 계산
- React·TypeScript 프런트엔드와 Supabase 연동
- Capacitor 기반 Android 앱 구성 및 웹·앱의 계정 데이터 공유

**Tech:** `React` `TypeScript` `Vite` `Tailwind CSS` `Supabase` `Recharts` `Capacitor`

---

### [Youth Campus](https://github.com/kyu-choi/youth_campus)

**모바일 중심 랜딩 페이지와 신청자 관리 기능을 구성한 웹 프로젝트**입니다.

- 모바일 우선 랜딩 페이지
- JavaScript의 설정·서비스·화면 렌더링 역할 분리
- Supabase 데이터 조회와 정적 데이터 fallback 구조
- 관리자 페이지의 신청자 검색·필터·정렬 및 상세 조회
- 입금 상태·매칭 상태·메모 수정과 1:1 매칭 저장

**Tech:** `HTML` `CSS` `JavaScript` `Supabase`

---

## Learning Archive

### [42 Projects](https://github.com/kyu-choi/42-projects)

42 Gyeongsan 과정의 **C/C++ 시스템 프로그래밍 프로젝트 모음**입니다.

| 프로젝트 | 주요 학습 내용 |
| --- | --- |
| Libft · ft_printf · get_next_line | 문자열·메모리 처리, 가변 인자, 파일 디스크립터와 버퍼 관리 |
| push_swap | 스택 기반 정렬과 명령 수 최적화 |
| minitalk · Philosophers | UNIX signal 기반 IPC, 스레드·뮤텍스·동시성 |
| minishell | 명령어 파싱, 프로세스, 파이프, 리다이렉션 |
| so_long · miniRT | 2D 게임과 맵 검증, 레이 트레이싱과 벡터 연산 |
| Cpp-Module | 클래스, 상속, 다형성, 예외 처리 |
| Born2beroot · NetPractice | Linux 시스템 관리, IP·서브넷·라우팅 |

### [Inception](https://github.com/kyu-choi/inception) — 학습 중

42 Inception 과제를 준비하며 **컨테이너와 웹 인프라의 동작 원리**를 정리하고 있습니다.
현재 공개 저장소는 README 학습 문서 중심으로 구성되어 있습니다.

- Docker Image·Container·Volume·Network와 Docker Compose
- Linux Namespace·cgroup 및 컨테이너 프로세스 구조
- NGINX·TLS, WordPress·PHP-FPM, MariaDB의 연결 관계
- 환경변수·Secret·데이터 영속성 개념

### [Physical-Ai](https://github.com/kyu-choi/Physical-Ai)

Python과 로봇 소프트웨어 개발에 필요한 내용을 노트북, 예제 코드, 문서로 정리한 저장소입니다.

- Python·NumPy, 센서 데이터 처리, 파일·JSON·로그 분석
- 스레드·프로세스·Queue 기반 동시성 실습
- OpenCV, 카메라 보정, YOLO, Kalman Filter
- SLAM·AMCL, Dijkstra·A*·RRT·RRT* 경로 탐색

---

## Current Focus

- **Systems:** HTTP 서버와 네트워크 I/O의 동작 이해
- **Embedded:** 주변장치 제어와 보드 간 통신 경험 확장
- **Robotics:** 센서·제어·웹 인터페이스 통합과 실행 결과 기록
- **Infrastructure:** Docker와 서비스 구성 원리 학습
- **Web & App:** 사용자가 데이터를 기록하고 확인할 수 있는 서비스 개선

저수준 동작을 이해하는 것에서 시작해 실제 장치와 서비스까지 연결하는 개발자를 목표로 합니다.

---

## GitHub

[Profile](https://github.com/kyu-choi) · [Repositories](https://github.com/kyu-choi?tab=repositories)

---

### 꾸준히 만들고, 기록하고, 개선합니다.
