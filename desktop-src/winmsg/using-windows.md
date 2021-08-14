---
description: 本章節中的範例說明如何執行與使用 windows 相關聯的工作。
ms.assetid: 7695fb64-3918-4d9a-8cd8-01d20edd9c55
title: 使用 Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75681987a4bc012618135f666b3ff973880b8129d2ad1ee896bcdbed266d179d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118436964"
---
# <a name="using-windows"></a>使用 Windows

本節中的範例說明如何執行下列工作：

-   [建立主視窗](#creating-a-main-window)
-   [建立、列舉及調整子 Windows](#creating-enumerating-and-sizing-child-windows)
-   [終結視窗](#destroying-a-window)
-   [使用分層 Windows](#using-layered-windows)

## <a name="creating-a-main-window"></a>建立主視窗

應用程式所建立的第一個視窗通常是主視窗。 您可以使用 [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) 函式來建立主視窗，指定視窗類別、視窗名稱、視窗樣式、大小、位置、功能表控制碼、實例控制碼和建立資料。 主視窗屬於應用程式定義的視窗類別，因此您必須先註冊視窗類別並提供類別的視窗程式，才能建立主視窗。

大部分的應用程式通常會使用 [**WS \_ OVERLAPPEDWINDOW**](window-styles.md) 樣式來建立主視窗。 此樣式會為視窗提供標題列、視窗功能表、調整大小框線，以及最小化和最大化按鈕。 [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa)函式會傳回可唯一識別視窗的控制碼。

下列範例會建立一個屬於應用程式定義視窗類別的主視窗。 視窗名稱（ **主視窗**）將會出現在視窗的標題列中。 藉由結合 [**ws \_ VSCROLL**](window-styles.md) 和 **Ws \_ HSCROLL** 樣式與 **Ws \_ OVERLAPPEDWINDOW** 樣式，應用程式除了 **ws \_ OVERLAPPEDWINDOW** 樣式所提供的元件之外，還會建立具有水準和垂直捲動條的主視窗。 四次的 **CW \_ USEDEFAULT** 常數會將視窗的初始大小和位置設定為系統定義的預設值。 藉由指定 **Null** 而非功能表控點，視窗將會為視窗類別定義功能表。


```
HINSTANCE hinst; 
HWND hwndMain; 
 
// Create the main window. 
 
hwndMain = CreateWindowEx( 
    0,                      // no extended styles           
    "MainWClass",           // class name                   
    "Main Window",          // window name                  
    WS_OVERLAPPEDWINDOW |   // overlapped window            
             WS_HSCROLL |   // horizontal scroll bar        
             WS_VSCROLL,    // vertical scroll bar          
    CW_USEDEFAULT,          // default horizontal position  
    CW_USEDEFAULT,          // default vertical position    
    CW_USEDEFAULT,          // default width                
    CW_USEDEFAULT,          // default height               
    (HWND) NULL,            // no parent or owner window    
    (HMENU) NULL,           // class menu used              
    hinst,                  // instance handle              
    NULL);                  // no window creation data      
 
if (!hwndMain) 
    return FALSE; 
 
// Show the window using the flag specified by the program 
// that started the application, and send the application 
// a WM_PAINT message. 
 
ShowWindow(hwndMain, SW_SHOWDEFAULT); 
UpdateWindow(hwndMain); 
```



請注意，上述範例會在建立主視窗之後呼叫 [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) 函式。 這樣做的原因是，系統不會在建立後自動顯示主視窗。 藉由將 **SW \_ SHOWDEFAULT** 旗標傳遞給 **ShowWindow**，應用程式可讓啟動應用程式的程式設定主視窗的初始顯示狀態。 [**UpdateWindow**](/windows/win32/api/winuser/nf-winuser-updatewindow)函式會將它的第一個 [**WM \_ 油漆**](../gdi/wm-paint.md)訊息傳送給視窗。

## <a name="creating-enumerating-and-sizing-child-windows"></a>建立、列舉及調整子 Windows

您可以使用子視窗，將視窗的工作區分割成不同的功能區域。 建立子視窗就像建立主視窗一樣，您也可以使用 [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) 函數。 若要建立應用程式定義視窗類別的視窗，您必須先註冊視窗類別並提供視窗程式，然後再建立子視窗。 您必須提供子視窗的 [**WS \_ 子**](window-styles.md) 系樣式，並在建立時指定子視窗的父視窗。

下列範例會建立三個大小相同的子視窗，將應用程式主視窗的工作區分割成三個功能區域。 每個子視窗的高度與主視窗的工作區高度相同，但每一個視窗的寬度都是三分之一。 主視窗會建立子視窗來回應 [**WM \_ 建立**](wm-create.md) 訊息，而主視窗會在其本身的視窗建立程式期間收到此訊息。 因為每個子視窗都有 [**WS \_ 框線**](window-styles.md) 樣式，所以每個都有一個細線框線。 此外，因為未指定 **WS \_ VISIBLE** 樣式，所以一開始會隱藏每個子視窗。 另外也請注意，每個子視窗都被指派一個子視窗識別碼。

主視窗會調整子視窗的大小並放置子視窗，以回應其大小變更時，主視窗接收到的 [**WM \_ 大小**](wm-size.md) 訊息。 為了回應 **WM \_ 大小**，主視窗會使用 [**GetClientRect**](/windows/win32/api/winuser/nf-winuser-getclientrect) 函數抓取其工作區的維度，然後將維度傳遞給 [**EnumChildWindows**](/windows/win32/api/winuser/nf-winuser-enumchildwindows) 函數。 **EnumChildWindows** 會依次將控制碼傳遞至應用程式定義的 [**EnumChildProc**](/previous-versions/windows/desktop/legacy/ms633493(v=vs.85)) 回呼函數。 此函式會藉由呼叫 [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) 函式來調整每個子視窗的大小和位置;大小和位置是以主視窗工作區的維度和子視窗的識別碼為基礎。 之後， **EnumChildProc** 會呼叫 [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) 函式，讓視窗可見。


```
#define ID_FIRSTCHILD  100 
#define ID_SECONDCHILD 101 
#define ID_THIRDCHILD  102 
 
LONG APIENTRY MainWndProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    RECT rcClient; 
    int i; 
 
    switch(uMsg) 
    { 
        case WM_CREATE: // creating main window  
 
            // Create three invisible child windows. 

            for (i = 0; i < 3; i++) 
            { 
                CreateWindowEx(0, 
                               "ChildWClass", 
                               (LPCTSTR) NULL, 
                               WS_CHILD | WS_BORDER, 
                               0,0,0,0, 
                               hwnd, 
                               (HMENU) (int) (ID_FIRSTCHILD + i), 
                               hinst, 
                               NULL); 
            }
 
            return 0; 
 
        case WM_SIZE:   // main window changed size 
 
            // Get the dimensions of the main window's client 
            // area, and enumerate the child windows. Pass the 
            // dimensions to the child windows during enumeration. 
 
            GetClientRect(hwnd, &rcClient); 
            EnumChildWindows(hwnd, EnumChildProc, (LPARAM) &rcClient); 
            return 0; 

        // Process other messages. 
    } 
    return DefWindowProc(hwnd, uMsg, wParam, lParam); 
} 
 
BOOL CALLBACK EnumChildProc(HWND hwndChild, LPARAM lParam) 
{ 
    LPRECT rcParent; 
    int i, idChild; 
 
    // Retrieve the child-window identifier. Use it to set the 
    // position of the child window. 
 
    idChild = GetWindowLong(hwndChild, GWL_ID); 
 
    if (idChild == ID_FIRSTCHILD) 
        i = 0; 
    else if (idChild == ID_SECONDCHILD) 
        i = 1; 
    else 
        i = 2; 
 
    // Size and position the child window.  
 
    rcParent = (LPRECT) lParam; 
    MoveWindow(hwndChild, 
               (rcParent->right / 3) * i, 
               0, 
               rcParent->right / 3, 
               rcParent->bottom, 
               TRUE); 
 
    // Make sure the child window is visible. 
 
    ShowWindow(hwndChild, SW_SHOW); 
 
    return TRUE;
}
```



## <a name="destroying-a-window"></a>終結視窗

您可以使用 [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) 函數來終結視窗。 一般而言，應用程式會在終結視窗之前傳送 [**WM \_ 關閉**](wm-close.md) 訊息，讓視窗有機會在視窗終結之前提示使用者進行確認。 當使用者按一下 [視窗] 功能表中的 [**關閉**] 時，包含視窗功能表的視窗會自動收到 **WM \_ 關閉** 訊息。 如果使用者確認應該終結視窗，應用程式會呼叫 **DestroyWindow**。 將 [**WM \_**](wm-destroy.md) 終結訊息從螢幕中移除之後，系統會將它傳送至視窗。 為了回應 **WM 終結 \_**，此視窗會儲存其資料並釋出它所配置的任何資源。 主視窗會藉由呼叫 [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage)函式來結束應用程式，以結束其對 **WM \_ 摧毀** 的處理。

下列範例顯示如何在終結視窗之前提示使用者確認。 為了回應 [**WM \_ 關閉**](wm-close.md)，此範例會顯示一個對話方塊，其中包含 **[是**]、[ **否**] 和 [ **取消** ] 按鈕。 如果使用者按一下 **[是]**，則會呼叫 [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) ;否則，不會終結視窗。 因為被終結的視窗是主視窗，此範例會呼叫 [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) 以回應 [**WM 終結 \_**](wm-destroy.md)。


```
case WM_CLOSE: 
 
    // Create the message box. If the user clicks 
    // the Yes button, destroy the main window. 
 
    if (MessageBox(hwnd, szConfirm, szAppName, MB_YESNOCANCEL) == IDYES) 
        DestroyWindow(hwndMain); 
    else 
        return 0; 
 
case WM_DESTROY: 
 
    // Post the WM_QUIT message to 
    // quit the application terminate. 
 
    PostQuitMessage(0); 
    return 0;
```



## <a name="using-layered-windows"></a>使用分層 Windows

若要讓對話方塊成為半透明視窗，請先照常建立對話方塊。 然後，在 [**WM \_ INITDIALOG**](../dlgbox/wm-initdialog.md)上，設定視窗擴充樣式的分層位，並使用所需的 Alpha 值來呼叫 [**SetLayeredWindowAttributes**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes) 。 程式碼可能如下所示：


```
// Set WS_EX_LAYERED on this window 
SetWindowLong(hwnd, 
              GWL_EXSTYLE, 
              GetWindowLong(hwnd, GWL_EXSTYLE) | WS_EX_LAYERED);

// Make this window 70% alpha
SetLayeredWindowAttributes(hwnd, 0, (255 * 70) / 100, LWA_ALPHA);
```



請注意， [**SetLayeredWindowAttributes**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes) 的第三個參數是範圍從0到255的值，其中0讓視窗完全透明，而255使其完全不透明。 此參數模仿 [**AlphaBlend**](/windows/win32/api/wingdi/nf-wingdi-alphablend)函式的更多用途 [**BLENDFUNCTION**](/windows/win32/api/wingdi/ns-wingdi-blendfunction) 。

若要再次使此視窗完全不透明，請呼叫 [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga)來移除 **WS \_ EX \_ 分層** 位，然後要求視窗重新繪製。 移除此位是為了讓系統知道它可以釋出一些與分層和重新導向相關聯的記憶體。 程式碼可能如下所示：


```
// Remove WS_EX_LAYERED from this window styles
SetWindowLong(hwnd, 
              GWL_EXSTYLE,
              GetWindowLong(hwnd, GWL_EXSTYLE) & ~WS_EX_LAYERED);

// Ask the window and its children to repaint
RedrawWindow(hwnd, 
             NULL, 
             NULL, 
             RDW_ERASE | RDW_INVALIDATE | RDW_FRAME | RDW_ALLCHILDREN);
```



為了使用階層式子視窗，應用程式必須在資訊清單中宣告自己的 Windows 8 感知。

 

 
