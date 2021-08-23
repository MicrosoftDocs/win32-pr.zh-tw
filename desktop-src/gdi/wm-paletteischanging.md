---
description: WM \_ PALETTEISCHANGING 訊息會通知應用程式，應用程式會實現它的邏輯調色板。
ms.assetid: 64ec1042-0ab5-496f-9a88-2f293b412704
title: 'WM_PALETTEISCHANGING 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b0de17e7957e4b03c0a8fb942e7c0e4f94a3329e53cb039ce1d7f0a8c33aa89
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119717678"
---
# <a name="wm_paletteischanging-message"></a>WM \_ PALETTEISCHANGING 訊息

**WM \_ PALETTEISCHANGING** 訊息會通知應用程式，應用程式會實現它的邏輯調色板。

視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

即將實現其邏輯調色板的視窗控制碼。

</dd> <dt>

*lParam* 
</dt> <dd>

不使用這個參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果應用程式處理此訊息，它應該會傳回零。

## <a name="remarks"></a>備註

變更其調色板的應用程式不會在變更選擇區和傳送 [**WM \_ PALETTECHANGED**](wm-palettechanged.md) 訊息之前等候此訊息的確認。 如此一來，當應用程式收到此訊息時，可能已經變更了此元件。

如果應用程式忽略或無法處理這個訊息，而第二個應用程式發現它的選擇區，而第一個應用程式使用的是選擇區索引，則在後續的繪圖作業期間，使用者可能會看到非預期的色彩。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[色彩總覽](colors.md)
</dt> <dt>

[色彩訊息](color-messages.md)
</dt> <dt>

[**WM \_ PALETTECHANGED**](wm-palettechanged.md)
</dt> <dt>

[**WM \_ QUERYNEWPALETTE**](wm-querynewpalette.md)
</dt> </dl>

 

 
