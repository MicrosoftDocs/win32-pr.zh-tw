---
title: 'IVMVirtualMachine DiscardUndoDisks 方法 (VPCCOMInterfaces .h) '
description: 捨棄虛擬復原磁片。
ms.assetid: 5c3a4b3f-ea58-498c-b7cf-54f028fa061c
keywords:
- DiscardUndoDisks 方法 Virtual PC
- DiscardUndoDisks 方法 Virtual PC，IVMVirtualMachine 介面
- IVMVirtualMachine 介面 Virtual PC，DiscardUndoDisks 方法
topic_type:
- apiref
api_name:
- IVMVirtualMachine.DiscardUndoDisks
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d548b69a6cfebc383a0233f01ef19ad14d051474
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465525"
---
# <a name="ivmvirtualmachinediscardundodisks-method"></a>IVMVirtualMachine：:D iscardUndoDisks 方法

\[Windows 8 不能再使用 Windows Virtual PC。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

捨棄虛擬復原磁片。

## <a name="syntax"></a>語法


```C++
HRESULT DiscardUndoDisks();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼/值                                                                                                                                                            | Description                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0</dt> </dl>                                  | 作業成功。<br/>                                                                        |
| <dl> <dt>**VM \_E \_ VM \_ 不明**</dt> <dt>0xA0040207</dt> </dl>            | 未知的設定。<br/>                                                                        |
| <dl> <dt>**VM \_E \_ VM \_ 正在執行 \_ 或 \_ 已儲存的**</dt> <dt>0xA004020B</dt> </dl> | 當虛擬機器正在執行或處於儲存狀態時，無法捨棄虛擬復原磁片。<br/> |
| <dl> <dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt> </dl>            | 已發生未預期的錯誤。<br/>                                                                    |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualMachine 定義為 f7092aa1-33ed-4f78-a59f-c00adfc2edd7<br/>          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> </dl>

 

