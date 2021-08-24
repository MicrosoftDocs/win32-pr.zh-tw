---
description: 抓取 batterys 目前的標記。
ms.assetid: 0bbe59ba-e037-47ce-a54a-6500ea7c9bc5
title: 'IOCTL_BATTERY_QUERY_TAG 控制程式代碼 (Poclass) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_BATTERY_QUERY_TAG
api_type:
- HeaderDef
api_location:
- Poclass.h
- BatClass.h
ms.openlocfilehash: c68c9dc2385803155a6c0f8fd2a5b7c84cedaa8e78c98ae2baca6909104e7315
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143511"
---
# <a name="ioctl_battery_query_tag-control-code"></a>IOCTL \_ 電池 \_ 查詢 \_ 標記控制程式代碼

抓取電池的目前標記。

若要執行這項作業，請使用下列參數呼叫 [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 函數。


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,            // handle to battery
  IOCTL_BATTERY_QUERY_TAG,     // dwIoControlCode
  (LPVOID) lpInBuffer,         // input buffer
  (DWORD) nInBufferSize,       // size of input buffer
  (LPVOID) lpOutBuffer,        // output buffer
  (DWORD) nOutBufferSize,      // size of output buffer
  (LPDWORD) lpBytesReturned,   // number of bytes returned
  (LPOVERLAPPED) lpOverlapped);// OVERLAPPED structure
```



## <a name="parameters"></a>參數

<dl> <dt>

*hDevice* 
</dt> <dd>

要從中抓取標記之電池的控制碼。 若要取出設備控制碼，請呼叫 [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) 函式。

</dd> <dt>

*dwIoControlCode* 
</dt> <dd>

作業的控制項程式碼。 此值會識別要執行的特定作業，以及要在其上執行的裝置類型。 針對此作業使用 **IOCTL \_ 電池 \_ 查詢 \_ 標記** 。

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

**ULONG** 輸入緩衝區的指標。 值指出沒有電池時要等候的毫秒數。 -1 的值表示要求將會無限期等候 (或直到其他事件) 取消為止。

</dd> <dt>

*nInBufferSize* 
</dt> <dd>

輸入緩衝區的大小（以位元組為單位）。

</dd> <dt>

*lpOutBuffer* 
</dt> <dd>

**ULONG** 輸出緩衝區的指標。 成功時，此緩衝區會包含目前的電池標記，它可以是任何值，但電池 \_ 標記 \_ 無效。 失敗時，如果 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)傳回錯誤碼錯誤檔案，則此緩衝區包含值 **電池 \_ 標記 \_ 無效**。 **\_ \_ \_**

</dd> <dt>

*nOutBufferSize* 
</dt> <dd>

輸出緩衝區的大小 (以位元組為單位)。

</dd> <dt>

*lpBytesReturned* 
</dt> <dd>

變數的指標，此變數會接收儲存在 *lpOutBuffer* 緩衝區中的資料大小（以位元組為單位）。

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

此電池 IOCTL 會抓取電池的目前標記。 電池標籤是唯一的非零值，會在實體電池重新插入、更換或進行任何特性變更時變更。 如需電池標記何時變更、如何偵測變更，以及應用程式應該在電池標記變更後如何進行的詳細資訊，請參閱 [電池資訊](battery-information.md) 總覽主題中的電池標記一節。 當電池不存在時，此要求會等待指定的時間，如果仍然沒有電池，則會傳回 **\_ \_ \_ 找不** 到的錯誤檔案，並將電池標籤設為 **\_ \_ 無效** 的電池標記。 如需詳細資訊， (查看電池資訊。 ) 

所有的電池資訊要求都需要呼叫者提供相符的電池標記。 這可確保呼叫端會針對每個要求接收相同電池的資訊，並確保呼叫端知道電池變更，而不會進行持續輪詢。

如需這項作業的重迭 i/o 含意，請參閱 [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 主題的「備註」一節。

## <a name="examples"></a>範例

如需範例，請參閱 [列舉電池裝置](enumerating-battery-devices.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                                                                                                                                                                                                         |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                                                                                                                                                                                |
| 標頭<br/>                   | <dl> <dt>Poclass .h;</dt><dt>Windows server 2008 R2、Windows 7、Windows Server 2008、Windows Vista、Windows Server 2003 和 Windows XP 上的 BatClass .h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[電池資訊](battery-information.md)
</dt> <dt>

[電源管理控制碼](power-management-control-codes.md)
</dt> <dt>

[**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[**IOCTL \_ 電池 \_ 查詢 \_ 資訊**](ioctl-battery-query-information.md)
</dt> <dt>

[**IOCTL \_ 電池 \_ 查詢 \_ 狀態**](ioctl-battery-query-status.md)
</dt> <dt>

[**IOCTL \_ 電池 \_ 設定 \_ 資訊**](ioctl-battery-set-information.md)
</dt> </dl>

 

