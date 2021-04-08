---
title: 'IVMVirtualMachineEvents OnDiskOutOfSpace 方法 (VPCCOMInterfaces .h) '
description: 接收 VM 所需磁片的可用空間不足的通知。
ms.assetid: 1c431904-fffd-4513-8670-b9723f53edf1
keywords:
- OnDiskOutOfSpace 方法 Virtual PC
- OnDiskOutOfSpace 方法 Virtual PC，IVMVirtualMachineEvents 介面
- IVMVirtualMachineEvents 介面 Virtual PC，OnDiskOutOfSpace 方法
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnDiskOutOfSpace
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ac2d5f45068dc8cd7341d0a599b2da4e5c7655a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843035"
---
# <a name="ivmvirtualmachineeventsondiskoutofspace-method"></a>IVMVirtualMachineEvents：： OnDiskOutOfSpace 方法

\[Windows 8 不能再使用 Windows Virtual PC。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

收到通知，表示虛擬機器 (VM) 所需磁片的可用空間不足。 如果可用空間低於 100 MB，則會以警告的形式接收此事件，如果可用空間低於 20 MB，則會再次收到此事件作為錯誤，VM 將會暫停。

## <a name="syntax"></a>語法


```C++
HRESULT OnDiskOutOfSpace(
  [in] VARIANT_BOOL criticallyLow
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*criticallyLow* \[在\]
</dt> <dd>

如果磁片的可用空間小於 20 mb，則設定為 **variant \_ TRUE** ，如果可用空間超過 20 mb 但小於 100 mb，則設定為 **variant \_ FALSE** 。

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

 

