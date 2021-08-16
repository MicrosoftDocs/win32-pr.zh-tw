---
description: 線上說明可以有各式各樣的表單，從詳細的概念資訊到快速定義。 本主題包含下列各節。
title: 處理線上說明
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2a3f6034-6ba6-4204-a2e1-59995fbf40fe
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: caf576d723b27e1c81bb715ea04743740930b5bb257f03eb3ca0a9ab697affd1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118223680"
---
# <a name="handling-online-help"></a>處理線上說明

線上說明可以有各式各樣的表單，從詳細的概念資訊到快速定義。 本主題包含下列各節。

-   [關於說明](#about-help)
    -   [協助要求](#help-requests)
    -   [協助顯示和 Windows 說明](#help-display-and-windows-help)
-   [使用說明](#using-help)
    -   [在對話方塊中提供協助](#providing-help-in-a-dialog-box)
    -   [設定次要說明視窗的外觀](#setting-the-appearance-of-a-secondary-help-window)

## <a name="about-help"></a>關於說明

方便使用的應用程式有一個重要元素，可在線上說明中立即取得。 Windows 提供的函式和訊息，與 Windows 說明應用程式搭配使用時，可讓您輕鬆地在應用程式中執行線上說明。 本總覽討論支援線上說明的 Windows 元素。 它會說明如何使用這些專案來提供使用者要求協助的方法，並說明如何使用 Windows 說明應用程式來顯示說明。

### <a name="help-requests"></a>協助要求

大部分以 Windows 為基礎的應用程式會以各種不同的形式提供線上說明資訊，範圍從概念說明，到說明應用程式功能的快顯說明用途，以提供應用程式使用者介面中個別元素的快速定義。 您可以使用函式和訊息，為使用者提供各種不同的方法來要求存取此資訊。 下列各節將說明這些說明要求。

### <a name="help-menu"></a>說明功能表

大部分的應用程式會在主視窗中包含 [說明 **] 功能表，** 以提供使用者存取說明資訊的許可權。 當使用者從 [說明 **] 功能表選取** 專案時，對應的視窗程式會收到一個可識別所選取專案的 [**WM \_ 命令**](../menurc/wm-command.md) 訊息。 應用程式會藉由顯示適當的說明資訊來回應，例如說明主題清單、索引或應用程式簡介。

### <a name="help-from-the-keyboard"></a>鍵盤上的協助

Windows 可讓使用者在每次使用者按下 F1 鍵時，藉由通知應用程式，從鍵盤提供協助資訊的存取權。 當使用者按下按鍵時，系統會將 [**WM \_**](wm-help.md) 說明訊息傳送至具有鍵盤焦點的視窗。 如果視窗是子視窗 (例如) 對話方塊中的控制項， [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函式會將訊息傳遞至父視窗。 如果按下 F1 時，功能表為使用中狀態，系統會將訊息傳送至與功能表相關聯的視窗。 應用程式會顯示與焦點或作用中的視窗、控制項或功能表相關聯的說明資訊來回應。 例如，如果使用者在對話方塊中選取控制項，並按 F1 鍵，則應用程式會顯示該控制項的說明資訊。

WM 說明的 *lParam* 參數是 [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo)結構的指標，其中包含要求說明之專案的詳細資訊。 [**\_**](wm-help.md) 您可以使用此資訊來決定要顯示的說明主題。 **HELPINFO** 結構也包含使用者按下按鍵時，滑鼠游標的座標。 您可以使用這項資訊，根據滑鼠游標的位置提供說明。

### <a name="help-from-the-mouse"></a>滑鼠的協助

Windows 可讓使用者在按一下問題 (？ ) 按鈕之後，每次使用者按一下滑鼠右鍵，或按一下視窗、控制項或功能表，以存取滑鼠的協助資訊。 應用程式會顯示與指定視窗、控制項或功能表相關聯的說明資訊來回應。

當使用者按一下滑鼠右鍵時，系統會傳送 [**WM \_ CONTEXTMENU**](../menurc/wm-contextmenu.md) 訊息。 按一下的視窗會接收訊息。 如果視窗是子視窗（例如控制項），則 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函式會將訊息傳遞至父視窗。 **WM \_ CONTEXTMENU** 訊息會指定滑鼠游標的座標。 X 座標是在 *lParam* 參數的低序位字組中，而 y 座標則是在高序位字中。 如果使用者按一下控制項， *wParam* 參數就是收到點擊之控制項的控制碼。

當使用者按一下視窗標題列中出現的 [問題 (？] ) 按鈕後，系統會傳送一則 WM 說明訊息， [**\_ 讓**](wm-help.md) 使用者在視窗中按一下某個專案。 建立視窗時，您可以在 [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa)函式中指定 **WS \_ EX \_ CONTEXTHELP** 樣式，以將問題按鈕新增至標題列。 WM 說明的 *lParam* 參數是 [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo)結構的指標，其中包含要求說明之專案的詳細資訊，包括使用者按下滑鼠按鍵時的滑鼠游標座標。 **\_**

建議您只在對話方塊中使用 [問題] 按鈕。 在過去，應用程式會提供對話方塊 **中的 [說明] 按鈕，** 以提供使用者存取對話方塊的協助資訊。 不再建議使用這個方法。 請改用 [問題] 按鈕。

### <a name="help-display-and-windows-help"></a>協助顯示和 Windows 說明

一旦應用程式收到協助的要求，它應該會顯示適當的說明資訊。 由於 Windows Help 應用程式提供一致的使用者介面，因此建議應用程式使用 Windows 的說明，而不是其他方法。 若要指示 Windows 說明來顯示說明資訊，應用程式會使用 [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa)函式，指定詳細資料，例如要顯示的資訊，以及要在其中顯示的視窗表單。 下列各節說明如何使用 **WinHelp** 來顯示說明資訊。

### <a name="help-files"></a>說明檔

若要查看說明資訊，您必須在呼叫 [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) 函數時指定說明檔。 說明檔必須有 Windows 協助 ( .hlp) 檔案格式和一或多個主題。 每個主題都是不同的資訊單位，例如概念描述、一組指示、圖片、詞彙定義等等。 主題必須是唯一的識別，以便 Windows 有助於在要求時找到它們。 就內部而言，Windows 說明會使用主題識別碼來尋找主題，但是應用程式最常使用內容識別碼 (唯一整數值) 來指定要顯示的主題。 說明檔作者必須明確地將內容識別碼對應至 \[ \] 用來建立說明檔之專案檔的 [對應] 區段中的主題識別碼。

當您指定說明檔，但未指定路徑時， [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) 會尋找說明目錄或 path 環境變數所指定之目錄中的說明檔。 此外， **WinHelp** 可以找到名稱列于下列登錄位置的說明檔：

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            Help
```

若要利用登錄，您必須建立與您的說明檔名稱相同的值名稱。 指派給該名稱的值必須是說明檔所在的目錄。

如果 [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) 找不到指定的說明檔，則會顯示一個對話方塊，讓使用者指定說明檔的位置。 因為 **WinHelp** 會將位置資訊儲存在登錄中，所以不會再詢問相同說明檔的位置。

如需有關如何撰寫和建立說明檔的詳細資訊，請參閱您的開發工具所提供的檔。

### <a name="starting-windows-help"></a>開始 Windows 說明

下列範例會使用 [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa)函式來啟動 Windows help 應用程式，並將說明檔開啟至其內容主題。


```
HWND hwnd;     // main window handle 
BOOL bResult   // for checking Boolean function result 

bResult = WinHelp(hWnd, "WINNT.HLP", HELP_CONTENTS, 0L);
```



下一個範例會開啟使用者說明檔、在檔案中搜尋與關鍵字字串相關聯的主題，然後顯示主題。


```
HWND hwnd;     // main window handle 
BOOL bResult   // for checking Boolean function result 

bResult = WinHelp(hWnd, "WINNT.HLP", HELP_KEY, (DWORD) "finding topics");
```



### <a name="help-topics-dialog-box"></a>說明主題對話方塊

您可以使用 **help \_ FINDER** 命令呼叫 [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa)函式來顯示 [**說明主題**] 對話方塊。 [ **說明主題** ] 對話方塊可讓使用者藉由查看主題的標題、與主題相關聯的關鍵字，或主題中找到的單字和片語，來選取要顯示的主題。 當使用者選擇 [說明] 功能表中的命令（例如說明主題）時，應用程式通常會顯示此對話方塊。 如果應用程式中沒有特定的視窗、控制項或功能表具有焦點或作用中，應用程式也可能會顯示此對話方塊。

在過去，應用程式已使用「說明」 **\_ 內容** 和「 **協助」 \_ 索引** 命令搭配 [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) 函式來顯示「內容」主題和說明檔的關鍵字索引。 不再建議使用這些命令。 請改用 **HELP \_ FINDER** 命令。

### <a name="information-topics"></a>資訊主題

您可以使用 HELP CONTEXT 命令呼叫 [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) 函式 \_ ，並指定主題的內容識別碼，來顯示特定主題。 應用程式通常會使用說明 \_ 內容命令來回應使用者對於包含概念性資訊或程式說明的主題，而不是特定控制項或功能表的相關資訊。 在這種情況下，使用者可能會在返回應用程式之前，繼續流覽說明檔尋找相關資訊。

help \_ CONTEXT 命令會叫用 Windows 說明的一般實例，讓使用者能夠尋找說明檔中的其他主題。 它通常會顯示主要的 [說明] 視窗，其中包含標題列、系統功能表、最小化和最大化按鈕、主功能表、選擇性巡覽列、調整大小框線和工作區。 所選主題的文字會出現在工作區中，使用者可以使用主視窗中的 [熱連結] 或 [流覽] 按鈕，流覽說明檔。 Windows 說明的一般實例也可以用來顯示一或多個次要視窗中的說明，而不是主視窗。

### <a name="pop-up-topics"></a>彈出主題

您可以使用 HELP [](/windows/desktop/api/Winuser/nf-winuser-winhelpa) \_ WM \_ help 或 Help CONTEXTMENU 命令呼叫 WinHelp 函式，來顯示包含特定控制項或功能表資訊的彈出主題 \_ 。 這些命令會在相對應的控制項或功能表附近的快顯視窗中顯示主題。 為了讓使用者在應用程式中立即返回工作，當使用者按下按鍵或按下滑鼠左鍵時，快顯視窗就會立即終結。

\_ \_ 當您處理適用于控制項視窗的 [**WM 說明 \_**](wm-help.md)訊息時，請使用 help WM help 命令。 因為大部分的控制項都會將 WM 說明訊息傳遞至 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)函式，所以對應的對話方塊程式 (或父視窗程式) 處理此訊息。 **\_** 對話方塊程式必須將控制項的陣列和內容識別碼組傳遞給 [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) ，以及 [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo)結構的 **hItemHandle** 成員中指定的控制控制碼，而不是提供特定的內容識別碼。 **\_** 函式會判斷已產生 **WM \_** 說明訊息之控制項的識別碼，並使用相符的內容識別碼來顯示適當的主題。

\_處理 [**WM \_ CONTEXTMENU**](../menurc/wm-contextmenu.md)訊息時，請使用 HELP CONTEXTMENU 命令。 因為大部分的控制項都會將 **WM \_ CONTEXTMENU** 訊息傳遞至 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函式，所以對應的對話方塊程式 (或父視窗程式) 處理此訊息。 此程式會指定控制項的陣列和內容識別碼組;它也會在呼叫 [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa)時指定 *wParam* 參數中的控制碼，讓函式可以從陣列中挑選適當的內容識別碼，並顯示適當的主題。 不同于 HELP \_ WM \_ help 命令，help \_ CONTEXTMENU 會先在功能表中顯示 [ **這是什麼？** ] 命令。 如果使用者選擇命令， **WinHelp** 會顯示主題。 否則，就會取消要求。

您也可以使用 HELP \_ CONTEXTPOPUP 命令，並指定主題的內容識別碼，以顯示快捷方式主題。 此命令類似于 help \_ CONTEXT 命令，但會叫用 help \_ WM help \_ 和 help CONTEXTMENU 所使用 Windows 說明的快顯實例 \_ 。 應用程式可以使用此命令來回應 [**WM \_**](wm-help.md) 說明訊息，以顯示在對話方塊中不是控制項的功能表和視窗的說明。 若要最有效地使用此命令，應用程式應該將內容識別碼指派給這些功能表和視窗。

您可以將內容識別碼指派給應用程式中的任何視窗或功能表。 當產生 [**wm \_**](wm-help.md) 說明訊息時，系統會在 [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) 結構中包含內容識別碼，該結構會傳遞至 **WM \_** 說明訊息中的父視窗。 父視窗接著可以將內容識別碼傳遞給 [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) ，以顯示要求的說明主題。

您可以使用 [**SetWindowCoNtextHelpId**](/windows/desktop/api/Winuser/nf-winuser-setwindowcontexthelpid) 函式，將內容識別碼指派給視窗或控制項，並使用 [**SetMenuCoNtextHelpId**](/windows/desktop/api/Winuser/nf-winuser-setmenucontexthelpid) 函式將內容識別碼指派給功能表。 您可以使用 [**GetWindowCoNtextHelpId**](/windows/desktop/api/Winuser/nf-winuser-getwindowcontexthelpid) 或 [**GetMenuCoNtextHelpId**](/windows/desktop/api/Winuser/nf-winuser-getmenucontexthelpid) 函式，來取得視窗或功能表的內容識別碼。

### <a name="keyword-searches"></a>關鍵字搜尋

您可以藉由將關鍵字指派給說明檔中的主題，讓使用者尋找和查看主題。 關鍵字只是與一或多個主題相關聯的字串。 Windows[說明] 會收集說明檔中的所有關鍵詞，將它們放在資料表中，並顯示在 [**說明主題**] 對話方塊的 [索引] 清單中。 當使用者選取關鍵字時，Windows 說明] 會顯示相關聯的說明主題，或者，如果有一個以上的主題與關鍵字相關聯，則會顯示使用者可以選擇的主題清單。

在應用程式中，您可以使用 HELP \_ 鍵、help \_ PARTIALKEY 或 help \_ MULTIKEY 命令搭配 [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) 函式，根據整個或部分關鍵字來搜尋和顯示說明主題。 您可以指定命令、關鍵字字串、說明檔，以及主控視窗的控制碼。 在所有情況下，如果找到單一相符項， **WinHelp** 會顯示對應的主題。 如果找到多個相符的函式，此函式會顯示 [找到的主題] 對話方塊，而使用者可以選擇要查看的主題。 如果找不到相符項， **WinHelp** 會顯示 [說明] 索引鍵的索引清單 (以及 [說明] \_ \_ PARTIALKEY) 或顯示錯誤訊息 ([說明 \_ MULTIKEY) ]。

您的應用程式可以 [**藉由使用**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) 分號分隔關鍵字，在單一呼叫中搜尋多個關鍵字。  (針對 Windows 第3版所建立的說明檔，不支援搜尋多個關鍵字。*x*) 它也可以在多個說明檔中搜尋關鍵字。如果指定的說明檔具有包含： Index 或： Link 命令的 ( cnt) 檔案的內容。 使用 HELP \_ KEY 命令， **WinHelp** 會在這些命令指定的所有檔案中搜尋關鍵字。 透過 [說明] MULTIKEY 和 [說明] \_ \_ PARTIALKEY 命令，此函式會搜尋除了： Link 命令指定的所有檔案。

根據預設，Windows 有助於辨識說明來源檔案中的 K 註腳字元所識別的關鍵字表。 您可以藉由在說明來源檔案中新增 K 以外的註腳字元（含關鍵字定義）來指示 Windows 協助建立額外的關鍵字表。 不過 (註腳字元 A 是保留的。 ) 您必須在建立說明檔時，于專案檔的 [選項] 區段中使用 MULTIKEY 語句，以定義任何其他關鍵字資料表 \[ \] 。

應用程式可以使用 HELP \_ SETINDEX 命令搭配 [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa)函數來指示 Windows 說明，以在其索引清單中顯示 K 以外的關鍵字資料表。 若要指示 Windows 協助搜尋替代關鍵字表中的關鍵字，應用程式可以使用 Help \_ MULTIKEY 命令。 您可以在 [**MULTIKEYHELP**](/windows/win32/api/winuser/ns-winuser-multikeyhelpa) 結構中指定關鍵字和關鍵字表，並將它傳遞給 **WinHelp**。

當 [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) 顯示主題時，它會在主題的 ">" 註腳所指定的視窗中，顯示在內容檔案的： Base 命令所指定的視窗中，或在主視窗中。 如果當您呼叫 **WinHelp** 時，主視窗已經開啟至不同的說明檔，則函式會在搜尋時隱藏主視窗。 在此情況下，請取消 [ **找到的主題** ] 和 [ **說明主題** ] 對話方塊關閉主視窗。

### <a name="secondary-help-windows"></a>次要說明視窗

Windows 輔助應用程式的主視窗稱為主視窗。 Windows說明也可以在次要視窗中顯示說明主題。 不同于主要說明視窗，次要視窗不包含功能表列。 您可以在次要視窗中包含巡覽列，也可以將按鈕加入至橫條。 您也可以選擇讓 Windows 協助自動調整次要視窗的高度，以配合主題。

您必須在說明專案檔的 [windows] 區段中定義次要視窗 \[ \] ，以提供每個視窗的名稱和選擇性的初始大小和位置。 您可以指示 Windows 的輔助應用程式在次要視窗中顯示主題，方法是將角括弧附加 (>) ，並將您為次要視窗定義的名稱附加至說明檔的名稱。 產生的字串接著會傳遞至 [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) 函數。

應用程式可以變更主要或次要視窗的大小和位置，方法是在 WinHelp 的呼叫中指定 [**HELPWININFO**](/windows/win32/api/winuser/ns-winuser-helpwininfoa)結構的位址和 HELP \_ SETWINPOS 命令。 [](/windows/desktop/api/Winuser/nf-winuser-winhelpa) **HELPWININFO** 指定視窗的名稱，以及其新的大小和位置。

### <a name="training-card-help"></a>訓練卡說明

使用「智慧卡說明」時，應用程式可以顯示一連串的指示，引導使用者完成工作的步驟。 訓練卡通常包含說明與 TCard 宏相關聯之特定步驟和按鈕的文字，可讓使用者告訴應用程式接下來該怎麼做。 定型卡只能顯示在次要視窗中，而且不能包含說明檔中其他主題的熱連結。

應用程式會藉由呼叫 [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa)函式並指定 help \_ TCARD 命令與其他命令（例如說明內容），來起始 Windows 說明的定型卡實例 \_ 。 接著，當使用者按一下訓練卡中的按鈕時，按一下指派給 TCard 宏的作用點，或關閉訓練卡，Windows 可將一則 [**\_ TCard**](wm-tcard.md)訊息傳送給應用程式，以協助通知應用程式。 *WParam* 參數會識別按鈕或使用者動作，而 *lParam* 參數會包含其他資料，其意義取決於 *wParam* 的值。

### <a name="canceling-help"></a>取消說明

Windows[說明] 需要應用程式明確取消說明，讓它可以釋放用來追蹤應用程式及其說明檔的任何資源。 應用程式可以隨時呼叫 [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) 函式並指定 HELP QUIT 命令，來進行這項作業 \_ 。 請注意，Windows 說明的快顯實例並不適用。 應用程式不應該嘗試關閉快顯視窗實例。

如果應用程式已對 [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa)進行任何呼叫，它必須在關閉其主視窗之前先取消說明 (例如，以回應 \_ 主視窗程式) 中的 WM 終結訊息。 應用程式只需要呼叫一次 **WinHelp** 即可取消說明，無論它已開啟多少說明檔。 Windows在所有應用程式或 Dll 都已取消說明之前，[說明] 會保持執行狀態。

若要關閉 Windows 說明的訓練卡實例，您必須同時指定 [說明 TCARD] 和 [說明]，以便在 \_ \_ 呼叫 [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa)時結束命令。 如果使用者先將其取消，則應用程式不需要取消 Windows 協助的訓練卡實例。 Windows當使用者藉由將 *wParam* 參數設定為 IDCLOSE 的 [**WM \_ TCARD**](wm-tcard.md)訊息傳送給您，以協助通知應用程式。

## <a name="using-help"></a>使用說明

本節說明如何為對話方塊提供即時線上說明，以及如何設定次要說明視窗的外觀。

-   [在對話方塊中提供協助](#providing-help-in-a-dialog-box)
-   [設定次要說明視窗的外觀](#setting-the-appearance-of-a-secondary-help-window)

### <a name="providing-help-in-a-dialog-box"></a>在對話方塊中提供協助

若要在對話方塊中提供即時線上說明，您必須建立由 **DWORD** 值配對所組成的陣列。 每一組中的第一個值都是對話方塊中控制項的識別碼，而第二個值則是控制項之說明主題的內容識別碼。 陣列應該在對話方塊中包含每個控制項的一對識別碼。

對話方塊程式必須處理 [**wm \_**](wm-help.md) 說明和 [**wm \_ CONTEXTMENU**](../menurc/wm-contextmenu.md) 訊息。 當使用者按一下滑鼠右鍵時，對話方塊程式會收到 Wm 說明，當使用者按下按鍵和 **WM \_ CONTEXTMENU** 時。 **\_**

WM 說明的 *lParam* 參數包含 [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo)結構的位址。 [**\_**](wm-help.md) 此結構的 **hItemHandle** 成員會識別使用者已要求協助的控制項。 您必須將這個控制碼傳遞給 [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) 函式，以及 help \_ WM \_ help 命令、說明檔的名稱，以及識別碼陣列的指標。 **WinHelp** 函式會在陣列中搜尋指定控制項的控制項識別碼，然後取得對應的說明內容識別碼。 接下來，此函式會將說明內容識別碼傳遞至 Windows 說明，這會尋找對應的主題，並將其顯示在快顯視窗中。 如果控制項有-1 的識別碼，系統會搜尋下一個控制項，此控制項是 tab 鍵停止，然後使用它的識別碼來尋找說明內容識別碼。 基於這個理由，請務必將靜態文字放在資源檔中的控制項之前。

呼叫 [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) 函式時，處理 [**wm \_ CONTEXTMENU**](../menurc/wm-contextmenu.md) 類似于處理具有下列兩個例外狀況的 [**wm \_**](wm-help.md) 說明：

-   您可以從 [**WM \_ CONTEXTMENU**](../menurc/wm-contextmenu.md)傳遞 *wParam* 參數，這是傳送訊息之控制項的控制碼。
-   您可以指定 **help \_ CONTEXTMENU** 命令，而不是 **help \_ WM \_ help**。

**help \_ CONTEXTMENU** 命令會在顯示 [說明] 主題之前，讓 Windows 說明來顯示功能表。 此功能表為系統定義。 它可讓使用者顯示控制項的說明，或顯示 [ **說明主題** ] 對話方塊。

下列範例顯示如何在對話方塊中執行即時線上說明。


```
LRESULT CALLBACK EditDlgProc(HWND hwndDlg, UINT uMsg, 
                             WPARAM wParam, LPARAM lParam) 
{ 
    // Create an array of control identifiers and context identifiers. 
    static DWORD aIds[ ] = 
    { 
        ID_SAVE,   IDH_SAVE, 
        ID_DELETE, IDH_DELETE, 
        ID_COPY,   IDH_COPY, 
        ID_PASTE,  IDH_PASTE, 
        0,0 
    }; 

    switch (uMsg) 
    { 
        case WM_HELP: 
            WinHelp(((LPHELPINFO)lParam)->hItemHandle, "helpfile.hlp", 
                    HELP_WM_HELP, (DWORD)(LPSTR)aIds); 
            break; 

        case WM_CONTEXTMENU: 
            WinHelp((HWND)wParam, "helpfile.hlp", HELP_CONTEXTMENU, 
                    (DWORD)(LPVOID)aIds); 
            break; 
        
        // Process other messages here. 
    } 
    return FALSE; 
}
```



### <a name="setting-the-appearance-of-a-secondary-help-window"></a>設定次要說明視窗的外觀

應用程式可以藉由將說明 \_ SETWINPOS 命令和 [**HELPWININFO**](/windows/win32/api/winuser/ns-winuser-helpwininfoa) 結構的位址傳遞至 [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) 函數，來設定次要說明視窗的大小、位置和顯示狀態。 **HELPWININFO** 的成員會指定要變更的視窗名稱，以及視窗的新大小、位置和顯示狀態。

下列範例會設定名為 "wnd<> menu" 的次要視窗外觀 \_ 。 您必須在說明專案檔的 [WINDOWS] 區段中定義該名稱 \[ \] 。


```
BOOL DoWindowSize(VOID) 
{ 
    HANDLE hhwi; 
    LPHELPWININFO lphwi; 
    WORD wSize; 
    char *szWndName = "wnd_menu"; 
    size_t NameLength;      // Does not include the terminating null character
    HRESULT hr
    BOOL retval;

    hr = StringCbLengthA(szWndName, STRSAFE_MAX_CCH, &NameLength);
    
    if (SUCCEEDED(hr))
    {
        // Add 1 to account for the name string's terminating null character.
        NameLength++;
        
        // The HELPWININFO structure contains a minimal TCHAR array of size [2] 
        // that is used for the window name. Since sizeof(HELPWININFO) 
        // includes those two TCHARS, they must be subtracted from the 
        // total when adding the actual string length to calculate the  
        // size of the structure. 
        wSize = sizeof(HELPWININFO) - 2 + NameLength; 
    }
    else
        // Something's amiss with the string.
        return FALSE;
        
    hhwi  = GlobalAlloc(GHND, wSize); 
    lphwi = (LPHELPWININFO)GlobalLock(hhwi); 

    lphwi->wStructSize = wSize; 
    lphwi->x    = 256;      // horizontal position 
    lphwi->y    = 256;      // vertical position 
    lphwi->dx   = 767;      // width 
    lphwi->dy   = 512;      // height 
    lphwi->wMax = SW_SHOW;  // show the window 
    
    // secondary window
    hr = StringCbCopyA(lphwi->rgchMember, sizeof(lphwi->rgchMember), szWndName);
    
    if (SUCCEEDED(hr))
    {
        WinHelp(hwnd, "myhelp.hlp", HELP_SETWINPOS, (DWORD)lphwi); 
     
        GlobalUnlock(hhwi); 
        GlobalFree(hhwi); 

        return TRUE; 
    }
    else
        // There was a problem copying the window name.
        return FALSE;
}
```



 

 
