---
title: FSCTL_DFS_GET_PKT_ENTRY_STATE 控制碼 (LmDfs.h)
description: FSCTL_DFS_GET_PKT_ENTRY_STATE 控制程式代碼可以取得與 NetDfsGetClientInfo 函式相同的資訊，但可在某些設定中提供更佳的效能，而這些設定在 DFS 伺服器上會有高延遲。
ms.assetid: d4eec104-128b-43b5-9fae-08ab0b977dec
topic_type:
- apiref
api_name:
- FSCTL_DFS_GET_PKT_ENTRY_STATE
api_location:
- LmDfs.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f742f863e40f4abd13ef3c24a0ddce0981922cc40ab8d55c31393d519139f03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118810312"
---
# <a name="fsctl_dfs_get_pkt_entry_state-control-code"></a>FSCTL_DFS_GET_PKT_ENTRY_STATE 控制程式代碼

**FSCTL_DFS_GET_PKT_ENTRY_STATE** 控制程式代碼可以取得與 [**NetDfsGetClientInfo**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetclientinfo)函式相同的資訊，但可在某些設定中提供更佳的效能，而這些設定在 DFS 伺服器上會有高延遲。 除非有效能問題，否則不建議使用 **FSCTL_DFS_GET_PKT_ENTRY_STATE** 控制項程式碼。

若要執行這項作業，請使用下列參數呼叫 [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 函數。

```C++
BOOL 
   WINAPI 
   DeviceIoControl( (HANDLE)       hDevice,            // handle to device
                    (DWORD)        FSCTL_DFS_GET_PKT_ENTRY_STATE, // dwIoControlCode(LPDWORD)      lpInBuffer,         // input buffer
                    (DWORD)        nInBufferSize,      // size of input buffer
                    (LPDWORD)      lpOutBuffer,        // output buffer
                    (DWORD)        nOutBufferSize,     // size of output buffer
                    (LPDWORD)      lpBytesReturned,    // number of bytes returned
                    (LPOVERLAPPED) lpOverlapped );     // OVERLAPPED structure
```

## <a name="parameters"></a>參數

<dl> <dt>

*hDevice* [in]
</dt> <dd>

裝置的控制碼。 若要取得裝置控制碼，請呼叫 [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) 函式。

</dd> <dt>

*dwIoControlCode* [in]
</dt> <dd>

作業的控制項程式碼。 使用 **FSCTL_DFS_GET_PKT_ENTRY_STATE** 進行此作業。

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

[**DFS_GET_PKT_ENTRY_STATE_ARG**](/windows/win32/api/lmdfs/ns-lmdfs-dfs_get_pkt_entry_state_arg)結構的位址和後面的 1-3 Unicode 字串。

</dd> <dt>

*nInBufferSize* [in]
</dt> <dd>

*LpInBuffer* 參數所指向之緩衝區的大小（以位元組為單位）。

</dd> <dt>

*lpOutBuffer* [out]
</dt> <dd>

**DFS_INFO_ \#** 結構的位址，以及 **DFS_INFO_ \#** 結構所指向的任何字串和結構。 傳回的特定結構取決於傳入輸入緩衝區之 [**DFS_GET_PKT_ENTRY_STATE_ARG**](/windows/win32/api/lmdfs/ns-lmdfs-dfs_get_pkt_entry_state_arg)結構中的 **層級** 成員。

</dd> <dt>

*nOutBufferSize* [in]
</dt> <dd>

*LpOutBuffer* 參數所指向之緩衝區的大小（以位元組為單位）。 由於傳回的 **DFS_INFO_ \#** 結構所參考的字串和結構也在輸出緩衝區中，這個緩衝區應大於指定的 **DFS_INFO_ \#** 結構。

</dd> <dt>

*lpBytesReturned* [out]
</dt> <dd>

變數的指標，此變數會接收儲存在輸出緩衝區中的資料大小（以位元組為單位）。

如果輸出緩衝區太小，但至少足以容納 **DWORD**，則呼叫會失敗、 [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) 會傳回 **ERROR_MORE_DATA**，而且輸出緩衝區的第一個 **DWORD** 會包含所需的大小。 如果輸出緩衝區無法保存 **DWORD** ，則呼叫會失敗並出現 **ERROR_INSUFFICIENT_BUFFER**，且 *lpBytesReturned* 為零。

如果 *lpOverlapped* 為 **null**，則 *lpBytesReturned* 不可以是 **null**。 即使作業未傳回輸出資料，而且 *lpOutBuffer* 為 **Null**， [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 也會使用 *lpBytesReturned*。 在這類作業之後， *lpBytesReturned* 的值就沒有意義。

如果 *lpOverlapped* 不是 **null**， *lpBytesReturned* 可以是 **null**。 如果這個參數不是 **Null** ，而且作業傳回資料，則 *lpBytesReturned* 會在重迭的作業完成之前無意義。 若要取出傳回的位元組數目，請呼叫 [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult)。 如果 *hDevice* 參數與 i/o 完成埠相關聯，您可以藉由呼叫 [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)來取得傳回的位元組數目。

</dd> <dt>

*lpOverlapped* [in]
</dt> <dd>

重 [**迭結構的**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) 指標。

如果在未指定 **FILE_FLAG_OVERLAPPED** 的情況下開啟 *hDevice* ，則會忽略 *lpOverlapped* 。

如果使用 **FILE_FLAG_OVERLAPPED** 旗標開啟 *hDevice* ，則會以非同步) 作業的重迭 (來執行此作業。 在此情況下， *lpOverlapped* 必須指向包含事件物件控制碼 [**的有效重**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) 迭結構。 否則，函式會以無法預期的方式失敗。

針對重迭的作業， [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) 會立即傳回，而當作業完成時，就會發出事件物件的信號。 否則，在作業完成或發生錯誤之前，函數不會傳回。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果作業順利完成， [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 會傳回非零值。

如果作業失敗或擱置中， [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 會傳回零。 若要取得擴充的錯誤資訊，請呼叫 [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)。

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                             |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                                       |
| 標頭<br/>                   | <dl> <dt>LmDfs (包含 LmDfs) </dt> </dl> |

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[**NetDfsGetClientInfo**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetclientinfo)
</dt> </dl>
