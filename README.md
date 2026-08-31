# 안녕하세요, 손준호입니다 👋

현재 온디바이스 AI와 임베디드 소프트웨어 개발을 공부하고 있습니다.

## 👨‍💻 About Me

- 온디바이스 AI SW 개발 과정 수강 중 (26.7 ~ 27.2 수료 예정)
- C 기반 STM32 임베디드 시스템 설계 및 구현
- 센서 데이터 수집·처리 및 UART / I2C / DMA 통신 학습
- Python 기반 프로그램 및 PySide6 GUI 애플리케이션 개발
- OpenCV와 YOLO를 활용한 컴퓨터 비전 학습

## 🛠 Tech Stack

`C` `STM32` `STM32 HAL` `I2C` `UART` `DMA`
`Python` `PySide6` `OpenCV` `YOLO` `Git`

## 📌 Project

### [⚙️ Bluetooth 기반 회전체 상태 모니터링 시스템](https://github.com/wooseokkim1992-byte/firmware_project)

STM32 2-Node 구조를 기반으로 회전체의 진동과 소음을 측정하고,
이상 상태를 판정하여 원격 관제 및 안전 정지를 수행하는 임베디드 시스템입니다.

**주요 기능**
- MPU6050 3축 가속도 기반 진동 데이터 수집
- Offset 보정 및 Filtering을 통한 진동 성분 추출
- RMS / Peak 기반 진동 특징값 계산
- NORMAL / WARNING / DANGER 상태 판정
- Sound Sensor ADC + DMA 연속 데이터 수집
- HC-05 Bluetooth 기반 STM32 간 양방향 통신
- OLED / LCD / RGB LED / Buzzer를 이용한 상태 관제
- DANGER 또는 E-STOP 발생 시 Relay를 통한 모터 안전 정지

**담당 역할**
- MPU6050 센서 제어 및 3축 가속도 데이터 처리
- 진동 Offset / 중력 성분 제거 및 Noise Filtering
- 3축 합성 진동값 및 RMS / Peak 계산
- Threshold / Hysteresis / Persistence 기반 상태 판정 로직 구현
- 진동 상태와 Relay 정지 기능 통합 및 테스트

**Tech**
`STM32F411RE` `C` `STM32 HAL` `MPU6050`
`I2C` `ADC` `DMA` `UART` `HC-05` `Git`

---

### [🎬 Movie Poster Quiz](https://github.com/ruruo1385/mini_proj_one)

영화 포스터의 일부분을 보고 제목을 맞히는 PySide6 기반 객관식 퀴즈 게임입니다.

- 난이도별 포스터 분할 크기 적용
- 제한시간과 점수 시스템 구현
- 영화 정보 및 이미지 데이터 처리
- 실행 파일 빌드 및 배포

**Tech**
`Python` `PySide6`
