---
description: 本節說明如何執行與視窗程式相關聯的下列工作。
ms.assetid: acc68991-4689-44dc-8547-a7b6153b0f62
title: 使用視窗程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f05e5999b216ad8c51be4de6fdec80b5f58ff94956f8c1129d74c3f7075a90eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028296"
---
# <a name="using-window-procedures"></a>使用視窗程式

本節說明如何執行與視窗程式相關聯的下列工作。

-   [設計視窗程式](#designing-a-window-procedure)
-   [建立視窗程式與視窗類別的關聯](#associating-a-window-procedure-with-a-window-class)
-   [子類別化視窗](#subclassing-a-window)

## <a name="designing-a-window-procedure"></a>設計視窗程式

下列範例顯示一般視窗程式的結構。 視窗程式在 **switch** 語句中使用 message 引數，並以個別的 **case** 語句處理個別訊息。 請注意，每個案例都會針對每個訊息傳回特定值。 針對它未處理的訊息，視窗程式會呼叫 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函數。


```
LRESULT CALLBACK MainWndProc(
    HWND hwnd,        // handle to window
    UINT uMsg,        // message identifier
    WPARAM wParam,    // first message parameter
    LPARAM lParam)    // second message parameter
{ 
 
    switch (uMsg) 
    { 
        case WM_CREATE: 
            // Initialize the window. 
            return 0; 
 
        case WM_PAINT: 
            // Paint the window's client area. 
            return 0; 
 
        case WM_SIZE: 
            // Set the size and position of the window. 
            return 0; 
 
        case WM_DESTROY: 
            // Clean up window-specific data objects. 
            return 0; 
 
        // 
        // Process other messages. 
        // 
 
        default: 
            return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    } 
    return 0; 
} 
```



當您建立視窗之後，就會傳送 [**WM \_ NCCREATE**](wm-nccreate.md) 訊息，但如果應用程式傳回 **FALSE** 來回應此訊息，則 [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) 函式會失敗。 在您的視窗建立之後，會傳送 [**WM \_ 建立**](wm-create.md) 訊息。

當您的視窗即將終結時，會傳送 [**WM 損 \_ 毀**](wm-destroy.md) 訊息。 [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow)函式會負責終結要終結之視窗的任何子視窗。 在終結視窗之前，會立即傳送 [**WM \_ NCDESTROY**](wm-ncdestroy.md) 訊息。

視窗程式至少應該處理 [**WM \_ 繪製**](../gdi/wm-paint.md) 訊息來自行繪製。 一般來說，它也應該處理滑鼠和鍵盤訊息。 請參閱個別訊息的描述，以判斷您的視窗程式是否應該處理這些訊息。

您的應用程式可以呼叫 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函數，做為訊息處理的一部分。 在這種情況下，應用程式可以先修改訊息參數，然後再將訊息傳遞至 **DefWindowProc**，或者它可以在執行自己的作業之後繼續進行預設處理。

對話方塊程式會收到 [**wm \_ INITDIALOG**](../dlgbox/wm-initdialog.md) 訊息，而不是使用 [**wm \_ 建立**](wm-create.md) 訊息，而且不會將未處理的訊息傳遞至 [**DefDlgProc**](/windows/win32/api/winuser/nf-winuser-defdlgprocw) 函式。 否則，對話方塊程式與視窗程式完全相同。

## <a name="associating-a-window-procedure-with-a-window-class"></a>建立視窗程式與視窗類別的關聯

在註冊類別時，您會將視窗程式與視窗類別產生關聯。 您必須以類別的相關資訊填入 [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) 結構，而且 **lpfnWndProc** 成員必須指定視窗程式的位址。 若要註冊類別，請將 **WNDCLASS** 結構的位址傳遞給 [**RegisterClass**](/windows/win32/api/winuser/nf-winuser-registerclassa) 函數。 在註冊視窗類別之後，視窗程式會自動與以該類別建立的每個新視窗相關聯。

下列範例顯示如何將上一個範例中的視窗程式與視窗類別產生關聯。


```
int APIENTRY WinMain( 
    HINSTANCE hinstance,  // handle to current instance 
    HINSTANCE hinstPrev,  // handle to previous instance 
    LPSTR lpCmdLine,      // address of command-line string 
    int nCmdShow)         // show-window type 
{ 
    WNDCLASS wc; 
 
    // Register the main window class. 
    wc.style = CS_HREDRAW | CS_VREDRAW; 
    wc.lpfnWndProc = (WNDPROC) MainWndProc; 
    wc.cbClsExtra = 0; 
    wc.cbWndExtra = 0; 
    wc.hInstance = hinstance; 
    wc.hIcon = LoadIcon(NULL, IDI_APPLICATION); 
    wc.hCursor = LoadCursor(NULL, IDC_ARROW); 
    wc.hbrBackground = GetStockObject(WHITE_BRUSH); 
    wc.lpszMenuName =  "MainMenu"; 
    wc.lpszClassName = "MainWindowClass"; 
 
    if (!RegisterClass(&wc)) 
       return FALSE; 
 
    // 
    // Process other messages. 
    // 
 
} 
```



## <a name="subclassing-a-window"></a>子類別化視窗

若要子類別化視窗的實例，請呼叫 [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) 函式，並指定視窗的控制碼，以將 GWL \_ WNDPROC 旗標和子類別程式的指標子類別化。 **SetWindowLong** 會傳回原始視窗程式的指標;使用這個指標可將訊息傳遞至原始程式。 子類別視窗程式必須使用 [**CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca) 函數來呼叫原始視窗程式。

> [!Note]  
> 若要撰寫與32位和64位版本的 Windows 相容的程式碼，請使用 [**SetWindowLongPtr**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra)函數。

 

下列範例顯示如何在對話方塊中子類別化編輯控制項的實例。 當控制項有輸入焦點時，子類別視窗程式可讓編輯控制項接收所有鍵盤輸入，包括 ENTER 和 TAB 鍵。


```
WNDPROC wpOrigEditProc; 
 
LRESULT APIENTRY EditBoxProc(
    HWND hwndDlg, 
    UINT uMsg, 
    WPARAM wParam, 
    LPARAM lParam) 
{ 
    HWND hwndEdit; 
 
    switch(uMsg) 
    { 
        case WM_INITDIALOG: 
            // Retrieve the handle to the edit control. 
            hwndEdit = GetDlgItem(hwndDlg, ID_EDIT); 
 
            // Subclass the edit control. 
            wpOrigEditProc = (WNDPROC) SetWindowLong(hwndEdit, 
                GWL_WNDPROC, (LONG) EditSubclassProc); 
            // 
            // Continue the initialization procedure. 
            // 
            return TRUE; 
 
        case WM_DESTROY: 
            // Remove the subclass from the edit control. 
            SetWindowLong(hwndEdit, GWL_WNDPROC, 
                (LONG) wpOrigEditProc); 
            // 
            // Continue the cleanup procedure. 
            // 
            break; 
    } 
    return FALSE; 
        UNREFERENCED_PARAMETER(lParam); 
} 
 
// Subclass procedure 
LRESULT APIENTRY EditSubclassProc(
    HWND hwnd, 
    UINT uMsg, 
    WPARAM wParam, 
    LPARAM lParam) 
{ 
    if (uMsg == WM_GETDLGCODE) 
        return DLGC_WANTALLKEYS; 
 
    return CallWindowProc(wpOrigEditProc, hwnd, uMsg, 
        wParam, lParam); 
} 
```



 

 
