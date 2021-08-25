---
title: 如何建立 List-View 控制項
description: 本主題將示範如何建立清單視圖控制項。 若要建立清單視圖控制項，請使用 CreateWindow 或 CreateWindowEx 函式，並指定 WC \_ LISTVIEW 視窗類別。
ms.assetid: FEAA0ACA-A086-46DF-9DD2-A3E32F2CCDA3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d71eddfb60a2ea035a5afe62423289da40a47b61841d3ba58c4cafa2824a65b2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119826608"
---
# <a name="how-to-create-a-list-view-control"></a>如何建立 List-View 控制項

本主題將示範如何建立清單視圖控制項。 若要建立清單視圖控制項，請使用 [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) 或 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 函式，並指定 [**WC \_ LISTVIEW**](common-control-window-classes.md) 視窗類別。

您也可以建立清單視圖控制項作為對話方塊範本的一部分。 您必須指定 [**WC \_ LISTVIEW**](common-control-window-classes.md) 做為類別名稱。 若要使用清單視圖控制項作為對話方塊範本的一部分，您必須在建立對話方塊的實例之前，先呼叫 [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) 或 [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) 。

## <a name="what-you-need-to-know"></a>您必須知道的事項

### <a name="technologies"></a>技術

-   [Windows控制](window-controls.md)

### <a name="prerequisites"></a>必要條件

-   C/C++
-   Windows消費者介面程式設計

## <a name="instructions"></a>指示


請先呼叫 [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex)函式，並在隨附的 **InitCommonControlsEx** 結構中指定 [**ICC \_ LISTVIEW \_ 類別**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex)位，以註冊視窗類別。 這可確保已載入通用控制項 DLL。 接下來，使用 [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) 或 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 函式，並指定 [**WC \_ LISTVIEW**](common-control-window-classes.md) 視窗類別。

> [!Note]  
> 依預設，清單視圖控制項會使用圖示標題字型。 不過，您可以使用 [**WM \_ SETFONT**](/windows/desktop/winmsg/wm-setfont) 訊息來指定要用於文字的字型。 您應該先傳送此訊息，然後再插入任何專案。 控制項會使用由 **WM \_ SETFONT** 訊息所指定的字型維度來判斷間距和版面配置。 您也可以自訂每個專案的字型。 如需詳細資訊，請參閱 [自訂繪製](custom-draw.md)。

 

下列 c + + 程式碼範例會在報表檢視中建立清單視圖控制項。


```C++
// CreateListView: Creates a list-view control in report view.
// Returns the handle to the new control
// TO DO:  The calling procedure should determine whether the handle is NULL, in case 
// of an error in creation.
//
// HINST hInst: The global handle to the applicadtion instance.
// HWND  hWndParent: The handle to the control's parent window. 
//
HWND CreateListView (HWND hwndParent) 
{
    INITCOMMONCONTROLSEX icex;           // Structure for control initialization.
    icex.dwICC = ICC_LISTVIEW_CLASSES;
    InitCommonControlsEx(&icex);

    RECT rcClient;                       // The parent window's client area.

    GetClientRect (hwndParent, &rcClient); 

    // Create the list-view window in report view with label editing enabled.
    HWND hWndListView = CreateWindow(WC_LISTVIEW, 
                                     L"",
                                     WS_CHILD | LVS_REPORT | LVS_EDITLABELS,
                                     0, 0,
                                     rcClient.right - rcClient.left,
                                     rcClient.bottom - rcClient.top,
                                     hwndParent,
                                     (HMENU)IDM_CODE_SAMPLES,
                                     g_hInst,
                                     NULL); 

    return (hWndListView);
}

```




一般而言，清單視圖應用程式可讓使用者從某個視圖變更為另一個視圖。

下列 c + + 程式碼範例會變更清單視圖的視窗樣式，進而變更視圖。


```C++
// SetView: Sets a list-view's window style to change the view.
// hWndListView: A handle to the list-view control. 
// dwView:       A value specifying the new view style.
//
VOID SetView(HWND hWndListView, DWORD dwView) 
{ 
    // Retrieve the current window style. 
    DWORD dwStyle = GetWindowLong(hWndListView, GWL_STYLE); 
    
    // Set the window style only if the view bits changed.
    if ((dwStyle & LVS_TYPEMASK) != dwView) 
    {
        SetWindowLong(hWndListView,
                      GWL_STYLE,
                      (dwStyle & ~LVS_TYPEMASK) | dwView);
    }               // Logical OR'ing of dwView with the result of 
}                   // a bitwise AND between dwStyle and 
                    // the Unary complenent of LVS_TYPEMASK.

```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[清單視圖控制項參考](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[關於 List-View 控制項](list-view-controls-overview.md)
</dt> <dt>

[使用 List-View 控制項](using-list-view-controls.md)
</dt> </dl>

 

 