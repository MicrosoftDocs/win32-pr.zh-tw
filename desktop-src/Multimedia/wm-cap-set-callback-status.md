---
title: 'WM_CAP_SET_CALLBACK_STATUS 訊息 (Vfw .h) '
description: WM \_ CAP \_ 設定 \_ 回呼 \_ 狀態訊息會在應用程式中設定狀態回呼函數。 當捕捉視窗狀態變更時，AVICap 會呼叫這個程式。 您可以使用 capSetCallbackOnStatus 宏明確地傳送此訊息。
ms.assetid: 451ba9f9-7bfb-4c57-af6c-d5f691f39618
keywords:
- WM_CAP_SET_CALLBACK_STATUS message Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_STATUS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 493893a51d51b1ce61d43ff54461bb71c08a9f6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464492"
---
# <a name="wm_cap_set_callback_status-message"></a>WM \_ CAP \_ 設定 \_ 回呼 \_ 狀態訊息

**WM \_ CAP \_ 設定 \_ 回呼 \_ 狀態** 消息會在應用程式中設定狀態回呼函數。 當捕捉視窗狀態變更時，AVICap 會呼叫這個程式。 您可以使用 [**capSetCallbackOnStatus**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonstatus) 宏明確地傳送此訊息。


```C++
WM_CAP_SET_CALLBACK_STATUS 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*
</dt> <dd>

狀態回呼函數的指標，其類型為 [**capStatusCallback**](/windows/desktop/api/Vfw/nc-vfw-capstatuscallbacka)。 針對此參數指定 **Null** ，以停用先前安裝的狀態回呼函數。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回 **TRUE** ; 如果串流捕捉或單一框架捕獲會話正在進行中，則傳回 **FALSE** 。

## <a name="remarks"></a>備註

應用程式可以選擇性地設定狀態回呼函數。 如果設定，AVICap 會在下列情況下呼叫此程式：

-   已完成捕獲會話。
-   Capture 驅動程式已成功連線到捕捉視窗。
-   建立最佳的調色板。
-   報告的已捕獲框架數目。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                       |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Vfw。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[影片捕獲](video-capture.md)
</dt> <dt>

[影片捕獲訊息](video-capture-messages.md)
</dt> </dl>

 

 





