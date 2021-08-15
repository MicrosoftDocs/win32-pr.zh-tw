---
title: 處理螢幕保護裝置
description: Microsoft WIN32 API 支援稱為螢幕保護裝置的特殊應用程式。
ms.assetid: cda5e690-71fe-4df7-b8a2-3a2ad65b1bfb
keywords:
- 螢幕保護裝置
- 主控台，螢幕保護裝置
- ScreenSaverConfigureDialog
- 模組定義檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b61343cd586ed022c334b797a77320ee25eccdf48653b4732adc597f4aedde26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975718"
---
# <a name="handling-screen-savers"></a>處理螢幕保護裝置

Microsoft WIN32 API 支援稱為 *螢幕保護裝置* 的特殊應用程式。 當滑鼠和鍵盤閒置一段指定的時間時，就會啟動畫面保護。 原因有下列兩個原因：

-   保護螢幕免于靜態映射所造成的 phosphor 燒錄。
-   隱藏畫面上的機密資訊。

本主題分為下列各節。

-   [關於螢幕保護裝置](#about-screen-savers)
-   [使用螢幕保護裝置函式](#using-the-screen-saver-functions)
    -   [建立螢幕保護裝置程式](#creating-a-screen-saver)
    -   [安裝新的螢幕保護裝置程式](#installing-new-screen-savers)
    -   [將說明新增至 [螢幕保護裝置設定] 對話方塊](#adding-help-to-the-screen-saver-configuration-dialog-box)

## <a name="about-screen-savers"></a>關於螢幕保護裝置

Windows 主控台中的桌面應用程式可讓使用者從螢幕保護裝置清單中選取，指定螢幕保護裝置啟動之前應經過的時間、設定螢幕保護裝置，以及預覽螢幕保護裝置。 當 Windows 啟動時，或當使用者透過主控台啟動畫面保護時，就會自動載入螢幕保護裝置。

選擇螢幕保護裝置之後，Windows 會監視按鍵和滑鼠移動，然後在閒置一段時間後啟動畫面保護。 但是，如果有下列任何一種情況，Windows 不會啟動畫面保護：

-   作用中的應用程式不是以 Windows 為基礎的應用程式。
-   有以電腦為基礎的訓練 (CBT) 視窗。
-   作用中的應用程式會接收包含 *wParam* 參數設定為 SC SCREENSAVE 值的 [WM \_ SYSCOMMAND](../menurc/wm-syscommand.md)訊息 \_ ，但不會將訊息傳遞至 [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca)函數。

**螢幕保護裝置的安全性內容**

螢幕保護裝置的安全性內容取決於使用者是否以互動方式登入。 如果叫用螢幕保護裝置時以互動方式登入使用者，螢幕保護裝置會在互動式使用者的安全性內容中執行。 如果沒有任何使用者登入，螢幕保護裝置的安全性內容將取決於所使用的 Windows 版本。

-   WindowsXP 和 Windows 2000-螢幕保護裝置會在具有帳戶限制的 LocalSystem 內容中執行。
-   Windows 2003-螢幕保護裝置會在 LocalService 的內容中執行，並移除擁有權限，並停用系統管理員群組。
-   不適用於 Windows NT4。

安全性內容會決定可以從螢幕保護裝置完成的特殊許可權作業層級。

**Windows Vista 和更新版本：** 如果原則啟用密碼保護，則不論應用程式如何使用 SC SCREENSAVE 通知，都會啟動畫面保護 \_ 。

螢幕保護裝置包含特定匯出的函式、資源定義和變數宣告。 螢幕保護裝置程式庫包含 **主要** 功能，以及螢幕保護裝置程式所需的其他啟動程式碼。 當螢幕保護裝置啟動時，螢幕保護裝置程式庫中的啟動程式碼會建立全螢幕視窗。 此視窗的視窗類別宣告如下：


```
WNDCLASS cls; 
cls.hCursor        = NULL; 
cls.hIcon          = LoadIcon(hInst, MAKEINTATOM(ID_APP)); 
cls.lpszMenuName   = NULL; 
cls.lpszClassName  = "WindowsScreenSaverClass"; 
cls.hbrBackground  = GetStockObject(BLACK_BRUSH); 
cls.hInstance      = hInst; 
cls.style          = CS_VREDRAW  | CS_HREDRAW | CS_SAVEBITS | CS_DBLCLKS; 
cls.lpfnWndProc    = (WNDPROC) ScreenSaverProc; 
cls.cbWndExtra     = 0; 
cls.cbClsExtra     = 0;
```



若要建立螢幕保護裝置，大部分的開發人員會建立包含三個必要功能的原始程式碼模組，並將它們與螢幕保護裝置程式庫連結。 螢幕保護裝置模組只負責設定本身以及提供視覺效果。

螢幕保護裝置模組中的三個必要功能之一是 [**ScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc)。 此函式會處理特定的訊息，並將任何未處理的訊息傳遞回螢幕保護裝置程式庫。 以下是一些 **ScreenSaverProc** 處理的一般訊息。



| 訊息        | 意義                                                                                                                                                                                    |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WM \_ 建立     | 從 Regedit.ini 檔案取出任何初始化資料。 設定螢幕保護裝置視窗的視窗計時器。 執行任何其他必要的初始化。                                     |
| WM \_ ERASEBKGND | 清除 [螢幕保護裝置] 視窗，並為後續的繪圖作業做好準備。                                                                                                               |
| WM \_ 計時器      | 執行繪圖作業。                                                                                                                                                                |
| WM 損 \_ 毀    | 終結應用程式處理 [WM \_ 建立](../winmsg/wm-create.md) 訊息時所建立的計時器。 執行任何其他必要的清除。 |



 

[**ScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc) 藉由呼叫 [**DefScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-defscreensaverproc) 函式，將未處理的訊息傳遞至螢幕保護裝置程式庫。 下表說明此函數如何處理各種訊息。



| 訊息         | 動作                                                                    |
|-----------------|---------------------------------------------------------------------------|
| WM \_ SETCURSOR   | 將游標設為 null 資料指標，並將它從畫面中移除。           |
| WM \_ 油漆       | 小畫家螢幕背景。                                              |
| WM \_ LBUTTONDOWN | 終止螢幕保護裝置。                                               |
| WM \_ MBUTTONDOWN | 終止螢幕保護裝置。                                               |
| WM \_ RBUTTONDOWN | 終止螢幕保護裝置。                                               |
| WM \_ KEYDOWN     | 終止螢幕保護裝置。                                               |
| WM \_ MOUSEMOVE   | 終止螢幕保護裝置。                                               |
| WM \_ 啟用    | 如果 *wParam* 參數設定為 **FALSE**，則終止螢幕保護裝置。 |



 

螢幕保護裝置模組中的第二個必要功能是 [**ScreenSaverConfigureDialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog)。 此函式會顯示對話方塊，讓使用者可以設定螢幕保護裝置 (應用程式必須提供對應的對話方塊範本) 。 當使用者在主控台的 [螢幕保護裝置] 對話方塊中選取 [安裝] 按鈕時，Windows 會顯示 [**設定**] 對話方塊。

螢幕保護裝置模組中的第三個必要功能是 [**RegisterDialogClasses**](/windows/desktop/api/scrnsave/nf-scrnsave-registerdialogclasses)。 所有螢幕保護裝置應用程式都必須呼叫此函式。 不過，在 [設定] 對話方塊中不需要特殊 windows 或自訂控制項的應用程式可以直接傳回 **TRUE**。 需要特殊 windows 或自訂控制項的應用程式應該使用此函式來註冊對應的視窗類別。

除了建立支援上述三個函式的模組之外，螢幕保護裝置還應該提供圖示。 只有當螢幕保護裝置以獨立應用程式的形式執行時，才會顯示此圖示。  (由主控台執行，則螢幕保護裝置的副檔名必須為 .scr;若要以獨立應用程式的形式執行，它必須有 .exe 的副檔名。 ) 在 \_ Scrnsave .h 標頭檔中定義的常數識別碼應用程式必須在螢幕保護裝置程式的資源檔中識別該圖示。

最後一個需求是螢幕保護裝置的描述字串。 螢幕保護裝置的資源檔必須包含主控台顯示為螢幕保護裝置名稱的字串。 描述字串必須是資源檔的字串資料表中的第一個字串， (以序數值 1) 識別。 但是，如果螢幕保護裝置的檔案名很長，則主控台會忽略描述字串。 在這種情況下，檔案名會用來做為描述字串。

## <a name="using-the-screen-saver-functions"></a>使用螢幕保護裝置函式

本節使用從螢幕保護裝置應用程式取得的範例程式碼來說明下列工作：

-   [建立螢幕保護裝置程式](#creating-a-screen-saver)
-   [安裝新的螢幕保護裝置程式](#installing-new-screen-savers)
-   [將說明新增至 [螢幕保護裝置設定] 對話方塊](#adding-help-to-the-screen-saver-configuration-dialog-box)

### <a name="creating-a-screen-saver"></a>建立螢幕保護裝置程式

從1到10秒的間隔，此範例中的應用程式會以四種色彩的其中一種來重新繪製畫面：白色、淺灰色、暗灰色和黑色。 應用程式會在每次收到 [WM \_ 計時器](../winmsg/wm-timer.md) 訊息時繪製畫面。 使用者可以藉由選取應用程式的 [設定] 對話方塊，並調整單一水準捲軸，來調整傳送此訊息的間隔。

### <a name="screen-saver-library"></a>螢幕保護裝置程式庫

靜態螢幕保護裝置函式包含在螢幕保護裝置程式庫中。 有兩個版本的程式庫可用： Scrnsave .lib 和 Scrnsavw。 您必須使用下列其中一項鍊接您的專案。 Scrnsave 可用於使用 ANSI 字元的螢幕保護裝置，而 Scrnsavw 則用於使用 Unicode 字元的螢幕保護裝置。 與 Scrnsavw 連結的螢幕保護裝置只會在支援 Unicode 的 Windows 平臺上執行，而與 Scrnsave 連結的螢幕保護裝置會在任何 Windows 平臺上執行。

### <a name="supporting-the-configuration-dialog-box"></a>支援設定對話方塊

大部分的螢幕保護裝置都會提供設定對話方塊，讓使用者指定自訂資料，例如獨特的色彩、繪圖速度、線條粗細、字型等等。 若要支援 [設定] 對話方塊，應用程式必須提供對話方塊範本，而且也必須支援 [**ScreenSaverConfigureDialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog) 函數。 以下是範例應用程式的對話方塊範本。


```
DLG_SCRNSAVECONFIGURE DIALOG 6, 18, 160, 63
LANGUAGE LANG_NEUTRAL, SUBLANG_NEUTRAL
STYLE DS_MODALFRAME | WS_POPUP | WS_VISIBLE | WS_CAPTION | WS_SYSMENU
CAPTION "Sample Screen-Saver Setup"
FONT 8, "MS Shell Dlg"
BEGIN
    GROUPBOX      "Redraw Speed", 101, 0, 6, 98, 40
    SCROLLBAR     ID_SPEED, 5, 31, 89, 10
    LTEXT         "Fast", 103, 6, 21, 20, 8
    LTEXT         "Slow", 104, 75, 21, 20, 8
    PUSHBUTTON    "OK", ID_OK, 117, 10, 40, 14
    PUSHBUTTON    "Cancel", ID_CANCEL, 117, 32, 40, 14
END
```



您必須使用十進位值2003來定義用來識別對話方塊範本的常數，如下列範例所示：


```
#define  DLG_SCRNSAVECONFIGURE 2003
```



下列範例顯示在範例應用程式中找到的 [**ScreenSaverConfigureDialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog) 函式。


```
#define MINVEL  1                 // minimum redraw speed value     
#define MAXVEL  10                // maximum redraw speed value    
#define DEFVEL  5                 // default redraw speed value    
 
LONG    lSpeed = DEFVEL;          // redraw speed variable         
  
extern HINSTANCE hMainInstance;   // screen saver instance handle  
 
CHAR   szAppName[80];             // .ini section name             
CHAR   szTemp[20];                // temporary array of characters  
CHAR   szRedrawSpeed[ ] = "Redraw Speed";   // .ini speed entry 
CHAR   szIniFile[MAXFILELEN];     // .ini or registry file name  
 
BOOL WINAPI ScreenSaverConfigureDialog(hDlg, message, wParam, lParam) 
HWND     hDlg; 
UINT     message; 
DWORD    wParam; 
LONG     lParam; 
HRESULT  hr;
{ 
    static HWND hSpeed;   // handle to speed scroll bar 
    static HWND hOK;      // handle to OK push button  
 
    switch(message) 
    { 
        case WM_INITDIALOG: 
 
            // Retrieve the application name from the .rc file.  
            LoadString(hMainInstance, idsAppName, szAppName, 
                       80 * sizeof(TCHAR)); 
 
            // Retrieve the .ini (or registry) file name. 
            LoadString(hMainInstance, idsIniFile, szIniFile, 
                       MAXFILELEN * sizeof(TCHAR)); 
 
            // TODO: Add error checking to verify LoadString success
            //       for both calls.
            
            // Retrieve any redraw speed data from the registry. 
            lSpeed = GetPrivateProfileInt(szAppName, szRedrawSpeed, 
                                          DEFVEL, szIniFile); 
 
            // If the initialization file does not contain an entry 
            // for this screen saver, use the default value. 
            if(lSpeed > MAXVEL || lSpeed < MINVEL) 
                lSpeed = DEFVEL; 
 
            // Initialize the redraw speed scroll bar control.
            hSpeed = GetDlgItem(hDlg, ID_SPEED); 
            SetScrollRange(hSpeed, SB_CTL, MINVEL, MAXVEL, FALSE); 
            SetScrollPos(hSpeed, SB_CTL, lSpeed, TRUE); 
 
            // Retrieve a handle to the OK push button control.  
            hOK = GetDlgItem(hDlg, ID_OK); 
 
            return TRUE; 
 
        case WM_HSCROLL: 

            // Process scroll bar input, adjusting the lSpeed 
            // value as appropriate. 
            switch (LOWORD(wParam)) 
                { 
                    case SB_PAGEUP: 
                        --lSpeed; 
                    break; 
 
                    case SB_LINEUP: 
                        --lSpeed; 
                    break; 
 
                    case SB_PAGEDOWN: 
                        ++lSpeed; 
                    break; 
 
                    case SB_LINEDOWN: 
                        ++lSpeed; 
                    break; 
 
                    case SB_THUMBPOSITION: 
                        lSpeed = HIWORD(wParam); 
                    break; 
 
                    case SB_BOTTOM: 
                        lSpeed = MINVEL; 
                    break; 
 
                    case SB_TOP: 
                        lSpeed = MAXVEL; 
                    break; 
 
                    case SB_THUMBTRACK: 
                    case SB_ENDSCROLL: 
                        return TRUE; 
                    break; 
                } 

                if ((int) lSpeed <= MINVEL) 
                    lSpeed = MINVEL; 
                if ((int) lSpeed >= MAXVEL) 
                    lSpeed = MAXVEL; 
 
                SetScrollPos((HWND) lParam, SB_CTL, lSpeed, TRUE); 
            break; 
 
        case WM_COMMAND: 
            switch(LOWORD(wParam)) 
            { 
                case ID_OK: 
 
                    // Write the current redraw speed variable to
                    // the .ini file. 
                    hr = StringCchPrintf(szTemp, 20, "%ld", lSpeed);
                    if (SUCCEEDED(hr))
                        WritePrivateProfileString(szAppName, szRedrawSpeed, 
                                                  szTemp, szIniFile); 
 
                case ID_CANCEL: 
                    EndDialog(hDlg, LOWORD(wParam) == ID_OK); 

                return TRUE; 
            } 
    } 
    return FALSE; 
}
```



除了提供對話方塊範本和支援 [**ScreenSaverConfigureDialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog) 函式之外，應用程式也必須支援 [**RegisterDialogClasses**](/windows/desktop/api/scrnsave/nf-scrnsave-registerdialogclasses) 函數。 此函式會註冊螢幕保護裝置程式所需的任何非標準視窗類別。 因為範例應用程式只在其對話方塊程式中使用標準視窗類別，所以此函式只會傳回 **TRUE**，如下列範例所示：


```
BOOL WINAPI RegisterDialogClasses(hInst) 
HANDLE  hInst; 
{ 
    return TRUE; 
}
```



### <a name="supporting-the-screen-saver-window-procedure"></a>支援螢幕保護裝置視窗程式

每個螢幕保護裝置都必須支援一個名為 [**ScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc)的視窗程式。 和大部分的視窗程式一樣， **ScreenSaverProc** 會處理一組特定的訊息，並將任何未處理的訊息傳遞至預設程式。 但是， **ScreenSaverProc** 會將未處理的訊息傳遞給 [**DefScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-defscreensaverproc)函式，而不是將它們傳遞給 [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca)函數。 **ScreenSaverProc** 和一般視窗程式之間的另一個差異是，傳遞至 **ScreenSaverProc** 的控制碼會識別整個桌面，而不是用戶端視窗。 下列範例顯示範例螢幕保護裝置的 **ScreenSaverProc** 視窗程式。


```
LONG WINAPI ScreenSaverProc(hwnd, message, wParam, lParam) 
HWND  hwnd; 
UINT  message; 
DWORD wParam; 
LONG  lParam; 
{ 
    static HDC          hdc;      // device-context handle  
    static RECT         rc;       // RECT structure  
    static UINT         uTimer;   // timer identifier  
 
    switch(message) 
    { 
        case WM_CREATE: 
 
            // Retrieve the application name from the .rc file. 
            LoadString(hMainInstance, idsAppName, szAppName, 80 * sizeof(TCHAR)); 
 
            // Retrieve the .ini (or registry) file name. 
            LoadString(hMainInstance, idsIniFile, szIniFile, MAXFILELEN * sizeof(TCHAR)); 
 
            // TODO: Add error checking to verify LoadString success
            //       for both calls.
            
            // Retrieve any redraw speed data from the registry.  
            lSpeed = GetPrivateProfileInt(szAppName, szRedrawSpeed, 
                                          DEFVEL, szIniFile); 
 
            // Set a timer for the screen saver window using the 
            // redraw rate stored in Regedit.ini. 
            uTimer = SetTimer(hwnd, 1, lSpeed * 1000, NULL); 
            break; 
 
        case WM_ERASEBKGND: 
 
            // The WM_ERASEBKGND message is issued before the 
            // WM_TIMER message, allowing the screen saver to 
            // paint the background as appropriate. 

            hdc = GetDC(hwnd); 
            GetClientRect (hwnd, &rc); 
            FillRect (hdc, &rc, GetStockObject(BLACK_BRUSH)); 
            ReleaseDC(hwnd,hdc); 
            break; 
 
        case WM_TIMER: 
 
            // The WM_TIMER message is issued at (lSpeed * 1000) 
            // intervals, where lSpeed == .001 seconds. This 
            // code repaints the entire desktop with a white, 
            // light gray, dark gray, or black brush each 
            // time a WM_TIMER message is issued. 

            hdc = GetDC(hwnd); 
            GetClientRect(hwnd, &rc); 
            if (i++ <= 4) 
                FillRect(hdc, &rc, GetStockObject(i)); 
            else 
                (i = 0); 
            ReleaseDC(hwnd,hdc); 
            break; 
 
        case WM_DESTROY: 
 
            // When the WM_DESTROY message is issued, the screen saver 
            // must destroy any of the timers that were set at WM_CREATE 
            // time. 

            if (uTimer) 
                KillTimer(hwnd, uTimer); 
            break; 
    } 
 
    // DefScreenSaverProc processes any messages ignored by ScreenSaverProc. 
    return DefScreenSaverProc(hwnd, message, wParam, lParam); 
}
```



### <a name="creating-a-module-definition-file"></a>建立模組定義檔

[**ScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc)和 [**ScreenSaverConfigureDialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog)函數必須在應用程式的模組定義檔中匯出;但是， [**RegisterDialogClasses**](/windows/desktop/api/scrnsave/nf-scrnsave-registerdialogclasses)不應該匯出。 下列範例顯示範例應用程式的模組定義檔。


```
NAME    SSTEST.SCR 

DESCRIPTION 'SCRNSAVE : Test' 
 
STUB    'WINSTUB.EXE' 
EXETYPE WINDOWS 
 
CODE    MOVEABLE 
DATA    MOVEABLE MULTIPLE 
 
HEAPSIZE  1024 
STACKSIZE 4096 
 
EXPORTS 
        ScreenSaverProc 
        ScreenSaverConfigureDialog
```



### <a name="installing-new-screen-savers"></a>安裝新的螢幕保護裝置程式

在編譯可用螢幕保護裝置的清單時，主控台會在 Windows 啟動目錄中搜尋副檔名為 .scr 的檔案。 由於螢幕保護裝置是具有 .exe 副檔名的標準 Windows 可執行檔，因此您必須將它們重新命名，使其具有 .scr 副檔名，並將其複製到正確的目錄。

### <a name="adding-help-to-the-screen-saver-configuration-dialog-box"></a>將說明新增至 [螢幕保護裝置設定] 對話方塊

螢幕保護裝置程式的 [設定] 對話方塊通常會包含 [說明 **] 按鈕。** 螢幕保護裝置應用程式可以檢查 [說明] 按鈕識別碼，並以其他 Windows 架構應用程式中提供的相同方式來呼叫 [**WinHelp**](/windows/desktop/api/winuser/nf-winuser-winhelpa)函數。

 

 