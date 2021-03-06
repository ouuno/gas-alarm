# gas-alarm

**이산화탄소 농도 알림 및 환기 장치**

## **기능**

### **기본**

| 농도 단계 | ppm 범위 | LED | 부저 |
|:--------:|:--------:|:--------:|:--------:|
| **0** | - 700 ppm | X | X |
| **1** | 700 ppm - 1000 ppm | 녹색(Green) | X |
| **2** | 1000 ppm - 2000 ppm | 황색(Yellow) | X |
| **3** | 2000 ppm - 3000 ppm | 적색(Red) | 긴 주기 |
| **4** | 3000 ppm - | 적색(Red) | 짧은 주기 |

* **LCD**
    - 현재 농도 단계 & ppm 농도 출력
    - 오른쪽 아래에 음소거 설정 여부 출력 (음소거 되어있으면 '\*M\*'이 표시됨)

* **팬**
    - 농도 단계가 `4`인 경우, 작동 시작
    - 농도 단계가 `2 이하`일 때 까지 작동 유지

### **부저 중지 / 음소거**

* 농도 단계가 `3`인 경우
    - 부저를 일시 중지할 수 있음 (120초)
    - 음소거가 되어있는 경우, 부저가 울리지 않음

* 농도 단계가 `4`인 경우
    - 부저를 일시 중지할 수 **없음**
    - 음소거가 되어있더라도 부저가 울림

## **부품 목록**

### *Arduino UNO*

### 사용 모듈 (제품번호, 라이브러리)

* CO2 Sensor ([MG811](https://github.com/smart-tech-benin/MG811.git))
* RGB LED (KY-016)
* LCD ([I2C LCD 1602](https://github.com/fdebrabander/Arduino-LiquidCrystal-I2C-library.git))
* Fan Motor (SZH-EK061)
