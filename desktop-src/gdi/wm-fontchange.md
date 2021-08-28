---
description: 應用程式會在 \_ 變更字型資源的集區之後，將 WM FONTCHANGE 訊息傳送至系統中的所有最上層視窗。
ms.assetid: 4774308e-2f18-4a35-a769-56871f3c29a2
title: 'WM_FONTCHANGE 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12c88edaf2db356fea2b92ce05769360ac9c8664e913ff6e5a05daaf245d1204
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119399928"
---
# <a name="wm_fontchange-message"></a>WM \_ FONTCHANGE 訊息

應用程式會在變更字型資源的集區之後，將 **WM \_ FONTCHANGE** 訊息傳送至系統中的所有最上層視窗。

若要傳送此訊息，請使用下列參數呼叫 [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) 函數。


```C++
SendMessage( 
  (HWND)  hWnd,              
  WM_FONTCHANGE,            
  (WPARAM)  wParam,          
  (LPARAM)  lParam            
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

## <a name="remarks"></a>備註

從系統新增或移除字型 (例如使用 [**AddFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-addfontresourcea) 或) [**RemoveFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea) 函式的應用程式，應該會將此訊息傳送至所有最上層視窗。

若要將 **WM \_ FONTCHANGE** 訊息傳送至所有最上層視窗，應用程式可以呼叫 **SendMessage** 函式，並將 *hwnd* 參數設定為 hwnd \_ 廣播。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[字型和文字總覽](fonts-and-text.md)
</dt> <dt>

[字型和文字訊息](font-and-text-messages.md)
</dt> <dt>

[**AddFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-addfontresourcea)
</dt> <dt>

[**RemoveFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea)
</dt> </dl>

 

 
