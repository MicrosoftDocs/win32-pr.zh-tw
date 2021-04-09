---
title: 'WM_CAP_GET_VIDEOFORMAT 訊息 (Vfw .h) '
description: WM \_ CAP \_ GET \_ VIDEOFORMAT 訊息會取得使用中的影片格式或影片格式所需大小的複本。 您可以使用 capGetVideoFormat 和 capGetVideoFormatSize 宏明確地傳送此訊息。
ms.assetid: ac72dfdb-fe1a-4007-bdce-41e5e67d076a
keywords:
- WM_CAP_GET_VIDEOFORMAT message Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_GET_VIDEOFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 072d71366efee550b037d4a20388817954937854
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934343"
---
# <a name="wm_cap_get_videoformat-message"></a>WM \_ CAP \_ 取得 \_ VIDEOFORMAT 訊息

**WM \_ CAP \_ GET \_ VIDEOFORMAT** 訊息會取得使用中的影片格式或影片格式所需大小的複本。 您可以使用 [**capGetVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capgetvideoformat) 和 [**capGetVideoFormatSize**](/windows/desktop/api/Vfw/nf-vfw-capgetvideoformatsize) 宏明確地傳送此訊息。


```C++
WM_CAP_GET_VIDEOFORMAT 
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

[**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo)結構的指標。 您也可以指定 **Null** 來取得所需的位元組數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回影片格式的大小（以位元組為單位），如果捕捉視窗未連接到 capture 驅動程式，則傳回零。 對於需要調色板的影片格式，也會傳回目前的調色板。

## <a name="remarks"></a>備註

由於壓縮的影片格式大小需求不同，因此應用程式必須先取出大小，然後配置記憶體，最後要求影片格式資料。

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

 

