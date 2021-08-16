---
description: '\_ \_ \_ \_ 當讀取資料或將資料寫入遠端檔案時，IOCTL LMR 停用本機緩衝控制程式代碼會停用本機用戶端記憶體中的資料快取。 這是在公用標頭中無法使用的內部定義控制項程式碼。'
ms.assetid: a464671b-253c-4f35-84a2-2619cb15b009
title: IOCTL_LMR_DISABLE_LOCAL_BUFFERING 控制程式代碼
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
ms.openlocfilehash: 88a6fff0955fb9e0c57c7ea5fae99f532c7c6d4dcc3578a75e07da3f35867f9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117827179"
---
# <a name="ioctl_lmr_disable_local_buffering-control-code"></a>IOCTL \_ LMR \_ 停用 \_ 本機 \_ 緩衝控制程式代碼

當讀取資料或將資料寫入遠端檔案時， **IOCTL \_ LMR \_ 停用 \_ 本機 \_ 緩衝** 控制程式代碼會停用本機用戶端記憶體中的資料快取。 這是在公用標頭中無法使用的內部定義控制項程式碼。

若要執行這項作業，請使用下列參數呼叫 [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) 函數。


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,             // handle to device
  IOCTL_LMR_DISABLE_LOCAL_BUFFERING, // dwIoControlCode
  (LPVOID) NULL,                // lpInBuffer
  (DWORD) 0,                    // nInBufferSize
  (LPVOID) NULL,                // lpOutBuffer
  (DWORD) 0,                    // nOutBufferSize
  (LPDWORD) lpBytesReturned,    // number of bytes returned
  (LPOVERLAPPED) lpOverlapped   // OVERLAPPED structure
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hDevice* \[在\]
</dt> <dd>

遠端檔案的控制碼。 若要取得此控制碼，請呼叫 [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) 函數。

</dd> <dt>

*dwIoControlCode* \[在\]
</dt> <dd>

作業的控制項程式碼。 使用此作業的值0x140390。

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

未使用，必須是 **Null**。

</dd> <dt>

*nInBufferSize* \[在\]
</dt> <dd>

輸入緩衝區的大小（以位元組為單位）。 必須為零。

</dd> <dt>

*lpOutBuffer* \[擴展\]
</dt> <dd>

未使用，必須是 **Null**。

</dd> <dt>

*nOutBufferSize* \[在\]
</dt> <dd>

輸出緩衝區的大小 (以位元組為單位)。 必須為零。

</dd> <dt>

*lpBytesReturned* \[擴展\]
</dt> <dd>

變數的指標，此變數會接收儲存在輸出緩衝區中的資料大小（以位元組為單位）。

如果輸出緩衝區太小，則呼叫會失敗，而 [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) 函數會傳回 **錯誤的 \_ \_ 緩衝區**，而 *lpBytesReturned* 為零。

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

**IOCTL \_ LMR 停 \_ 用 \_ 本機 \_ 緩衝** 控制程式代碼是由系統在內部定義為0x140390，而不是在公用標頭檔中。 特殊用途的應用程式會使用它，在讀取資料或將資料寫入遠端檔案時，停用本機用戶端記憶體中的資料快取。 停用本機緩衝之後，設定會維持有效，直到檔案的所有開啟的控制碼都已關閉，且重新導向程式會清除其內部資料結構。

一般用途的應用程式不應使用 **IOCTL \_ LMR 停用 \_ \_ 本機 \_ 緩衝**，因為這可能會導致網路流量過高，以及相關聯的效能損失。 在嘗試充分利用網路頻寬的情況下，只有在專門應用程式中透過網路移動大量資料時，才應該使用 **IOCTL \_ LMR \_ 停用 \_ 本機 \_ 緩衝** 控制程式代碼。 例如， [**CopyFile**](/windows/win32/api/winbase/nf-winbase-copyfile) 和 [**CopyFileEx**](/windows/win32/api/winbase/nf-winbase-copyfileexa) 函數會使用 **IOCTL \_ LMR 停用 \_ \_ 本機 \_ 緩衝** 處理，以改善大型檔案複製的效能。

**IOCTL \_LMR \_ 停用 \_ 本機 \_ 緩衝** 並非由本機檔案系統所執行，而且將會失敗，並出現錯誤 **錯誤 \_ 無效 \_** 的函式。 發出 IOCTL LMR 停用遠端目錄控制碼上的 **\_ \_ \_ 本機 \_ 緩衝** 控制程式代碼將會失敗，且 **\_ 不 \_ 支援錯誤錯誤**。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> </dl>

 

 
