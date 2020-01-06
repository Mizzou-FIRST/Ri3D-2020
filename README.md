# Mizzou FIRST Ri3D 2020

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

| Input | Function |
| ----- | -------- |


## CAN Config

| Device Name   | ID  |
| ------------- | --- |
| PDB           | 1   |
| PCM           | 2   |
| Fly_Motor_R   | 3   |
| Fly_Motor_L   | 4   |
| Climb_Motor_M | 5   |
| Climb_Motor_S | 6   |
| ExtraTalon    | 7   |
| ExtraVictor   | 8   |

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

| Name          | Number |
| ------------- | ------ |
| Joy_L         | 0      |
| Joy_R         | 1      |
| Drive_Motors  | 2      |
| Climb_Motor_M | 3      |
| Climb_Motor_S | 4      |
| Intake_Motor  | 5      |
| Fly_Motor_R   | 6      |
| Fly_Motor_L   | 7      |

### typedef_enum_Begin_State

Begin state machine

| Name         | Number |
| ------------ | ------ |
| Joy_Setup    | 0      |
| Drive_Setup  | 1      |
| Climb_Setup  | 2      |
| Intake_Setup | 3      |
| Fly_Setup    | 4      |
| Stop         | 5      |

### typedef_enum_Teleop_State

Teleop state machine

| Name         | Number |
| ------------ | ------ |
| Read Joy     | 0      |
| Calc Drive   | 1      |
| Calc Intake  | 2      |
| Calc Lift    | 3      |
| Calc Fly     | 4      |
| Write Drive  | 5      |
| Write Intake | 6      |
| Write Lift   | 7      |
| Write Fly    | 8      |

### typedef_cluster_Teleop_Local_Data

| Name          | Type                     | I/O    |
| ------------- | ------------------------ | ------ |
| JoyStick_L    | typedef_cluster_Joystick | Input  |
| JoyStick_R    | typedef_cluster_Joystick | Input  |
| Drive_Forward | Double                   | Output |
| Drive_Twist   | Double                   | Output |
| Intake        | Double                   | Output |
| Lift          | Double                   | Output |
| Fly_SP        | Double                   | Output |

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
