# Day Log


### 12.07.2024
#### 水下清洗ROV装配：

- [ ] 10g环氧树脂

- [x] 1号插头焊接10pin：
    - 6pin舵机
    - 2pin水泵

- [ ] 2号插头焊接10pin：
    - 4pin网线
    - 2pin开关
    - 4pin摄像头
  
- [ ] 3号插头焊接10pin：
    - 4pin深度传感器排线
    - 4pinLED

- [ ] 组装另一摄像头模块
    - 排摄像头USB线
    - 灌装环氧树脂
    - 4h后套上橡胶圈

- [ ] 摄像头模块装配上铝型材
- [ ] 舵机模块装配上铝型材
- [ ] 水泵模块装配上铝型材
- [ ] 电子管内线缆连接 ！！！
    - a. 编排 18pin 和 20pin 的**Molex公头**线序
      > **18pin公头** 为6个电机在电子管内的红黑黄线，分别对应到外部6个电机(即通过端盖上外圈的6个稍细插头连接到外部)
      > **20pin公头** 为4pin深度传感器+4pinLED+6pin舵机+2pin开关在电子管内的接线，分别对应到外部的相应组件(即通过端盖上中间的3个稍粗插头连接到外部)
    - b. 根据a步编排的Molex公头线序对应布置**Molex母头**线序
      > 即将端盖上相应的压线插入Molex母头，并能与公头插接后一一对应正确
    - c. 用万用表检测是否存在坏道

#### 捕鱼达人ROV装配：

- [ ] [电子管]推进器Molex压线**18**pin:
    - **公头**：6红6黑6黄 = 18 
    > 其中6黄一端为Molex母头，另一端为杜邦母头
    - **母头**：6红6黑6黄 = 18

- [ ] [电子管]-外部组件Molex**母头**压线**20**pin:
    - 4pin深度传感器(4灰白色)
    - 4pinLED(2红2黑)
    - 2pin开关(2红)
  
- [ ] [电子管]-外部组件Molex**公头**压线**20**pin:
    - 4pin深度传感器(4灰白色)
    - 4pinLED(2红2黑)
    - 2pin开关(2红)

- [ ] [电子管]-外部组件xh2.54**母头**压线:
    - 4pinUSB线
    - 4pin网线

- [ ] [电子管]-外部组件xh2.54**公头**压线:
    - 4pinUSB线
    - 4pin网线

- [ ] 1号插头无需焊接10pin:
    - 2pin蓝诱鱼灯
    - 2pin绿诱鱼灯
    - 2pin绿诱鱼灯(是否需要三灯？)

- [ ] 2号插头焊接10pin：
    - 4pin网线
    - 2pin开关
    - 4pin摄像头
    - 灌装环氧树脂

- [ ] 3号插头焊接10pin：
    - 4pin深度传感器排线
    - 4pinLED
    - 灌装环氧树脂

- [ ] 6推进器装配上铝型材
- [ ] 侧翼板装配上铝型材
- [ ] 2个诱鱼灯装配上ROV


### 11.07.2024
水下清洗ROV组装：

- [x] 电子管接线18pin：
    - 4pin深度传感器排线(4灰白色)
    - 6pin舵机(2黄2红2黑)
    - 4pinLED(2红2黑)
    - 2pin水泵(1红1黑)
    - 2pin开关(2红)


- [ ] 1号插头焊接10pin：
    - 6pin舵机
    - 2pin水泵

- [ ] 2号插头焊接10pin：
    - 4pin网线
    - 2pin开关

- [ ] 3号插头焊接10pin：
    - 4pin深度传感器排线
    - 4pinLED


### 10.07.2024
水下清洗ROV：
- [x] 组装框架
- [x] 组装电机(其中1个需要重新灌装**环氧树脂**)
- [x] 电子管**压线**接线
- [x] LED灯**环氧树脂**灌装
- [ ] 压力传感器**环氧树脂**灌装


### 08.07.2024
- [x] 大创2023项目 >> A1资料整理
- [x] 连接舵机云台




# ROV
![百年校庆Logo](百年校庆LOGO.png)

## Electronic Pipe

### RC input and output
**RC Inputs**
These are the default channel mappings for RC input:

Channel|Meaning
----|-------
1	|Pitch
2	|Roll
3	|Throttle
4	|Yaw
5	|Forward
6	|Lateral
7	|Camera Pan
8	|Camera Tilt*
9	|Lights 1 Level
10	|Lights 2 Level
11	|Video Switch

Pixhawk Label|Servo Channel
--------|---
Main 1	|1
Main 2	|2
Main 3	|3
Main 4	|4
Main 5	|5
Main 6	|6
Main 7	|7
Main 8	|8
Aux 1	|9
Aux 2	|10
Aux 3	|11
Aux 4	|12
Aux 5	|13
Aux 6	|14

![RCradio.cpp](/NoteImages/image-1.png)

---
### Software Reference
1. [Raspberry Pi Pinout](https://pinout.vvzero.com/)
2. [QGC Guide](https://docs.qgroundcontrol.com/Stable_V4.3/en/qgc-user-guide/)
3. [Ardusub](https://www.ardusub.com/)
4. [RC input and output](https://www.ardusub.com/developers/rc-input-and-output.html)


---
## Modeling



### 外部组件
1. LED灯位置
2. LED驱动器位置
3. 推进器涵道与铝型材连接部件（[推进器参数](#thruster)）
4. 推进器位置
5. 推进器与铝型材的连接部件(2020角码)
6. 摄像头位置
7. MOS管位置

### 电子管
1. 端盖
2. 橡胶圈


### 特殊组件
#### 水下清洗ROV
1. 喷水系统
2. 舵机![舵机信息](/NoteImages/image-2.png)

#### 捕鱼达人ROV
1. 诱鱼灯位置及支架
2. 



---
### Modeling Reference
1. <span id="thruster">推进器参数</span>
![推进器参数](/NoteImages/image.png)



