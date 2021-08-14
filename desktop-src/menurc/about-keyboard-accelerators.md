---
title: 關於鍵盤加速器
description: 本主題討論鍵盤加速器。
ms.assetid: cbf7619d-289d-40c9-9a06-6ce47026d43f
keywords:
- Windows消費者介面，使用者輸入
- Windows消費者介面，鍵盤快速鍵
- 使用者輸入，鍵盤快速鍵
- 捕獲使用者輸入，鍵盤快捷
- 鍵盤加速器
- 加速器
- WM_COMMAND 訊息
- WM_SYS 命令訊息
- 快速鍵對應表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b81240feb0ca21028c9d1813f4c8004e1c3bb932fe1ec8767e3719c26e7a5db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117870727"
---
# <a name="about-keyboard-accelerators"></a>關於鍵盤加速器

快速鍵與功能表緊密相關，可讓使用者存取應用程式的命令集。 一般而言，使用者會依賴應用程式的功能表來學習命令集，然後切換到使用加速器，因為它們對應用程式更熟練。 加速器可提供比功能表更快、更直接的命令存取。 應用程式至少應該提供更常用命令的快速鍵。 雖然加速器通常會產生以功能表項目形式存在的命令，但是它們也可以產生沒有對等功能表項目的命令。

本節涵蓋下列主題。

