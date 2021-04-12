---
title: 'IVMVirtualMachineEvents OnEnhancedVideoModeChanged 方法 (VPCCOMInterfaces .h) '
description: 收到虛擬機器的增強型影片模式支援已變更的通知。
ms.assetid: be22a859-4687-4647-9f53-f79ae8ad52a5
keywords:
- OnEnhancedVideoModeChanged 方法 Virtual PC
- OnEnhancedVideoModeChanged 方法 Virtual PC，IVMVirtualMachineEvents 介面
- IVMVirtualMachineEvents 介面 Virtual PC，OnEnhancedVideoModeChanged 方法
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnEnhancedVideoModeChanged
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29bbc67fe298c1a47d853072d8c58ab5b3ce1988
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464181"
---
# <a name="ivmvirtualmachineeventsonenhancedvideomodechanged-method"></a>IVMVirtualMachineEvents：： OnEnhancedVideoModeChanged 方法

\[Windows 8 不能再使用 Windows Virtual PC。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

收到虛擬機器的增強型影片模式支援已變更的通知。

## <a name="syntax"></a>語法


```C++
HRESULT OnEnhancedVideoModeChanged(
  [in] VARIANT_BOOL enhancedVideoMode
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*enhancedVideoMode* \[在\]
</dt> <dd>

指出是否有增強的影片模式可用。

</dd> </dl>

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

 

