# SMG2 TripodBossReturns

## Megaleg in SMG2

This is the long awaited port of Megaleg to SMG2!

Below is a list of everything that's included:
- The ObjectData archives for every individual piece of Megaleg, as well as Megaleg's ""model"".
- The "TripodBoss", "TripodBossBaseJointPosition", "TripodBossStepPoint", "TripodBossCore", "TripodBossGuardWall", "TripodBossShell", "TripodBossKillerGenerater", "TripodBossBottomKillerCannon", "TripodBossUnderKillerCannon", "TripodBossUpperKillerCannon", "TripodBossCoin", and "TripodBossPurpleCoin" objects in the Editor.
- The "TripodBossStepStartArea" area in the Editor.
- The "TripodBossFixParts" and "TripodBossRotateParts" ProductMapObjDataTable classes.
- The "CAM_TYPE_TRIPOD_BOSS_JOINT" and "CAM_TYPE_CHARMED_TRIPOD_BOSS" camera types.

Below is a list of other things that you will need:

- A level editor

## Credits
@shibbo - Decompiling a majority of TripodBoss and it's related classes
@headpenguin - double checked all of the decompilation work to try and find errors
@superhackio - Ported and enhanced SMG1 code to SMG2

## Setup
It is adviced to reference the template mod for this port. Regardless here are some parameters that we could document.

### TripodBoss
| Parameter | Description |
| --- | --- |
| Obj_arg0 | The object to display inside TripodBossCore. Default is 13 (Grand Star). Reference Obj_arg7 on CrystalCage. |
| Obj_arg1 | (New) If set, the stage's music won't be overridden by Megaleg's cutscenes. |
| Obj_arg2 | (New) If set, the opening cutscene will be skipped and Megaleg will already be in place. |
| SW_DEAD | Activated after the destruction cutscene(?). |
| SW_A | Starts the opening cutscene when activated. |
| SW_B | Starts destruction cutscene when activated. |

### TripodBossCore
| Parameter | Description |
| --- | --- |
| Obj_arg0 | Connected Joint ID on TripodBossBaseJointPosition. |
| Obj_arg7 | (New) If set, the object cannot be destroyed. |
| SW_DEAD | Activated when destroyed. |

### TripodBossShell
| Parameter | Description |
| --- | --- |
| Obj_arg0 | Connected Joint ID on TripodBossBaseJointPosition. |
| SW_DEAD | Activated when destroyed. |

### TripodBossGuardWall
| Parameter | Description |
| --- | --- |
| Obj_arg0 | Connected Joint ID on TripodBossBaseJointPosition. |
| SW_APPEAR | Starts appearance cutscene when activated. |

### TripodBossBaseJointPosition
| Parameter | Description |
| --- | --- |
| Obj_arg0 | Joint ID. |

### TripodBossFixParts (ProductMapObjDataTable class)
| Parameter | Description |
| --- | --- |
| Obj_arg0 | Connected Joint ID on TripodBossBaseJointPosition. |
| Obj_arg1 | Unknown. |
| Obj_arg2 | Unknown. |

### TripodBossRotateParts (ProductMapObjDataTable class)
| Parameter | Description |
| --- | --- |
| Obj_arg0 | Connected Joint ID on TripodBossBaseJointPosition. |
| Obj_arg1 | Unknown. |
| Obj_arg2 | Unknown. |
| RotateSpeed | Negative values make the gears rotate clockwise. |
| RotateAxis | 0 = X-axis, 1 = Y-axis, 2 = Z-axis. |
The MapPart parameters might be identical to RotateMoveObj.

### TripodBossCoin / TripodBossPurpleCoin (New)
| Parameter | Description |
| --- | --- |
| Obj_arg0 | Connected Joint ID on TripodBossBaseJointPosition. |