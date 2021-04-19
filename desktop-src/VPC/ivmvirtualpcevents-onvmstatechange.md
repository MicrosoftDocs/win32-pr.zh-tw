---
title: 'IVMVirtualPCEvents OnVMStateChange 方法 (VPCCOMInterfaces .h) '
description: '收到虛擬機器的狀態已變更的通知。 |IVMVirtualPCEvents OnVMStateChange 方法 (VPCCOMInterfaces .h) '
ms.assetid: a79afe14-9b7d-4528-ad38-e9b5ad068561
keywords:
- OnVMStateChange 方法 Virtual PC
- OnVMStateChange 方法 Virtual PC，IVMVirtualPCEvents 介面
- IVMVirtualPCEvents 介面 Virtual PC，OnVMStateChange 方法
topic_type:
- apiref
api_name:
- IVMVirtualPCEvents.OnVMStateChange
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2d0a8bd9a362c558c307fb4719c95a9ba8cbf4a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106991957"
---
# <a name="ivmvirtualpceventsonvmstatechange-method"></a>IVMVirtualPCEvents：： OnVMStateChange 方法

\[Windows 8 不能再使用 Windows Virtual PC。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

收到虛擬機器的狀態已變更的通知。

## <a name="syntax"></a>語法


```C++
HRESULT OnVMStateChange(
  [in] BSTR      virtualMachineConfig,
  [in] VMVMState virtualMachineState
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*virtualMachineConfig* \[在\]
</dt> <dd>

虛擬機器的名稱。

</dd> <dt>

*virtualMachineState* \[在\]
</dt> <dd>

虛擬機器的新狀態。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

用戶端程式必須執行這個介面方法，以接收來自 [**IVMVirtualPC**](ivmvirtualpc.md)的 **vmVirtualPCEvent \_ VMStateChanged** 事件的通知。 若要監視特定的虛擬機器，請使用 [**IVMVirtualMachineEvents：： OnStateChange**](ivmvirtualmachineevents-onstatechange.md) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | DIID \_ IVMVirtualPCEvents 定義為 efed1ef1-3c09-41f7-a9c2-7e29fa286c9d<br/>        |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMVirtualPCEvents**](ivmvirtualpcevents.md)
</dt> </dl>

 

