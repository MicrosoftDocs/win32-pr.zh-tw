---
title: 'IVMVirtualMachineEvents OnGuestShutdown 方法 (VPCCOMInterfaces .h) '
description: 收到客體作業系統關機的通知。
ms.assetid: a70c746a-f1ce-4f93-b41b-b03dc83f3da2
keywords:
- OnGuestShutdown 方法 Virtual PC
- OnGuestShutdown 方法 Virtual PC，IVMVirtualMachineEvents 介面
- IVMVirtualMachineEvents 介面 Virtual PC，OnGuestShutdown 方法
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnGuestShutdown
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 481b6dd6e13dc17d7f9a22ef366e984c2663279c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509100"
---
# <a name="ivmvirtualmachineeventsonguestshutdown-method"></a>IVMVirtualMachineEvents：： OnGuestShutdown 方法

\[Windows 8 不能再使用 Windows Virtual PC。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

收到客體作業系統關機的通知。

## <a name="syntax"></a>語法


```C++
HRESULT OnGuestShutdown();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | DIID \_ IVMVirtualMachineEvents 定義為9d84f560-bb67-4961-bd12-a4da780c67e4<br/>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMVirtualMachineEvents**](ivmvirtualmachineevents.md)
</dt> </dl>

 

