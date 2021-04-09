---
title: 'ICM_DRAW_CHANGEPALETTE 訊息 (Vfw .h) '
description: ICM \_ DRAW \_ CHANGEPALETTE 訊息會通知轉譯驅動程式，表示電影調色板正在變更。 您可以使用 ICDrawChangePalette 宏明確地傳送此訊息。
ms.assetid: 974fc0d8-d0c7-4a82-af84-68b53f753259
keywords:
- ICM_DRAW_CHANGEPALETTE message Windows 多媒體
topic_type:
- apiref
api_name:
- ICM_DRAW_CHANGEPALETTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6364abb2c535158b2e64ff311041b00490c5958c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843756"
---
# <a name="icm_draw_changepalette-message"></a>ICM \_ 繪圖 \_ CHANGEPALETTE 訊息

**ICM \_ DRAW \_ CHANGEPALETTE** 訊息會通知轉譯驅動程式，表示電影調色板正在變更。 您可以使用 [**ICDrawChangePalette**](/windows/desktop/api/Vfw/nf-vfw-icdrawchangepalette) 宏明確地傳送此訊息。


```C++
ICM_DRAW_CHANGEPALETTE 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = 0; 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*
</dt> <dd>

[**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo)結構的指標，其中包含新的格式和選擇性色彩表。

</dd> </dl>

## <a name="return-value"></a>傳回值

\_如果成功則傳回 ICERR OK，否則傳回 **FALSE** 。

## <a name="remarks"></a>備註

這則訊息應該由可安裝的轉譯處理常式所支援，這些處理常式會使用包含調色板的內部結構來繪製 Dib。

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

 

