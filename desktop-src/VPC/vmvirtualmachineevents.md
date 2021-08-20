---
title: 'VMVirtualMachineEvents 列舉 (VPCCOMInterfaces) '
description: 指定 VM 事件。
ms.assetid: 158bdada-6fd3-488c-9ff1-e04df9a79127
keywords:
- VMVirtualMachineEvents 列舉虛擬電腦
topic_type:
- apiref
api_name:
- VMVirtualMachineEvents
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5079aee6752c260cd6bab9ee9022d22fd891eb6adf36ad0ec4d1c9987b6ff508
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998338"
---
# <a name="vmvirtualmachineevents-enumeration"></a>VMVirtualMachineEvents 列舉

\[WindowsVirtual PC 不再適用于 Windows 8。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

指定虛擬機器 (VM) 事件。

## <a name="syntax"></a>Syntax


```C++
typedef enum  { 
  vmVirtualMachineEvent_StateChanged              = 1,
  vmVirtualMachineEvent_RequestShutdown           = 2,
  vmVirtualMachineEvent_Reset                     = 3,
  vmVirtualMachineEvent_TripleFault               = 4,
  vmVirtualMachineEvent_HeartbeatStopped          = 5,
  vmVirtualMachineEvent_ConfigurationChanged      = 6,
  vmVirtualMachineEvent_EnhancedVideoModeChanged  = 7,
  vmVirtualMachineEvent_AdditionsUninstalled      = 8,
  vmVirtualMachineEvent_AdditionsAvailable        = 9,
  vmVirtualMachineEvent_GuestShutdown             = 10,
  vmVirtualMachineEvent_GuestLogoff               = 11,
  vmVirtualMachineEvent_DiskOutOfSpace            = 12
} VMVirtualMachineEvents;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="vmVirtualMachineEvent_StateChanged"></span><span id="vmvirtualmachineevent_statechanged"></span><span id="VMVIRTUALMACHINEEVENT_STATECHANGED"></span>**vmVirtualMachineEvent \_ StateChanged**
</dt> <dd>

VM 的狀態已變更。

</dd> <dt>

<span id="vmVirtualMachineEvent_RequestShutdown"></span><span id="vmvirtualmachineevent_requestshutdown"></span><span id="VMVIRTUALMACHINEEVENT_REQUESTSHUTDOWN"></span>**vmVirtualMachineEvent \_ RequestShutdown**
</dt> <dd>

已要求關機。

</dd> <dt>

<span id="vmVirtualMachineEvent_Reset"></span><span id="vmvirtualmachineevent_reset"></span><span id="VMVIRTUALMACHINEEVENT_RESET"></span>**vmVirtualMachineEvent \_ 重設**
</dt> <dd>

VM 已重設。

</dd> <dt>

<span id="vmVirtualMachineEvent_TripleFault"></span><span id="vmvirtualmachineevent_triplefault"></span><span id="VMVIRTUALMACHINEEVENT_TRIPLEFAULT"></span>**vmVirtualMachineEvent \_ TripleFault**
</dt> <dd>

VM 發生三個錯誤。

</dd> <dt>

<span id="vmVirtualMachineEvent_HeartbeatStopped"></span><span id="vmvirtualmachineevent_heartbeatstopped"></span><span id="VMVIRTUALMACHINEEVENT_HEARTBEATSTOPPED"></span>**vmVirtualMachineEvent \_ HeartbeatStopped**
</dt> <dd>

已停止 VM 的信號。 這通常表示客體作業系統已損毀。

</dd> <dt>

<span id="vmVirtualMachineEvent_ConfigurationChanged"></span><span id="vmvirtualmachineevent_configurationchanged"></span><span id="VMVIRTUALMACHINEEVENT_CONFIGURATIONCHANGED"></span>**vmVirtualMachineEvent \_ ConfigurationChanged**
</dt> <dd>

此 VM 設定中的值已變更

</dd> <dt>

<span id="vmVirtualMachineEvent_EnhancedVideoModeChanged"></span><span id="vmvirtualmachineevent_enhancedvideomodechanged"></span><span id="VMVIRTUALMACHINEEVENT_ENHANCEDVIDEOMODECHANGED"></span>**vmVirtualMachineEvent \_ EnhancedVideoModeChanged**
</dt> <dd>

VM 的影片模式已變更。

</dd> <dt>

<span id="vmVirtualMachineEvent_AdditionsUninstalled"></span><span id="vmvirtualmachineevent_additionsuninstalled"></span><span id="VMVIRTUALMACHINEEVENT_ADDITIONSUNINSTALLED"></span>**vmVirtualMachineEvent \_ AdditionsUninstalled**
</dt> <dd>

已從 VM 卸載整合元件。

</dd> <dt>

<span id="vmVirtualMachineEvent_AdditionsAvailable"></span><span id="vmvirtualmachineevent_additionsavailable"></span><span id="VMVIRTUALMACHINEEVENT_ADDITIONSAVAILABLE"></span>**vmVirtualMachineEvent \_ AdditionsAvailable**
</dt> <dd>

客體作業系統中提供整合功能。

</dd> <dt>

<span id="vmVirtualMachineEvent_GuestShutdown"></span><span id="vmvirtualmachineevent_guestshutdown"></span><span id="VMVIRTUALMACHINEEVENT_GUESTSHUTDOWN"></span>**vmVirtualMachineEvent \_ GuestShutdown**
</dt> <dd>

客體作業系統正在關機。

</dd> <dt>

<span id="vmVirtualMachineEvent_GuestLogoff"></span><span id="vmvirtualmachineevent_guestlogoff"></span><span id="VMVIRTUALMACHINEEVENT_GUESTLOGOFF"></span>**vmVirtualMachineEvent \_ GuestLogoff**
</dt> <dd>

從客體作業系統登出的使用者。

</dd> <dt>

<span id="vmVirtualMachineEvent_DiskOutOfSpace"></span><span id="vmvirtualmachineevent_diskoutofspace"></span><span id="VMVIRTUALMACHINEEVENT_DISKOUTOFSPACE"></span>**vmVirtualMachineEvent \_ DiskOutOfSpace**
</dt> <dd>

VM 所需的磁碟空間不足。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMVirtualMachineEvents**](ivmvirtualmachineevents.md)
</dt> </dl>

 

