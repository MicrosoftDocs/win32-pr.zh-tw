---
description: 在主題變更事件之後廣播至每個視窗。 主題變更事件的範例包括啟用主題、停用主題，或從某個主題轉換成另一個主題。
ms.assetid: 1a4051ac-cc6e-4520-ab66-d0a41a8a4c73
title: 'WM_THEMECHANGED 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b070cb492fa5db94acb97cd07f3de87455189d542aaaad2a51a3e0ecc6b4268d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118199907"
---
# <a name="wm_themechanged-message"></a>WM \_ THEMECHANGED 訊息

在主題變更事件之後廣播至每個視窗。 主題變更事件的範例包括啟用主題、停用主題，或從某個主題轉換成另一個主題。


```C++
#define WM_THEMECHANGED                 0x031A
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

此參數已保留備用。

</dd> <dt>

*lParam* 
</dt> <dd>

此參數已保留備用。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **LRESULT**

如果應用程式處理此訊息，它應該會傳回零。

## <a name="remarks"></a>備註

視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。

> [!Note]  
> 此訊息是由作業系統所公佈。 應用程式通常不會傳送此訊息。

 

主題是控制面板的規格，因此會將控制項的視覺元素與功能分開處理。

若要釋放現有的主題控制碼，請呼叫 [**CloseThemeData**](/windows/win32/api/uxtheme/nf-uxtheme-closethemedata)。 若要取得新的主題控制碼，請使用 [**OpenThemeData**](/windows/win32/api/uxtheme/nf-uxtheme-openthemedata)。

在 **WM \_ THEMECHANGED** 廣播之後，任何現有的主題控制碼都無效。 有主題感知的視窗應該在收到 **WM \_ THEMECHANGED** 訊息時，釋放並重新開啟其任何既有的主題控制碼。 如果 [**OpenThemeData**](/windows/win32/api/uxtheme/nf-uxtheme-openthemedata) 函式傳回 **Null**，則視窗應該繪製 unthemed。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**其他資源**
</dt> <dt>

[**CloseThemeData**](/windows/win32/api/uxtheme/nf-uxtheme-closethemedata)
</dt> <dt>

[**IsThemeActive**](/windows/win32/api/uxtheme/nf-uxtheme-isthemeactive)
</dt> <dt>

[**OpenThemeData**](/windows/win32/api/uxtheme/nf-uxtheme-openthemedata)
</dt> </dl>

 

 
