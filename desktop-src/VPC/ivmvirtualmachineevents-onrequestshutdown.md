---
title: 'IVMVirtualMachineEvents OnRequestShutdown 方法 (VPCCOMInterfaces .h) '
description: 接收已發出關機要求的通知。
ms.assetid: e04131fd-5ca7-4392-9725-ba62b905324a
keywords:
- OnRequestShutdown 方法 Virtual PC
- OnRequestShutdown 方法 Virtual PC，IVMVirtualMachineEvents 介面
- IVMVirtualMachineEvents 介面 Virtual PC，OnRequestShutdown 方法
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnRequestShutdown
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 929c9a293e760a12ace62766cbd7a0c016980fc2399cdde494402a272d90fe0d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118123168"
---
# <a name="ivmvirtualmachineeventsonrequestshutdown-method"></a>IVMVirtualMachineEvents：： OnRequestShutdown 方法

\[WindowsVirtual PC 不再適用于 Windows 8。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

接收已發出關機要求的通知。

## <a name="syntax"></a>語法


```C++
HRESULT OnRequestShutdown();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

每當虛擬機器會話即將關閉時，就會呼叫這個方法。 用戶端程式必須執行這個介面方法，以接收來自 [**IVMVirtualMachine**](ivmvirtualmachine.md)的 **vmVirtualMachineEvent \_ RequestShutdown** 事件的通知。

只有當虛擬機器會話即將關閉時，才會傳送此事件通知。 作業系統關閉常式（例如 [**IVMGuestOS：： shutdown**](ivmguestos-shutdown.md)）不會直接引發此事件，除非它們也嘗試執行虛擬硬體的軟體電源。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | DIID \_ IVMVirtualMachineEvents 定義為9d84f560-bb67-4961-bd12-a4da780c67e4<br/>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMVirtualMachineEvents**](ivmvirtualmachineevents.md)
</dt> </dl>

 

