---
description: 決定與視窗相關聯之文字的長度（以字元為單位）。
ms.assetid: 9e185435-a624-4380-adfd-be4f3645ee5d
title: 'WM_GETTEXTLENGTH 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1bc01f6f7a2b74df41e97a84bb4d7e17d9c3e21966215fcbcca04222d1d5537f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119710388"
---
# <a name="wm_gettextlength-message"></a>WM \_ GETTEXTLENGTH 訊息

決定與視窗相關聯之文字的長度（以字元為單位）。


```C++
#define WM_GETTEXTLENGTH                0x000E
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

未使用此參數，且必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

未使用此參數，且必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **LRESULT**

傳回值是文字的長度（以字元為單位），不包括終止的 null 字元。

## <a name="remarks"></a>備註

若為編輯控制項，要複製的文字是編輯控制項的內容。 在下拉式方塊中，文字是編輯控制項的內容 (或下拉式方塊的靜態文字) 部分。 若為按鈕，文字就是按鈕名稱。 若為其他視窗，則文字為視窗標題。 若要判斷清單方塊中專案的長度，應用程式可以使用 [**LB \_ GETTEXTLEN**](../controls/lb-gettextlen.md) 訊息。

傳送 **WM \_ GETTEXTLENGTH** 訊息時， [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函式會傳回文字的長度（以字元為單位）。 在某些條件下， **DefWindowProc** 函式會傳回大於文字實際長度的值。 這種情況會發生在 ANSI 和 Unicode 的特定混合中，而且是因為系統允許在文字內的 (DBCS) 字元中存在雙位元組字元集。 不過，傳回值一律會至少與文字的實際長度一樣大：因此，您可以一律使用它來引導緩衝區配置。 當應用程式同時使用 ANSI 函式和使用 Unicode 的通用對話時，就可能會發生這種行為。

若要取得文字的確切長度，請使用 [**WM \_ GETTEXT**](wm-gettext.md)、 [**LB \_ GETTEXT**](../controls/lb-gettext.md)或 [**CB \_ GETLBTEXT**](../controls/cb-getlbtext.md) 訊息或 [**GetWindowText**](/windows/win32/api/winuser/nf-winuser-getwindowtexta) 函數。

將 **WM \_ GETTEXTLENGTH** 訊息傳送至非文字靜態控制項（例如靜態點陣圖或靜態圖示 controlc）並不會傳回字串值。 相反地，它會傳回零。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**GetWindowText**](/windows/win32/api/winuser/nf-winuser-getwindowtexta)
</dt> <dt>

[**GetWindowTextLength**](/windows/win32/api/winuser/nf-winuser-getwindowtextlengtha)
</dt> <dt>

[**WM \_ GETTEXT**](wm-gettext.md)
</dt> <dt>

**概念**
</dt> <dt>

[Windows](windows.md)
</dt> <dt>

**其他資源**
</dt> <dt>

[**CB \_ GETLBTEXT**](../controls/cb-getlbtext.md)
</dt> <dt>

[**LB \_ GETTEXT**](../controls/lb-gettext.md)
</dt> <dt>

[**LB \_ GETTEXTLEN**](../controls/lb-gettextlen.md)
</dt> </dl>

 

 
