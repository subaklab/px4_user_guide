# FunCub QuadPlane (Pixhawk)

Fun Cub QuadPlane VTOL은 표준 tailplane 비행체(Multiplex FunCub)로 쿼드콥터 시스템이 추가되었습니다.


핵심 정보:

- **프레임:** Multiplex FunCub
- **Flight controller:** Pixhawk

![Fun cub VTOL](../../images/fun_cub_vtol_complete.jpg)

Fun Cub은 비교적 저렴하고 날리기 쉽습니다. 개조한 후에는 무거워지고 비행성이 떨어집니다. 여전히 잘 날지만 전진 비행(forward flight)에 대략 75% throttle이 필요합니다.


## 구성품

실제 비행체는 대략 위에 이미지에서 보는 바와 같습니다.(여기서 사용한 것은 Multiplex Fun Cub이며 다른 유사항 모델도 사용가능) 최소 필요한 구성품 :

-   Multiplex FunCub (혹은 유사품)
-   Pixhawk 혹은 호환
-   디지털 airspeed 센서
-   900 kV 모터 (Iris 추진 세트 - 모터와 ESC)
-   10" props 쿼드 모터 (10x45 혹은 10x47)
-   10" prop fixed-wing 모터 (10×7)
-   GPS 모듈
-   4S 배터리
-   쿼드 모터 마운팅 가능한 알루미늄 프레임 (10x10mm square 튜브, 1mm 두께)
-   4200mAh 4S 배터리로 ~2.3kg 이상 올리기 가능

## 구조

구조는 아래 보이는 것처럼 알루미늄으로 구성되어 있습니다.

![quad_frame](../../images/fun_cub_aluminium_frame_for_vtol.jpg)
![Fun Cub -frame for vtol mounted](../../images/fun_cub_aluminium_frame_for_vtol_mounted.jpg)

## 연결

Pixhawk과 외부연결은 다음과 같습니다.(방향은 "비행체에 올리기"에서 보는 바와 같음)

> **성공** servo 방향은 QGroundControl의 PWM_OUTPUT group에 있는 PWM\_REV 파라미터를 사용해서 반대방향으로도 가능합니다.(cogwheel tab으로 왼쪽 메뉴의 마지막 아이템)

Port | Connection
--- | ---
MAIN 1 | Front right motor (CCW)
MAIN 2 | Back left motor (CCW)
MAIN 3 | Front left motor (CW)
MAIN 4 | Back right motor (CW)
AUX 1  | Left aileron TODO
AUX 2  | Right aileron
AUX 3  | Elevator
AUX 4  | Rudder
AUX 5  | Throttle

연결과 설정에 관한 추가 정보는 다음을 참고하세요 :
[표준 VTOL 연결과 설정](../config/standard_configuration_vtol_quad.md). <!-- replace with Pixhawk Wiring Quickstart -->

## 에어프레임 설정

아래 QGroundControl에서 보는 바와 같이 프레임을 설정
(위에 있는 **Apply and Restart** 클릭하는 것을 잊지마세요).

![QCG - Fun Cub 쿼드 펌웨어](../../images/qgc_firmware_standard_vtol_fun_cub_quad.png)

## 비디오

{% youtube %}
http://www.youtube.com/watch?v=4K8yaa6A0ks
{% endyoutube %}



## 지원

VTOL 개조나 설정에 대해서 궁금한 사항이 있으면 <http://discuss.px4.io/c/vtol>에 방문해 주세요.
