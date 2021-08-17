---
title: 'VMShutdownAction 列舉 (VPCCOMInterfaces) '
description: 指定當主機關機或 vpc.exe 進程結束時，如何關閉虛擬機器。
ms.assetid: 271a685a-cac9-4a15-b363-bf8873fd5324
keywords:
- VMShutdownAction 列舉虛擬電腦
topic_type:
- apiref
api_name:
- VMShutdownAction
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df1f8b5bc21021e7771c14c0c3c6399e1d6342d7ebe3803759c8adb5c45024cb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119248408"
---
# <a name="vmshutdownaction-enumeration"></a>VMShutdownAction 列舉

\[WindowsVirtual PC 不再適用于 Windows 8。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

指定當主機關機或 vpc.exe 進程結束時，如何關閉虛擬機器 (VM) 。

## <a name="syntax"></a>Syntax


```C++
typedef enum  { 
  vmShutdownAction_Save      = 0,
  vmShutdownAction_TurnOff   = 1,
  vmShutdownAction_Shutdown  = 2
} VMShutdownAction;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="vmShutdownAction_Save"></span><span id="vmshutdownaction_save"></span><span id="VMSHUTDOWNACTION_SAVE"></span>**vmShutdownAction \_ 儲存**
</dt> <dd>

儲存 VM 狀態。

</dd> <dt>

<span id="vmShutdownAction_TurnOff"></span><span id="vmshutdownaction_turnoff"></span><span id="VMSHUTDOWNACTION_TURNOFF"></span>**vmShutdownAction \_ TurnOff**
</dt> <dd>

在不復原磁片磁碟機的情況下關閉 VM。

</dd> <dt>

<span id="vmShutdownAction_Shutdown"></span><span id="vmshutdownaction_shutdown"></span><span id="VMSHUTDOWNACTION_SHUTDOWN"></span>**vmShutdownAction \_ 關機**
</dt> <dd>

如果有整合元件可供使用，請關閉 VM 上的客體作業系統而不復原磁片磁碟機，否則會儲存 VM。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| Product<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[WindowsVirtual PC 列舉](virtual-pc-enumerations.md)
</dt> <dt>

[**IVMVirtualMachine::ShutdownActionOnQuit**](ivmvirtualmachine-shutdownactiononquit.md)
</dt> </dl>

 

