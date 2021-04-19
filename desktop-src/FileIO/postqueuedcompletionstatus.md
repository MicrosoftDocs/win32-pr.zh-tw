---
description: 將 i/o 完成封包張貼至 i/o 完成通訊埠。
ms.assetid: 69a9b1e5-2d40-42de-a14a-f7b6f29bf571
title: 'PostQueuedCompletionStatus 函式 (IoAPI) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PostQueuedCompletionStatus
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-io-l1-1-0.dll
- KernelBase.dll
- MinKernelBase.dll
- API-MS-Win-Core-io-l1-1-1.dll
- api-ms-win-downlevel-kernel32-l1-1-0.dll
ms.openlocfilehash: f12de10032df7fec32dd9a577353dd20c0f4eaa5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106995863"
---
# <a name="postqueuedcompletionstatus-function"></a>PostQueuedCompletionStatus 函式

將 i/o 完成封包張貼至 i/o 完成通訊埠。

## <a name="syntax"></a>語法


```C++
BOOL WINAPI PostQueuedCompletionStatus(
  _In_     HANDLE       CompletionPort,
  _In_     DWORD        dwNumberOfBytesTransferred,
  _In_     ULONG_PTR    dwCompletionKey,
  _In_opt_ LPOVERLAPPED lpOverlapped
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*CompletionPort* \[在\]
</dt> <dd>

I/o 完成通訊埠的控制碼，i/o 完成封包將張貼至此。

</dd> <dt>

*dwNumberOfBytesTransferred* \[在\]
</dt> <dd>

要透過 [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)函數的 *lpNumberOfBytesTransferred* 參數傳回的值。

</dd> <dt>

*dwCompletionKey* \[在\]
</dt> <dd>

要透過 [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)函數的 *lpCompletionKey* 參數傳回的值。

</dd> <dt>

*lpOverlapped* \[在中，選擇性\]
</dt> <dd>

要透過 [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)函數的 *lpOverlapped* 參數傳回的值。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回非零的值。

如果此函式失敗，則傳回值為零。 若要取得延伸錯誤資訊，請呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 。

## <a name="remarks"></a>備註

I/o 完成封包會滿足 [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) 函式的未完成呼叫。 此函式會傳回三個值，這些值會傳遞為 **PostQueuedCompletionStatus** 呼叫的第二、第三和第四個參數。 系統不會使用或驗證這些值。 尤其是， *lpOverlapped* 參數不需要指向重迭的 [**結構。**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped)

在 Windows 8 和 Windows Server 2012 中，下列技術支援此功能。



| 技術                                           | 支援      |
|------------------------------------------------------|----------------|
| 伺服器訊息區 (SMB) 3.0 通訊協定<br/>   | Yes<br/> |
| SMB 3.0 透明容錯移轉 (TFO) <br/>        | Yes<br/> |
| 具有向外延展檔案共用的 SMB 3.0 (因此) <br/>   | Yes<br/> |
| 叢集共用磁碟區檔案系統 (CsvFS) <br/> | Yes<br/> |
| 彈性檔案系統 (ReFS)<br/>              | Yes<br/> |



 

CsvFs 將會針對壓縮檔進行重新導向的 IO。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows XP \[ 桌面應用程式 \| UWP 應用程式\]<br/>                                                                                                                                                                                                                                                       |
| 最低支援的伺服器<br/> | Windows Server 2003 \[ desktop app \| UWP 應用程式\]<br/>                                                                                                                                                                                                                                              |
| 標頭<br/>                   | <dl> <dt>IoAPI (包含 Windows .h) ;</dt><dt>Windows server 2008 R2、windows 7、Windows server 2008、Windows Vista、Windows server 2003 和 WINDOWS XP (的 WinBase，包括 windows .h) </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Kernel32.lib</dt> </dl>                                                                                                                                                                                                                  |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>                                                                                                                                                                                                                  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CreateIoCompletionPort**](createiocompletionport.md)
</dt> <dt>

[檔案管理功能](file-management-functions.md)
</dt> <dt>

[**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)
</dt> <dt>

[**重疊**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped)
</dt> </dl>

 

