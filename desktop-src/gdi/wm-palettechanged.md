---
description: '\_當具有鍵盤焦點的視窗已實現其邏輯調色板，進而變更系統調色板時，會將 WM PALETTECHANGED 訊息傳送至所有最上層和重迭的視窗。'
ms.assetid: 2eed568b-1a16-47d2-ae26-3f1dec35e893
title: 'WM_PALETTECHANGED 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5a02bffe5206c7550cce2ec62203f3dbea2d246
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692588"
---
# <a name="wm_palettechanged-message"></a>WM \_ PALETTECHANGED 訊息

當具有鍵盤焦點的視窗已實現其邏輯調色板，進而變更系統調色板時，會將 **WM \_ PALETTECHANGED** 訊息傳送至所有最上層和重迭的視窗。 此訊息可讓使用色彩選擇區但沒有鍵盤焦點的視窗實現其邏輯調色板，並更新其工作區。

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

造成系統調色板變更的視窗控制碼。

</dd> <dt>

*lParam* 
</dt> <dd>

不使用這個參數。

</dd> </dl>

## <a name="remarks"></a>備註

此訊息必須傳送至所有最上層和重迭的視窗，包括變更系統調色板的視窗。 如果有任何子視窗使用調色板，則也必須將此訊息傳遞給它們。

若要避免建立無限迴圈，接收此訊息的視窗必須找不到其調色板，除非它判斷 *wParam* 不包含自己的視窗控制碼。

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

[**WM \_ PALETTEISCHANGING**](wm-paletteischanging.md)
</dt> <dt>

[**WM \_ QUERYNEWPALETTE**](wm-querynewpalette.md)
</dt> </dl>

 

 
