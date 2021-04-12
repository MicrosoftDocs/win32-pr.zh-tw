---
description: 本主題說明應用程式用來建立及使用 windows 的程式設計項目;管理 windows 之間的關聯性;和大小、移動和顯示視窗。
ms.assetid: e325f8dc-004f-44a9-9122-3be5e44764d6
title: 關於 Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e2df510deea689d70bd1ebf5e59cafc92b0389d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104192826"
---
# <a name="about-windows"></a>關於 Windows

本主題說明應用程式用來建立及使用 windows 的程式設計項目;管理 windows 之間的關聯性;和大小、移動和顯示視窗。

此總覽包含下列主題。

-   [桌面視窗](#desktop-window)
-   [應用程式視窗](#application-windows)
    -   [工作區](#client-area)
    -   [非工作區](#nonclient-area)
-   [控制項和對話方塊](#controls-and-dialog-boxes)
-   [視窗屬性](#window-attributes)
    -   [類別名稱](#class-name)
    -   [視窗名稱](#window-name)
    -   [視窗樣式](#window-style)
    -   [延伸視窗樣式](#extended-window-style)
    -   [位置](#position)
    -   [大小](#size)
    -   [父系或擁有者視窗控制碼](#parent-or-owner-window-handle)
    -   [功能表控制碼或 Child-Window 識別碼](#menu-handle-or-child-window-identifier)
    -   [應用程式實例控制碼](#application-instance-handle)
    -   [建立資料](#creation-data)
    -   [視窗控制代碼](#window-handle)
-   [視窗建立](#creation-data)
    -   [建立主視窗](#main-window-creation)
    -   [視窗建立訊息](#window-creation-messages)
    -   [多執行緒應用程式](#multithread-applications)

## <a name="desktop-window"></a>桌面視窗

當您啟動系統時，它會自動建立桌面視窗。 *桌面視窗* 是系統定義的視窗，會繪製畫面的背景，並做為所有應用程式所顯示所有視窗的基底。

桌面視窗使用點陣圖來繪製畫面的背景。 點陣圖建立的模式稱為 *桌面壁紙*。 根據預設，桌面視窗會使用登錄中指定的 .bmp 檔中的點陣圖作為桌面壁紙。

[**GetDesktopWindow**](/windows/win32/api/winuser/nf-winuser-getdesktopwindow)函式會將控制碼傳回至桌面視窗。

系統設定應用程式（例如主控台專案）會藉由使用 [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) 函式，將 *wAction* 參數設定為 **SPI \_ SETDESKWALLPAPER** ，以及指定點陣圖檔案名的 *lpvParam* 參數，來變更桌面背景圖樣。 然後， **SystemParametersInfo** 會從指定的檔案載入點陣圖、使用點陣圖來繪製畫面的背景，並在登錄中輸入新的檔案名。

## <a name="application-windows"></a>應用程式視窗

每個以圖形為基礎的應用程式會建立至少一個視窗（稱為 *主視窗*），作為使用者和應用程式之間的主要介面。 大部分的應用程式也會直接或間接地建立其他視窗，以執行與主視窗相關的工作。 每個視窗會在顯示輸出和接收來自使用者的輸入時播放一個部分。

當您啟動應用程式時，系統也會將工作列按鈕與應用程式產生關聯。 *工作列按鈕* 包含程式圖示和標題。 當應用程式在作用中時，其工作列按鈕會顯示為 [已推送] 狀態。

應用程式視窗包含標題列、功能表列、視窗功能表 (先前稱為系統功能表) 、[最小化] 按鈕、[最大化] 按鈕、[還原] 按鈕、[關閉] 按鈕、調整大小框線、用戶端區域、水準捲軸以及垂直捲動條等元素。 應用程式的主視窗通常包含所有這些元件。 下圖顯示一般主視窗中的這些元件。

![一般視窗](images/cswin-02.png)

### <a name="client-area"></a>工作區

工作 *區* 是視窗的一部分，其中應用程式會顯示輸出，例如文字或圖形。 例如，桌面發佈應用程式會在工作區中顯示檔的目前頁面。 應用程式必須提供稱為視窗程式的函式，以處理視窗的輸入，並在工作區中顯示輸出。 如需詳細資訊，請參閱 [Window 程序](window-procedures.md)。

### <a name="nonclient-area"></a>非工作區

標題列、功能表列、視窗功能表、最小化和最大化按鈕、大小調整框線和捲軸，統稱為視窗的 *非工作區*。 系統會管理非工作區的大部分層面;應用程式會管理其工作區的外觀和行為。

*標題列* 會顯示應用程式定義的圖示和文字行;一般而言，文字會指定應用程式的名稱，或表示視窗的用途。 應用程式會指定建立視窗時的圖示和文字。 標題列也可以讓使用者使用滑鼠或其他指標裝置來移動視窗。

大部分的應用程式都包含一個 *功能表列* ，其中列出應用程式所支援的命令。 功能表列中的專案代表命令的主要類別。 按一下功能表列上的專案，通常會開啟快顯功能表，其專案對應至指定類別中的工作。 藉由按一下命令，使用者會指示應用程式執行工作。

系統會建立並管理 *視窗功能表* 。 它包含一組標準的功能表項目，使用者在選擇時，會設定視窗的大小或位置、關閉應用程式，或執行工作。 如需詳細資訊，請參閱 [功能表](/windows/desktop/menurc/menus)。

右上角的按鈕會影響視窗的大小和位置。 當您按一下 [ *最大化] 按鈕* 時，系統會將視窗放大到畫面的大小並放置視窗，因此它會涵蓋整個桌面，減去工作列。 同時，系統會以 [還原] 按鈕取代 [最大化] 按鈕。 當您按一下 [ *還原] 按鈕* 時，系統會將視窗還原為其先前的大小與位置。 當您按一下 [ *最小化] 按鈕* 時，系統會將視窗縮小至工作列按鈕的大小、將視窗放在工作列按鈕上，然後將工作列按鈕顯示為正常狀態。 若要將應用程式還原為其先前的大小和位置，請按一下其工作列按鈕。 當您按一下 [ *關閉] 按鈕* 時，應用程式會結束。

*調整框線* 是視窗周邊周圍的區域，可讓使用者使用滑鼠或其他指標裝置來調整視窗的大小。

*水準捲軸* 和 *垂直捲動條* 會將滑鼠或鍵盤輸入轉換為應用程式用來水準或垂直移動用戶端區域內容的值。 例如，顯示冗長檔的文字處理應用程式通常會提供垂直捲動條，讓使用者可以在檔中向上和向下翻頁。

## <a name="controls-and-dialog-boxes"></a>控制項和對話方塊

應用程式除了主視窗（包括控制項和對話方塊）之外，還可以建立數種類型的視窗。

*控制項* 是應用程式用來從使用者取得特定資訊片段的視窗，例如要開啟的檔案名或文字選取範圍的所需位置。 應用程式也會使用控制項來取得控制應用程式特定功能所需的資訊。 例如，文字處理應用程式通常會提供一個控制項，讓使用者開啟和關閉自動換行。 如需詳細資訊，請參閱 [Windows 控制項](/windows/desktop/Controls/window-controls)。

控制項一律會與另一個視窗（通常是對話方塊）一起使用。 *對話方塊* 是包含一或多個控制項的視窗。 應用程式會使用對話方塊來提示使用者完成命令所需的輸入。 例如，包含開啟檔案之命令的應用程式會顯示一個對話方塊，其中包含使用者指定路徑和檔案名的控制項。 對話方塊通常不會使用與主視窗相同的一組視窗元件。 大部分的標題列、視窗功能表、框線 (非調整大小) 和工作區，但它們通常沒有功能表列、最小化和最大化按鈕或捲軸。 如需詳細資訊，請參閱 [對話方塊](/windows/desktop/dlgbox/dialog-boxes)。

*訊息方塊* 是特殊的對話方塊，會對使用者顯示附注、警告或警告。 例如，訊息方塊可告知使用者執行工作時，應用程式發生的問題。 如需詳細資訊，請參閱 [訊息方塊](/windows/desktop/dlgbox/about-dialog-boxes)。

## <a name="window-attributes"></a>視窗屬性

建立視窗時，應用程式必須提供下列資訊。  (的 [視窗控制碼](#window-handle)例外，建立函式會傳回以唯一識別新的視窗。 ) 

-   [類別名稱](#class-name)
-   [視窗名稱](#window-name)
-   [視窗樣式](#window-style)
-   [延伸視窗樣式](#extended-window-style)
-   [位置](#position)
-   [大小](#size)
-   [父系或擁有者視窗控制碼](#parent-or-owner-window-handle)
-   [功能表控制碼或 Child-Window 識別碼](#menu-handle-or-child-window-identifier)
-   [應用程式實例控制碼](#application-instance-handle)
-   [建立資料](#creation-data)
-   [視窗控制代碼](#window-handle)

下列各節將描述這些視窗屬性。

### <a name="class-name"></a>類別名稱

每個視窗都屬於一個視窗類別。 應用程式必須先註冊視窗類別，才能建立該類別的任何視窗。 *視窗類別* 會定義視窗外觀和行為的大部分層面。 視窗類別的主要元件是 *視窗* 程式，這個函式會接收和處理傳送至視窗的所有輸入和要求。 系統會以 *訊息* 的形式提供輸入和要求。 如需詳細資訊，請參閱 [視窗類別](window-classes.md)、 [視窗程式](window-procedures.md)和 [訊息和訊息佇列](messages-and-message-queues.md)。

### <a name="window-name"></a>視窗名稱

*視窗名稱* 是識別使用者視窗的文字字串。 主視窗、對話方塊或訊息方塊通常會在其標題列中顯示其視窗名稱（如果有的話）。 根據控制項的類別，控制項可能會顯示其視窗名稱。 例如，按鈕、編輯控制項和靜態控制項，會在控制項所佔用的矩形內顯示其視窗名稱。 不過，清單方塊和下拉式方塊等控制項不會顯示其視窗名稱。

若要在建立視窗之後變更視窗名稱，請使用 [**SetWindowText**](/windows/win32/api/winuser/nf-winuser-setwindowtexta) 函數。 此函數會使用 [**GetWindowTextLength**](/windows/win32/api/winuser/nf-winuser-getwindowtextlengtha) 和 [**GetWindowText**](/windows/win32/api/winuser/nf-winuser-getwindowtexta) 函式，從視窗中取出目前的視窗名稱字串。

### <a name="window-style"></a>視窗樣式

每個視窗都有一個或多個視窗樣式。 視窗樣式是一個名為的常數，定義視窗的外觀和行為，而不是由視窗的類別指定。 應用程式通常會在建立 windows 時設定視窗樣式。 它也可以在使用 [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) 函式建立視窗之後設定樣式。

系統以及類別的視窗程式，會解讀視窗樣式。

某些視窗樣式適用于所有視窗，但大部分適用于特定視窗類別的視窗。 一般視窗樣式是由以 WS 前置詞開頭的常數來表示 \_ ，它們可以與 OR 運算子結合以形成不同類型的視窗，包括主視窗、對話方塊和子視窗。 特定類別的視窗樣式定義了屬於預先定義之控制項類別的 windows 外觀和行為。 例如， **捲軸** 類別會指定捲軸控制項，但 [**Sbs \_ HORZ**](../controls/scroll-bar-control-styles.md) 和 **sbs \_ 垂直** 樣式會決定是否要建立水準或垂直捲動條控制項。

如需可供 windows 使用的樣式清單，請參閱下列主題：

-   [**視窗樣式**](window-styles.md)
-   [按鈕樣式](../controls/button-styles.md)
-   [下拉式列示方塊樣式](../controls/combo-box-styles.md)
-   [編輯控制項樣式](../controls/edit-control-styles.md)
-   [清單方塊樣式](../controls/list-box-styles.md)
-   [Rich Edit 控制項樣式](../controls/rich-edit-control-styles.md)
-   [捲軸控制項樣式](../controls/scroll-bar-control-styles.md)
-   [靜態控制項樣式](../controls/static-control-styles.md)

### <a name="extended-window-style"></a>延伸視窗樣式

每個視窗都可以選擇性地有一或多個擴充的視窗樣式。 *擴充的視窗樣式* 是一個命名常數，定義視窗類別或其他視窗樣式未指定之視窗外觀和行為的層面。 應用程式通常會在建立 windows 時設定擴充的視窗樣式。 它也可以在使用 [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) 函式建立視窗之後設定樣式。

如需詳細資訊，請參閱 [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa)。

### <a name="position"></a>位置

視窗的位置會定義為其左上角的座標。 這些座標（有時稱為視窗座標）一律相對於畫面的左上角，也就是子視窗的父視窗工作區的左上角。 例如，將座標 (10，10) 的最上層視窗會放置在畫面左上角的10個圖元，並將其向下10個圖元。 具有座標 (10，10) 的子視窗，會在其父視窗的工作區左上角的右邊加上10個圖元，並將其向下10個圖元下放置。

[**WindowFromPoint**](/windows/win32/api/winuser/nf-winuser-windowfrompoint)函式會抓取視窗的控制碼，以佔用畫面上的特定點。 同樣地， [**ChildWindowFromPoint**](/windows/win32/api/winuser/nf-winuser-childwindowfrompoint) 和 [**ChildWindowFromPointEx**](/windows/win32/api/winuser/nf-winuser-childwindowfrompointex) 函式會抓取子視窗的控制碼，以佔用父視窗工作區中的特定點。 雖然 **ChildWindowFromPointEx** 可以忽略隱藏、停用以及透明的子視窗，但是 **ChildWindowFromPoint** 無法。

### <a name="size"></a>大小

視窗的大小 (寬度和高度) 以圖元為單位。 視窗可以有零寬度或高度。 如果應用程式將視窗的寬度和高度設定為零，系統會將大小設定為預設的最小視窗大小。 若要探索預設的最小視窗大小，應用程式會使用 [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) 函數搭配 **Sm \_ CXMIN** 和 **sm \_ CYMIN** 旗標。

應用程式可能需要建立具有特定大小之工作區的視窗。 [**AdjustWindowRect**](/windows/win32/api/winuser/nf-winuser-adjustwindowrect)和 [**AdjustWindowRectEx**](/windows/win32/api/winuser/nf-winuser-adjustwindowrectex)函式會根據工作區所需的大小，計算視窗所需的大小。 應用程式可以將產生的大小值傳遞至 [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) 函數。

應用程式可以調整視窗的大小，使其變得非常大。不過，它不應該調整視窗的大小，使其大於螢幕。 在設定視窗的大小之前，應用程式應該使用 [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) 搭配 **Sm \_ CXSCREEN** 和 **sm \_ CYSCREEN** 旗標來檢查畫面的寬度和高度。

### <a name="parent-or-owner-window-handle"></a>父系或擁有者視窗控制碼

視窗可以有父視窗。 具有父系的視窗稱為 *子視窗*。 *父視窗* 提供用來放置子視窗的座標系統。 擁有父視窗會影響視窗外觀的各個層面;例如，會裁剪子視窗，讓子視窗的任何部分不能出現在其父視窗的框線之外。

沒有父系或其父系為桌面視窗的視窗，稱為 *最上層視窗*。 應用程式可以使用 [**EnumWindows**](/windows/win32/api/winuser/nf-winuser-enumwindows) 函式來取得畫面上每個最上層視窗的控制碼。 **EnumWindows** 會將每個最上層視窗的控制碼傳遞至應用程式定義的回呼函數 [**EnumWindowsProc**](/previous-versions/windows/desktop/legacy/ms633498(v=vs.85))。

最上層視窗可擁有或由另一個視窗擁有。 *擁有的視窗* 一律會出現在其擁有者視窗前方，當其擁有者視窗最小化時，就會隱藏起來，而且當其擁有者視窗損毀時，會加以終結。 如需詳細資訊，請參閱 [擁有的視窗](window-features.md#owned-windows)。

### <a name="menu-handle-or-child-window-identifier"></a>功能表控制碼或 Child-Window 識別碼

子視窗可以有一個 *子視窗* 識別碼，這是一個與子視窗相關聯的唯一應用程式定義值。 子視窗識別碼在建立多個子視窗的應用程式中特別有用。 建立子視窗時，應用程式會指定子視窗的識別碼。 建立視窗之後，應用程式可以使用 [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) 函數來變更視窗的識別碼，或使用 [**GetWindowLong**](/windows/win32/api/winuser/nf-winuser-getwindowlonga) 函式來取得識別碼。

除了子視窗，每個視窗都可以有功能表。 應用程式可以包含功能表，方法是在註冊視窗的類別或建立視窗時提供功能表控制碼。

### <a name="application-instance-handle"></a>應用程式實例控制碼

每個應用程式都有與其相關聯的實例控制碼。 當應用程式啟動時，系統會提供應用程式的實例控制碼。 因為它可以執行相同應用程式的多個複本，所以系統會在內部使用實例控制碼，以區分應用程式的一個實例與另一個實例。 應用程式必須在許多不同的視窗中指定實例控制碼，包括建立 windows 的視窗。

### <a name="creation-data"></a>建立資料

每個視窗都可以有相關聯的應用程式定義建立資料。 當您第一次建立視窗時，系統會將的資料指標傳遞至要建立之視窗的視窗程式。 視窗程式會使用資料來初始化應用程式定義的變數。

### <a name="window-handle"></a>視窗控制代碼

建立視窗之後，建立函數會傳回可唯一識別視窗的 *視窗控制碼* 。 視窗控制碼具有 **HWND** 資料類型;應用程式在宣告持有視窗控制碼的變數時，必須使用此型別。 應用程式會在其他函式中使用此控制碼，將其動作導向至視窗。

應用程式可以使用 [**FindWindow**](/windows/win32/api/winuser/nf-winuser-findwindowa) 函式，來探索具有指定類別名稱或視窗名稱的視窗是否存在於系統中。 如果有這種視窗存在， **FindWindow** 會傳回視窗的控制碼。 若要將搜尋限制為特定應用程式的子視窗，請使用 [**FindWindowEx**](/windows/win32/api/winuser/nf-winuser-findwindowexa) 函數。

[**IsWindow**](/windows/win32/api/winuser/nf-winuser-iswindow)函式會判斷視窗控制碼是否識別有效的現有視窗。 有些特殊的常數可以取代某些函式中的視窗控制碼。 例如，應用程式可以使用 [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage)和 [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta)函式中的 **hwnd \_ 廣播**，或 [**MapWindowPoints**](/windows/desktop/api/winuser/nf-winuser-mapwindowpoints)函式中的 **hwnd \_ 桌面**。

## <a name="window-creation"></a>視窗建立

若要建立應用程式視窗，請使用 [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) 或 [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) 函數。 您必須提供定義視窗屬性所需的資訊。 **CreateWindowEx** has a parameter, *dwExStyle*, that **CreateWindow** does not have; otherwise, the functions are identical. 事實上， **CreateWindow** 只會呼叫 **CreateWindowEx** ，並將 *dwExStyle* 參數設定為零。 基於這個理由，此總覽的其餘部分只會參考 **CreateWindowEx**。

本節包含下列主題：

-   [建立主視窗](#main-window-creation)
-   [視窗建立訊息](#window-creation-messages)
-   [多執行緒應用程式](#multithread-applications)

> [!Note]  
> 還有其他功能可以用來建立特殊用途的視窗，例如對話方塊和訊息方塊。 如需詳細資訊，請參閱 [**對話方塊**](/windows/desktop/api/winuser/nf-winuser-dialogboxa)、 [**CreateDialog**](/windows/desktop/api/winuser/nf-winuser-createdialoga)和 [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox)。

 

### <a name="main-window-creation"></a>建立主視窗

每個以 Windows 為基礎的應用程式都必須有 [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) 作為其進入點函式。 **WinMain** 會執行一些工作，包括註冊主視窗的視窗類別和建立主視窗。 **WinMain** 會藉由呼叫 [**RegisterClass**](/windows/win32/api/winuser/nf-winuser-registerclassa) 函數來註冊主視窗類別，並藉由呼叫 [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) 函式來建立主視窗。

您的 [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) 函式也可以將應用程式限制為單一實例。 使用 [**CreateMutex**](/windows/desktop/api/synchapi/nf-synchapi-createmutexa) 函式建立命名 mutex。 如果 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 傳回 **錯誤 \_ 已經 \_ 存在**，則應用程式的另一個實例 (它建立了 Mutex) ，您應該結束 **WinMain**。

系統不會在建立時自動顯示主視窗;相反地，應用程式必須使用 [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) 函式來顯示主視窗。 建立主視窗之後，應用程式的 [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) 函式會呼叫 **ShowWindow**，並傳遞兩個參數：主視窗的控制碼，以及指定主視窗第一次顯示時是否應最小化或最大化的旗標。 一般來說，旗標可以設定為以 SW 前置詞開頭的任何常數 \_ 。 不過，呼叫 **ShowWindow** 以顯示應用程式的主視窗時，旗標必須設定為 [ **SW \_ SHOWDEFAULT**]。 此旗標會指示系統將視窗顯示為啟動應用程式之程式的指示。

如果已使用 [**RegisterClass**](/windows/win32/api/winuser/nf-winuser-registerclassa)的 unicode 版本註冊視窗類別，則視窗只會收到 unicode 訊息。 若要判斷視窗是否使用 Unicode 字元集，請呼叫 [**IsWindowUnicode**](/windows/win32/api/winuser/nf-winuser-iswindowunicode)。

### <a name="window-creation-messages"></a>Window-Creation 訊息

建立任何視窗時，系統會將訊息傳送至視窗的視窗程式。 系統會在建立視窗的非工作區之後傳送 [**wm \_ NCCREATE**](wm-nccreate.md) 訊息，並在建立工作區之後傳送 [**wm \_ 建立**](wm-create.md) 訊息。 視窗程式會在系統顯示視窗之前，收到這兩個訊息。 這兩個訊息都包含 [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) 結構的指標，其中包含 [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) 函數中指定的所有資訊。 一般而言，視窗程式會在接收這些訊息時執行初始化工作。

建立子視窗時，系統會在傳送 [**wm \_ NCCREATE**](wm-nccreate.md)和 [**WM \_ 建立**](wm-create.md)訊息之後，將 [**wm \_ PARENTNOTIFY**](/previous-versions/windows/desktop/inputmsg/wm-parentnotify)訊息傳送至父視窗。 它也會在建立視窗時傳送其他訊息。 這些訊息的數目和順序取決於視窗類別和樣式，以及用來建立視窗的函數。 這些訊息會在此說明檔的其他主題中說明。

### <a name="multithread-applications"></a>多執行緒應用程式

以 Windows 為基礎的應用程式可以有多個執行緒執行，而且每個執行緒都可以建立視窗。 建立視窗的執行緒必須包含其視窗程式的程式碼。

應用程式可以使用 [**EnumThreadWindows**](/windows/win32/api/winuser/nf-winuser-enumthreadwindows) 函式來列舉特定執行緒所建立的視窗。 此函式會將控制碼傳遞至每個執行緒視窗，然後再傳遞至應用程式定義的回呼函式 [**EnumThreadWndProc**](/previous-versions/windows/desktop/legacy/ms633496(v=vs.85))。

[**GetWindowThreadProcessId**](/windows/win32/api/winuser/nf-winuser-getwindowthreadprocessid)函數會傳回建立特定視窗之執行緒的識別碼。

若要設定另一個執行緒所建立之視窗的顯示狀態，請使用 [**ShowWindowAsync**](/windows/win32/api/winuser/nf-winuser-showwindowasync) 函數。

 

 
