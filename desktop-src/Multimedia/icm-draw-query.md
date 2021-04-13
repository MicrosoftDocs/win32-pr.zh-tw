---
title: 'ICM_DRAW_QUERY 訊息 (Vfw .h) '
description: ICM \_ DRAW \_ 查詢訊息會查詢轉譯驅動程式，以判斷它是否可以轉譯特定格式的資料。 您可以使用 ICDrawQuery 宏明確地傳送此訊息。
ms.assetid: b829a04b-c1be-47c6-96e9-a6dc6f802811
keywords:
- ICM_DRAW_QUERY message Windows 多媒體
topic_type:
- apiref
api_name:
- ICM_DRAW_QUERY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27266484cffa503583df32b60c6e8a0c04f344f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465668"
---
# <a name="icm_draw_query-message"></a>ICM \_ 繪製 \_ 查詢訊息

**ICM \_ DRAW \_ 查詢** 訊息會查詢轉譯驅動程式，以判斷它是否可以轉譯特定格式的資料。 您可以使用 [**ICDrawQuery**](/windows/desktop/api/Vfw/nf-vfw-icdrawquery) 宏明確地傳送此訊息。


```C++
ICM_DRAW_QUERY 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = 0; 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*
</dt> <dd>

[**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo)結構的指標，其中包含輸入格式。

</dd> </dl>

## <a name="return-value"></a>傳回值

\_如果驅動程式能以指定的格式或 ICERR BADFORMAT 轉譯資料，則會傳回 ICERR OK （否則為） \_ 。

## <a name="remarks"></a>備註

這則訊息與 [**ICM \_ DRAW \_ 開始**](icm-draw-begin.md) 訊息不同之處在于，它會查詢驅動程式的一般意義。 **ICM \_DRAW \_ BEGIN** 會決定驅動程式是否可以在特定情況下使用指定的格式來繪製資料，例如延展影像。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                       |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Vfw。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[影片壓縮管理員](video-compression-manager.md)
</dt> <dt>

[影片壓縮訊息](video-compression-messages.md)
</dt> </dl>

 

