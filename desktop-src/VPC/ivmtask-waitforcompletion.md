---
title: 'IVMTask WaitForCompletion 方法 (VPCCOMInterfaces .h) '
description: 等候工作完成或指定的逾時間隔。
ms.assetid: 28718c54-4411-4c69-89de-35ea6a8d074c
keywords:
- WaitForCompletion 方法 Virtual PC
- WaitForCompletion 方法 Virtual PC，IVMTask 介面
- IVMTask 介面 Virtual PC，WaitForCompletion 方法
topic_type:
- apiref
api_name:
- IVMTask.WaitForCompletion
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 950cc19bad2a0f5804f994fe9279cec649d7c2f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967749"
---
# <a name="ivmtaskwaitforcompletion-method"></a>IVMTask：： WaitForCompletion 方法

\[Windows 8 不能再使用 Windows Virtual PC。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

等候工作完成或指定的逾時間隔。

## <a name="syntax"></a>語法


```C++
HRESULT WaitForCompletion(
  [in] long timeout
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*timeout* \[在\]
</dt> <dd>

這個方法在將控制權傳回給呼叫者之前，會等候工作完成的時間（以毫秒為單位）。 值為-1 時，會指定方法會等候，直到工作完成而沒有時間。其他有效的超時值範圍從0到4000000毫秒。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼/值                                                                                                                                                 | Description                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0</dt> </dl>                       | 作業成功。<br/>         |
| <dl> <dt>**E \_INVALIDARG**</dt> <dt>0x80000003</dt> </dl>      | *Timeout* 參數無效。<br/> |
| <dl> <dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt> </dl> | 已發生未預期的錯誤。<br/>     |



 

## <a name="remarks"></a>備註

**WaitForCompletion** 方法會讓目前的執行執行緒進入睡眠狀態，直到它傳回為止。 除非在任何情況下完成工作，否則不建議指定無限等候 (timeout =-1) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMTask 定義為 ab72b222-6e9c-48ae-aa54-85e3e635767c<br/>                    |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMTask**](ivmtask.md)
</dt> </dl>

 