-   [快速鍵對應表](#accelerator-tables)
-   [快速鍵-資料表建立](#accelerator-table-creation)
-   [快速鍵按鍵指派](#accelerator-keystroke-assignments)
-   [加速器和功能表](#accelerators-and-menus)
-   [UI 狀態](#ui-state)

## <a name="accelerator-tables"></a>快速鍵對應表

快速鍵對應表包含 [**ACCEL**](/windows/win32/api/winuser/ns-winuser-accel) 結構的陣列，每一個都定義個別的快速鍵。 每個 **ACCEL** 結構都包含下列資訊：

-   快速鍵的按鍵組合。
-   快速鍵的識別碼。
-   各種旗標。 這包括一個指定系統是否要在使用快速鍵時，反白顯示對應的功能表項目（如果有的話），以提供視覺效果的意見反應

若要處理指定之執行緒的快速鍵按鍵，開發人員必須在與執行緒訊息佇列相關聯的訊息迴圈中呼叫 [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) 函數。 **TranslateAccelerator** 函式會監視對訊息佇列的鍵盤輸入，檢查是否有符合快速鍵對應表中專案的按鍵組合。 當 **TranslateAccelerator** 找到符合的結果時，它會將鍵盤輸入轉譯 (也就是， [**Wm \_ KEYUP**](/windows/desktop/inputdev/wm-keyup) 和 [**wm \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown) 訊息) 至 [**WM \_ 命令**](wm-command.md) 或 [**wm \_ SYSCOMMAND**](wm-syscommand.md) 訊息，然後將訊息傳送至指定視窗的視窗程式。 下圖顯示加速器的處理方式。

![鍵盤加速器處理模型](images/cskac-01.png)

[**WM \_ 命令**](wm-command.md)訊息包含造成 [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora)產生訊息之快速鍵的識別碼。 視窗程式會檢查識別碼，以判斷訊息的來源，然後據以處理訊息。

快速鍵對應表存在於兩個不同的層級。 系統會維護適用于所有應用程式的單一全系統快速鍵對應表。 應用程式無法修改系統加速器表格。 如需系統加速器資料表所提供之快速鍵的描述，請參閱 [快速鍵按鍵指派](#accelerator-keystroke-assignments)。

系統也會維護每個應用程式的快速鍵對應表。 應用程式可以定義任何數目的快速鍵對應表，以搭配自己的視窗使用。 唯一的32位控制碼 (**HACCEL**) 識別每個資料表。 不過，指定的執行緒一次只能有一個使用中的快速鍵對應表。 傳遞至 [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) 函式之快速鍵對應表的控制碼，會決定執行緒使用中的快速鍵對應表。 您可以隨時將不同的快速鍵表格控制碼傳遞至 **TranslateAccelerator**，以變更使用中的快速鍵對應表。

## <a name="accelerator-table-creation"></a>Accelerator-Table 建立

若要建立應用程式的快速鍵對應表，必須執行幾個步驟。 首先，資源編譯器會用來建立快速鍵對應表資源，並將它們加入至應用程式的可執行檔。 在執行時間， [**LoadAccelerators**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa) 函數是用來將快速鍵對應表載入至記憶體，並取得快速鍵對應表的控制碼。 這個控制碼會傳遞至 [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) 函式，以啟動快速鍵對應表。

您也可以在執行時間為應用程式建立快速鍵對應表，方法是將 [**ACCEL**](/windows/win32/api/winuser/ns-winuser-accel) 結構的陣列傳遞至 [**CreateAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-createacceleratortablea) 函數。 這個方法支援應用程式中的使用者定義加速器。 如同 [**LoadAccelerators**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa) 函式， **CreateAcceleratorTable** 會傳回可傳遞至 [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) 以啟動快速鍵對應表的快速鍵對應表控制碼。

系統會自動終結 [**LoadAccelerators**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa) 所載入或由 [**CreateAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-createacceleratortablea)所建立的快速鍵對應表。 不過，應用程式可以藉由呼叫 [**DestroyAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-destroyacceleratortable) 函式終結快速鍵對應表來釋出正在執行的資源。

您可以複製和修改現有的快速鍵對應表。 您可以使用 [**CopyAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-copyacceleratortablea) 函數來複製現有的快速鍵對應表。 在修改複製之後，藉由呼叫 [**CreateAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-createacceleratortablea)來取出新快速鍵對應表的控制碼。 最後，會將控制碼傳遞至 [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) ，以啟動新的資料表。

## <a name="accelerator-keystroke-assignments"></a>快速鍵按鍵指派

您可以使用 ASCII 字元碼或虛擬金鑰程式碼來定義加速器。 ASCII 字元碼可讓加速器區分大小寫。 因此，使用 ASCII "C" 字元將加速器定義為 ALT + C 而不是 ALT + c。 不過，區分大小寫的加速器可能會令人困惑。 例如，如果 CAPS LOCK 機碼關閉或 SHIFT 鍵已關閉，則會產生 ALT + C 加速器，但如果兩者都關閉，則不會產生。

一般而言，加速器不需要區分大小寫，因此大部分的應用程式會使用加速器的虛擬金鑰程式碼，而不是 ASCII 字元碼。

請避免與應用程式功能表助憶鍵衝突的加速器，因為加速器會覆寫助憶鍵，而這可能會讓使用者混淆。 如需功能表助憶鍵的詳細資訊，請參閱 [功能表](menus.md)。

如果應用程式定義的加速器也定義于系統加速器資料表中，則應用程式定義的加速器會覆寫系統加速器，但只會在應用程式的內容中。 不過，請避免這種作法，因為它會防止系統加速器在使用者介面中執行其標準角色。 下列清單描述整個系統的加速器：



| 加速器                 | Description                                                                                                      |
|------------------|-------------------------------------------------------------------------------------------------------|
| ALT+ESC          | 切換至下一個應用程式。                                                                     |
| ALT+F4           | 關閉應用程式或視窗。                                                                    |
| ALT+連字號       | 開啟文件視窗的 [ **視窗]** 功能表。                                                      |
| ALT + PRINT SCREEN | 將使用中視窗中的影像複製到剪貼簿。                                              |
| ALT 鍵 + 空格鍵     | 開啟應用程式主視窗的 [ **視窗]** 功能表。                                          |
| ALT+TAB          | 切換至下一個應用程式。                                                                     |
| Ctrl+Esc         | 切換至 [ **開始** ] 功能表。                                                                       |
| CTRL+F4          | 關閉使用中的群組或文件視窗。                                                           |
| F1               | 啟動應用程式的說明檔（如果有的話）。                                                    |
| 列印畫面     | 將畫面上的影像複製到剪貼簿。                                                     |
| SHIFT + ALT + TAB    | 切換至先前的應用程式。 使用者必須在按下 TAB 鍵時按住 ALT + SHIFT。 |



 

## <a name="accelerators-and-menus"></a>加速器和功能表

使用快速鍵與選擇功能表項目相同：兩個動作都會導致系統將 [**wm \_ 命令**](wm-command.md) 或 [**wm \_ SYSCOMMAND**](wm-syscommand.md) 訊息傳送至對應的視窗程式。 **WM \_ 命令** 訊息包含一個識別碼，可讓視窗程式檢查以判斷訊息的來源。 如果加速器產生了 **WM \_ 命令** 訊息，則識別碼是快速鍵的識別碼。 同樣地，如果功能表項目產生了 **WM \_ 命令** 訊息，則識別碼會是功能表項目的識別碼。 因為加速器提供從功能表中選擇命令的快捷方式，所以應用程式通常會將相同的識別碼指派給快速鍵和對應的功能表項目。

應用程式會以與對應的功能表項目 **wm \_ 命令** 訊息完全相同的方式來處理加速器 [**WM \_ 命令**](wm-command.md)訊息。 不過， **WM \_ 命令** 訊息包含旗標，可指定訊息是否源自于快速鍵或功能表項目，以因應快速鍵的處理方式與對應的功能表項目不同。 [**WM \_ SYSCOMMAND**](wm-syscommand.md)訊息未包含此旗標。

此識別碼會判斷加速器是否會產生 [**wm \_ 命令**](wm-command.md) 或 [**wm \_ SYSCOMMAND**](wm-syscommand.md) 訊息。 如果識別碼的值與 [系統] 功能表中的功能表項目相同，則加速器會產生 **WM \_ SYSCOMMAND** 訊息。 否則，加速器會產生 **WM \_ 命令** 訊息。

如果快速鍵具有與功能表項目相同的識別碼，且功能表項目為灰色或停用，則會停用加速器，而且不會產生 [**wm \_ 命令**](wm-command.md) 或 [**wm \_ SYSCOMMAND**](wm-syscommand.md) 訊息。 此外，如果對應的視窗最小化，則加速器不會產生命令訊息。

當使用者使用對應至功能表項目的快速鍵時，視窗程式會收到 [**wm \_ INITMENU**](wm-initmenu.md) 和 [**wm \_ INITMENUPOPUP**](wm-initmenupopup.md) 訊息，如同使用者選取功能表項目一樣。 如需如何處理這些訊息的詳細資訊，請參閱 [功能表](menus.md)。

對應至功能表項目的快速鍵應該包含在功能表項目的文字中。

## <a name="ui-state"></a>UI 狀態

Windows 可讓應用程式隱藏或顯示其 UI 中的各種功能。 這些設定稱為 UI 狀態。 UI 狀態包含下列設定：

-   焦點指標 (例如按鈕上的焦點矩形) 
-   鍵盤快速鍵 (以控制項標籤中的底線來表示) 

視窗可以傳送訊息來要求 UI 狀態的變更、可以查詢 UI 狀態，或強制執行其子視窗的特定狀態。 這些訊息如下所示。



| 訊息                                       | 描述                                |
|-----------------------------------------------|--------------------------------------------|
| [**WM \_ CHANGEUISTATE**](wm-changeuistate.md) | 指出 UI 狀態應變更。 |
| [**WM \_ QUERYUISTATE**](wm-queryuistate.md)   | 抓取視窗的 UI 狀態。       |
| [**WM \_ UPDATEUISTATE**](wm-updateuistate.md) | 變更 UI 狀態。                      |



 

依預設，最上層視窗的所有子視窗都會以與其父系相同的 UI 狀態來建立。

系統會處理對話方塊中控制項的 UI 狀態。 在建立對話方塊時，系統會據以初始化 UI 狀態。 所有子控制項都會繼承此狀態。 建立對話方塊之後，系統會監視使用者的擊鍵。 如果 UI 狀態設定是隱藏的，且使用者使用鍵盤流覽，系統會更新 UI 狀態。 例如，如果使用者按下 Tab 鍵將焦點移至下一個控制項，系統就會呼叫 [**WM \_ CHANGEUISTATE**](wm-changeuistate.md) ，讓焦點指標變成可見。 如果使用者按下 ALT 鍵，系統就會呼叫 **WM \_ CHANGEUISTATE** 來顯示鍵盤快捷視窗。

如果控制項支援在其所包含的 UI 元素之間進行導覽，則可以更新它自己的 UI 狀態。 控制項可以呼叫 [**WM \_ QUERYUISTATE**](wm-queryuistate.md) 來取出和快取初始的 UI 狀態。 每當控制項收到 [**wm \_ UPDATEUISTATE**](wm-updateuistate.md) 訊息時，它就可以更新其 UI 狀態，並將 [**WM \_ CHANGEUISTATE**](wm-changeuistate.md) 訊息傳送到其父系。 每個視窗會繼續將訊息傳送到其父系，直到到達最上層視窗為止。 最上層視窗會將 **WM \_ UPDATEUISTATE** 訊息傳送至視窗樹狀結構中的視窗。 如果視窗未通過 **WM \_ CHANGEUISTATE** 訊息，它就不會到達最上層視窗，也不會更新 UI 狀態。

 

 