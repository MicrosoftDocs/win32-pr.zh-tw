---
description: 設定電腦的電源狀態。 這種方法的用法已被取代。 請改為在相關聯的 PowerManagementService 類別中使用 SetPowerState 方法。
ms.assetid: c2196f35-f687-4d82-a068-f8499f77473a
title: CIM_ComputerSystem 類別的 SetPowerState 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ComputerSystem.SetPowerState
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9c9e264e8ec62c1e49e92226d1abc8ac902c0b2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104026894"
---
# <a name="setpowerstate-method-of-the-cim_computersystem-class"></a>CIM SetPowerState 類別的方法 \_

設定電腦的電源狀態。 這種方法的用法已被取代。 請改為在相關聯的 **PowerManagementService** 類別中使用 **SetPowerState** 方法。

## <a name="syntax"></a>語法


```mof
uint32 SetPowerState(
  [in] uint32   PowerState,
  [in] datetime Time
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*>powerstate* \[在\]
</dt> <dd>

電腦系統所需的狀態。

<dt>

<span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>

**Full Power** (1) 


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

省 **電-低電源模式** (2) 


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

省 **電-待命** (3) 


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Other"></span><span id="power_save_-_other"></span><span id="POWER_SAVE_-_OTHER"></span>

省 **電-其他** (4) 


</dt> <dd></dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

**電源週期** (5) 


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

**關閉** (6) 的電源


</dt> <dd></dd> <dt>

<span id="Hibernate"></span><span id="hibernate"></span><span id="HIBERNATE"></span>

**休眠** (7) 


</dt> <dd></dd> <dt>

<span id="Soft_Off"></span><span id="soft_off"></span><span id="SOFT_OFF"></span>

**軟關閉** (8) 


</dt> <dd></dd> </dl> </dd> <dt>

*時間* \[在\]
</dt> <dd>

Time 指出應該設定電源狀態的時間，可以是一般的日期時間值，或做為間隔值， (在) 收到方法調用時的間隔開始時間。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8.1<br/>                                                                                  |
| 最低支援的伺服器<br/> | Windows Server 2012 R2<br/>                                                                       |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ 未進行**](cim-computersystem.md)
</dt> </dl>

 

 




