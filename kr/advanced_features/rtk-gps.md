# RTK GPS

RTK (Real Time Kinematik)은 센티미터 레벨까지 GPS 정확성을 증가시킵니다. PX4는 [u-blox M8P](https://www.u-blox.com/en/product/neo-m8p) GPS 장치로 RTK GPS을 지원합니다. 이 페이지에서 필요한 셋업에 대해서 설명합니다.

여러분이 필요한 것 :

- u-blox M8P GPS 장치 2개
- QGroundControl이 설치된 랩톱/PC (아직 모바일 장치는 지원하지 않음)
- WiFi가진 비행체를 랩톱에 연결 (예제로 Pixracer)

WiFi 링크로 대역폭이 충분한지 항상 테스트했습니다. telemetry 링크를 사용하는 것도 가능합니다.

## 셋업 & 사용법

기본 GPS 장치는 사용할 때 고정된 위치에 있어야 합니다. 따라서 움직이지 않게 하고 하늘을 바로 바라보게 합니다. 빌딩 건물에 가로막히지 않도록 합니다. 높은 곳에 위치시키는 것이 좋습니다.(삼각대를 사용하거나 지붕 위에) 일반 GPS와 비교할때 RTK는 더 민감해서 주의를 기울여서 셋업해야 합니다.

처음으로 QGroundControl을 시작하고 기본 GPS를 USB를 이용해서 랩톱에 연결합니다. GPS는 자동으로 인식합니다. 콘솔 윈도우 출력으로 전환해서 매초 업데이트되는 것을 볼 수 있습니다.(아래 이미지 참고) 콘솔로 QGroundControl을 시작시켰다면, 상태 업데이트도 볼 수 있습니다.(동작하지 않는 경우 일반 어플리케이션 셋팅에서 RTK GPS에 자동연결이 설정되어 있는지 확인합니다.)

![survey-in 스크린샷](../../images/qgc_rtk_survey_in.png)

survey-in 진행 상태입니다. 베이스 스테이션의 정확한 위치를 추정하기 위한 시작 동작입니다. 설정되는데 적어도 3분이 걸리며 1미터의 정확도까지 도달해야만 합니다. 현재 정확도가 콘솔에 출력됩니다. 완료되는데 수 분이 걸리는데 GPS신호 수신에 따라 다를 수 있습니다.

survey-in이 실행되는 동안, 비행체를 동작시키고 QGroundControl에 연결할 수 있습니다. 비행체에 추가로 셋업이 필요하지는 않습니다. 일단 survey-in 절차가 끝나면, QGroundControl이 자동으로 RTCM 보정 데이터를 비행체로 보내기 시작합니다. 잠시 후에 RTK 모드로 전환해야만하며 이는 GPS 상태(3D RTK GPS Lock)로 표시됩니다. :

![RTK GPS 상태](../../images/qgc_rtk_gps_status.png)

2개 RTK 모드 : 유동과 고정. 유동 모드가 더 쉽지만 고정 모드보다 덜 정확합니다.(추가 설명은 [여기](http://www.ehow.com/info_12245568_difference-between-rtk-fix-rtk-float.html)) 신호강도가 충분한 경우에 시스템은 자동으로 고정 모드로 전환됩니다.

이제 비행을 시작할 수 있습니다!

일부 파라미터는 튜닝이 필요할 수 있습니다. 기본 파라미터들은 GPS 정확도가 센티미터가 아닌 미터로 가정하고 튜닝하기 때문입니다.

## 비디오 데모

{% youtube %}
https://youtu.be/en_a5XBx2vU
{% endyoutube %}

(Michael Ammann이 제작한 비디오)
