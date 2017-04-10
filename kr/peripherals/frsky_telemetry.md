# FrSky Telemetry

PX4는 D (예전)와 S (새로운) FrSky telemetry를 지원합니다. FMUv4 기반 보드(Pixracer)에는 이미 필요한 인테페이스가 포함되어 있습니다. 예전 보드(Pixhawk)에는 S.PORT 어댑터 보드에 UART가 필요합니다.

## Pixracer

> **성공** FrSky telemetry는 Pixracer에서 자동으로 시작되고 D나 S 모드를 탐지하므로 별도의 설정이 필요없습니다.

D-port(D4R-II와 동일 모델)를 지원하는 리시버 : Pixracer FrSky TX 라인을 D4R-II 라인에 연결하며 GND도 연결.
S-port를 지원하는 리시버 : Pixracer FrSky Tx와 Rx 라인(라인을 함께 납땜)을 함께 X 시리즈 리시버의 S.port 핀에 연결하며 GND도 연결.
