---
title: 'WM_CAP_SET_CALLBACK_VIDEOSTREAM 訊息 (Vfw .h) '
description: WM \_ CAP \_ SET \_ 回呼 \_ m 訊息會在應用程式中設定回呼函數。
ms.assetid: 590089b8-7a8d-476b-9b81-f96bf73b0369
keywords:
- WM_CAP_SET_CALLBACK_VIDEOSTREAM 訊息 Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_VIDEOSTREAM
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2cdb4d7d18997fe437609b43a266242f04bd0bc2bb25429191d944240706244
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118940716"
---
# <a name="wm_cap_set_callback_videostream-message"></a>WM \_ CAP \_ 設定 \_ 回呼 \_ m 訊息

**WM \_ CAP \_ SET \_ 回呼 \_ m** 訊息會在應用程式中設定回呼函數。 當視訊緩衝區填滿時，AVICap 會在串流處理期間呼叫此程式。 您可以使用 [**capSetCallbackOnVideoStream**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonvideostream) 宏明確地傳送此訊息。


```C++
WM_CAP_SET_CALLBACK_VIDEOSTREAM 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*
</dt> <dd>

影片資料流程回呼函數的指標，其類型為 [**capVideoStreamCallback**](/windows/desktop/api/Vfw/nc-vfw-capvideocallback)。 針對此參數指定 **Null** ，以停用先前安裝的影片資料流程回呼函式。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回 **TRUE** ; 如果串流捕捉或單一框架捕獲會話正在進行中，則傳回 **FALSE** 。

## <a name="remarks"></a>備註

捕捉視窗會先呼叫回呼函式，再將捕獲的框架寫入磁片。 這可讓應用程式視需要修改框架。

如果影片資料流程回呼函式用於串流捕捉，則必須先安裝該程式，然後再啟動 capture 會話，而且在會話期間必須保持啟用狀態。 您可以在串流處理的結束之後停用此功能。

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

 

 





