---
title: 'WM_CAP_SET_VIDEOFORMAT 訊息 (Vfw .h) '
description: WM \_ CAP \_ 設定 \_ VIDEOFORMAT 訊息會設定所捕獲影片資料的格式。 您可以使用 capSetVideoFormat 宏明確地傳送此訊息。
ms.assetid: 4f9cf90d-7ccb-4fc7-aad5-3d7e082526be
keywords:
- WM_CAP_SET_VIDEOFORMAT 訊息 Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_SET_VIDEOFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c543f613fedf54518579829d6825bd20dc4738ae03cb77f0996f8a58a123cb76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118135011"
---
# <a name="wm_cap_set_videoformat-message"></a>WM \_ CAP \_ 設定 \_ VIDEOFORMAT 訊息

**WM \_ CAP \_ 設定 \_ VIDEOFORMAT** 訊息會設定所捕獲影片資料的格式。 您可以使用 [**capSetVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capsetvideoformat) 宏明確地傳送此訊息。


```C++
WM_CAP_SET_VIDEOFORMAT 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (psVideoFormat); 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*
</dt> <dd>

**S** 所參考之結構的大小（以位元組為單位）。

</dd> <dt>

<span id="psVideoFormat"></span><span id="psvideoformat"></span><span id="PSVIDEOFORMAT"></span>*psVideoFormat*
</dt> <dd>

[**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo)結構的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回 **TRUE** ，否則傳回 **FALSE** 。

## <a name="remarks"></a>備註

由於影片格式是裝置特定的，因此應用程式應該檢查此函式的傳回值，以判斷驅動程式是否接受格式。

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

 

