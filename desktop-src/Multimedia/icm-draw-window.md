---
title: 'ICM_DRAW_WINDOW 訊息 (Vfw .h) '
description: ICM \_ 繪圖 \_ 視窗訊息會通知轉譯驅動程式，表示需要重新繪製為 ICM \_ 繪圖 \_ 開始訊息指定的視窗。
ms.assetid: 4df1b9a7-8d61-4e79-8f43-1e7ee266375c
keywords:
- ICM_DRAW_WINDOW message Windows 多媒體
topic_type:
- apiref
api_name:
- ICM_DRAW_WINDOW
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 290b123fadcaf46a315c42e3ce9a530c5d5d36c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464992"
---
# <a name="icm_draw_window-message"></a>ICM \_ 繪製 \_ 視窗訊息

**Icm \_ 繪圖 \_ 視窗** 訊息會通知轉譯驅動程式，表示需要重新繪製為 [**ICM \_ 繪圖 \_ 開始**](icm-draw-begin.md)訊息指定的視窗。 視窗已移動或暫時遮蔽。 您可以使用 [**ICDrawWindow**](/windows/desktop/api/Vfw/nf-vfw-icdrawwindow) 宏明確地傳送此訊息。


```C++
ICM_DRAW_WINDOW 
wParam = (DWORD_PTR) (LPVOID) prc; 
lParam = 0; 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="prc"></span><span id="PRC"></span>*中國*
</dt> <dd>

螢幕座標中目的地矩形的指標。 如果這個參數指向空的矩形，則應該關閉繪製。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則會傳回 ICERR \_ OK，否則會傳回錯誤。

## <a name="remarks"></a>備註

此訊息是由執行自己的非同步解壓縮、時間和繪圖的硬體所支援。

影片重迭驅動程式會在視窗被遮蔽或移動時，使用此訊息來繪製。 當其他視窗完全隱藏指定給 [**ICM \_ 繪圖 \_ 開始**](icm-draw-begin.md) 的視窗時，目的地矩形會是空的。 當發生這種情況時，驅動程式應該關閉影片重迭硬體。

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

 

 





