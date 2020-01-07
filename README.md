# Mizzou FIRST Ri3D 2020

Rio DNS: roboRIO-3792-FRC.local

Rio IP: 10.37.92.2

## Adam's Sleepy Checklist

- Fix CAN
  - Add Motor Controller
  - Validate IDs
  - Fix Begin
- Drink Water
- Setup Drive
- Setup Intake
- Setup Err

## Controls

Joysticks used are Logitec 3D Pros

### Joystick Right - Drive

| Input           | Function       |
| --------------- | -------------- |
| Y Axis Forward  | Drive forward  |
| Y Axis Backward | Drive backward |
| Z Axis Left     | Turn left      |
| Z Axis Right    | Turn right     |

### Joystick Left - Actuators

| Input   | Function     |
| ------- | ------------ |
| Trigger | Intake Motor |

## CAN Config

| Device Name   | ID  |
| ------------- | --- |
| PDB           | 1   |
| PCM           | 2   |
| Fly_Motor_R   | 3   |
| Fly_Motor_L   | 4   |
| Winch_Motor_M | 5   |
| Winch_Motor_S | 6   |
| Erector       | 7   |
| Fortune       | 8   |
| CrabWalk      | 9   |

## I/O

| Name               | Port  |
| ------------------ | ----- |
| Sparkx Front Left  | PWM 0 |
| Sparkx Rear Left   | PWM 1 |
| Sparkx Front Right | PWM 2 |
| Sparkx Rear Right  | PWM 3 |
| Sparkx Intake      | PWM 4 |

## TypeDefs

### typedef_enum_refnums

| Name             | Number |
| ---------------- | ------ |
| Joy_L            | 0      |
| Joy_R            | 1      |
| Drive_Motors     | 2      |
| Drive_Encoders_R | 3      |
| Drive_Encoders_L | 4      |
| Winch_Motor_M    | 5      |
| Winch_Motor_S    | 6      |
| Erector_Motor    | 7      |
| Slider_Motor     | 8      |
| Intake_Motor     | 9      |
| Fly_Motor_R      | 10     |
| Fly_Motor_L      | 11     |
| Fortune_Motor    | 12     |

### typedef_enum_Begin_State

Begin state machine

| Name             | Number |
| ---------------- | ------ |
| Joy_Setup        | 0      |
| Drive_Setup      | 1      |
| Encoder_Setup    | 2      |
| Winch_Setup      | 3      |
| Erector_Setup    | 4      |
| Slider_Setup     | 5      |
| Intake_Setup     | 6      |
| Fly_Setup        | 7      |
| Fortune_Setup    | 8      |
| Compressor_Setup | 9      |
| Stop             | 10     |

### typedef_enum_Teleop_State

Teleop state machine

| Name          | Number |
| ------------- | ------ |
| Read_Joy      | 0      |
| Read_Encoders | 1      |
| Calc_Drive    | 1      |
| Calc_Intake   | 2      |
| Calc_Fly      | 3      |
| Calc_Winch    | 4      |
| Calc_Erector  | 5      |
| Calc_Slider   | 6      |
| Calc_Fortune  | 7      |
| Write_Drive   | 8      |
| Write_Intake  | 9      |
| Write_Fly     | 10     |
| Write_Winch   | 11     |
| Write_Erector | 12     |
| Write_Slider  | 13     |
| Write_Fortune | 14     |
| Stop          | 15     |

### typedef_cluster_Teleop_Local_Data

| Name            | Type                     | I/O    |
| --------------- | ------------------------ | ------ |
| JoyStick_L      | typedef_cluster_Joystick | Input  |
| JoyStick_R      | typedef_cluster_Joystick | Input  |
| Drive_Encoder_L | Double                   | Input  |
| Drive_Encoder_R | Double                   | Input  |
| Drive_Forward   | Double                   | Output |
| Drive_Twist     | Double                   | Output |
| Intake_PWR      | Double                   | Output |
| Fly_SP          | Double                   | Output |
| Winch_SP        | Double                   | Output |
| Erector_SP      | Double                   | Output |
| Slider_PWR      | Double                   | Output |
| Fortune_SP      | Double                   | Output |

### typedef_cluster_Joystick

| Name      | Type    |
| --------- | ------- |
| X         | Double  |
| Y         | Double  |
| Z         | Double  |
| Throttle  | Double  |
| Trigger   | Boolean |
| Thumb     | Boolean |
| Top 3     | Boolean |
| Top 4     | Boolean |
| Top 5     | Boolean |
| Top 6     | Boolean |
| Bottom 7  | Boolean |
| Bottom 8  | Boolean |
| Bottom 9  | Boolean |
| Bottom 10 | Boolean |
| Bottom 11 | Boolean |
| Bottom 12 | Boolean |
