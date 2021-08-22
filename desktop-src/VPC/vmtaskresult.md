---
title: 'VMTaskResult 列舉 (VPCCOMInterfaces) '
description: 指定工作的結果。
ms.assetid: 34aa193a-466d-492e-8648-467c286a8c11
keywords:
- VMTaskResult 列舉虛擬電腦
topic_type:
- apiref
api_name:
- VMTaskResult
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0884d89776ac840586f221f21f8335f1d93c18886fd36bbe790164ebd1ba4cd8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998438"
---
# <a name="vmtaskresult-enumeration"></a>VMTaskResult 列舉

\[WindowsVirtual PC 不再適用于 Windows 8。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

指定工作的結果。

## <a name="syntax"></a>Syntax


```C++
typedef enum  { 
  vmTaskResult_Success                      = 0,
  vmTaskResult_Cancelled                    = 1,
  vmTaskResult_UnexpectedError              = 2,
  vmTaskResult_OutOfMemoryError             = 3,
  vmTaskResult_DiskRelatedError             = 4,
  vmTaskResult_IncompatibleSavedStateError  = 5,
  vmTaskResult_TimeOutError                 = 6,
  vmTaskResult_IllegalValueError            = 7,
  vmTaskResult_ThreadCrashError             = 8,
  vmTaskResult_ShutdownAbort                = 9
} VMTaskResult;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="vmTaskResult_Success"></span><span id="vmtaskresult_success"></span><span id="VMTASKRESULT_SUCCESS"></span>**vmTaskResult \_ 成功**
</dt> <dd>

工作成功。

</dd> <dt>

<span id="vmTaskResult_Cancelled"></span><span id="vmtaskresult_cancelled"></span><span id="VMTASKRESULT_CANCELLED"></span>**vmTaskResult 已 \_ 取消**
</dt> <dd>

工作已取消。

</dd> <dt>

<span id="vmTaskResult_UnexpectedError"></span><span id="vmtaskresult_unexpectederror"></span><span id="VMTASKRESULT_UNEXPECTEDERROR"></span>**vmTaskResult \_ UnexpectedError**
</dt> <dd>

工作發生未預期的錯誤。

</dd> <dt>

<span id="vmTaskResult_OutOfMemoryError"></span><span id="vmtaskresult_outofmemoryerror"></span><span id="VMTASKRESULT_OUTOFMEMORYERROR"></span>**vmTaskResult \_ OutOfMemoryError**
</dt> <dd>

沒有足夠的記憶體可完成工作。

</dd> <dt>

<span id="vmTaskResult_DiskRelatedError"></span><span id="vmtaskresult_diskrelatederror"></span><span id="VMTASKRESULT_DISKRELATEDERROR"></span>**vmTaskResult \_ DiskRelatedError**
</dt> <dd>

工作寫入磁片時發生錯誤 (請確定有足夠的磁碟空間) 。

</dd> <dt>

<span id="vmTaskResult_IncompatibleSavedStateError"></span><span id="vmtaskresult_incompatiblesavedstateerror"></span><span id="VMTASKRESULT_INCOMPATIBLESAVEDSTATEERROR"></span>**vmTaskResult \_ IncompatibleSavedStateError**
</dt> <dd>

因為儲存的狀態不相容，所以無法還原虛擬機器。

</dd> <dt>

<span id="vmTaskResult_TimeOutError"></span><span id="vmtaskresult_timeouterror"></span><span id="VMTASKRESULT_TIMEOUTERROR"></span>**vmTaskResult \_ >timeouterror**
</dt> <dd>

工作已超時。

</dd> <dt>

<span id="vmTaskResult_IllegalValueError"></span><span id="vmtaskresult_illegalvalueerror"></span><span id="VMTASKRESULT_ILLEGALVALUEERROR"></span>**vmTaskResult \_ IllegalValueError**
</dt> <dd>

工作處理時讀取了不合法的喜好設定值。

</dd> <dt>

<span id="vmTaskResult_ThreadCrashError"></span><span id="vmtaskresult_threadcrasherror"></span><span id="VMTASKRESULT_THREADCRASHERROR"></span>**vmTaskResult \_ ThreadCrashError**
</dt> <dd>

與工作相關聯的執行緒已損毀。

</dd> <dt>

<span id="vmTaskResult_ShutdownAbort"></span><span id="vmtaskresult_shutdownabort"></span><span id="VMTASKRESULT_SHUTDOWNABORT"></span>**vmTaskResult \_ ShutdownAbort**
</dt> <dd>

要求的關機已中止。

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

[**IVMTask：： Result**](ivmtask-result.md)
</dt> </dl>

 

