---
description: 同時捕獲多個完成埠專案。
ms.assetid: 3996c02c-562c-4697-a091-e241ad54b239
title: 'GetQueuedCompletionStatusEx 函式 (IoAPI) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetQueuedCompletionStatusEx
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-io-l1-1-0.dll
- KernelBase.dll
- MinKernelBase.dll
- API-MS-Win-Core-io-l1-1-1.dll
- api-ms-win-downlevel-kernel32-l1-1-0.dll
ms.openlocfilehash: f81bc0c997e3637fa941cb5a23f6394ba1f585566c8d633cadb00c9fd75ac805
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119696118"
---
# <a name="getqueuedcompletionstatusex-function"></a>GetQueuedCompletionStatusEx 函式

同時捕獲多個完成埠專案。 它會等候與指定完成埠相關聯的暫止 i/o 作業完成。

若要一次清除一個自動完成封包，請使用 [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) 函數。

## <a name="syntax"></a>語法


```C++
BOOL WINAPI GetQueuedCompletionStatusEx(
  _In_  HANDLE             CompletionPort,
  _Out_ LPOVERLAPPED_ENTRY lpCompletionPortEntries,
  _In_  ULONG              ulCount,
  _Out_ PULONG             ulNumEntriesRemoved,
  _In_  DWORD              dwMilliseconds,
  _In_  BOOL               fAlertable
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*CompletionPort* \[在\]
</dt> <dd>

完成埠的控制碼。 若要建立完成埠，請使用 [**CreateIoCompletionPort**](createiocompletionport.md) 函數。

</dd> <dt>

*lpCompletionPortEntries* \[擴展\]
</dt> <dd>

在輸入時，指向預先配置的重迭 [**\_ 專案**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry) 結構陣列。

在輸出時，會接收包含專案之重迭 [**\_ 專案**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry) 結構的陣列。 陣列元素的數目是由 *ulNumEntriesRemoved* 所提供。

每個 i/o 期間傳送的位元組數、表示每個 i/o 發生之檔案的完成索引鍵，以及每個原始 i/o 中所使用的重迭結構位址，全都會在 *lpCompletionPortEntries* 陣列中傳回。

</dd> <dt>

*ulCount* \[在\]
</dt> <dd>

要移除的專案數目上限。

</dd> <dt>

*ulNumEntriesRemoved* \[擴展\]
</dt> <dd>

變數的指標，此變數會接收實際移除的專案數。

</dd> <dt>

*dwMilliseconds* \[在\]
</dt> <dd>

呼叫端願意等候完成封包出現在完成埠上的毫秒數。 如果完成封包未出現在指定的時間內，則函式會超時並傳回 **FALSE**。

如果 *dwMilliseconds* 是 **無限** (0xffffffff) ，函式永遠不會有時間。如果 *dwMilliseconds* 為零，而且沒有可清除佇列的 i/o 作業，則函式會立即發生時間。

</dd> <dt>

*fAlertable* \[在\]
</dt> <dd>

如果此參數為 **FALSE**，則函式不會傳回，直到超時期間經過或抓取專案為止。

如果參數為 **TRUE** 且沒有可用的專案，則函式會執行可提供警示等候。 當系統將 i/o 完成常式或 APC 排入執行緒，而且執行緒執行函式時，執行緒會傳回。

當指定的 [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) 或 [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) 函式已完成，且呼叫的執行緒是起始作業的執行緒時，就會將完成常式排入佇列。 當您呼叫 [**QueueUserAPC**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-queueuserapc)時，系統會將 APC 排入佇列。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功或零 (**FALSE** ，則傳回非零 (**TRUE**) ) 否則為零。

若要取得擴充的錯誤資訊，請呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)。

## <a name="remarks"></a>備註

此函式會將具有指定完成埠的執行緒產生關聯。 執行緒最多可與一個完成埠相關聯。

當至少有一個暫止 i/o 完成時，此函式會傳回 **TRUE** ，但可能有一或多個 i/o 作業失敗。 請注意，此函式的使用者會透過查看每個重迭 [**\_ 專案**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry)中包含在 **lpOverlapped** 成員的狀態，來檢查 *lpCompletionPortEntries* 參數中傳回的專案清單，以判斷哪一個對應至任何可能的失敗 i/o 作業。

未清除任何 i/o 作業時，此函數會傳回 **FALSE** 。 這通常表示處理此呼叫的參數時發生錯誤，或 *CompletionPort* 控制碼已關閉或無效。 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)函式會提供延伸的錯誤資訊。

如果對 [**GetQueuedCompletionStatusEx**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) 的呼叫失敗，因為與其相關聯的控制碼已關閉，則函式會傳回 **FALSE** ，而 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 會傳回錯誤已 **放棄的 \_ \_ 等候 \_ 0**。

伺服器應用程式可能會有數個執行緒呼叫相同完成埠的 **GetQueuedCompletionStatusEx** 函式。 當 i/o 作業完成時，會以先進先出的順序將它們排入此埠。 如果執行緒正在主動等候此呼叫，一個或多個佇列的要求只會完成該執行緒的呼叫。

如需 i/o 完成埠理論、使用方式和相關聯函式的詳細資訊，請參閱 [I/o 完成埠](i-o-completion-ports.md)。

在 Windows 8 和 Windows Server 2012 中，下列技術支援此函數。



| 技術                                           | 支援      |
|------------------------------------------------------|----------------|
| 伺服器訊息區 (SMB) 3.0 通訊協定<br/>   | Yes<br/> |
| SMB 3.0 透明容錯移轉 (TFO) <br/>        | Yes<br/> |
| 具有向外延展檔案共用的 SMB 3.0 (因此) <br/>   | Yes<br/> |
| 叢集共用磁碟區檔案系統 (CsvFS) <br/> | Yes<br/> |
| 彈性檔案系統 (ReFS)<br/>              | Yes<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | WindowsVista \[ desktop apps \| UWP 應用程式\]<br/>                                                                                                                                                                                                                   |
| 最低支援的伺服器<br/> | WindowsServer 2008 \[ desktop app \| UWP 應用程式\]<br/>                                                                                                                                                                                                             |
| 標頭<br/>                   | <dl> <dt>IoAPI (包含 Windows .h) ;</dt><dt>Windows server 2008 R2、Windows 7、Windows Server 2008 和 Windows Vista (的 WinBase .h 包含 Windows .h) </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Kernel32.lib</dt> </dl>                                                                                                                                                                                 |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>                                                                                                                                                                                 |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**總覽主題**
</dt> <dt>

[檔案管理功能](file-management-functions.md)
</dt> <dt>

[I/o 完成埠](i-o-completion-ports.md)
</dt> <dt>

[使用 Windows 標頭](/windows/desktop/WinProg/using-the-windows-headers)
</dt> <dt>

**函數**
</dt> <dt>

[**ConnectNamedPipe**](/windows/desktop/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe)
</dt> <dt>

[**CreateIoCompletionPort**](createiocompletionport.md)
</dt> <dt>

[**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[**GetQueuedCompletionStatusEx**](getqueuedcompletionstatusex-func.md)
</dt> <dt>

[**LockFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-lockfileex)
</dt> <dt>

[**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile)
</dt> <dt>

[**PostQueuedCompletionStatus**](postqueuedcompletionstatus.md)
</dt> <dt>

[**TransactNamedPipe**](/windows/desktop/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe)
</dt> <dt>

[**WaitCommEvent**](/windows/desktop/api/winbase/nf-winbase-waitcommevent)
</dt> <dt>

[**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile)
</dt> </dl>

 

