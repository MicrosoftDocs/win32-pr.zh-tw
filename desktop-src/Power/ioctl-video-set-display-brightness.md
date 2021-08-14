---
description: 設定目前的 AC 和 DC 背光等級。
ms.assetid: baa77811-046d-4a07-b3df-2a31fba2d9a7
title: 'IOCTL_VIDEO_SET_DISPLAY_BRIGHTNESS 控制程式代碼 (Ntddvdeo) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_VIDEO_SET_DISPLAY_BRIGHTNESS
api_type:
- HeaderDef
api_location:
- Ntddvdeo.h
ms.openlocfilehash: ec4bb5200378f9f530913f26d33bfbd485d81ae184c7b478a51c90bca18d95da
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961848"
---
# <a name="ioctl_video_set_display_brightness-control-code"></a>IOCTL \_ 影片 \_ 集 \_ 顯示 \_ 亮度控制項程式碼

設定目前的 AC 和 DC 背光等級。

若要執行這項作業，請使用下列參數呼叫 [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 函數。


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,            // handle to device
  IOCTL_VIDEO_SET_DISPLAY_BRIGHTNESS, // dwIoControlCode
  (LPVOID) lpInBuffer,         // input buffer
  (DWORD) nInBufferSize,       // size of the input buffer
  NULL,                        // lpOutBuffer
  0,                           // nOutBufferSize 
  (LPDWORD) lpBytesReturned,   // number of bytes returned
  (LPOVERLAPPED) lpOverlapped  // OVERLAPPED structure
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

作業的控制項程式碼。 此值會識別要執行的特定作業，以及要在其上執行的裝置類型。 使用 **IOCTL \_ VIDEO \_ SET \_ 顯示器 \_ 亮度** 進行這種操作。

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

[**顯示 \_ 亮度**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85))結構的指標。

</dd> <dt>

*nInBufferSize* 
</dt> <dd>

*LpOutBuffer* 所指向的緩衝區大小（以位元組為單位）。

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

變數的指標，此變數會接收輸出緩衝區中函數所傳回的實際位元組計數。

如果 *lpOverlapped* 為 **Null** (nonoverlapped i/o) ，則會在內部使用 *lpBytesReturned* ，且不能是 **null**。

如果 *lpOverlapped* 不是 **null** (重迭的 i/o) ， *lpBytesReturned* 可以是 **null**。

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

在 [**顯示 \_ 亮度**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85))結構的 **ucACBrightness** 和 **ucDCBrightness** 成員中指定的值，必須先前由 [**IOCTL \_ 影片 \_ 查詢 \_ 支援的 \_ 亮度**](ioctl-video-query-supported-brightness.md)傳回。 例如，如果支援的值為10、20、30、40、50、60、70、80、90和100，則使用值33會是錯誤。

用來建立包含這項功能（Ntddvdeo）之應用程式的標頭檔，隨附于 Microsoft Windows 驅動程式開發工具組 (DDK) 。 如需取得 DDK 的詳細資訊，請參閱 [https://www.microsoft.com/whdc/devtools/ddk/default.mspx](https://msdn.microsoft.com/windows/hardware/gg454513) 。

或者，您可以定義此控制項程式碼，如下所示：

``` syntax
#define IOCTL_VIDEO_SET_DISPLAY_BRIGHTNESS \
  CTL_CODE(FILE_DEVICE_VIDEO, 0x127, METHOD_BUFFERED, FILE_ANY_ACCESS)
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
</dt> <dt>

[**顯示 \_ 亮度**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85))
</dt> <dt>

[**IOCTL \_ 影片 \_ 查詢 \_ 顯示 \_ 亮度**](ioctl-video-query-display-brightness.md)
</dt> <dt>

[**IOCTL \_ 影片 \_ 查詢 \_ 支援的 \_ 亮度**](ioctl-video-query-supported-brightness.md)
</dt> </dl>

 

