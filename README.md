# Mizzou FIRST Ri3D 2020

## CAN Config

| Device Name | ID  |
| ----------- | --- |
| Fly_Motor_R | 0   |
| Fly_Motor_L | 1   |

## I/O

| Name               | Port  |
| ------------------ | ----- |
| Sparkx Rear Left   | PWM 0 |
| Sparkx Rear Right  | PWM 1 |
| Sparkx Front Left  | PWM 2 |
| Sparkx Front Right | PWM 3 |
| Sparkx Intake      | PWM4  |

## TypeDefs

### typedef_enum_refnums

| Name          | Number |
| ------------- | ------ |
| Joy_L         | 0      |
| Joy_R         | 1      |
| Drive_Motors  | 2      |
| Lift_Motors   | 3      |
| Intake_Motors | 4      |
| Fly_Motor_R   | 5      |
| Fly_Motor_L   | 6      |

### typedef_enum_Begin_State

Begin state machine

| Name         | Number |
| ------------ | ------ |
| Joy_Setup    | 0      |
| Drive_Setup  | 1      |
| Lift_Setup   | 2      |
| Intake_Setup | 3      |
| Fly_Setup    | 4      |
| Stop         | 5      |

### typedef_enum_Teleop_State

Teleop state machine

| Name        | Number |
| ----------- | ------ |
| Read Joy    | 0      |
| Calc Drive  | 1      |
| Write Drive | 2      |

### typedef_cluster_Teleop_Local_Data

| Name          | Type                     | I/O    |
| ------------- | ------------------------ | ------ |
| JoyStick_L    | typedef_cluster_Joystick | Input  |
| JoyStick_R    | typedef_cluster_Joystick | Input  |
| Drive_Forward | Double                   | Output |
| Drive_Twist   | Double                   | Output |

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
