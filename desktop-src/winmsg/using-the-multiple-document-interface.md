---
description: 本節說明如何執行與多個檔介面相關聯的工作。
ms.assetid: 024744d3-362f-4162-8d0a-d4dac61de808
title: 使用多重文件介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5e24aed7abc3640b441345520203c8a02e025e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980027"
---
# <a name="using-the-multiple-document-interface"></a>使用多重文件介面

本節說明如何執行下列工作：

-   [註冊子系和框架視窗類別](#registering-child-and-frame-window-classes)
-   [建立框架和子視窗](#creating-frame-and-child-windows)
-   [寫入主要訊息迴圈](#writing-the-main-message-loop)
-   [撰寫框架視窗程式](#writing-the-frame-window-procedure)
-   [撰寫子視窗程式](#writing-the-child-window-procedure)
-   [建立子視窗](#creating-a-child-window)

為了說明這些工作，本節包含 Multipad 的範例， (MDI) 應用程式的一般多重文件介面。

## <a name="registering-child-and-frame-window-classes"></a>註冊子系和框架視窗類別

一般的 MDI 應用程式必須註冊兩個視窗類別：一個用於框架視窗，另一個用於其子視窗。 如果應用程式支援多個檔案類型 (例如，試算表和圖表) ，則必須為每個類型註冊視窗類別。

框架視窗的類別結構類似于非 MDI 應用程式中主視窗的類別結構。 MDI 子視窗的類別結構與非 MDI 應用程式中的子視窗結構稍有不同，如下所示：

-   類別結構應該要有一個圖示，因為使用者可以將 MDI 子視窗的最小化，如同一般的應用程式視窗。
-   由於 MDI 子視窗不能有自己的功能表，因此功能表名稱應為 **Null**。
-   類別結構應該在視窗結構中保留額外的空間。 使用這個空間，應用程式可以將資料（例如檔案名）與特定的子視窗建立關聯。

下列範例顯示 Multipad 如何註冊其框架和子視窗類別。


```
BOOL WINAPI InitializeApplication() 
{ 
    WNDCLASS wc; 
 
    // Register the frame window class. 
 
    wc.style         = 0; 
    wc.lpfnWndProc   = (WNDPROC) MPFrameWndProc; 
    wc.cbClsExtra    = 0; 
    wc.cbWndExtra    = 0; 
    wc.hInstance     = hInst; 
    wc.hIcon         = LoadIcon(hInst, IDMULTIPAD); 
    wc.hCursor       = LoadCursor((HANDLE) NULL, IDC_ARROW); 
    wc.hbrBackground = (HBRUSH) (COLOR_APPWORKSPACE + 1); 
    wc.lpszMenuName  = IDMULTIPAD; 
    wc.lpszClassName = szFrame; 
 
    if (!RegisterClass (&wc) ) 
        return FALSE; 
 
    // Register the MDI child window class. 
 
    wc.lpfnWndProc   = (WNDPROC) MPMDIChildWndProc; 
    wc.hIcon         = LoadIcon(hInst, IDNOTE); 
    wc.lpszMenuName  = (LPCTSTR) NULL; 
    wc.cbWndExtra    = CBWNDEXTRA; 
    wc.lpszClassName = szChild; 
 
    if (!RegisterClass(&wc)) 
        return FALSE; 
 
    return TRUE; 
} 
```



## <a name="creating-frame-and-child-windows"></a>建立框架和子視窗

在註冊其視窗類別之後，MDI 應用程式即可建立其視窗。 首先，它會使用 [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) 或 [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) 函數來建立框架視窗。 在建立框架視窗之後，應用程式會使用 **CreateWindow** 或 **CreateWindowEx** 再次建立其用戶端視窗。 應用程式應該將 MDICLIENT 指定為用戶端視窗的類別名稱; **MDICLIENT** 是系統定義的預先註冊視窗類別。 **CreateWindow** 或 **CreateWindowEx** 的 *lpvParam* 參數應指向 [**CLIENTCREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-clientcreatestruct)結構。 此結構包含下表中描述的成員：



| member           | 描述                                                                                                                                                                                                                                                                                                           |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **hWindowMenu**  | 用來控制 MDI 子視窗的視窗功能表控制碼。 當建立子視窗時，應用程式會將其標題以功能表項目的形式加入至 [視窗] 功能表。 然後，使用者可以按一下 [視窗] 功能表上的標題，以啟用子視窗。                                                               |
| **idFirstChild** | 指定第一個 MDI 子視窗的識別碼。 第一個建立的 MDI 子視窗會指派此識別碼。 其他視窗則會以遞增的視窗識別碼來建立。 當子視窗損毀時，系統會立即重新指派視窗識別碼，讓其範圍保持連續。 |



 

將子視窗的標題新增至 [視窗] 功能表時，系統會將識別碼指派給子視窗。 當使用者按一下子視窗的標題時，框架視窗會在 *wParam* 參數中收到含有識別碼的 [**WM \_ 命令**](../menurc/wm-command.md)訊息。 您應指定 **idFirstChild** 成員的值，此值不會與框架視窗功能表中的功能表項目識別碼衝突。

Multipad 的框架視窗程式會在處理 [**WM \_ 建立**](wm-create.md) 訊息時建立 MDI 用戶端視窗。 下列範例顯示如何建立用戶端視窗。


```
case WM_CREATE: 
    { 
        CLIENTCREATESTRUCT ccs; 
 
        // Retrieve the handle to the window menu and assign the 
        // first child window identifier. 
 
        ccs.hWindowMenu = GetSubMenu(GetMenu(hwnd), WINDOWMENU); 
        ccs.idFirstChild = IDM_WINDOWCHILD; 
 
        // Create the MDI client window. 
 
        hwndMDIClient = CreateWindow( "MDICLIENT", (LPCTSTR) NULL, 
            WS_CHILD | WS_CLIPCHILDREN | WS_VSCROLL | WS_HSCROLL, 
            0, 0, 0, 0, hwnd, (HMENU) 0xCAC, hInst, (LPSTR) &ccs); 
 
        ShowWindow(hwndMDIClient, SW_SHOW); 
    } 
    break; 
```



子視窗的標題會新增至 [視窗] 功能表的底部。 如果應用程式使用 [**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua) 函式將字串加入至 [視窗] 功能表，當 (子視窗建立或終結) 時，子視窗的標題就可以覆寫這些字串。 將字串加入至其視窗功能表的 MDI 應用程式應該使用 [**InsertMenu**](/windows/win32/api/winuser/nf-winuser-insertmenua) 函式，並確認子視窗的標題尚未覆寫這些新的字串。

使用 **WS \_ CLIPCHILDREN** 樣式來建立 MDI 用戶端視窗，以防止視窗繪製在其子視窗上。

## <a name="writing-the-main-message-loop"></a>寫入主要訊息迴圈

MDI 應用程式的主要訊息迴圈類似于非 MDI 應用程式處理快速鍵的訊息。 不同之處在于，MDI 訊息迴圈會先呼叫 [**TranslateMDISysAccel**](/windows/win32/api/winuser/nf-winuser-translatemdisysaccel) 函式，再檢查應用程式定義的快速鍵或分派訊息。

下列範例顯示一般 MDI 應用程式的訊息迴圈。 請注意，如果發生錯誤， [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) 可以傳回-1。


```
MSG msg;
BOOL bRet;

while ((bRet = GetMessage(&msg, (HWND) NULL, 0, 0)) != 0)
{
    if (bRet == -1)
    {
        // handle the error and possibly exit
    }
    else 
    { 
        if (!TranslateMDISysAccel(hwndMDIClient, &msg) && 
                !TranslateAccelerator(hwndFrame, hAccel, &msg))
        { 
            TranslateMessage(&msg); 
            DispatchMessage(&msg); 
        } 
    } 
}
```



[**TranslateMDISysAccel**](/windows/win32/api/winuser/nf-winuser-translatemdisysaccel)函式會將 [**wm 的 \_ KEYDOWN**](../inputdev/wm-keydown.md)訊息轉譯成 [**wm \_ SYSCOMMAND**](../menurc/wm-syscommand.md)訊息，並將它們傳送至作用中的 MDI 子視窗。 如果訊息不是 MDI 快速鍵訊息，則函式會傳回 **FALSE**，在此情況下，應用程式會使用 [**TranslateAccelerator**](/windows/win32/api/winuser/nf-winuser-translateacceleratora) 函式來判斷是否已按下任何應用程式定義的快速鍵。 如果沒有，迴圈會將訊息分派至適當的視窗程式。

## <a name="writing-the-frame-window-procedure"></a>撰寫框架視窗程式

MDI 框架視窗的視窗程式與非 MDI 應用程式主視窗的程式類似。 差別在於框架視窗程式會將它未處理的所有訊息傳遞至 [**DefFrameProc**](/windows/win32/api/winuser/nf-winuser-defframeproca) 函式，而不是 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函數。 此外，框架視窗程式也必須傳遞其處理的訊息，包括下表所列的訊息。



| 訊息                                  | 回應                                                                                                                                                                                                                                                            |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ 命令**](../menurc/wm-command.md)     | 啟用使用者選擇的 MDI 子視窗。 當使用者從 MDI 框架視窗的 [視窗] 功能表選擇 MDI 子視窗時，就會傳送此訊息。 伴隨此訊息的視窗識別碼會識別要啟用的 MDI 子視窗。 |
| [**WM \_ MENUCHAR**](../menurc/wm-menuchar.md)   | 當使用者按下 ALT + – (減號) 按鍵組合時，開啟現用 MDI 子視窗的 [視窗] 功能表。                                                                                                                                                      |
| [**WM \_ SETFOCUS**](../inputdev/wm-setfocus.md) | 將鍵盤焦點傳遞至 MDI 用戶端視窗，然後將它傳遞給使用中的 MDI 子視窗。                                                                                                                                                         |
| [**WM \_ 大小**](wm-size.md)              | 調整 MDI 用戶端視窗的大小，使其符合新框架視窗的工作區。 如果框架視窗程式將 MDI 用戶端視窗的大小調整為不同的大小，則不應將訊息傳遞至 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函式。                   |



 

Multipad 中的框架視窗程式稱為 MPFrameWndProc。 MPFrameWndProc 處理其他訊息的方式，與非 MDI 應用程式的處理方式類似。 [**WM \_**](../menurc/wm-command.md)Multipad 中的命令訊息是由本機定義的 CommandHandler 函數所處理。 針對 Multipad 未處理的命令訊息，CommandHandler 會呼叫 [**DefFrameProc**](/windows/win32/api/winuser/nf-winuser-defframeproca) 函數。 如果 Multipad 預設不使用 **DefFrameProc** ，則使用者無法從 [視窗] 功能表啟動子視窗，因為按一下視窗的功能表項目所傳送的 **WM \_ 命令** 訊息將會遺失。

## <a name="writing-the-child-window-procedure"></a>撰寫子視窗程式

如同框架視窗程式，MDI 子視窗程式預設會使用特殊函式來處理訊息。 子視窗程式未處理的所有訊息都必須傳遞至 [**DefMDIChildProc**](/windows/win32/api/winuser/nf-winuser-defmdichildproca) 函式，而不是傳遞至 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函數。 此外，某些視窗管理訊息必須傳遞至 **DefMDIChildProc**，即使應用程式處理訊息，MDI 才能正確運作。 以下是應用程式必須傳遞給 **DefMDIChildProc** 的訊息。



| 訊息                                       | 回應                                                                                                                                                                                                                                                  |
|-----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ CHILDACTI加值稅E**](wm-childactivate.md) | 當 MDI 子視窗調整大小、移動或顯示時，執行啟用處理。 必須傳遞此訊息。                                                                                                                                        |
| [**WM \_ GETMINMAXINFO**](wm-getminmaxinfo.md) | 根據 MDI 用戶端視窗目前的大小，計算最大化的 MDI 子視窗大小。                                                                                                                                                  |
| [**WM \_ MENUCHAR**](../menurc/wm-menuchar.md)        | 將訊息傳遞至 MDI 框架視窗。                                                                                                                                                                                                               |
| [**WM \_ 移動**](wm-move.md)                   | 重新計算 MDI 用戶端捲軸（如果有的話）。                                                                                                                                                                                                 |
| [**WM \_ SETFOCUS**](../inputdev/wm-setfocus.md)      | 啟動子視窗（如果它不是作用中的 MDI 子視窗）。                                                                                                                                                                                     |
| [**WM \_ 大小**](wm-size.md)                   | 執行變更視窗大小所需的作業，尤其是為了最大化或還原 MDI 子視窗。 無法將此訊息傳遞至 [**DefMDIChildProc**](/windows/win32/api/winuser/nf-winuser-defmdichildproca) 函式會產生高度不當的結果。 |
| [**WM \_ SYSCOMMAND**](../menurc/wm-syscommand.md)    | 處理視窗 (先前稱為系統) 功能表命令： **sc \_ NEXTWINDOW**、 **sc \_ PREVWINDOW**、 **sc \_ MOVE**、 **sc \_ SIZE** 和 **sc \_ 最大化**。                                                                                                        |



 

## <a name="creating-a-child-window"></a>建立子視窗

若要建立 MDI 子視窗，應用程式可以呼叫 [**CreateMDIWindow**](/windows/win32/api/winuser/nf-winuser-createmdiwindowa) 函式，或將 [**WM \_ MDICREATE**](wm-mdicreate.md) 訊息傳送至 MDI 用戶端視窗。  (應用程式可使用 [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) 函式搭配 **WS \_ EX \_ MDICHILD** 樣式來建立 MDI 子視窗。 ) 單一執行緒的 MDI 應用程式可以使用任一種方法來建立子視窗。 多執行緒 MDI 應用程式中的執行緒必須使用 **CreateMDIWindow** 或 **CreateWindowEx** 函數，在不同的執行緒中建立子視窗。

[**WM \_ MDICREATE**](wm-mdicreate.md)訊息的 *lParam* 參數是 [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa)結構的最遠指標。 結構包含四個維度成員： **x** 和 **y**，表示視窗的水準和垂直位置，以及 **cx** 和 **cy**（表示視窗的水準和垂直範圍）。 這些成員都可以由應用程式明確指派，也可以設定為 **CW \_ USEDEFAULT**，在此情況下，系統會根據串聯演算法來選取位置、大小或兩者。 在任何情況下，全部四個成員都必須初始化。 Multipad 使用所有維度的 **CW \_ USEDEFAULT** 。

[**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa)結構的最後一個成員是 **樣式** 成員，它可能包含視窗的樣式位。 若要建立可以有視窗樣式組合的 MDI 子視窗，請指定 [ **mdi \_ ALLCHILDSTYLES** ] 視窗樣式。 未指定此樣式時，MDI 子視窗會將 **ws \_ 最小化**、 **ws \_ 最大化**、 **ws \_ HSCROLL** 和 **ws \_ VSCROLL** 樣式設定為預設值。

Multipad 會使用位於原始程式檔 MPFILE 的本機定義 AddFile 函式 (，建立其 MDI 子視窗。C) 。 AddFile 函式會將視窗 [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa)結構的 **szTitle** 成員指派給要編輯的檔案名稱或「未命名」，以設定子視窗的標題。 **SzClass** 成員會設定為 Multipad 的 InitializeApplication 函式中所註冊的 MDI 子視窗類別名稱。 **HOwner** 成員會設定為應用程式的實例控制碼。

下列範例會顯示 Multipad 中的 AddFile 函數。


```
HWND APIENTRY AddFile(pName) 
TCHAR * pName; 
{ 
    HWND hwnd; 
    TCHAR sz[160]; 
    MDICREATESTRUCT mcs; 
 
    if (!pName) 
    { 
 
        // If the pName parameter is NULL, load the "Untitled" 
        // string from the STRINGTABLE resource and set the szTitle 
        // member of MDICREATESTRUCT. 
 
        LoadString(hInst, IDS_UNTITLED, sz, sizeof(sz)/sizeof(TCHAR)); 
        mcs.szTitle = (LPCTSTR) sz; 
    } 
    else 
 
        // Title the window with the full path and filename, 
        // obtained by calling the OpenFile function with the 
        // OF_PARSE flag, which is called before AddFile(). 
 
        mcs.szTitle = of.szPathName; 
 
    mcs.szClass = szChild; 
    mcs.hOwner  = hInst; 
 
    // Use the default size for the child window. 
 
    mcs.x = mcs.cx = CW_USEDEFAULT; 
    mcs.y = mcs.cy = CW_USEDEFAULT; 
 
    // Give the child window the default style. The styleDefault 
    // variable is defined in MULTIPAD.C. 
 
    mcs.style = styleDefault; 
 
    // Tell the MDI client window to create the child window. 
 
    hwnd = (HWND) SendMessage (hwndMDIClient, WM_MDICREATE, 0, 
        (LONG) (LPMDICREATESTRUCT) &mcs); 
 
    // If the file is found, read its contents into the child 
    // window's client area. 
 
    if (pName) 
    { 
        if (!LoadFile(hwnd, pName)) 
        { 
 
            // Cannot load the file; close the window. 
 
            SendMessage(hwndMDIClient, WM_MDIDESTROY, 
                (DWORD) hwnd, 0L); 
        } 
    } 
    return hwnd; 
} 
```



在 [**wm \_ MDICREATE**](wm-mdicreate.md)訊息的 *lParam* 參數中傳遞的指標會傳遞給 [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa)函數，並顯示為 [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa)結構中傳遞給 [**WM \_ 建立**](wm-create.md)訊息的第一個成員。 在 Multipad 中，子視窗會在 **WM \_ 建立** 訊息處理期間，藉由在其額外的資料中初始化檔變數，以及藉由建立編輯控制項的子視窗，來初始化本身。

 

 
