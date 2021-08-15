---
description: IOCTL \_ copychunk 可控制項程式碼會起始資料範圍的伺服器端複本，也稱為區塊。
ms.assetid: 36f68840-bd5c-4cfc-a8ad-0cfbbdc5a2a9
title: IOCTL_COPYCHUNK 控制程式代碼
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COPY_CHUNK
api_type:
- NA
api_location: ''
ms.openlocfilehash: 415e94d8ed19d3248beb31d8a5e6327e1adc11078483d4f60fcd42699e4dab89
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001728"
---
# <a name="ioctl_copychunk-control-code"></a>IOCTL \_ copychunk 可控制項程式碼

**IOCTL \_ copychunk 可** 控制項程式碼會起始資料範圍的伺服器端複本，也稱為區塊。

若要執行這項作業，請使用下列參數呼叫 [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) 函數。


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,             // handle to device
  IOCTL_COPYCHUNK,              // dwIoControlCode
  (LPVOID) lpInBuffer,          // input buffer
  (DWORD) nInBufferSize,        // size of input buffer
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

檔案的控制碼，該檔案是伺服器端複製作業的目標。 若要取得此控制碼，請呼叫 [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) 函數。

</dd> <dt>

*dwIoControlCode* \[在\]
</dt> <dd>

作業的控制項程式碼。 使用 **IOCTL \_ copychunk 可** 進行此作業。

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

輸入緩衝區的指標，也就是 **SRV \_ copychunk 可 \_ 複製** 結構。 如需詳細資訊，請參閱＜備註＞一節。

</dd> <dt>

*nInBufferSize* \[在\]
</dt> <dd>

輸入緩衝區的大小（以位元組為單位）。

</dd> <dt>

*lpOutBuffer* \[擴展\]
</dt> <dd>

輸出緩衝區的指標，也就是 **SRV \_ copychunk 可 \_ 回應** 結構。 如需詳細資訊，請參閱＜備註＞一節。

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
#define IOCTL_COPYCHUNK CTL_CODE(FILE_DEVICE_NETWORK_FILE_SYSTEM, 262, METHOD_BUFFERED,  FILE_READ_ACCESS)

typedef struct _SRV_COPYCHUNK {
    LARGE_INTEGER SourceOffset;
    LARGE_INTEGER DestinationOffset;
    ULONG  Length;
} SRV_COPYCHUNK, *PSRV_COPYCHUNK;

typedef struct _SRV_COPYCHUNK_COPY {
    SRV_RESUME_KEY SourceFile;
    ULONG          ChunkCount;
    ULONG          Reserved;
    SRV_COPYCHUNK  Chunk[1];    // Array
} SRV_COPYCHUNK_COPY, *PSRV_COPYCHUNK_COPY;

typedef struct _SRV_COPYCHUNK_RESPONSE {
    ULONG          ChunksWritten;
    ULONG          ChunkBytesWritten;
    ULONG          TotalBytesWritten;
} SRV_COPYCHUNK_RESPONSE, *PSRV_COPYCHUNK_RESPONSE;
```

這些成員可以依照下列方式描述。



| member                                                                                                                                       | 描述                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SourceOffset"></span><span id="sourceoffset"></span><span id="SOURCEOFFSET"></span>**SourceOffset**<br/>                     | 從原始程式檔開頭到要複製之區塊的位移（以位元組為單位）。<br/>                                                                                                                                                                                                                                                                     |
| <span id="DestinationOffset"></span><span id="destinationoffset"></span><span id="DESTINATIONOFFSET"></span>**DestinationOffset**<br/> | 從目標檔案開頭到要複製區塊的位置位移（以位元組為單位）。<br/>                                                                                                                                                                                                                                               |
| <span id="Length"></span><span id="length"></span><span id="LENGTH"></span>**長度**<br/>                                             | 要複製之區塊中的資料位元組數。 必須大於零且小於或等於 1 MB。 **長度** \***ChunkCount** 必須小於或等於 16 MB。<br/>                                                                                                                                                                         |
| <span id="SourceFile"></span><span id="sourcefile"></span><span id="SOURCEFILE"></span>**SourceFile**<br/>                             | 索引鍵，表示含有要複製之資料的原始程式檔。 此金鑰是透過 [**FSCTL \_ SRV \_ 要求 \_ 繼續 \_ 金鑰**](fsctl-srv-request-resume-key.md)取得的。<br/>                                                                                                                                                                                   |
| <span id="ChunkCount"></span><span id="chunkcount"></span><span id="CHUNKCOUNT"></span>**ChunkCount**<br/>                             | 要複製的區塊數目。 必須大於零且小於或等於256。<br/>                                                                                                                                                                                                                                                                |
| <span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**保留**<br/>                                     | 這個成員是保留供系統使用;請勿使用。<br/>                                                                                                                                                                                                                                                                                                        |
| <span id="Chunk"></span><span id="chunk"></span><span id="CHUNK"></span>**塊**<br/>                                                 | **ChunkCount** **SRV \_ copychunk 可** 結構的陣列，每個要複製的區塊都有一個。 這個陣列的長度（以位元組為單位）必須是 **ChunkCount** \* sizeof (**SRV \_ copychunk 可**) 。<br/>                                                                                                                                                                       |
| <span id="ChunksWritten"></span><span id="chunkswritten"></span><span id="CHUNKSWRITTEN"></span>**ChunksWritten**<br/>                 | 如果作業失敗，並 **出現 \_ 錯誤 \_ 參數無效**，此值會指出伺服器將在單一要求中接受的區塊數目上限，也就是256。 否則，此值會指出已成功寫入的區塊數目。<br/>                                                                                               |
| <span id="ChunkBytesWritten"></span><span id="chunkbyteswritten"></span><span id="CHUNKBYTESWRITTEN"></span>**ChunkBytesWritten**<br/> | 如果作業失敗，並 **出現 \_ 錯誤 \_ 參數無效**，則這個值會指出伺服器允許在單一區塊中寫入的最大位元組數目，也就是 1 MB。 否則，此值會指出未成功處理的最後一個區塊中已成功寫入的位元組數目， (是否發生部分寫入) 。<br/> |
| <span id="TotalBytesWritten"></span><span id="totalbyteswritten"></span><span id="TOTALBYTESWRITTEN"></span>**TotalBytesWritten**<br/> | 如果作業失敗並 **出現錯誤 \_ \_ 參數無效**，此值會指出伺服器將在單一要求中複製的最大位元組數目，也就是 16 MB。 否則，此值會指出已成功寫入的位元組數目。<br/>                                                                                                 |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[**FSCTL \_ SRV \_ 要求 \_ 繼續 \_ 金鑰**](fsctl-srv-request-resume-key.md)
</dt> </dl>

 

 
