---
description: WM \_ QUERYNEWPALETTE 訊息會通知視窗，指出它即將接收鍵盤焦點，讓視窗有機會在收到焦點時，實現其邏輯調色板。
ms.assetid: bc9f76ca-62af-4f0b-8791-49269a1b23d1
title: 'WM_QUERYNEWPALETTE 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ca664bbb6fb30a0508f9429dd62af489c092db7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973049"
---
# <a name="wm_querynewpalette-message"></a>WM \_ QUERYNEWPALETTE 訊息

**WM \_ QUERYNEWPALETTE** 訊息會通知視窗，指出它即將接收鍵盤焦點，讓視窗有機會在收到焦點時，實現其邏輯調色板。

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

不使用這個參數。

</dd> <dt>

*lParam* 
</dt> <dd>

不使用這個參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果視窗發現其邏輯元件，則必須傳回 **TRUE**;否則，它必須傳回 **FALSE**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[色彩總覽](colors.md)
</dt> <dt>

[色彩訊息](color-messages.md)
</dt> <dt>

[**WM \_ PALETTECHANGED**](wm-palettechanged.md)
</dt> <dt>

[**WM \_ PALETTEISCHANGING**](wm-paletteischanging.md)
</dt> </dl>

 

 
