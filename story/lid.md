# 화면부 조립

## 새 디스플레이에 순정 펜 디지타이저 붙이기

“그럼 펜 입력은 어떻게 하죠?”라고 물으실 만합니다. 기존 디스플레이에서 펜 디지타이저를 떼어 새 패널에 붙이기로 했습니다. 예전에 X60T를 개조하면서 ESP32-S3 SuperMini로 디지타이저를 USB에 연결한 적이 있습니다. 이번에도 같은 방식입니다. [X60T 디지타이저 USB 연결 기록](https://github.com/bulat-chu/WACOM-ThinkPad-X60T-Digitizer/blob/main/SU-1208E-01X.md)

<img width="1715" height="1098" alt="LCD 패널 뒷면에 부착한 펜 디지타이저와 배선" src="https://github.com/user-attachments/assets/85a62d07-b1c6-4f65-aab6-781372e2b21d" />

저도 새 패널에 붙인 디지타이저가 펜을 인식할지 걱정했습니다. 다행히 패널 뒷면에는 금속박 대신 거울처럼 빛나는 플라스틱 필름이 붙어 있어서 스타일러스를 잘 인식했습니다. 다만 두 가지 짚어 둘 점이 있습니다.

- LCD 패널의 제어 기판을 조심스럽게 떼어 낸 다음, 그 밑에 디지타이저를 붙여야 합니다.
- 펜은 정상적으로 작동했지만 디스플레이 가장자리의 금속 프레임 근처에서는 감도가 떨어지는 구간이 있습니다. 이 부분은 어쩔 수 없었습니다.

패널 자체가 Framework에서 작동하는지도 확인했습니다. 40핀 → 30핀 변환 어댑터로 연결하니 문제없이 화면이 나왔습니다.

<img width="2048" height="1536" alt="나란히 놓인 펜 디지타이저와 교체용 LCD 패널" src="https://github.com/user-attachments/assets/dac21135-027c-4feb-8e00-caff54802a2a" />

<img width="2048" height="1536" alt="Framework에 연결해 화면 출력을 확인한 LCD 패널" src="https://github.com/user-attachments/assets/9d1f50cf-3260-4e4b-a569-e75795172dee" />

디스플레이와 디지타이저가 전기적으로 호환된다는 건 확인했습니다. 두 부품이 안에서 흔들리지 않도록 디스플레이와 뒷덮개 사이에 끼울 스페이서(`spacer.stp`)도 만들었습니다. 스페이서를 넣기 전에 완충용 스펀지를 먼저 깔았습니다.

<img width="2958" height="2279" alt="화면 뒷덮개 안쪽에 넣은 격자 모양 스페이서" src="https://github.com/user-attachments/assets/5ae363c3-53ea-4350-bb14-2b86ad0bd3d2" />

<img width="1565" height="987" alt="디지타이저와 제어 기판이 보이는 디스플레이 뒷면" src="https://github.com/user-attachments/assets/835d38de-026b-46a9-a903-f6586baa4993" />

## 카메라와 케이블 설치

그로부터 두어 달이 지나 카메라와 케이블을 달았습니다.

<img width="2048" height="1536" alt="화면부 위쪽에 자리를 잡은 카메라 모듈" src="https://github.com/user-attachments/assets/7c0ca7d7-328f-4c0f-8214-4504c6ef19e8" />

카메라 고정용 지지대를 두세 개 3D 프린터로 출력합니다. 화면 앞쪽 베젤(B-Shell)의 카메라 구멍에 렌즈가 오도록 지지대 위치를 맞춘 뒤 접착합니다.

<img width="2048" height="1536" alt="분리한 카메라 모듈과 베젤 안쪽의 고정 지지대" src="https://github.com/user-attachments/assets/9af30257-36f5-4fad-b2f7-927546bf4cfa" />

카메라를 올려 위치를 확인하고 리본 케이블이 지나갈 자리를 표시합니다. 표시한 부분을 줄로 조금 갈아 내면 케이블이 들어갑니다.

<img width="1024" height="768" alt="카메라 리본 케이블이 베젤 가장자리를 지나는 모습" src="https://github.com/user-attachments/assets/a36d7eed-3a52-42fe-8a11-f70d439f6809" />

<img width="1280" height="960" alt="베젤에서 카메라 모듈을 분리해 케이블 자리를 드러낸 모습" src="https://github.com/user-attachments/assets/624a5d7c-7477-42dc-9394-951ac1022442" />

사진에서 보이듯이 디스플레이 패널을 가운데에 고정하는 데는 고무 스페이서를 썼습니다.

## 베젤 조립

베젤에 지문 인식기와 3.3 V 전압 레귤레이터를 나사로 고정합니다.

Framework 카메라의 마이크 위치를 맞춰 베젤에 구멍을 뚫습니다. 조도 센서와 표시등의 투명 창에는 투명 필라멘트를 짧게 잘라 끼웠습니다.

덮개가 닫혔는지 감지하는 센서용 자석도 베젤에 붙입니다. **자석 위치는 베젤의 맨 위에서 119 mm 아래이며, 극성은 어느 쪽이든 괜찮습니다.**

<img width="1024" height="768" alt="지문 인식기와 전압 레귤레이터를 장착한 화면 베젤의 안쪽" src="https://github.com/user-attachments/assets/79183e67-a070-4569-84c2-75713c4fd6f0" />

이제 케이블을 연결해 밖으로 빼고 베젤을 닫습니다.

<img width="1851" height="1536" alt="베젤을 닫기 전 화면부 내부와 힌지 쪽으로 빼낸 케이블" src="https://github.com/user-attachments/assets/9b760d5b-bc5a-48b8-a5b5-64fd3fa73866" />

<img width="1802" height="1480" alt="베젤을 조립한 뒤 정면에서 본 화면부" src="https://github.com/user-attachments/assets/0fa5ff41-9e15-4879-beaf-6b026bce7ef0" />

---

남은 일은 상태 표시등과 버튼을 연결하고, 패널에 보호 유리나 필름을 붙이는 겁니다.

다음 편이 이어질지도, 안 이어질지도, 어쩌면…….

<img width="1599" height="774" alt="정면을 바라보는 두 남자의 영화 장면" src="https://github.com/user-attachments/assets/5da26d0f-5502-4c25-9bac-30b41dff6d2d" />
