---
description: 抓取目前的 AC 和 DC 背光等級和目前的電源狀態。
ms.assetid: c7b7c302-6e92-46a7-b9a6-e3f2a3e44d1b
title: 'IOCTL_VIDEO_QUERY_DISPLAY_BRIGHTNESS 控制程式代碼 (Ntddvdeo) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_VIDEO_QUERY_DISPLAY_BRIGHTNESS
api_type:
- HeaderDef
api_location:
- Ntddvdeo.h
ms.openlocfilehash: 673930fbde301c031049316255c9bcee40fd4e6a4f3c362977caf6e0569c5f5b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143411"
---
# <a name="ioctl_video_query_display_brightness-control-code"></a>IOCTL \_ 影片 \_ 查詢 \_ 顯示 \_ 亮度控制項程式碼

\[此控制項程式碼可在 [需求] 區段中指定的作業系統中使用。 Windows Server 2008 和 Windows Vista 中已移除對此控制項程式碼的支援。 請改用 [**WmiMonitorBrightness**](/windows/desktop/WmiCoreProv/wmimonitorbrightness) 類別。\]

抓取目前的 AC 和 DC 背光等級和目前的電源狀態。

若要執行這項作業，請使用下列參數呼叫 [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 函數。


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,                // handle to device
  IOCTL_VIDEO_QUERY_DISPLAY_BRIGHTNESS,  // dwIoControlCode
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

作業的控制項程式碼。 此值會識別要執行的特定作業，以及要在其上執行的裝置類型。 使用 **IOCTL \_ 影片 \_ 查詢 \_ 顯示 \_ 亮度** 來進行這種操作。

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

將接收 [**顯示 \_ 亮度**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85)) 結構之緩衝區的指標。

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

用來建立包含這項功能（Ntddvdeo）之應用程式的標頭檔，隨附于 Microsoft Windows 驅動程式開發工具組 (DDK) 。 如需取得 DDK 的詳細資訊，請參閱 [https://www.microsoft.com/whdc/devtools/ddk/default.mspx](https://msdn.microsoft.com/windows/hardware/gg454513) 。

或者，您可以定義此控制項程式碼，如下所示：

``` syntax
#define IOCTL_VIDEO_QUERY_DISPLAY_BRIGHTNESS \
  CTL_CODE(FILE_DEVICE_VIDEO, 0x126, METHOD_BUFFERED, FILE_ANY_ACCESS)
```

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows僅限 XP （含 SP1） \[ 桌面應用程式\]<br/>                                  |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 用戶端支援結束<br/>    | Windows XP 含 SP2<br/>                                                        |
| 伺服器支援結束<br/>    | Windows Server 2003 R2<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Ntddvdeo。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[背光控制項介面](backlight-control-interface.md)
</dt> <dt>

[**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[**顯示 \_ 亮度**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85))
</dt> <dt>

[**IOCTL \_ 影片 \_ 集 \_ 顯示 \_ 亮度**](ioctl-video-set-display-brightness.md)
</dt> </dl>

 

