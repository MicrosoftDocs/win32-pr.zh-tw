---
description: Windows 介面包含名為工作列的特殊應用程式桌面工具列。 您可以使用工作列來進行這類工作，像是在開啟的視窗和啟動新的應用程式之間切換。
ms.assetid: 14d520e7-7c15-441d-9662-24b972d208ac
title: 工作列
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8a4943c242b0b3f0993a4cf542c8625e19cf25c32b71cb01e4ef8581d12d64c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119773718"
---
# <a name="the-taskbar"></a>工作列

Windows 介面包含名為 *工作列* 的特殊 [應用程式桌面工具列](application-desktop-toolbars.md)。 您可以使用工作列來進行這類工作，像是在開啟的視窗和啟動新的應用程式之間切換。

> [!Note]  
> 如需 Windows 7 時對工作列所做之變更的相關資訊，請參閱[工作列擴充](taskbar-extensions.md)功能。

 

本主題包含下列各節。

-   [關於工作列](#about-the-taskbar)
    -   [工作列顯示選項](#taskbar-display-options)
    -   [將快捷方式新增至 [開始] 功能表](#adding-shortcuts-to-the-start-menu)
    -   [管理工作列按鈕](#managing-taskbar-buttons)
    -   [新增、修改和刪除通知區域中的圖示](#adding-modifying-and-deleting-icons-in-the-notification-area)
    -   [工作列建立通知](#taskbar-creation-notification)
-   [使用工作列](#using-the-taskbar)
    -   [新增和刪除通知區域中的工作列圖示](#adding-and-deleting-taskbar-icons-in-the-notification-area)
    -   [接收滑鼠事件](#receiving-mouse-events)

## <a name="about-the-taskbar"></a>關於工作列

工作列包含下列各項：

-   **開始** 功能表
-   快速啟動 bar (Windows Vista 及更早版本) 
-   工作列按鈕
-   工具列 (選用) 
-   [通知] 區域

[ **開始** ] 功能表包含可存取程式、檔和設定的命令。 這些命令包括 **所有程式**、 **檔**、 **主控台**、 **遊戲**、說明 **及支援**、 **關機** 以及 **搜尋程式和** 檔案。

從舊版 Windows **開始** 包含 **尋找** 和 **執行** 之類的專案，Windows Vista 和更新版本的 **搜尋程式和** 檔案中包含的功能。

快速啟動列（在 Windows 7 之前的 Windows 版本中提供）包含應用程式的快捷方式。 Windows 提供預設專案（例如 Windows Internet Explorer），而且使用者可以加入他們選擇的任何其他快捷方式。 此區域中的圖示只會回應按一下。 在 Windows 7 和更新版本中，這項功能會包含在工作列按鈕中。

每當應用程式建立無主視窗（也就是沒有父代且具有適當擴充樣式位的視窗）時，Shell 會在工作列上放置一個按鈕 (請參閱 [管理工作列按鈕](#managing-taskbar-buttons)，如下) 。 若要切換至視窗，使用者可以按一下視窗按鈕。 從 Windows 7 起，這項功能已經大幅擴充。 如需詳細資訊，請參閱 [工作列擴充](taskbar-extensions.md)功能。

應用程式可以將圖示放在通知區域中，以指出作業的狀態，或通知使用者有關事件的狀態。 例如，應用程式可能會在通知區域中放置印表機圖示，以顯示列印工作正在進行中。 不過，在 Windows 7 和更新版本中，必須透過應用程式的工作列按鈕提供通知區域先前提供的部分資訊。 通知區域位於工作列的右邊緣 (如果工作列為水準) ，或如果工作列垂直) ，則位於底部 (。 如需詳細資訊，請參閱 [通知和通知區域](notification-area.md)。

如果選取此選項，通知區域也會顯示目前的時間。 此選項會找到：

-   **Windows 7 和更新版本**：**通知區域圖示** 主控台應用程式的 [**開啟或關閉系統圖示**] 頁面中的 [**時鐘**] 下拉式清單 (也可透過通知區域屬性) 存取。
-   **Windows Vista**： [**工作列] 和 [開始] 功能表**[屬性] 視窗的 [通知]**區域** 頁面中的 [**時鐘**] 核取方塊。
-   **Windows XP**： [**工作列] 和 [開始功能表** 屬性] 視窗中的 [**顯示時鐘**] 核取方塊。

使用者可以在工作列上按一下滑鼠右鍵，以顯示快捷方式功能表。 快捷方式功能表包含了串聯視窗、堆疊視窗、並排顯示視窗、顯示桌面、開始工作管理員以及設定工作列屬性的命令。 快速鍵功能表也提供選項，可讓您從工作列新增或移除一組工具列。 您可以藉由在 CATID DeskBand 類別下註冊，將新的工具列新增至這個功能表中 \_ 。 如需詳細資訊，請參閱 [執行頻外物件](band-objects.md)。 請注意，從 Windows 7，工作列和通知區域都有個別的快捷方式功能表。 這些快捷方式功能表會共用一些選項，例如視窗排列，並加入其他選項。

### <a name="taskbar-display-options"></a>工作列顯示選項

工作列支援兩種顯示選項：自動隱藏，而且在 Windows Vista 及更早版本中，Always On 頂端 (工作列在 Windows 7 和更新版本) 中一律處於此模式。 若要設定這些選項，使用者必須開啟工作列快捷方式功能表，按一下 [ **屬性**]，然後選取或清除 [ **自動隱藏工作列** ] 核取方塊或 [ **將工作列保持在其他視窗上方** ] 核取方塊。 若要取得這些顯示選項的狀態，請使用 [**ABM \_ >getstate**](abm-getstate.md) 訊息。 如果您想要在這些顯示選項的狀態變更時收到通知，請在您的視窗程式中處理 [**ABN \_ STATECHANGE**](abn-statechange.md) 通知訊息。 若要變更這些顯示選項的狀態，請使用 [**ABM \_ SETSTATE**](abm-setstate.md) 訊息。

*工作區* 是工作列未遮蔽的畫面部分。 若要取得工作區域的大小，請使用已設定的 **SPI \_ GETWORKAREA** 值來呼叫 [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)函式。 若要取出描述工作列位置的矩形座標，請使用 [**ABM \_ GETTASKBARPOS**](abm-gettaskbarpos.md) 訊息。

您可以使用 [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos)，明確地設定等於畫面大小的視窗矩形大小，以涵蓋工作列。 針對 Windows 2000 系統或更新版本，視窗必須缺少 [**ws \_ 標題**](../winmsg/window-styles.md)或 [**ws \_ THICKFRAME**](../winmsg/window-styles.md)，否則視窗必須調整大小，才能讓工作區涵蓋整個畫面。 也特別是對於這些系統而言，如果工作列設定為 Always On Top，則只有在應用程式是前景應用程式時，它才會保持隱藏。

### <a name="adding-shortcuts-to-the-start-menu"></a>將快捷方式新增至 [開始] 功能表

若要將專案新增至 Microsoft Windows NT 4.0、Windows 2000 和更新版本，或 Windows 95 或更新版本的 [**程式**] 子功能表中，請遵循下列步驟。

1.  使用 [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka)介面建立 [shell 連結](./links.md)。
2.  使用 [**SHGetSpecialFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetspecialfolderlocation)傳遞 [**CSIDL \_ 程式**](csidl.md)，以取得 [程式] 資料夾的 PIDL。
3.  將 Shell 連結新增至 [程式] 資料夾。 您也可以在 [程式] 資料夾中建立資料夾，並將連結新增至該資料夾。

### <a name="managing-taskbar-buttons"></a>管理工作列按鈕

每當應用程式建立不是所擁有的視窗時，Shell 會在工作列上建立一個按鈕。 若要確定視窗按鈕是放置在工作列上，請建立具有 [**WS \_ EX \_ APPWINDOW**](../winmsg/extended-window-styles.md) 延伸樣式的無主視窗。 若要防止視窗按鈕放在工作列上，請建立具有 [**WS \_ EX \_ 工具視窗**](../winmsg/extended-window-styles.md) 延伸樣式的無主視窗。 或者，您也可以建立隱藏的視窗，讓這個隱藏視窗成為可見視窗的擁有者。

只有當視窗的樣式支援可見的工作列按鈕時，Shell 才會從工作列移除視窗的按鈕。 如果您想要以動態方式將視窗的樣式變更為不支援可見工作列按鈕的樣式，您必須使用 [ **SW \_ 隱藏**) ] 來呼叫 [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) 、變更視窗樣式，然後顯示視窗，以將視窗的樣式隱藏在第一個 (。

視窗按鈕通常會包含應用程式圖示和標題。 但是，如果應用程式不包含系統功能表，則會建立沒有圖示的視窗按鈕。

如果您想要讓應用程式在視窗非使用中時讓使用者注意，請使用 [**FlashWindow**](/windows/win32/api/winuser/nf-winuser-flashwindow) 函數讓使用者知道訊息正在等候。 此函式會將視窗按鈕閃爍。 當使用者按一下 [視窗] 按鈕以啟動視窗時，您的應用程式就會顯示訊息。

### <a name="modifying-the-contents-of-the-taskbar"></a>修改工作列的內容

Shell32.dll [4.71 版和更新版本](versions.md)新增了修改工作列內容的功能。 您現在可以從應用程式新增、移除和啟動工作列按鈕。 啟用專案並不會啟動視窗;它會顯示在工作列上按下的專案。

工作列修改功能是在元件物件模型中執行， (COM) 物件 (CLSID \_ TaskbarList ) ，它會公開 [**ITaskbarList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist) 介面 (IID \_ ITaskbarList) 。 您必須呼叫 [**ITaskbarList：： HrInit**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist-hrinit) 方法來初始化物件。 然後，您可以使用 [**ITaskbarList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist) 介面的方法來修改工作列的內容。

### <a name="adding-modifying-and-deleting-icons-in-the-notification-area"></a>新增、修改和刪除通知區域中的圖示

使用 [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) 函式來新增、修改或刪除通知區域中的圖示。 **Shell \_ NotifyIcon** 的 *dwMessage* 參數是用來指定要採取之動作的工作列訊息。 *Pnid* 參數是 [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa)結構的指標，用來識別圖示並傳遞系統處理訊息所需的任何其他資訊。

您可以使用通知區域圖示來執行下列動作。

-   若要將圖示加入至工作列的通知區域，請呼叫 [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) ，並將 *DWMESSAGE* 參數設定為 NIM \_ add。 [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa)結構是用來指定圖示的控制碼和識別碼，以及任何工具提示文字。 如果使用者已在工作列內容中選取 [ **顯示時鐘** ] 核取方塊，系統就會將圖示放在時鐘的最左邊。 否則，圖示會出現在工作列的右側或底部。 任何現有的圖示都會向左移動，以騰出空間給新的圖示。
-   若要修改圖示的資訊，包括其圖示控制碼、工具提示文字和回呼訊息識別碼，請呼叫 [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) ，並將 *dwMessage* 設定為 NIM \_ modify。
-   若要刪除通知區域中的圖示，請呼叫 [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) ，並將 *DWMESSAGE* 參數設定為 NIM \_ delete。

當您完成使用者介面作業之後，請呼叫 [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) ，並將 *dwMessage* 設定為 NIM SETFOCUS，以將焦點傳回至通知區域 \_ 。 例如，您可以在工作列圖示顯示快捷方式功能表時這麼做，但使用者按下 ESC 鍵即可取消。

### <a name="receiving-notification-area-callback-messages"></a>接收通知區域回呼訊息

應用程式通常會將圖示放在工作列的通知區域中，以做為狀態指示器。 您可以在使用者執行滑鼠動作時提供其他資訊，例如將滑鼠指標移到圖示上方或按一下圖示。

系統會傳送與特定圖示相關聯的應用程式定義回呼訊息，以通知您滑鼠和鍵盤事件。 如此一來，當使用者按一下圖示或按下按鍵選取圖示時，系統就可以通知應用程式。

當您將圖示新增至工作列時，您會定義圖示的回呼訊息。 回呼訊息識別碼是在以 NIM ADD 傳遞的 [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa)結構的 **uCallbackMessage** 成員中指定 \_ 。 當事件發生時，系統會將回呼訊息傳送至 **hWnd** 成員所指定視窗的視窗程式。 訊息的 *wParam* 參數包含發生事件的工作列圖示識別碼。 *LParam* 參數會保存與事件相關聯的滑鼠或鍵盤訊息。 例如，當滑鼠指標移至工作列圖示時， *lParam* 會包含 [**WM \_ MOUSEMOVE**](../inputdev/wm-mousemove.md)。

各種滑鼠事件的結果可摘要如下：

-   當使用者將滑鼠指標移到圖示上方時，系統會顯示 [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa)中所指定的工具提示文字。
-   當使用者按一下圖示時，您的應用程式會收到 [**WM \_ LBUTTONDOWN**](../inputdev/wm-lbuttondown.md) 通知。
-   當使用者以滑鼠右鍵按一下圖示時，您的應用程式會收到 [**WM \_ RBUTTONDOWN**](../inputdev/wm-rbuttondown.md) 通知。
-   當使用者按兩下該圖示時，您的應用程式會收到 [**WM \_ LBUTTONDBLCLK**](../inputdev/wm-lbuttondblclk.md) 通知。

一般而言，按一下圖示會導致應用程式顯示具有其他資訊的視窗，以滑鼠右鍵按一下以顯示快捷方式功能表，然後按兩下 [執行預設快捷方式功能表] 命令。

如需如何變更與通知區域圖示相關聯的工具提示文字的範例，請參閱 [狀態列圖示的氣球工具提示](../controls/tooltip-controls.md)。

shell 的5.0 版和更新版本會以不同的方式來 [**\_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona)滑鼠和鍵盤事件，而不像舊版 shell 版本 Windows NT 4.0、Windows 95 和 Windows 98。 差異如下：

-   如果使用者向鍵盤要求通知圖示的快捷方式功能表，5.0 版 Shell 會傳送一個 [**WM \_ CONTEXTMENU**](../menurc/wm-contextmenu.md) 訊息給相關聯的應用程式。 舊版會傳送 [**wm \_ RBUTTONDOWN**](../inputdev/wm-rbuttondown.md) 和 [**wm \_ RBUTTONUP**](../inputdev/wm-rbuttonup.md) 訊息。
-   如果使用者使用鍵盤選取 [通知] 圖示，並以空格鍵或 ENTER 鍵啟動它，則5.0 版 Shell 會將 **>nin \_ KEYSELECT** 通知傳送給相關聯的應用程式。 舊版會傳送 [**wm \_ RBUTTONDOWN**](../inputdev/wm-rbuttondown.md) 和 [**wm \_ RBUTTONUP**](../inputdev/wm-rbuttonup.md) 訊息。
-   如果使用者使用滑鼠選取 [通知] 圖示，並使用 ENTER 鍵啟動它，則5.0 版 Shell 會傳送 **>nin \_ SELECT** 通知給相關聯的應用程式。 舊版會傳送 [**wm \_ RBUTTONDOWN**](../inputdev/wm-rbuttondown.md) 和 [**wm \_ RBUTTONUP**](../inputdev/wm-rbuttonup.md) 訊息。
-   如果使用者將滑鼠指標移到與氣球工具提示相關聯的圖示上，版本 6.0 Shell (Windows XP) 傳送下列訊息。
    -   -   **>Nin \_BALLOONSHOW** -在顯示氣球時傳送 (球標排入佇列) 。
        -   **>Nin \_BALLOONHIDE** -當氣球消失時傳送，例如，當刪除圖示時。 如果因為超時或按下滑鼠，而關閉球標，則不會傳送此訊息。
        -   **>Nin \_BALLOONTIMEOUT** -當氣球因為 timeout 而關閉時傳送。
        -   **>Nin \_BALLOONUSERCLICK** -當氣球因為滑鼠按一下而關閉時傳送。

您可以藉由呼叫 [**shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) ，並將 *dwMessage* 設定為 **NIM \_ SETVERSION**，來選取 shell 的行為方式。 設定 [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa)結構的 **uVersion** 成員，以指出您是否想要5.0 版或5.0 版之前的行為。

### <a name="taskbar-creation-notification"></a>工作列建立通知

使用 Microsoft Internet Explorer 4.0 和更新版本時，Shell 會通知應用程式已建立工作列。 當工作列建立時，它會向 TaskbarCreated 字串註冊訊息，然後將此訊息廣播到所有最上層視窗。 當工作列應用程式接收到此訊息時，應假設它所新增的任何工作列圖示都已移除，並再次新增。 這項功能通常僅適用于 Shell 啟動時已在執行中的服務。 下列範例顯示非常簡單的方法來處理此案例。

在 Windows 10 上，當主顯示器的 DPI 變更時，工作列也會廣播此訊息。

```
LRESULT CALLBACK WndProc(HWND hWnd, 
                         UINT uMessage, 
                         WPARAM wParam, 
                         LPARAM lParam)
{
    static UINT s_uTaskbarRestart;

    switch(uMessage)
    {
        case WM_CREATE:
            s_uTaskbarRestart = RegisterWindowMessage(TEXT("TaskbarCreated"));
            break;
        
        default:
            if(uMessage == s_uTaskbarRestart)
                AddTaskbarIcons();
            break;
    }

    return DefWindowProc(hWnd, uMessage, wParam, lParam);
}
```



## <a name="using-the-taskbar"></a>使用工作列

本章節包含的範例將示範如何將圖示加入工作列通知區域，以及如何處理工作列圖示的回呼訊息。

### <a name="adding-and-deleting-taskbar-icons-in-the-notification-area"></a>新增和刪除通知區域中的工作列圖示

您可以藉由填妥 [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) 結構，然後將結構傳遞給 [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) ，並將 *dwMessage* 設定為 **NIM \_ add**，將圖示加入工作列通知區域中。 結構成員必須指定要加入圖示的視窗控制碼，以及圖示識別碼和圖示控制碼。 您也可以指定圖示的工具提示文字。 如果您需要接收圖示的滑鼠訊息，請指定系統應該用來將訊息傳送至視窗程式之回呼訊息的識別碼。

下列範例中的函式示範如何將圖示加入至工作列。


```
// MyTaskBarAddIcon - adds an icon to the notification area. 
// Returns TRUE if successful, or FALSE otherwise. 
// hwnd - handle to the window to receive callback messages 
// uID - identifier of the icon 
// hicon - handle to the icon to add 
// lpszTip - tooltip text 

BOOL MyTaskBarAddIcon(HWND hwnd, UINT uID, HICON hicon, LPSTR lpszTip) 
{ 
    BOOL res; 
    NOTIFYICONDATA tnid; 
 
    tnid.cbSize = sizeof(NOTIFYICONDATA); 
    tnid.hWnd = hwnd; 
    tnid.uID = uID; 
    tnid.uFlags = NIF_MESSAGE | NIF_ICON | NIF_TIP; 
    tnid.uCallbackMessage = MYWM_NOTIFYICON; 
    tnid.hIcon = hicon; 
    if (lpszTip) 
        hr = StringCbCopyN(tnid.szTip, sizeof(tnid.szTip), lpszTip, 
                           sizeof(tnid.szTip));
        // TODO: Add error handling for the HRESULT.
    else 
        tnid.szTip[0] = (TCHAR)'\0'; 
 
    res = Shell_NotifyIcon(NIM_ADD, &tnid); 
 
    if (hicon) 
        DestroyIcon(hicon); 
 
    return res; 
}
```



若要刪除工作列通知區域中的圖示，請填妥 [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa)結構，並將 *DwMessage* 設定為 **NIM \_ delete** 來呼叫 [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) 。 刪除工作列圖示時，請只指定結構的 **cbSize**、 **hWnd** 和 **uID** 成員。 例如：


```
// MyTaskBarDeleteIcon - deletes an icon from the notification area. 
// Returns TRUE if successful, or FALSE otherwise. 
// hwnd - handle to the window that added the icon. 
// uID - identifier of the icon to delete. 

BOOL MyTaskBarDeleteIcon(HWND hwnd, UINT uID) 
{ 
    BOOL res; 
    NOTIFYICONDATA tnid; 
 
    tnid.cbSize = sizeof(NOTIFYICONDATA); 
    tnid.hWnd = hwnd; 
    tnid.uID = uID; 
         
    res = Shell_NotifyIcon(NIM_DELETE, &tnid); 
    return res; 
}
```



### <a name="receiving-mouse-events"></a>接收滑鼠事件

如果您指定工作列圖示的回呼訊息，系統會在圖示的周框中出現滑鼠事件時，將訊息傳送至您的應用程式。 訊息的 *wParam* 參數會指定工作列圖示的識別碼，而訊息的 *lParam* 參數會指定系統產生的訊息，作為滑鼠事件的結果。

下列範例中的函式來自于將電池和印表機圖示新增至工作列的應用程式。 應用程式會在收到回呼訊息時呼叫函數。 此函式會判斷使用者是否已按下其中一個圖示，如果出現 click，則會呼叫應用程式定義的函式來顯示狀態資訊。


```
// On_MYWM_NOTIFYICON - processes callback messages for taskbar icons. 
// wParam - first message parameter of the callback message. 
// lParam - second message parameter of the callback message. 

void On_MYWM_NOTIFYICON(WPARAM wParam, LPARAM lParam) 
{ 
    UINT uID; 
    UINT uMouseMsg; 
 
    uID = (UINT) wParam; 
    uMouseMsg = (UINT) lParam; 
 
    if (uMouseMsg == WM_LBUTTONDOWN) 
    { 
        switch (uID) 
        { 
            case IDI_MYBATTERYICON: 
 
                // The user clicked the battery icon. Display the 
                // battery status. 
                ShowBatteryStatus(); 
                break; 
 
            case IDI_MYPRINTERICON: 
 
                // The user clicked the printer icon. Display the 
                // status of the print job. 
                ShowJobStatus(); 
                break; 
 
            default: 
                break; 
        } 
     } 

     return; 
 }
```



 

 
