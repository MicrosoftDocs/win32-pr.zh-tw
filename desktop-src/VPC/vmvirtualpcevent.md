---
title: 'VMVirtualPCEvent 列舉 (VPCCOMInterfaces) '
description: 指定 Windows 的虛擬電腦事件。
ms.assetid: 3b239cd0-d922-42de-8bcc-51f625c0d8b0
keywords:
- VMVirtualPCEvent 列舉虛擬電腦
topic_type:
- apiref
api_name:
- VMVirtualPCEvent
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c9d0b02fcdb13660440e2f29924c0d4df58721aa9d8b421333e6e1943b38234
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998318"
---
# <a name="vmvirtualpcevent-enumeration"></a>VMVirtualPCEvent 列舉

\[WindowsVirtual PC 不再適用于 Windows 8。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

指定 Windows 的虛擬電腦事件。

## <a name="syntax"></a>Syntax


```C++
typedef enum  { 
  vmVirtualPCEvent_VMStateChange  = 2,
  vmVirtualPCEvent_EventLogged    = 3
} VMVirtualPCEvent;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="vmVirtualPCEvent_VMStateChange"></span><span id="vmvirtualpcevent_vmstatechange"></span><span id="VMVIRTUALPCEVENT_VMSTATECHANGE"></span>**vmVirtualPCEvent \_ VMStateChange**
</dt> <dd>

虛擬機器的狀態已變更。

</dd> <dt>

<span id="vmVirtualPCEvent_EventLogged"></span><span id="vmvirtualpcevent_eventlogged"></span><span id="VMVIRTUALPCEVENT_EVENTLOGGED"></span>**vmVirtualPCEvent \_ EventLogged**
</dt> <dd>

Virtual PC 已記錄事件。

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

[**IVMVirtualPCEvents**](ivmvirtualpcevents.md)
</dt> </dl>

 

