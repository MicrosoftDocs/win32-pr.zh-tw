---
title: 'IVMVirtualMachine MergeUndoDisks 方法 (VPCCOMInterfaces .h) '
description: 合併虛擬復原磁片。
ms.assetid: 6445b097-220e-48c4-9a7b-1139ca7b3338
keywords:
- MergeUndoDisks 方法 Virtual PC
- MergeUndoDisks 方法 Virtual PC，IVMVirtualMachine 介面
- IVMVirtualMachine 介面 Virtual PC，MergeUndoDisks 方法
topic_type:
- apiref
api_name:
- IVMVirtualMachine.MergeUndoDisks
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48863bf998ebc02bac93aa9e74d8cdbe07265477
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317403"
---
# <a name="ivmvirtualmachinemergeundodisks-method"></a>IVMVirtualMachine：： MergeUndoDisks 方法

\[Windows 8 不能再使用 Windows Virtual PC。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

合併虛擬復原磁片。

## <a name="syntax"></a>語法


```C++
HRESULT MergeUndoDisks(
  [out, retval] IVMTask **undoMergeTask
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*undoMergeTask* \[退出，retval\]
</dt> <dd>

用來追蹤影像建立的 [**IVMTask**](ivmtask.md) 物件。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼/值                                                                                                                                                                            | Description                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0</dt> </dl>                                                  | 作業成功。<br/>                                                                                                |
| <dl> <dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt> </dl>                            | 已發生未預期的錯誤。<br/>                                                                                            |
| <dl> <dt>**E \_指標**</dt><dt>且顯示 0x80004003</dt> </dl>                                    | 參數為 **Null**。<br/>                                                                                                   |
| <dl> <dt>**HRESULT \_從 \_ WIN32 (\_ \_ \_ 找不到錯誤路徑)**</dt> <dt>0x80070003</dt> </dl> | 系統找不到 *convertedDiskImagePath* 參數所指定的路徑，或其中一個父磁片無效。<br/> |
| <dl> <dt>**E \_ACCESSDENIED**</dt> <dt>0x80070005</dt> </dl>                               | 目前的使用者沒有足夠的父系檔案存取權。<br/>                                                                 |
| <dl> <dt>**E \_處理**</dt> <dt>0x80070006</dt> </dl>                                     | 其中一個父磁片正在使用中。<br/>                                                                                           |
| <dl> <dt>**VM \_E \_ VM \_ 不明**</dt> <dt>0xA0040207</dt> </dl>                            | 未知的設定。<br/>                                                                                                |
| <dl> <dt>**VM \_E \_ VM \_ 正在**</dt>執行 <dt>0xA0040500</dt> </dl>                            | 虛擬機器未執行。<br/>                                                                                              |
| <dl> <dt>**VM \_E \_ FILE \_ READ \_ ONLY**</dt> <dt>0xA004067A</dt> </dl>                       | 虛擬復原磁片的父系會標示為唯讀。<br/>                                                                     |
| <dl> <dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt> </dl>                            | 已發生未預期的錯誤。<br/>                                                                                            |



 

## <a name="remarks"></a>備註

當虛擬機器仍在執行時，無法呼叫 **MergeUndoDisks** 。 使用 [**IVMVirtualMachine：： save**](ivmvirtualmachine-save.md) 可先儲存虛擬機器的狀態，然後再呼叫 **MergeUndoDisks**，或 [**IVMVirtualMachine：： TurnOff**](ivmvirtualmachine-turnoff.md) 以關閉虛擬機器，而不需事先儲存其目前的狀態。

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

 

