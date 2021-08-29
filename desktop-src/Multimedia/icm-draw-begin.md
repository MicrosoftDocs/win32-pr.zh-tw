---
title: 'ICM_DRAW_BEGIN 訊息 (Vfw .h) '
description: ICM \_ 繪製 \_ 開始訊息會通知轉譯驅動程式，以準備繪製資料。
ms.assetid: e5ecd7dd-376b-422c-bbb8-4e7c41e3cac8
keywords:
- ICM_DRAW_BEGIN 訊息 Windows 多媒體
topic_type:
- apiref
api_name:
- ICM_DRAW_BEGIN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 987b10f3820262d24e0da9c42ecd4841b15c47985538af79c4bc2f8e097018c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117987621"
---
# <a name="icm_draw_begin-message"></a>ICM \_繪製 \_ 開始訊息

**ICM \_ 繪製 \_ 開始** 訊息會通知轉譯驅動程式，以準備繪製資料。


```C++
ICM_DRAW_BEGIN 
wParam = (DWORD) (LPVOID) &icdrwBgn; 
lParam = sizeof(ICDRAW); 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="icdrwBgn"></span><span id="icdrwbgn"></span><span id="ICDRWBGN"></span>*icdrwBgn*
</dt> <dd>

[**ICDRAWBEGIN**](/windows/desktop/api/Vfw/ns-vfw-icdrawbegin)結構的指標，其中包含輸入格式。

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

**ICDRAWBEGIN** 的大小（以位元組為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

\_如果驅動程式支援以指定的方式和格式將資料繪製到螢幕，則會傳回 ICERR OK，否則會傳回錯誤碼。 可能的錯誤值包括下列各項。



| 值               | 意義                                                                       |
|---------------------|-------------------------------------------------------------------------------|
| ICERR \_ BADFORMAT    | 不支援輸入或輸出格式。                                      |
| ICERR \_ NOTSUPPORTED | 驅動程式不會直接繪製到螢幕上，或不支援此訊息。 |



 

## <a name="remarks"></a>備註

如果您希望驅動程式將資料解壓縮到緩衝區中，請傳送 [**ICM \_ 解壓縮 \_ 開始**](icm-decompress-begin.md)訊息。

**ICM \_ draw \_ BEGIN** 和 [**ICM \_ draw \_ END**](icm-draw-end.md)訊息不會被嵌套。 如果您的驅動程式收到 **ICM \_ draw \_ 開始**，然後再以 **ICM \_ DRAW \_ END** 停止解壓縮，則應該以新的參數重新開機解壓縮。

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

 

 





