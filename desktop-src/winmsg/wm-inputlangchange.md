---
description: 在應用程式的輸入語言變更後，傳送至最上層受影響的視窗。 您應該進行任何應用程式專屬的設定，並將訊息傳遞至 DefWindowProc 函式，此函式會將訊息傳遞給所有的第一層子視窗。
ms.assetid: 4d403b1d-f6f7-40d5-9bf5-6a9c4da0803c
title: 'WM_INPUTLANGCHANGE 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72f56367045fe72a8288220e1aeef662e648d702c3b48ead23bf179142dff92c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118436243"
---
# <a name="wm_inputlangchange-message"></a>WM \_ INPUTLANGCHANGE 訊息

在應用程式的輸入語言變更後，傳送至最上層受影響的視窗。 您應該進行任何應用程式專屬的設定，並將訊息傳遞至 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函式，此函式會將訊息傳遞給所有的第一層子視窗。 這些子視窗可以將訊息傳遞至 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) ，讓它將訊息傳遞給其子視窗，依此類推。

視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。

```C++
#define WM_INPUTLANGCHANGE              0x0051
```

## <a name="parameters"></a>參數

<dl> <dt>

*wParam*

</dt> <dd>
  
類型： **WPARAM**

新地區設定的 [字碼頁](../Intl/code-pages.md) 。

</dd> <dt>

*lParam*

</dt> <dd>
 
類型： **LPARAM**

**HKL** 輸入地區設定識別碼。 如需詳細資訊，請參閱 [語言、地區設定和鍵盤配置](../inputdev/about-keyboard-input.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **LRESULT**

如果應用程式處理此訊息，則應該傳回非零值。

## <a name="remarks"></a>備註

您可以透過[LCIDToLocaleName](/windows/win32/api/winnls/nf-winnls-lcidtolocalename)函式來取得鍵盤[地區設定名稱](../Intl/locale-names.md)。 您可以使用地區設定名稱來使用 [新式地區設定函數](/windows/win32/intl/calling-the--locale-name--functions)：

```cpp
case WM_INPUTLANGCHANGE:
{
    HKL hkl = (HKL)lParam;
    WCHAR localeName[LOCALE_NAME_MAX_LENGTH];
    LCIDToLocaleName(MAKELCID(LOWORD(hkl), SORT_DEFAULT), localeName, LOCALE_NAME_MAX_LENGTH, 0);

    WCHAR lang[9];
    GetLocaleInfoEx(localeName, LOCALE_SISO639LANGNAME2, lang, 9);
}
```

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |

## <a name="see-also"></a>另請參閱

**參考**

- [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
- [**WM \_ INPUTLANGCHANGEREQUEST**](wm-inputlangchangerequest.md)

**概念**

- [Windows](windows.md) 
