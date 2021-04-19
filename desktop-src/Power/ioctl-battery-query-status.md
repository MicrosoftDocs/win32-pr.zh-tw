---
description: 捕獲電池的目前狀態。
ms.assetid: 7a7bf429-9b2c-4faf-9f27-fb5fd8dd18df
title: 'IOCTL_BATTERY_QUERY_STATUS 控制程式代碼 (Poclass) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_BATTERY_QUERY_STATUS
api_type:
- HeaderDef
api_location:
- Poclass.h
- BatClass.h
ms.openlocfilehash: e2de9d3ab48aec13a9a5c1957a5f98aefbe6a09f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106975094"
---
# <a name="ioctl_battery_query_status-control-code"></a>IOCTL \_ 電池 \_ 查詢 \_ 狀態控制項程式碼

捕獲電池的目前狀態。

若要執行這項作業，請使用下列參數呼叫 [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 函數。


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,           // handle to battery
  IOCTL_BATTERY_QUERY_STATUS, // dwIoControlCode
  (LPVOID) lpInBuffer,        // input buffer
  (DWORD) nInBufferSize,      // size of input buffer
  (LPVOID) lpOutBuffer,       // output buffer
  (DWORD) nOutBufferSize,     // size of output buffer
  (LPDWORD) lpBytesReturned,  // number of bytes returned
  (LPOVERLAPPED) lpOverlapped // OVERLAPPED structure
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hDevice* 
</dt> <dd>

要傳回其資訊之電池的控制碼。 若要取出設備控制碼，請呼叫 [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) 函式。

</dd> <dt>

*dwIoControlCode* 
</dt> <dd>

作業的控制項程式碼。 此值會識別要執行的特定作業，以及要在其上執行的裝置類型。 使用 **IOCTL \_ 電池 \_ 查詢 \_ 狀態** 進行此作業。

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

[**電池 \_ 等待 \_ 狀態**](battery-wait-status-str.md)結構的指標。

</dd> <dt>

*nInBufferSize* 
</dt> <dd>

輸入緩衝區的大小（以位元組為單位）。

</dd> <dt>

*lpOutBuffer* 
</dt> <dd>

[**電池 \_ 狀態**](battery-status-str.md)結構的指標。

</dd> <dt>

*nOutBufferSize* 
</dt> <dd>

輸出緩衝區的大小 (以位元組為單位)。

</dd> <dt>

*lpBytesReturned* 
</dt> <dd>

變數的指標，此變數會接收 *lpOutBuffer* 緩衝區中傳回的資料大小（以位元組為單位）。

如果輸出緩衝區太小而無法傳回任何資料，則呼叫會失敗，而 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 會傳回錯誤碼 **錯誤 \_ 的 \_ 緩衝區**，而傳回的位元組計數為零。

如果 *lpOverlapped* 為 **null** (nonoverlapped I/o) ，則 *lpBytesReturned* 不可以是 **null**。

如果 *lpOverlapped* 不是 **null** (重迭的 i/o) ， *lpBytesReturned* 可以是 **null**。 如果這是重迭的作業，您可以藉由呼叫 [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) 函數來取得傳回的位元組數目。 如果 *hDevice* 與 i/o 完成埠相關聯，您可以藉由呼叫 [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) 函數來取得傳回的位元組數目。

</dd> <dt>

*lpOverlapped* 
</dt> <dd>

重 [**迭結構的**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) 指標。

如果使用檔案 **\_ 旗 \_** 標重迭旗標開啟 hDevice， *lpOverlapped* 必須 [**指向有效的**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped)重迭結構。 在此情況下， [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 會以 (非同步) 作業的重迭方式執行。 如果裝置是以檔案 **旗標重 \_ \_** 迭旗標開啟，且 *lpOverlapped* 為 **Null**，則函式會以無法預期的方式失敗。

如果在未指定檔案 **\_ 旗 \_** 標重迭旗標的情況下開啟 hDevice，則會忽略 *lpOverlapped* ，並且在作業完成或發生錯誤之前，不會傳回 [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)函數。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果作業順利完成， [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 會傳回非零值。

如果作業失敗或擱置中， [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 會傳回零。 若要取得擴充的錯誤資訊，請呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)。

## <a name="remarks"></a>備註

此電池 IOCTL 會在作業傳回時，捕獲電池的狀態。 輸入參數結構、 [**電池 \_ 等待 \_ 狀態**](battery-wait-status-str.md)，表示要處理和傳回電池狀態的時間。

電池狀態的要求可以立即傳回，或可設定為在完成之前等候特定的條件。 例如，您可以對電池資訊提出要求，直到電池容量達到指定的點或電池狀態變更為止。

所有的電池資訊要求都會完成，並在要求的 **BatteryTag** 元素不符合目前電池標記的時 **\_ \_ \_ 找不到錯誤** 檔案的狀態。  (如需詳細資訊，請參閱 [電池標記](battery-information.md) 。 ) 這是用來確保傳回的電池資訊符合所要求電池的資訊。

如需這項作業的重迭 i/o 含意，請參閱 [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 主題的「備註」一節。

## <a name="examples"></a>範例

如需範例，請參閱 [列舉電池裝置](enumerating-battery-devices.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                                                                                                                                                                                                         |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                                                                                                                                                                                |
| 標頭<br/>                   | <dl> <dt>Poclass .h;</dt><dt>Windows server 2008 R2、windows 7、Windows server 2008、Windows Vista、Windows server 2003 和 WINDOWS XP 上的 BatClass .h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[電池資訊](battery-information.md)
</dt> <dt>

[電源管理控制碼](power-management-control-codes.md)
</dt> <dt>

[**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[**電池 \_ 狀態**](battery-status-str.md)
</dt> <dt>

[**電池 \_ 等待 \_ 狀態**](battery-wait-status-str.md)
</dt> <dt>

[**IOCTL \_ 電池 \_ 查詢 \_ 資訊**](ioctl-battery-query-information.md)
</dt> <dt>

[**IOCTL \_ 電池 \_ 查詢 \_ 標記**](ioctl-battery-query-tag.md)
</dt> <dt>

[**IOCTL \_ 電池 \_ 設定 \_ 資訊**](ioctl-battery-set-information.md)
</dt> </dl>

 

