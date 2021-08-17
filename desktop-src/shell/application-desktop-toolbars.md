---
description: 應用程式桌面工具列 (也稱為 appbar) 是與 Windows 工作列類似的視窗。
ms.assetid: d9f63cb1-e2cc-4a3b-a3b8-de028e0f0123
title: 使用應用程式桌面工具列
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3c8604136040f5f3a1b4c1e9fcecb3b0c26b087724f477e592857ca4046d3a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119351448"
---
# <a name="using-application-desktop-toolbars"></a>使用應用程式桌面工具列

*應用程式桌面工具列* (也稱為 appbar) 是與 Windows 工作列類似的視窗。 它會錨定到畫面邊緣，通常會包含可讓使用者快速存取其他應用程式和視窗的按鈕。 系統會防止其他應用程式使用 appbar 所使用的桌面區域。 在任何指定時間，桌面上都可以有任意數目的透過像 appbars。

本主題包含下列各節。

-   [關於應用程式桌面工具列](#about-application-desktop-toolbars)
    -   [傳送訊息](#sending-messages)
    -   [註冊](#registration)
    -   [Appbar 大小和位置](#appbar-size-and-position)
    -   [自動隱藏應用程式桌面工具列](#autohide-application-desktop-toolbars)
    -   [Appbar 通知訊息](#appbar-notification-messages)
-   [註冊應用程式桌面工具列](#registering-an-application-desktop-toolbar)
-   [設定 Appbar 大小和位置](#setting-the-appbar-size-and-position)
-   [處理 Appbar 通知訊息](#processing-appbar-notification-messages)

## <a name="about-application-desktop-toolbars"></a>關於應用程式桌面工具列

Windows 提供可讓您利用系統所提供之 appbar 服務的 API。 這些服務可協助確保應用程式定義的透過像 appbars 能以另一個和工作列順暢地運作。 系統會維護每個 appbar 的相關資訊，並傳送透過像 appbars 訊息，通知他們可能會影響其大小、位置和外觀的事件。

### <a name="sending-messages"></a>傳送訊息

應用程式會使用一組特殊的訊息（稱為「appbar 訊息」）來新增或移除 appbar、設定 appbar 的大小和位置，以及取得工作列大小、位置和狀態的相關資訊。 若要傳送 appbar 訊息，應用程式必須使用 [**SHAppBarMessage**](/windows/desktop/api/Shellapi/nf-shellapi-shappbarmessage) 函數。 函數的參數包含訊息識別碼，例如 [**ABM \_ NEW**](abm-new.md)，以及 [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) 結構的位址。 結構成員包含系統處理指定訊息所需的資訊。

針對任何指定的 appbar 訊息，系統會使用 [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) 結構的某些成員，並忽略其他成員。 不過，系統一律會使用 **cbSize** 和 **hWnd** 成員，因此應用程式必須針對每個 appbar 訊息填滿這些成員。 **CbSize** 成員會指定結構的大小，而 **hWnd** 成員是 appbar 視窗的控制碼。

某些 appbar 訊息會要求系統的資訊。 處理這些訊息時，系統會將要求的資訊複製到 [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) 結構中。

### <a name="registration"></a>註冊

系統會保留透過像 appbars 的內部清單，並維護清單中每個橫條的相關資訊。 系統會使用此資訊來管理透過像 appbars、為它們執行服務，並傳送通知訊息給他們。

應用程式必須註冊 appbar (也就是將它新增至內部清單) ，然後才能從系統接收 appbar 服務。 若要註冊 appbar，應用程式會傳送 [**ABM 的 \_ 新**](abm-new.md) 訊息。 伴隨的 [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) 結構包含 appbar 視窗的控制碼和應用程式定義的訊息識別碼。 系統會使用訊息識別碼，將通知訊息傳送至 appbar 視窗的視窗程式。 如需詳細資訊，請參閱 Appbar 通知訊息。

應用程式會藉由傳送 [**ABM \_ 移除**](abm-remove.md) 訊息來取消註冊 appbar。 取消註冊 appbar 會將它從系統的透過像 appbars 內部清單中移除。 系統不會再將通知訊息傳送至 appbar，或防止其他應用程式使用 appbar 所使用的螢幕區域。 應用程式應該一律在終結 appbar 之前傳送 **ABM \_ 移除** 。

### <a name="appbar-size-and-position"></a>Appbar 大小和位置

應用程式應該設定 appbar 的大小和位置，讓它不會干擾任何其他透過像 appbars 或工作列。 每個 appbar 都必須錨定到畫面的特定邊緣，而且可以將多個透過像 appbars 錨定至邊緣。 但是，如果 appbar 錨定到與工作列相同的邊緣，系統就會確保工作列一律位於最外層的邊緣上。

若要設定 appbar 的大小和位置，應用程式會先傳送 [**ABM \_ QUERYPOS**](abm-querypos.md) 訊息，以針對 appbar 提出螢幕邊緣和周框矩形。 系統會決定工作列或其他 appbar 是否使用建議的矩形內的任何部分的螢幕區域，視需要) 調整矩形 (，並將調整的矩形傳回給應用程式。

接下來，應用程式會傳送 [**ABM \_ SETPOS**](abm-setpos.md) 訊息，以設定 appbar 的新周框。 同樣地，系統可能會調整矩形，再將它傳回給應用程式。 基於這個理由，應用程式應該使用 **ABM \_ SETPOS** 所傳回的調整矩形來設定最終大小和位置。 應用程式可以使用 [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) 函式，將 appbar 移至位置。

藉由使用兩個步驟的程式來設定大小和位置，系統可讓應用程式在移動作業期間提供中繼回饋給使用者。 例如，如果使用者拖曳 appbar，則應用程式可能會顯示陰影矩形，指出 appbar 實際移動之前的新位置。

應用程式應該在註冊之後設定其 appbar 的大小和位置，並在 appbar 收到 [**ABN \_ POSCHANGED**](abn-poschanged.md) 通知訊息時設定它的位置。 每當在工作列的大小、位置或可見度狀態發生變更，以及在螢幕上的另一個 appbar 調整大小、新增或移除時，appbar 就會收到這則通知訊息。

每當 appbar 收到 WM \_ 啟動訊息時，它應該會傳送 [**ABM \_ 啟動**](abm-activate.md) 訊息。 同樣地，當 appbar 收到 WM \_ WINDOWPOSCHANGED 訊息時，它必須呼叫 [**ABM \_ WINDOWPOSCHANGED**](abm-windowposchanged.md)。 傳送這些訊息可確保系統正確設定相同邊緣上任何自動隱藏透過像 appbars 的迭置順序。

### <a name="autohide-application-desktop-toolbars"></a>自動隱藏應用程式桌面工具列

自動隱藏 appbar 是一種一般隱藏的，但是當使用者將滑鼠游標移至與 appbar 相關聯的螢幕邊緣時，就會看到它。 當使用者將滑鼠游標移出橫條的周框時，appbar 會再次隱藏本身。

雖然系統在任何指定的時間都允許多個不同的透過像 appbars，但每個螢幕邊緣一次只允許一個自動隱藏 appbar，並以先服務為基礎。 系統會自動將自動隱藏 appbar (的迭置順序維持在其 z 順序群組內，但僅) 。

應用程式會使用 [**ABM \_ SETAUTOHIDEBAR**](abm-setautohidebar.md) 訊息來註冊或取消註冊自動隱藏 appbar。 訊息會指定 appbar 的邊緣，以及指定是否要註冊或取消註冊 appbar 的旗標。 如果正在註冊自動隱藏 appbar，但其中一個已與指定的邊緣相關聯，則訊息會失敗。 應用程式可以藉由傳送 [**ABM \_ GETAUTOHIDEBAR**](abm-getautohidebar.md) 訊息，來取得與邊緣相關聯的自動隱藏 appbar 控制碼。

自動隱藏 appbar 不需要註冊為一般 appbar;也就是說，它不需要藉由傳送 [**ABM 的 \_ 新**](abm-new.md) 訊息來註冊。 未由 **ABM \_ NEW** 註冊的 appbar 會與螢幕上相同邊緣上錨定的任何透過像 appbars 重迭。

### <a name="appbar-notification-messages"></a>Appbar 通知訊息

系統會傳送訊息，通知 appbar 可能會影響其位置和外觀的事件。 訊息會在應用程式定義的訊息內容中傳送。 應用程式會在傳送 [**ABM 的 \_ 新**](abm-new.md) 訊息以註冊 appbar 時，指定訊息的識別碼。 通知碼位於應用程式定義之訊息的 *wParam* 參數中。

當您將另一個 appbar 新增至螢幕邊緣，或在螢幕上的另一個 appbar 調整大小或移除時，appbar 會在工作列的大小、位置或可見度狀態變更時收到 [**ABN \_ POSCHANGED**](abn-poschanged.md) 通知訊息。 Appbar 應該藉由傳送 [**ABM \_ QUERYPOS**](abm-querypos.md) 和 [**ABM \_ SETPOS**](abm-setpos.md) 訊息來回應這則通知訊息。 如果 appbar 的位置已變更，則應該呼叫 [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) 函式，將其本身移至新的位置。

當工作列的自動隱藏或 alwayson 狀態變更時（也就是當使用者在工作列的屬性工作表上選取或清除 [**永遠開啟**] 或 [**自動隱藏**] 核取方塊時），系統就會傳送 [**ABN \_ STATECHANGE**](abn-statechange.md)通知訊息。 Appbar 可以使用此通知訊息，將其狀態設定為符合工作列的狀態（如有需要）。

當全螢幕應用程式啟動時，或當最後一個全螢幕應用程式關閉時，appbar 會收到 [**ABN \_ FULLSCREENAPP**](abn-fullscreenapp.md) 通知訊息。 *LParam* 參數會指出全螢幕應用程式是否開啟或關閉。 如果開啟，appbar 必須放到迭置順序的底部。 當最後一個全螢幕應用程式關閉時，appbar 應該會還原其 z 順序位置。

當使用者從工作列的快捷方式功能表中選取串聯、水準磚或垂直磚命令時，appbar 會收到 [**ABN \_ WINDOWARRANGE**](abn-windowarrange.md) 通知訊息。 系統會在重新排列 windows (*lParam* 為 **TRUE**) 之前，以及在排列 Windows (*lParam* 為 **FALSE**) 之後，將訊息傳送兩次。

Appbar 可以使用 [**ABN \_ WINDOWARRANGE**](abn-windowarrange.md) 訊息，將本身從 cascade 或磚作業中排除。 若要排除本身，appbar 應該在 *lParam* 為 **TRUE** 時隱藏本身，並在 *lParam* 為 **FALSE** 時顯示本身。 如果 appbar 隱藏本身以回應此訊息，則不需要傳送 [**ABM \_ QUERYPOS**](abm-querypos.md) 和 [**ABM \_ SETPOS**](abm-setpos.md) 訊息來回應 cascade 或並排顯示的作業。

## <a name="registering-an-application-desktop-toolbar"></a>註冊應用程式桌面工具列

應用程式必須藉由傳送 [**ABM 的 \_ 新**](abm-new.md) 訊息來註冊 appbar。 註冊 appbar 會將它新增至系統的內部清單，並為系統提供訊息識別碼，以用來將通知訊息傳送至 appbar。 在結束之前，應用程式必須藉由傳送 [**ABM \_ 移除**](abm-remove.md) 訊息來取消註冊 appbar。 取消註冊會從系統的內部清單中移除 appbar，並防止狀態列接收 appbar 通知訊息。

下列範例中的函式會根據布林值旗標參數的值來註冊或取消註冊 appbar。


```C++
// RegisterAccessBar - registers or unregisters an appbar. 
// Returns TRUE if successful, or FALSE otherwise. 

// hwndAccessBar - handle to the appbar 
// fRegister - register and unregister flag 

// Global variables 
//     g_uSide - screen edge (defaults to ABE_TOP) 
//     g_fAppRegistered - flag indicating whether the bar is registered 

BOOL RegisterAccessBar(HWND hwndAccessBar, BOOL fRegister) 
{ 
    APPBARDATA abd; 
    
    // An application-defined message identifier
    APPBAR_CALLBACK = (WM_USER + 0x01);
    
    // Specify the structure size and handle to the appbar. 
    abd.cbSize = sizeof(APPBARDATA); 
    abd.hWnd = hwndAccessBar; 

    if (fRegister) 
    { 
        // Provide an identifier for notification messages. 
        abd.uCallbackMessage = APPBAR_CALLBACK; 

        // Register the appbar. 
        if (!SHAppBarMessage(ABM_NEW, &abd)) 
            return FALSE; 

        g_uSide = ABE_TOP;       // default edge 
        g_fAppRegistered = TRUE; 

    } 
    else 
    { 
        // Unregister the appbar. 
        SHAppBarMessage(ABM_REMOVE, &abd); 
        g_fAppRegistered = FALSE; 
    } 

    return TRUE; 
}
```



## <a name="setting-the-appbar-size-and-position"></a>設定 Appbar 大小和位置

應用程式應該在註冊 appbar 之後、使用者使用者移動或調整 appbar，以及每次 appbar 收到 [**ABN \_ POSCHANGED**](abn-poschanged.md) 通知訊息時，設定 appbar 的大小和位置。 在設定 appbar 的大小和位置之前，應用程式會藉由傳送 [**ABM \_ QUERYPOS**](abm-querypos.md) 訊息，查詢系統是否有核准的周框。 系統會傳回不幹擾工作列或任何其他 appbar 的周框。 系統只會以矩形減法來調整矩形;這樣就不需要保留矩形的初始大小。 基於這個理由，appbar 應該會在傳送 **ABM \_ QUERYPOS** 之後，視需要重新調整矩形。

接下來，應用程式會使用 [**ABM \_ SETPOS**](abm-setpos.md) 訊息，將周框的矩形傳遞回系統。 然後，它會呼叫 [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) 函式，將 appbar 移至位置。

下列範例顯示如何設定 appbar 的大小和位置。


```C++
// AppBarQuerySetPos - sets the size and position of an appbar. 

// uEdge - screen edge to which the appbar is to be anchored 
// lprc - current bounding rectangle of the appbar 
// pabd - address of the APPBARDATA structure with the hWnd and cbSize members filled

void PASCAL AppBarQuerySetPos(UINT uEdge, LPRECT lprc, PAPPBARDATA pabd) 
{ 
    int iHeight = 0; 
    int iWidth = 0; 

    pabd->rc = *lprc; 
    pabd->uEdge = uEdge; 

    // Copy the screen coordinates of the appbar's bounding 
    // rectangle into the APPBARDATA structure. 
    if ((uEdge == ABE_LEFT) || (uEdge == ABE_RIGHT)) 
    { 
        iWidth = pabd->rc.right - pabd->rc.left; 
        pabd->rc.top = 0; 
        pabd->rc.bottom = GetSystemMetrics(SM_CYSCREEN); 
    } 
    else 
    { 
        iHeight = pabd->rc.bottom - pabd->rc.top; 
        pabd->rc.left = 0; 
        pabd->rc.right = GetSystemMetrics(SM_CXSCREEN); 
    } 

    // Query the system for an approved size and position. 
    SHAppBarMessage(ABM_QUERYPOS, pabd); 

    // Adjust the rectangle, depending on the edge to which the appbar is anchored.
    switch (uEdge) 
    { 
        case ABE_LEFT: 
            pabd->rc.right = pabd->rc.left + iWidth; 
            break; 

        case ABE_RIGHT: 
            pabd->rc.left = pabd->rc.right - iWidth; 
            break; 

        case ABE_TOP: 
            pabd->rc.bottom = pabd->rc.top + iHeight; 
            break; 

        case ABE_BOTTOM: 
            pabd->rc.top = pabd->rc.bottom - iHeight; 
            break; 
    } 

    // Pass the final bounding rectangle to the system. 
    SHAppBarMessage(ABM_SETPOS, pabd); 

    // Move and size the appbar so that it conforms to the 
    // bounding rectangle passed to the system. 
    MoveWindow(pabd->hWnd, 
               pabd->rc.left, 
               pabd->rc.top, 
               pabd->rc.right - pabd->rc.left, 
               pabd->rc.bottom - pabd->rc.top, 
               TRUE); 

}
```



## <a name="processing-appbar-notification-messages"></a>處理 Appbar 通知訊息

當全螢幕應用程式啟動 (或最後一個應用程式關閉) ，或是發生可能影響 appbar 大小和位置的事件時，appbar 會在工作列的狀態變更時收到通知訊息。 下列範例顯示如何處理各種通知訊息。


```C++
// AppBarCallback - processes notification messages sent by the system. 

// hwndAccessBar - handle to the appbar 
// uNotifyMsg - identifier of the notification message 
// lParam - message parameter 

void AppBarCallback(HWND hwndAccessBar, UINT uNotifyMsg, 
    LPARAM lParam) 
{ 
    APPBARDATA abd; 
    UINT uState; 

    abd.cbSize = sizeof(abd); 
    abd.hWnd = hwndAccessBar; 

    switch (uNotifyMsg) 
    { 
        case ABN_STATECHANGE: 

            // Check to see if the taskbar's always-on-top state has changed
            // and, if it has, change the appbar's state accordingly.
            uState = SHAppBarMessage(ABM_GETSTATE, &abd); 

            SetWindowPos(hwndAccessBar, 
                         (ABS_ALWAYSONTOP & uState) ? HWND_TOPMOST : HWND_BOTTOM, 
                         0, 0, 0, 0, 
                         SWP_NOMOVE | SWP_NOSIZE | SWP_NOACTIVATE); 

            break; 

        case ABN_FULLSCREENAPP: 

            // A full-screen application has started, or the last full-screen
            // application has closed. Set the appbar's z-order appropriately.
            if (lParam) 
            { 
                SetWindowPos(hwndAccessBar, 
                             (ABS_ALWAYSONTOP & uState) ? HWND_TOPMOST : HWND_BOTTOM, 
                             0, 0, 0, 0, 
                             SWP_NOMOVE | SWP_NOSIZE | SWP_NOACTIVATE); 
            } 
            else 
            { 
                uState = SHAppBarMessage(ABM_GETSTATE, &abd); 

                if (uState & ABS_ALWAYSONTOP) 
                    SetWindowPos(hwndAccessBar, 
                                 HWND_TOPMOST, 
                                 0, 0, 0, 0, 
                                 SWP_NOMOVE | SWP_NOSIZE | SWP_NOACTIVATE); 
            } 

        case ABN_POSCHANGED: 

            // The taskbar or another appbar has changed its size or position.
            AppBarPosChanged(&abd); 
            break; 
    } 
}
```



下列函式會調整 appbar 的周框，然後呼叫上一節中所含的應用程式定義 AppBarQuerySetPos 函式 () 來據以設定橫條圖的大小和位置。


```C++
// AppBarPosChanged - adjusts the appbar's size and position. 

// pabd - address of an APPBARDATA structure that contains information 
//        used to adjust the size and position. 

void PASCAL AppBarPosChanged(PAPPBARDATA pabd) 
{ 
    RECT rc; 
    RECT rcWindow; 
    int iHeight; 
    int iWidth; 

    rc.top = 0; 
    rc.left = 0; 
    rc.right = GetSystemMetrics(SM_CXSCREEN); 
    rc.bottom = GetSystemMetrics(SM_CYSCREEN); 

    GetWindowRect(pabd->hWnd, &rcWindow); 

    iHeight = rcWindow.bottom - rcWindow.top; 
    iWidth = rcWindow.right - rcWindow.left; 

    switch (g_uSide) 
    { 
        case ABE_TOP: 
            rc.bottom = rc.top + iHeight; 
            break; 

        case ABE_BOTTOM: 
            rc.top = rc.bottom - iHeight; 
            break; 

        case ABE_LEFT: 
            rc.right = rc.left + iWidth; 
            break; 

        case ABE_RIGHT: 
            rc.left = rc.right - iWidth; 
            break; 
    } 

    AppBarQuerySetPos(g_uSide, &rc, pabd); 
}
```



 

 
