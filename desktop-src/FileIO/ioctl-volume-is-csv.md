---
description: 判斷磁片區是否為 CSV 磁片區。
ms.assetid: 6B09B519-1E2F-4757-AAD5-1E4C81023E14
title: 'IOCTL_VOLUME_IS_CSV 控制程式代碼 (Ntddvol) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_VOLUME_IS_CSV
api_type:
- HeaderDef
api_location:
- Ntddvol.h
ms.openlocfilehash: 8121e1b89c88ad05a2c2be8537d7170bfabfc412
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320392"
---
# <a name="ioctl_volume_is_csv-control-code"></a>IOCTL \_ 磁片區 \_ 是 \_ CSV 控制項程式碼

判斷磁片區是否為 CSV 磁片區。

若要執行這項作業，請使用下列參數呼叫 [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 函數。


```C++
BOOL 
WINAPI 
DeviceIoControl( (HANDLE) hDevice,              // handle to device
                 IOCTL_VOLUME_IS_CSV,           // dwIoControlCode
                 NULL,                          // input buffer
                 0,                             // size of input buffer
                 (LPVOID) lpOutBuffer,          // lpOutBuffer
                 (DWORD) nOutBufferSize,        // nOutBufferSize
                 (LPDWORD) lpBytesReturned,     // number of bytes returned
                 (LPOVERLAPPED) lpOverlapped ); // OVERLAPPED structure
```



## <a name="parameters"></a>參數

<dl> <dt>

*hDevice* 
</dt> <dd>

磁片區的控制碼。 若要取出磁片區控制碼，請呼叫 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) 函數。 只有系統管理員可以開啟磁片區控制碼。

</dd> <dt>

*dwIoControlCode* 
</dt> <dd>

作業的控制項程式碼。 針對這項作業，使用 **IOCTL \_ 磁片區 \_ 是 \_ CSV** 。

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

未搭配此作業使用;設定為 **Null**。

</dd> <dt>

*nInBufferSize* 
</dt> <dd>

未搭配此作業使用;設定為零 (0) 。

</dd> <dt>

*lpOutBuffer* 
</dt> <dd>

如果磁片區是 CSV 磁片區，則為 **TRUE** 的指標;否則，函式呼叫會失敗。

</dd> <dt>

*nOutBufferSize* 
</dt> <dd>

輸出緩衝區的大小 (以位元組為單位)。

</dd> <dt>

*lpBytesReturned* 
</dt> <dd>

變數的指標，此變數會接收儲存在輸出緩衝區中的資料大小（以位元組為單位）。

如果 *lpOverlapped* 為 **null**，則 *lpBytesReturned* 不可以是 **null**。 即使作業未傳回輸出資料，而且 *lpOutBuffer* 為 **Null**， [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 也會使用 *lpBytesReturned*。 在這類作業之後， *lpBytesReturned* 的值就沒有意義。

如果 *lpOverlapped* 不是 **null**， *lpBytesReturned* 可以是 **null**。 如果這個參數不是 **Null** ，而且作業傳回資料，則 *lpBytesReturned* 會在重迭的作業完成之前無意義。 若要取出傳回的位元組數目，請呼叫 [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult)。 如果 *hDevice* 與 i/o 完成埠相關聯，您可以藉由呼叫 [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)來取得傳回的位元組數目。

</dd> <dt>

*lpOverlapped* 
</dt> <dd>

重 [**迭結構的**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) 指標。

如果在未指定檔案 **\_ 旗 \_** 標的情況下開啟 *hDevice* ，則會忽略 *lpOverlapped* 。

如果使用檔案 **\_ 旗 \_** 標重迭旗標開啟 hDevice，則會以 (非同步) 作業的重迭方式執行作業。 在此情況下， *lpOverlapped* 必須指向包含事件物件控制碼 [**的有效重**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) 迭結構。 否則，函式會以無法預期的方式失敗。

針對重迭的作業， [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 會立即傳回，而當作業完成時，就會發出事件物件的信號。 否則，在作業完成或發生錯誤之前，函數不會傳回。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果作業順利完成， [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 會傳回非零值。

如果作業失敗或擱置中， [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 會傳回零 (0) 。 若要取得擴充的錯誤資訊，請呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>Ntddvol。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)
</dt> <dt>

[**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[磁碟區管理控制碼](volume-management-control-codes.md)
</dt> </dl>

 

