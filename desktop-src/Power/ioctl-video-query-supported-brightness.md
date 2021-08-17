---
description: 抓取支援的背光等級。
ms.assetid: b4c1ee3f-af75-477e-b7ed-53be905374d7
title: 'IOCTL_VIDEO_QUERY_SUPPORTED_BRIGHTNESS 控制程式代碼 (Ntddvdeo) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_VIDEO_QUERY_SUPPORTED_BRIGHTNESS
api_type:
- HeaderDef
api_location:
- Ntddvdeo.h
ms.openlocfilehash: 0c41b6773b0ed64160e2ad8850b6092dd5ec987c3e6726ba1cd668909c266311
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143391"
---
# <a name="ioctl_video_query_supported_brightness-control-code"></a>IOCTL \_ 影片 \_ 查詢 \_ 支援的 \_ 亮度控制項程式碼

抓取支援的背光等級。

若要執行這項作業，請使用下列參數呼叫 [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 函數。


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,                // handle to device
  IOCTL_VIDEO_QUERY_SUPPORTED_BRIGHTNESS,  // dwIoControlCode
  NULL,                            // lpInBuffer
  0,                               // nInBufferSize
  (LPVOID) lpOutBuffer,            // output buffer
  (DWORD) nOutBufferSize,          // size of output buffer
  (LPDWORD) lpBytesReturned,       // number of bytes returned
  (LPOVERLAPPED) lpOverlapped      // OVERLAPPED structure
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hDevice* 
</dt> <dd>

的控制碼 \\ \\ 。 \\LCD 裝置。 若要取出設備控制碼，請呼叫 [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) 函式。

</dd> <dt>

*dwIoControlCode* 
</dt> <dd>

作業的控制項程式碼。 此值會識別要執行的特定作業，以及要在其上執行的裝置類型。 針對此作業使用 **IOCTL \_ 影片 \_ 查詢 \_ 支援的 \_ 亮度** 。

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

未搭配此作業使用;設定為 **Null**。

</dd> <dt>

*nInBufferSize* 
</dt> <dd>

未搭配此作業使用;設定為零。

</dd> <dt>

*lpOutBuffer* 
</dt> <dd>

接收可用電源等級陣列的緩衝區指標。 這個緩衝區的長度應為256個位元組。

</dd> <dt>

*nOutBufferSize* 
</dt> <dd>

輸出緩衝區的大小 (以位元組為單位)。

</dd> <dt>

*lpBytesReturned* 
</dt> <dd>

變數的指標，此變數會接收傳回的輸出資料大小（以位元組為單位）。

如果輸出緩衝區太小而無法傳回任何資料，則呼叫會失敗，而 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 會傳回錯誤碼錯誤的 \_ \_ 緩衝區，而傳回的位元組計數為零。

如果輸出緩衝區太小而無法容納所有資料，但可以保存某些專案，則作業系統會盡可能傳回最適合的值、呼叫會失敗、 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 傳回錯誤碼錯誤的 \_ \_ 資料，而 *lpBytesReturned* 則表示傳回的資料量。 您的應用程式應該使用相同的作業再次呼叫 [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) ，以指定新的起點。

如果 *lpOverlapped* 為 **null** (nonoverlapped I/o) ，則 *lpBytesReturned* 不可以是 **null**。

如果 *lpOverlapped* 不是 **null** (重迭的 i/o) ， *lpBytesReturned* 可以是 **null**。 如果這是重迭的作業，您可以藉由呼叫 [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) 函數來取得傳回的位元組數目。 如果 *hDevice* 與 i/o 完成埠相關聯，您可以藉由呼叫 [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) 函數來取得傳回的位元組數目。

</dd> <dt>

*lpOverlapped* 
</dt> <dd>

重 [**迭結構的**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) 指標。

如果使用檔案旗標重迭旗標開啟 *hDevice* \_ \_ ， *lpOverlapped* 必須指向有效的 [](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped)重迭結構。 在此情況下，作業會以 (非同步) 作業的重迭方式執行。 如果裝置是以檔案旗標重迭旗標開啟， \_ \_ 且 *lpOverlapped* 為 **Null**，則函式會以無法預期的方式失敗。

如果在未指定檔案旗標重迭旗標的情況下開啟 *hDevice* \_ \_ ，則會忽略 *lpOverlapped* ，除非作業完成或發生錯誤，否則 [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 不會傳回。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果作業順利完成， [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 會傳回非零值。

如果作業失敗或擱置中， [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 會傳回零。 若要取得擴充的錯誤資訊，請呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)。

## <a name="remarks"></a>備註

*LpOutBuffer* 陣列中的每個元素都是一個位元組的長度。 因此，當傳回時， *lpBytesReturned* 參數會指出支援的層級數目。 每個層級都是從0到100的值。 值愈大，背光愈亮。 無論電源來源為 AC 或 DC，都支援所有層級。

用來建立包含這項功能（Ntddvdeo）之應用程式的標頭檔，隨附于 Microsoft Windows 驅動程式開發工具組 (DDK) 。 如需取得 DDK 的詳細資訊，請參閱 [https://www.microsoft.com/whdc/devtools/ddk/default.mspx](https://msdn.microsoft.com/windows/hardware/gg454513) 。

或者，您可以定義此控制項程式碼，如下所示：

``` syntax
#define IOCTL_VIDEO_QUERY_SUPPORTED_BRIGHTNESS \
  CTL_CODE(FILE_DEVICE_VIDEO, 0x125, METHOD_BUFFERED, FILE_ANY_ACCESS)
```

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | WindowsVista、僅限 Windows XP 和 SP1 \[ desktop 應用程式\]<br/>                   |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Ntddvdeo。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[背光控制項介面](backlight-control-interface.md)
</dt> <dt>

[**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> </dl>

 

