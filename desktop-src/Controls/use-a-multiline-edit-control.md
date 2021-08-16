---
title: 如何建立多行編輯控制項
description: 本主題將示範如何藉由將多行編輯控制項新增至視窗的工作區，來執行簡單的單字處理器。
ms.assetid: B955CC42-F89F-48EB-A19A-ADA6E5273EF6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d11100d4d6f82c7a352d4ddacaa7fc05694b4d54125febc766a6d3f1c68376e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117829069"
---
# <a name="how-to-create-a-multiline-edit-control"></a>如何建立多行編輯控制項

本主題將示範如何藉由將多行編輯控制項新增至視窗的工作區，來執行簡單的單字處理器。 藉由使用多行編輯控制項，使用者可以從功能表選取 [編輯命令]。 這些命令可讓使用者執行簡單的編輯作業，例如復原先前的動作、剪下或複製剪貼簿的選取專案、貼上剪貼簿中的文字，以及刪除目前的選取專案。

## <a name="what-you-need-to-know"></a>您必須知道的事項

### <a name="technologies"></a>技術

-   [Windows控制](window-controls.md)

### <a name="prerequisites"></a>必要條件

-   C/C++
-   Windows消費者介面程式設計

## <a name="instructions"></a>指示


您的應用程式必須包含程式碼，以建立的實例，並初始化多行編輯控制項，然後處理使用者編輯命令。

下列 c + + 程式碼範例會藉由將多行編輯控制項新增至視窗的工作區，來實作為簡單字處理器的大部分功能。 系統會自動執行編輯控制項的 wordwrap 作業，也會處理垂直捲動條的處理， (藉由在) 的 [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa)函式呼叫中指定 [**ES \_ AUTOVSCROLL**](edit-control-styles.md)來建立。

使用者編輯命令會透過 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 通知訊息傳送至視窗進程。

> [!Note]  
> 如果視窗包含 Windows 功能區，則必須調整編輯控制項的大小，以容納功能區的高度。 如需詳細資訊，請參閱[Windows 功能區架構](/windows/desktop/windowsribbon/-uiplat-windowsribbon-entry)。

 



```C++
#define ID_EDITCHILD 100
 
LRESULT CALLBACK MainWndProc(HWND hwnd,      // window handle 
                             UINT message,   // type of message 
                             WPARAM wParam,  // additional information 
                             LPARAM lParam)  // additional information 
{ 
    static HWND hwndEdit; 
 
    TCHAR lpszLatin[] =  L"Lorem ipsum dolor sit amet, consectetur "
                         L"adipisicing elit, sed do eiusmod tempor " 
                         L"incididunt ut labore et dolore magna " 
                         L"aliqua. Ut enim ad minim veniam, quis " 
                         L"nostrud exercitation ullamco laboris nisi " 
                         L"ut aliquip ex ea commodo consequat. Duis " 
                         L"aute irure dolor in reprehenderit in " 
                         L"voluptate velit esse cillum dolore eu " 
                         L"fugiat nulla pariatur. Excepteur sint " 
                         L"occaecat cupidatat non proident, sunt " 
                         L"in culpa qui officia deserunt mollit " 
                         L"anim id est laborum."; 
 
    switch (message) 
    { 
        case WM_CREATE: 
            hwndEdit = CreateWindowEx(
                                0, L"EDIT",   // predefined class 
                                NULL,         // no window title 
                                WS_CHILD | WS_VISIBLE | WS_VSCROLL | 
                                ES_LEFT | ES_MULTILINE | ES_AUTOVSCROLL, 
                                0, 0, 0, 0,   // set size in WM_SIZE message 
                                hwnd,         // parent window 
                                (HMENU) ID_EDITCHILD,   // edit control ID 
                                (HINSTANCE) GetWindowLongPtr(hwnd, GWLP_HINSTANCE), 
                                NULL);        // pointer not needed 
 
            // Add text to the window. 
            SendMessage(hwndEdit, WM_SETTEXT, 0, (LPARAM) lpszLatin); 
 
            return 0; 
 
        case WM_COMMAND: 
            switch (wParam) 
            { 
                case IDM_EDUNDO: 
                    // Send WM_UNDO only if there is something to be undone. 
 
                    if (SendMessage(hwndEdit, EM_CANUNDO, 0, 0)) 
                        SendMessage(hwndEdit, WM_UNDO, 0, 0); 
                    else 
                    {
                        MessageBox(hwndEdit, 
                                   L"Nothing to undo.", 
                                   L"Undo notification", 
                                   MB_OK); 
                    }
                    break; 
 
                case IDM_EDCUT: 
                    SendMessage(hwndEdit, WM_CUT, 0, 0); 
                    break; 
 
                case IDM_EDCOPY: 
                    SendMessage(hwndEdit, WM_COPY, 0, 0); 
                    break; 
 
                case IDM_EDPASTE: 
                    SendMessage(hwndEdit, WM_PASTE, 0, 0); 
                    break; 
 
                case IDM_EDDEL: 
                    SendMessage(hwndEdit, WM_CLEAR, 0, 0); 
                    break; 

                case IDM_ABOUT: 
                    DialogBox(hInst,                // current instance 
                              L"AboutBox",           // resource to use 
                              hwnd,                 // parent handle 
                              (DLGPROC) About); 
                    break; 

                default: 
                    return DefWindowProc(hwnd, message, wParam, lParam); 
            } 
            break; 

        case WM_SETFOCUS: 
            SetFocus(hwndEdit); 
            return 0; 

        case WM_SIZE: 
            // Make the edit control the size of the window's client area. 

            MoveWindow(hwndEdit, 
                       0, 0,                  // starting x- and y-coordinates 
                       LOWORD(lParam),        // width of client area 
                       HIWORD(lParam),        // height of client area 
                       TRUE);                 // repaint window 
            return 0; 

        case WM_DESTROY: 
            PostQuitMessage(0); 
            return 0; 

        default: 
            return DefWindowProc(hwnd, message, wParam, lParam); 
    } 
    return NULL; 
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於編輯控制項](about-edit-controls.md)
</dt> <dt>

[編輯控制項參考](bumper-edit-control-edit-control-reference.md)
</dt> <dt>

[使用編輯控制項](/windows/desktop/Controls/using-edit-controls)
</dt> <dt>

[編輯控制項](edit-controls.md)
</dt> </dl>

 

 