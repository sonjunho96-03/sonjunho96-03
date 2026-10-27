# 안녕하세요, 손준호입니다 👋

**Embedded / On-device AI Software Developer**

STM32 기반 임베디드 시스템과 IoT 통신을 중심으로 공부하고 있으며,  
하드웨어 제어부터 Linux 네트워크 통신, Edge AI 시스템 연동까지 경험하고 있습니다.

---

## 👨‍💻 About Me

- 온디바이스 AI SW 개발 과정 수강 중
- C / STM32 기반 임베디드 펌웨어 개발
- GPIO, EXTI, ADC, DMA, I2C, UART, PWM 기반 주변장치 제어
- Bluetooth / Wi-Fi / TCP/IP를 활용한 MCU ↔ Linux 시스템 통신
- Raspberry Pi 기반 Linux Socket Programming 경험
- Python / OpenCV / YOLO 기반 Computer Vision 학습 중

---

## 🛠 Tech Stack

### Embedded
`C` `STM32F411RE` `STM32 HAL` `STM32CubeMX` `STM32CubeIDE`

`GPIO` `EXTI` `ADC` `DMA` `I2C` `UART` `PWM`

### IoT / Communication
`TCP/IP` `Linux Socket` `Bluetooth` `HC-05` `HC-06` `ESP-01 Wi-Fi`

### Linux / Edge
`Linux` `Raspberry Pi` `C Socket Programming`

### AI / Vision
`Python` `OpenCV` `YOLO`

### Tools
`Git` `GitHub` `PuTTY`

---

# 📌 Featured Projects

## 🏭 [AI Vision 기반 품질 검사 및 자동 분류 시스템](https://github.com/Lucas-SJeong/AI_IOT_OBJECT_CLASSIFIER)

STM32F411RE, Raspberry Pi, Jetson Nano를 연동하여  
AI 비전 검사 결과에 따라 제품을 자동 분류하는 **2인 팀 스마트 팩토리 프로젝트**입니다.

### Architecture

```text
HMI STM32 ─ Bluetooth ─ Raspberry Pi
                            │
                      TCP/IP Network
                       │           │
                  Jetson Nano   Motion STM32
                    YOLOv8       + ESP-01
                                      │
                                  Servo Motor
```

### 담당 역할 — Embedded Firmware & IoT Communication

**HMI STM32F411RE**
- STM32CubeMX 기반 Pin / Peripheral 설계
- 버튼 입력 및 Debouncing
- EXTI 기반 Emergency Stop
- ADC 가변저항 입력 처리
- I2C Character LCD 및 RGB LED 제어
- HC-06 Bluetooth UART 통신 구현

**Motion STM32F411RE**
- ESP-01 Wi-Fi AT Command 통신
- TCP Client 연결 및 패킷 처리
- `+IPD` 수신 데이터 파싱
- TIM4 PWM 기반 SG90 Servo Motor 제어
- PASS / FAIL 분류 및 HOME 자동 복귀 구현

**System Integration**
- `T8_HMI`, `T8_MOTION`, `T8_CTRL` 노드 연동
- Bluetooth / UART / Wi-Fi / TCP 통신 통합
- Raspberry Pi C Socket 기반 통신 Client 및 Server 연동 테스트
- STM32CubeIDE 전체 프로젝트 및 `.ioc` 설정 버전 관리

**Tech**

`STM32F411RE` `C` `STM32 HAL` `CubeMX`  
`UART` `I2C` `ADC` `EXTI` `PWM`  
`HC-06` `ESP-01` `TCP/IP` `Raspberry Pi` `Git`

---

## ⚙️ [Bluetooth 기반 회전체 상태 모니터링 시스템](https://github.com/wooseokkim1992-byte/firmware_project)

STM32 2-Node 구조를 기반으로 회전체의 진동과 소음을 실시간 측정하고,  
이상 상태를 판정하여 원격 관제 및 안전 정지를 수행하는 임베디드 시스템입니다.

### 담당 역할

- MPU6050 3축 가속도 데이터 수집
- Sensor Offset 및 중력 성분 제거
- Noise Filtering
- 3축 합성 진동값 계산
- RMS / Peak 특징값 추출
- Threshold / Hysteresis / Persistence 기반 상태 판정
- DANGER 상태와 Relay Motor Stop 기능 통합

### 주요 기능

- MPU6050 기반 진동 측정
- Sound Sensor ADC + DMA 연속 수집
- NORMAL / WARNING / DANGER 상태 판정
- HC-05 Bluetooth 기반 STM32 간 통신
- OLED / LCD / RGB LED / Buzzer 상태 표시
- E-STOP 및 위험 상태 발생 시 모터 안전 정지

**Tech**

`STM32F411RE` `C` `STM32 HAL` `MPU6050`  
`I2C` `ADC` `DMA` `UART` `HC-05`

---

## 🎬 [Movie Poster Quiz](https://github.com/ruruo1385/mini_proj_one)

영화 포스터의 일부분을 보고 제목을 맞히는  
PySide6 기반 데스크톱 퀴즈 애플리케이션입니다.

### 주요 기능

- 난이도별 이미지 분할
- 문제별 제한시간
- 점수 계산 시스템
- 영화 이미지 및 데이터 관리
- Windows 실행 파일 빌드

**Tech**

`Python` `PySide6`

---

## 🔎 Currently Learning

```text
Embedded C
STM32 Firmware
Linux System Programming
TCP/IP Communication
On-device AI
Computer Vision
```

하드웨어 제어와 AI 추론이 실제 장치에서 연결되는  
**Embedded / Edge AI System**을 만드는 것을 목표로 공부하고 있습니다.
