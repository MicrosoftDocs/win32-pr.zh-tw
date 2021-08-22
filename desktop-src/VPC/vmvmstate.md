---
title: 'VMVMState 列舉 (VPCCOMInterfaces) '
description: 指定虛擬機器的狀態。
ms.assetid: 952dab9d-3d38-4cc5-ab75-4ee5096f7923
keywords:
- VMVMState 列舉虛擬電腦
topic_type:
- apiref
api_name:
- VMVMState
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cff8beb6d0ea01ab60be7a7908fceec32422ef3a9ba06b801df2af94130c526
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998308"
---
# <a name="vmvmstate-enumeration"></a>VMVMState 列舉

\[WindowsVirtual PC 不再適用于 Windows 8。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

指定虛擬機器的狀態。

## <a name="syntax"></a>Syntax


```C++
typedef enum  { 
  vmVMState_Invalid        = 0,
  vmVMState_TurnedOff      = 1,
  vmVMState_Saved          = 2,
  vmVMState_TurningOn      = 3,
  vmVMState_Restoring      = 4,
  vmVMState_Running        = 5,
  vmVMState_Paused         = 6,
  vmVMState_Saving         = 7,
  vmVMState_TurningOff     = 8,
  vmVMState_MergingDrives  = 9,
  vmVMState_DeleteMachine  = 10
} VMVMState;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="vmVMState_Invalid"></span><span id="vmvmstate_invalid"></span><span id="VMVMSTATE_INVALID"></span>**vmVMState \_ 無效**
</dt> <dd>

如果虛擬機器存在) ，則不應發生的狀態 (無效。

</dd> <dt>

<span id="vmVMState_TurnedOff"></span><span id="vmvmstate_turnedoff"></span><span id="VMVMSTATE_TURNEDOFF"></span>**vmVMState \_ TurnedOff**
</dt> <dd>

關閉且不儲存。

</dd> <dt>

<span id="vmVMState_Saved"></span><span id="vmvmstate_saved"></span><span id="VMVMSTATE_SAVED"></span>**vmVMState \_ 已儲存**
</dt> <dd>

Off，但會儲存來賓。

</dd> <dt>

<span id="vmVMState_TurningOn"></span><span id="vmvmstate_turningon"></span><span id="VMVMSTATE_TURNINGON"></span>**vmVMState \_ TurningOn**
</dt> <dd>

開啟的進程。

</dd> <dt>

<span id="vmVMState_Restoring"></span><span id="vmvmstate_restoring"></span><span id="VMVMSTATE_RESTORING"></span>**vmVMState \_ 還原**
</dt> <dd>

正在還原狀態。

</dd> <dt>

<span id="vmVMState_Running"></span><span id="vmvmstate_running"></span><span id="VMVMSTATE_RUNNING"></span>**vmVMState \_ 正在執行**
</dt> <dd>

正在執行且未暫停。

</dd> <dt>

<span id="vmVMState_Paused"></span><span id="vmvmstate_paused"></span><span id="VMVMSTATE_PAUSED"></span>**vmVMState 已 \_ 暫停**
</dt> <dd>

正在執行和暫停。

</dd> <dt>

<span id="vmVMState_Saving"></span><span id="vmvmstate_saving"></span><span id="VMVMSTATE_SAVING"></span>**vmVMState \_ 儲存**
</dt> <dd>

正在儲存狀態。

</dd> <dt>

<span id="vmVMState_TurningOff"></span><span id="vmvmstate_turningoff"></span><span id="VMVMSTATE_TURNINGOFF"></span>**vmVMState \_ TurningOff**
</dt> <dd>

關閉的進程。

</dd> <dt>

<span id="vmVMState_MergingDrives"></span><span id="vmvmstate_mergingdrives"></span><span id="VMVMSTATE_MERGINGDRIVES"></span>**vmVMState \_ MergingDrives**
</dt> <dd>

在合併復原磁片磁碟機的過程中。

</dd> <dt>

<span id="vmVMState_DeleteMachine"></span><span id="vmvmstate_deletemachine"></span><span id="VMVMSTATE_DELETEMACHINE"></span>**vmVMState \_ DeleteMachine**
</dt> <dd>

正在刪除虛擬機器。

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

[**IVMVirtualMachine：： State**](ivmvirtualmachine-state.md)
</dt> <dt>

[**IVMVirtualMachineEvents：： OnStateChange**](ivmvirtualmachineevents-onstatechange.md)
</dt> <dt>

[**IVMVirtualPCEvents::OnVMStateChange**](ivmvirtualpcevents-onvmstatechange.md)
</dt> </dl>

 

