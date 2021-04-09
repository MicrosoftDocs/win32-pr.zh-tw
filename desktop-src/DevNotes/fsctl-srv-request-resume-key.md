---
description: FSCTL \_ SRV \_ 要求 \_ RESUME \_ KEY control 程式碼是用來抓取不透明的檔案參考，以與 IOCTL \_ copychunk 可控制項程式碼搭配使用。
ms.assetid: a6e0d253-5beb-4de8-8c40-d004f5794d47
title: FSCTL_SRV_REQUEST_RESUME_KEY 控制程式代碼
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FSCTL_SRV_REQUEST_RESUME_KEY
api_type:
- NA
api_location: ''
ms.openlocfilehash: 8f11b70f7b4bfd05cbd5f7c29323f1dca00083a4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847062"
---
# <a name="fsctl_srv_request_resume_key-control-code"></a>FSCTL \_ SRV \_ 要求 \_ 繼續 \_ 按鍵控制程式代碼

**FSCTL \_ SRV \_ 要求 \_ RESUME \_ KEY** control 程式碼是用來抓取不透明的檔案參考，以與 [**IOCTL \_ copychunk 可**](ioctl-copychunk.md)控制項程式碼搭配使用。

若要執行這項作業，請使用下列參數呼叫 [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) 函數。


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,             // handle to device
  FSCTL_SRV_REQUEST_RESUME_KEY, // dwIoControlCode
  NULL,                         // lpInBuffer
  0,                            // nInBufferSize
  (LPVOID) lpOutBuffer,         // output buffer
  (DWORD) nOutBufferSize,       // size of output buffer
  (LPDWORD) lpBytesReturned,    // number of bytes returned
  (LPOVERLAPPED) lpOverlapped   // OVERLAPPED structure
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hDevice* \[在\]
</dt> <dd>

要要求其來源檔案索引鍵之檔案的控制碼。 若要取得此控制碼，請呼叫 [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) 函數。

</dd> <dt>

*dwIoControlCode* \[在\]
</dt> <dd>

作業的控制項程式碼。 針對這項作業，請使用 **FSCTL \_ SRV \_ 要求 \_ 繼續 \_ 金鑰** 。

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

未搭配此作業使用;設定為 **Null**。

</dd> <dt>

*nInBufferSize* \[在\]
</dt> <dd>

未搭配此作業使用;設定為零。

</dd> <dt>

*lpOutBuffer* \[擴展\]
</dt> <dd>

輸出緩衝區的指標， **SRV \_ 要求 \_ 繼續索引 \_ 鍵** 結構。 如需詳細資訊，請參閱＜備註＞一節。

</dd> <dt>

*nOutBufferSize* \[在\]
</dt> <dd>

輸出緩衝區的大小 (以位元組為單位)。

</dd> <dt>

*lpBytesReturned* \[擴展\]
</dt> <dd>

變數的指標，此變數會接收儲存在輸出緩衝區中的資料大小（以位元組為單位）。

如果輸出緩衝區太小，則呼叫會失敗，而 [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) 函數會傳回 **錯誤 \_ 的 \_ 緩衝區**，而 *lpBytesReturned* 為零。

如果 *lpOverlapped* 參數為 **null**，則 *lpBytesReturned* 不可以是 **null**。 即使作業未傳回輸出資料，而且 *lpOutBuffer* 參數為 **Null**， [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) 仍會使用 *lpBytesReturned*。 在這類作業之後， *lpBytesReturned* 的值就沒有意義。

如果 *lpOverlapped* 不是 **null**， *lpBytesReturned* 可以是 **null**。 如果 *lpOverlapped* 不是 **Null** ，而且作業傳回資料，則在重迭的作業完成之前， *lpBytesReturned* 是無意義的。 若要取出傳回的位元組數目，請呼叫 [**GetOverlappedResult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult) 函數。 如果 *hDevice* 參數與 i/o 完成埠相關聯，您可以藉由呼叫 [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) 函數來取得傳回的位元組數目。

</dd> <dt>

*lpOverlapped* \[在\]
</dt> <dd>

重 [**迭結構的**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) 指標。

如果在未指定檔案 **\_ 旗 \_** 標的情況下開啟 hDevice 參數，則會忽略 *lpOverlapped* 。

如果使用檔案 **\_ 旗 \_** 標重迭旗標開啟 hDevice，則會以 (非同步) 作業的重迭方式執行作業。 在此情況下， *lpOverlapped* 必須指向包含事件物件控制碼 [**的有效重**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) 迭結構。 否則，函式會以無法預期的方式失敗。

針對重迭的作業， [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) 會立即傳回，而當作業完成時，就會發出事件物件的信號。 否則，必須等到作業完成或發生錯誤時，函數才會傳回。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果作業順利完成， [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) 會傳回非零值。

如果作業失敗或擱置中， [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) 會傳回零。 若要取得擴充的錯誤資訊，請呼叫 [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)。

## <a name="remarks"></a>備註

此控制項程式碼沒有相關聯的標頭檔。 您必須定義控制項程式碼和資料結構，如下所示。

``` syntax
#define FSCTL_SRV_REQUEST_RESUME_KEY CTL_CODE(FILE_DEVICE_NETWORK_FILE_SYSTEM, 30, METHOD_BUFFERED, FILE_ANY_ACCESS)

typedef struct _SRV_RESUME_KEY {
    UINT64 ResumeKey;
    UINT64 Timestamp;
    UINT64 Pid;
} SRV_RESUME_KEY, *PSRV_RESUME_KEY;

typedef struct _SRV_REQUEST_RESUME_KEY {
    SRV_RESUME_KEY Key;
    ULONG  ContextLength;
    BYTE   Context[1];
} SRV_REQUEST_RESUME_KEY, *PSRV_REQUEST_RESUME_KEY;
```

這些成員可以依照下列方式描述。



| member                                                                                                                       | 描述                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ResumeKey"></span><span id="resumekey"></span><span id="RESUMEKEY"></span>**ResumeKey**<br/>                 | 識別伺服器之原始程式檔的不透明值。<br/>                                                                                                   |
| <span id="Timestamp"></span><span id="timestamp"></span><span id="TIMESTAMP"></span>**時間 戳**<br/>                 | 識別開啟檔案之時間的不透明值。<br/>                                                                                               |
| <span id="Pid"></span><span id="pid"></span><span id="PID"></span>**Pid**<br/>                                         | 識別開啟檔案之進程的不透明值。<br/>                                                                                                |
| <span id="Key"></span><span id="key"></span><span id="KEY"></span>**關鍵**<br/>                                         | **SRV \_ RESUME \_ 鍵** 結構。 若要執行伺服器端複製作業，請將此結構與 [**IOCTL \_ copychunk 可**](ioctl-copychunk.md) 控制項程式碼搭配使用。<br/> |
| <span id="ContextLength"></span><span id="contextlength"></span><span id="CONTEXTLENGTH"></span>**CoNtextLength**<br/> | 這個成員是保留供系統使用;請勿使用。<br/>                                                                                                              |
| <span id="Context"></span><span id="context"></span><span id="CONTEXT"></span>**上下文**<br/>                         | 這個成員是保留供系統使用;請勿使用。<br/>                                                                                                              |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[**IOCTL \_ COPYCHUNK 可**](ioctl-copychunk.md)
</dt> </dl>

 

 
