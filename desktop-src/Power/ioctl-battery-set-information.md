---
description: 設定各種電池資訊。
ms.assetid: b827983d-5fb8-43f2-b732-541d16b3eb7b
title: 'IOCTL_BATTERY_SET_INFORMATION 控制程式代碼 (Poclass) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_BATTERY_SET_INFORMATION
api_type:
- HeaderDef
api_location:
- Poclass.h
- Batclass.h
ms.openlocfilehash: f540037486f16e920b3346620ff934b279652e7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849272"
---
# <a name="ioctl_battery_set_information-control-code"></a>IOCTL \_ 電池 \_ 設定 \_ 資訊控制程式代碼

設定各種電池資訊。 輸入參數結構（ [**電池 \_ 設定 \_ 資訊**](battery-set-information-str.md)）表示要設定的電池狀態資訊。

若要執行這項作業，請使用下列參數呼叫 [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 函數。


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,              // handle to battery
  IOCTL_BATTERY_SET_INFORMATION, // dwIoControlCode
  (LPVOID) lpInBuffer,           // input buffer
  (DWORD) nInBufferSize,         // size of input buffer
  NULL,                          // lpOutBuffer
  0,                             // nOutBufferSize
  (LPDWORD) lpBytesReturned,     // number of bytes returned
  (LPOVERLAPPED) lpOverlapped    // OVERLAPPED structure
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hDevice* 
</dt> <dd>

要設定資訊之電池的控制碼。 若要取出設備控制碼，請呼叫 [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) 函式。

</dd> <dt>

*dwIoControlCode* 
</dt> <dd>

作業的控制項程式碼。 此值會識別要執行的特定作業，以及要在其上執行的裝置類型。 請使用 **IOCTL \_ 電池 \_ 集 \_ 資訊** 進行這種操作。

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

[**電池 \_ 設定 \_ 資訊**](battery-set-information-str.md)結構的指標。

</dd> <dt>

*nInBufferSize* 
</dt> <dd>

輸入緩衝區的大小（以位元組為單位）。

</dd> <dt>

*lpOutBuffer* 
</dt> <dd>

未搭配此作業使用;設定為 **Null**。

</dd> <dt>

*nOutBufferSize* 
</dt> <dd>

未搭配此作業使用;設定為零。

</dd> <dt>

*lpBytesReturned* 
</dt> <dd>

變數的指標，此變數會接收 *lpOutBuffer* 緩衝區中傳回的資料大小（以位元組為單位）。

如果輸出緩衝區太小而無法傳回任何資料，則呼叫會失敗，而 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 會傳回錯誤碼錯誤的 \_ \_ 緩衝區，而傳回的位元組計數為零。

如果 *lpOverlapped* 為 **null** (nonoverlapped I/o) ，即使 *lpOutBuffer* 為 **Null**， *lpBytesReturned* 也不能是 **null**。

如果 *lpOverlapped* 不是 **null** (重迭的 i/o) ， *lpBytesReturned* 可以是 **null**。 如果這是重迭的作業，您可以藉由呼叫 [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) 函數來取得傳回的位元組數目。 如果 *hDevice* 與 i/o 完成埠相關聯，您可以藉由呼叫 [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) 函數來取得傳回的位元組數目。

</dd> <dt>

*lpOverlapped* 
</dt> <dd>

重 [**迭結構的**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) 指標。

如果使用檔案旗標重迭旗標開啟 *hDevice* \_ \_ ， *lpOverlapped* 必須指向有效的 [](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped)重迭結構。 在此情況下， [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 會以 (非同步) 作業的重迭方式執行。 如果裝置是以檔案旗標重迭旗標開啟， \_ \_ 且 *lpOverlapped* 為 **Null**，則函式會以無法預期的方式失敗。

如果在未指定檔案旗標重迭旗標的情況下開啟 *hDevice* \_ ，則 \_ 會忽略 *lpOverlapped* ，並且在作業完成或發生錯誤之前，不會傳回 [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 函數。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果作業順利完成， [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 會傳回非零值。

如果作業失敗或擱置中， [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 會傳回零。 若要取得擴充的錯誤資訊，請呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)。

## <a name="remarks"></a>備註

如果要求的電池標籤與 \_ \_ 目前的電池標記不符，則所有設定電池資訊的要求都會完成，並出現「找不到錯誤檔案的狀態」 \_ 。

如需這項作業的重迭 i/o 含意，請參閱 [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 主題的「備註」一節。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                                                                                                                                                                                                         |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                                                                                                                                                                                |
| 標頭<br/>                   | <dl> <dt>Poclass .h;</dt><dt>Windows server 2008 R2、windows 7、Windows server 2008、Windows Vista、Windows server 2003 和 WINDOWS XP 上的 Batclass .h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[電池資訊](battery-information.md)
</dt> <dt>

[電源管理控制碼](power-management-control-codes.md)
</dt> <dt>

[**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[**電池 \_ 設定 \_ 資訊**](battery-set-information-str.md)
</dt> <dt>

[**IOCTL \_ 電池 \_ 查詢 \_ 資訊**](ioctl-battery-query-information.md)
</dt> <dt>

[**IOCTL \_ 電池 \_ 查詢 \_ 狀態**](ioctl-battery-query-status.md)
</dt> <dt>

[**IOCTL \_ 電池 \_ 查詢 \_ 標記**](ioctl-battery-query-tag.md)
</dt> </dl>

 

