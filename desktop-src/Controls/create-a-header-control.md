---
title: 如何建立標題控制項
description: 本主題將示範如何建立標題控制項，並將它放在父視窗的工作區中。
ms.assetid: 094AF70C-2761-439E-A1E3-0FD04212FE87
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ae5bb3ae9c323d30384f5d058a61393bf6425c2a27dfe67faa9cbedd4b3289e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120063198"
---
# <a name="how-to-create-a-header-control"></a>如何建立標題控制項

本主題將示範如何建立標題控制項，並將它放在父視窗的工作區中。 您可以使用 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 函式來建立標題控制項，並指定 [**WC \_ 標頭**](common-control-window-classes.md) 視窗類別和適當的 [標題控制項樣式](header-control-styles.md)。 載入通用控制項 DLL 時，會註冊此視窗類別。 若要確定已載入此 DLL，請使用 [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) 函數。

## <a name="what-you-need-to-know"></a>您必須知道的事項

### <a name="technologies"></a>技術

-   [Windows控制](window-controls.md)

### <a name="prerequisites"></a>必要條件

-   C/C++
-   Windows消費者介面程式設計

## <a name="instructions"></a>指示


下列 c + + 程式碼範例會先呼叫 [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) 函式來載入通用控制項 DLL。 然後，它會呼叫 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 函式來建立標題控制項。 控制項一開始是隱藏的。 [**HDM \_ 版面**](hdm-layout.md)配置訊息是用來計算控制項在父視窗內的大小與位置。 然後，控制項會重新置放並使其成為可見。



```C++
// DoCreateHeader - creates a header control that is positioned along 
//     the top of the parent window's client area. 
// Returns the handle to the header control. 
// hwndParent - handle to the parent window. 
// 
// Global variable 
//    g_hinst - handle to the application instance 
extern HINSTANCE g_hinst; 
//
// child-window identifier
int ID_HEADER;
//
HWND DoCreateHeader(HWND hwndParent) 
{ 
        HWND hwndHeader; 
        RECT rcParent; 
        HDLAYOUT hdl; 
        WINDOWPOS wp; 
 
        // Ensure that the common control DLL is loaded, and then create 
        // the header control. 
        INITCOMMONCONTROLSEX icex;  //declare an INITCOMMONCONTROLSEX Structure
        icex.dwSize = sizeof(INITCOMMONCONTROLSEX);
        icex.dwICC = ICC_LISTVIEW_CLASSES;   //set dwICC member to ICC_LISTVIEW_CLASSES    
                                             // this loads list-view and header control classes.
    InitCommonControlsEx(&icex); 
 
        if ((hwndHeader = CreateWindowEx(0, WC_HEADER, (LPCTSTR) NULL, 
                WS_CHILD | WS_BORDER | HDS_BUTTONS | HDS_HORZ, 
                0, 0, 0, 0, hwndParent, (HMENU) ID_HEADER, g_hinst, 
                (LPVOID) NULL)) == NULL) 
            return (HWND) NULL; 
 
        // Retrieve the bounding rectangle of the parent window's 
        // client area, and then request size and position values 
        // from the header control. 
        GetClientRect(hwndParent, &rcParent); 
 
        hdl.prc = &rcParent; 
        hdl.pwpos = &wp; 
        if (!SendMessage(hwndHeader, HDM_LAYOUT, 0, (LPARAM) &hdl)) 
            return (HWND) NULL; 
 
        // Set the size, position, and visibility of the header control. 
        SetWindowPos(hwndHeader, wp.hwndInsertAfter, wp.x, wp.y, 
            wp.cx, wp.cy, wp.flags | SWP_SHOWWINDOW); 
 
        return hwndHeader; 
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於標題控制項](header-controls.md)
</dt> <dt>

[標題控制項參考](bumper-header-control-header-control-reference.md)
</dt> <dt>

[使用標題控制項](using-header-controls.md)
</dt> </dl>

 

 