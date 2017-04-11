# BirdsEyeView FireFly Y6 Tiltrotor VTOL (Pixhawk)

[BirdsEyeView FireFly Y6](https://www.birdseyeview.aero/products/firefly6-diy-25) Tiltrotor VTOL는 매핑, 스포츠, 화물 비행기입니다. 여기서는 *Pixhawk*을 사용하는 프레임에 대해서 만들고 설정하는 방법을 다룹니다. *QGroundControl*을 사용해서 PX4 오토파일롯을 설정하는 방법도 포함하고 있습니다.

핵심 정보:

- **프레임:** [BirdsEyeView FireFly Y6](https://www.birdseyeview.aero/products/firefly6-diy-25) DIY
- **Flight controller:** Pixhawk

![BirdsEyeView Firefly Y6](../../images/birdseyeview_firefly_y6_vtol_props.jpg)

## Airframe 셋업

### Propeller 방향

프로펠러가 제대로 설치되어 있는지 확인합니다. 여기 사진은 각 프로펠러의 방향을 보여줍니다. 위에 있는 모터는 CCW 방향으로 회전해야합니다. 반면에 바닥에 있는 모터는 CW 방향으로 회전해야 합니다. ESC는 모터에 이미 납땜이 된 상태이므로 회전 방향은 고정입니다.(위는 CCW고 바닥은 CW입니다.)

![BirdsEyeView Firefly Y6](../../images/birdseyeview_firefly_y6_vtol_props.jpg)

![](../../images/birdseyeview_firefly_y6_vtol_props_1.jpg)
![](../../images/birdseyeview_firefly_y6_vtol_props_2.jpg)
![](../../images/birdseyeview_firefly_y6_vtol_props_3.jpg)

### 오토파일롯과 주변장치와 연결

아래 사진은 Pixhawk, telemetry 라디오, GPS를 설치하는 방법 중에 하나를 보여줍니다. GPS를 전원분배보드(power distribution board) 위에 둔다면, 외부 magnetometer로 사용하기 어려울 수 있습니다.

![](../../images/birdseyeview_firefly_y6_vtol_firefly_internals.jpg)

위의 경우 내장 magnetometer에 심각한 자기 방해가 발생했습니다. 벤치 테스트에서 스로틀을 올리는 경우(프로펠러는 current flowing을 감당할 수 있어야) 드리프팅 헤딩(drifting heading)이 나타나면 외부 GPS magnetometer를 사용하고 사진과 같이 날개쪽으로 옮겨야 할 수도 있습니다. 물론 케이블 연결도 개선시켜야 합니다.

![](../../images/birdseyeview_firefly_y6_vtol_firefly_ext_mag.jpg)

### 모터와 Servo 셋업

- 모터를 Pixhawk의 메인 출력(MAIN OUT)에 연결
- tilt-rotor servo를 AUX OUT1에 연결
- 2개 elevon servo를 AUX OUT2-3에 연결
- 랜딩 기어의 servo 케이블을 AUX OUT4에 연결

![](../../images/birdseyeview_firefly_y6_vtol_firefly_motor_connections.jpg)

## 펌웨어 & 셋팅


*QGroundControl*를 사용해서 안정버전의 펌웨어를 설치합니다. *QGroundControl*에서 “**VTOL Tiltrotor**” 아래에 있는 “**BirdsEyeView Aerobotics FireFly6**” airfrmae 설정을 선택하고 재시작합니다.

![QGC - BirdsEyeView Firefly y6의 펌웨어 선택](../../images/qgc_firmware_tiltrotor_firefly_y6.png)

----

airframe이 유효하지 않는 경우 다음 파라미터를 설정하고 재시작합니다. :

-   SYS\_AUTOSTART to 13002
-   SYS\_AUTOCONFIG to 1

리부팅 후에 설정값은 표준 파워 팩과 매치합니다. 다음 테이블은 높은 효율 셋업을 이용할 때 가이드로 사용할 수 있습니다.


Parameter | Standard | High-Efficiency
--- | --- | ---
MC_PITCHRATE_FF | 0.0 | 0.0
MC_PITCHRATE_D | 0.004 | 0.005
MC_PITCHRATE_I | 0.002 | 0.09
MC_PITCHRATE_P | 0.14 | 0.125
MC_PITCH_P | 7.0 | 6.0
MC_ROLLRATE_FF | 0.0 | 0.0
MC_ROLLRATE_D | 0.005 | 0.003
MC_ROLLRATE_I | 0.002 | 0.06
MC_ROLLRATE_P | 0.19 | 0.125
MC_ROLL_P | 7.0 | 6.35
MC_YAW_FF | 0.5 | 0.3
MC_YAWRATE_FF | 0.0 | 0.0
MC_YAWRATE_D | 0.0 | 0.0
MC_YAWRATE_I | 0.02 | 0.0
MC_YAWRATE_P | 0.22 | 0.35
MC_YAW_P | 4.0 | 2.6


이제 시스템은 센서 칼리브레이션 준비가 되었으며 과정을 마치면 arming이 가능합니다.

노트:

-   fixed-wing으로 전환시키는데 필요한 전환 스위치를 할당해야 함
-   기본적으로 stabilization으로 되어 있음. fixed-wing에서 완전 수동 비행을 하고 싶은 경우, VT\_FW\_PERM\_STAB을 0으로 설정.

가장 먼저 해야할 일은 멀티콥터 모드로 시작하고 비행체에 익숙해지는 것입니다. 비행체의 PID 자세 제어기는 *QGroundControl* 로 튜닝이 가능합니다.
