---
title: 如何建立 ComboBoxEx 控制項
description: 本主題將示範如何建立 ComboBoxEx 控制項。
ms.assetid: E3D577AF-3290-431E-AA6C-1E9A9ED6448C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73989124982cb563fc008d7f3c543388cca685a5
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "103933756"
---
# <a name="how-to-create-a-comboboxex-control"></a>如何建立 ComboBoxEx 控制項

本主題將示範如何建立 ComboBoxEx 控制項。

## <a name="what-you-need-to-know"></a>您必須知道的事項

### <a name="technologies"></a>技術

-   [Windows 控制項](window-controls.md)

### <a name="prerequisites"></a>必要條件

-   C/C++
-   Windows 消費者介面程式設計

## <a name="instructions"></a>指示


若要建立 ComboBoxEx 控制項，請呼叫 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 函式，並使用 [**WC \_ ComboBoxEx**](common-control-window-classes.md) 做為視窗類別。 您必須先呼叫 [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) 函式來註冊視窗類別，並 \_ \_ 在伴隨的 [**InitCommonControlsEx**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) 結構中指定 ICC USEREX 類別位。

## <a name="complete-example"></a>完整範例

下列應用程式定義函式會使用主視窗中的 [**CBS \_ 下拉式**](combo-box-styles.md) 樣式來建立 ComboBoxEx 控制項。


```C++
// CreateComboEx - Registers the ComboBoxEx window class and creates
// a ComboBoxEx control in the client area of the main window.
//
// g_hwndMain - A handle to the main window.
// g_hinst    - A handle to the program instance.
HWND WINAPI CreateComboEx(void)
{
    HWND hwnd;
    INITCOMMONCONTROLSEX icex;

    icex.dwSize = sizeof(INITCOMMONCONTROLSEX);
    icex.dwICC = ICC_USEREX_CLASSES;

    InitCommonControlsEx(&icex);

    hwnd = CreateWindowEx(0, WC_COMBOBOXEX, NULL,
                    WS_BORDER | WS_VISIBLE |
                    WS_CHILD | CBS_DROPDOWN,
                    // No size yet--resize after setting image list.
                    0,      // Vertical position of Combobox
                    0,      // Horizontal position of Combobox
                    0,      // Sets the width of Combobox
                    100,    // Sets the height of Combobox
                    g_hwndMain,
                    NULL,
                    g_hinst,
                    NULL);

    return (hwnd);
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於 ComboBoxEx 控制項](comboboxex-controls.md)
</dt> <dt>

[ComboBoxEx 控制項參考](bumper-comboboxex-comboboxex-control-reference.md)
</dt> <dt>

[使用 ComboBoxEx 控制項](/windows/desktop/Controls/using-comboboxex)
</dt> <dt>

[ComboBoxEx](comboboxex-control-reference.md)
</dt> </dl>

 

 