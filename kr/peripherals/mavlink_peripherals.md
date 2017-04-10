# MAVLink (OSD/Telemetry)

## TELEM1 포트

telemetry 1 포트는 기본으로 57600 baud, 8N1을 기본설정으로 하며 MAVLink 스트림을 전송합니다.

## TELEM2 포트

MAVLink 설정은 OSD 모드에서 57600 baud를 기본값으로 합니다.

SYS_COMPANION 파라미터를 **드롭다운 메뉴**로 설정하는 경우 어플리케이션 시나리오에 따라서 모드를 선택할 수 있습니다.

-   컴패니온 컴퓨터 모드는 921600 baud
-   컴패니온 컴퓨터 모드는 57600 baud
-   OSD 모드는 57600 baud
-   Command / RC input 모드(수신 경우)는 57600 baud
-   일반 telemetry 모드는 57600 baud

![QGC Telemetry 셋업](../../images/qgc_telemetry_setup.png)
