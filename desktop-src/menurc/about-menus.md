---
title: 關於功能表
description: 本主題討論功能表。
ms.assetid: fd0b26f1-93cd-421b-9097-8502ab7681e9
keywords:
- 資源、功能表
- 功能表，關於
- 分
- 功能表列
- 最上層功能表
- 快顯功能表
- 下拉式功能表
- 功能表、最上層
- 功能表、快顯視窗
- 功能表、下拉式清單
- 功能表名稱
- 功能表、快捷方式
- 功能表、視窗
- 功能表、系統
- 功能表、控制項
- 捷徑功能表
- 視窗功能表
- 系統功能表
- 控制功能表
- 說明識別碼
- 功能表控點
- 功能表項目
- 命令專案
- 功能表項目識別碼
- 功能表項目位置
- 選取功能表項目
- 清除功能表項目
- 擁有者繪製功能表
- 功能表，已繪製的擁有者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34d35ddf55ad31ed27cc12c6adffa5517e0081db6d70b4d01d3b88780a8797bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034488"
---
# <a name="about-menus"></a>關於功能表

*功能表* 是指定選項或選項群組的專案清單， (應用程式的子功能表) 。 按一下功能表項目會開啟子功能表，或讓應用程式執行命令。 本節提供下列主題的相關資訊：

-   [功能表列和功能表](#menu-bars-and-menus)
    -   [快速鍵功能表](#shortcut-menus)
    -   [視窗功能表](#the-window-menu)
    -   [說明識別碼](#help-identifier)
-   [鍵盤存取功能表](#keyboard-access-to-menus)
    -   [標準鍵盤介面](#standard-keyboard-interface)
    -   [功能表存取金鑰](#menu-access-keys)
    -   [功能表快速鍵](#menu-shortcut-keys)
-   [功能表建立](#menu-creation)
    -   [功能表範本資源](#menu-template-resources)
    -   [記憶體中的功能表範本](#menu-template-in-memory)
    -   [功能表控點](#menu-handles)
    -   [功能表建立功能](#menu-creation-functions)
    -   [功能表顯示](#menu-display)
    -   [視窗類別功能表](#window-class-menus)
-   [功能表項目](#menu-items)
    -   [開啟子功能表的命令專案和專案](#command-items-and-items-that-open-submenus)
    -   [功能表項目識別碼](#menu-item-identifier)
    -   [功能表項目位置](#menu-item-position)
    -   [以程式設計方式存取功能表項目](#accessing-menu-items-programmatically)
    -   [預設功能表項目](#default-menu-items)
    -   [選取和清除功能表項目](#selected-and-clear-menu-items)
    -   [啟用、灰色和停用的功能表項目](#enabled-grayed-and-disabled-menu-items)
    -   [反白顯示的功能表項目](#highlighted-menu-items)
    -   [擁有者繪製的功能表項目](#owner-drawn-menu-items)
    -   [功能表項目分隔符號和分行符號號](#menu-item-separators-and-line-breaks)
-   [搭配功能表使用的訊息](#messages-used-with-menus)
-   [功能表損毀](#menu-destruction)

## <a name="menu-bars-and-menus"></a>功能表列和功能表

功能表會排列在階層中。 階層的最上層是 *功能表列*;其中包含功能表的清單，這些 *功能表* 中也可以包含 *子* 功能表。 功能表列有時候稱為 *最上層功能表*，功能表和子功能表也稱為 *快捷* 功能表。

功能表項目可以執行命令或開啟子功能表。 執行命令的專案稱為 *命令專案* 或 *命令*。

功能表列上的專案幾乎一律會開啟功能表。 功能表列很少包含命令專案。 從功能表列開啟的功能表會從功能表列下拉，有時也稱為 *下拉式功能表*。 出現下拉式功能表時，它會附加至功能表列。 功能表列上開啟下拉式功能表的功能表項目也稱為 *功能表名稱*。

功能表列上的功能表名稱代表應用程式所提供的主要命令類別。 從功能表列選取功能表名稱通常會開啟功能表，其功能表項目對應至類別中的命令。 例如，當使用者按下功能表列時，可能會包含 [檔案 **] 功能表名稱** ，並以功能表項目（例如 [ **新增**]、[ **開啟**] 和 [ **儲存**]）來啟用功能表。 若要取得功能表列的相關資訊，請呼叫 [**GetMenuBarInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenubarinfo)。

只有重迭或快顯視窗可以包含功能表列;子視窗不可包含一個。 如果視窗有標題列，系統就會將功能表列放在其下方。 功能表列一律可見。 不過，在使用者選取啟動它的功能表項目之前，並不會顯示子功能表。 如需重迭和快顯視窗的詳細資訊，請參閱 [視窗類型](/windows/desktop/winmsg/window-features)。

每個功能表都必須有擁有者視窗。 當使用者選取功能表或從功能表中選擇專案時，系統會將訊息傳送至功能表的擁有者視窗。

本節將討論下列主題。

-   [快速鍵功能表](#shortcut-menus)
-   [視窗功能表](#the-window-menu)
-   [說明識別碼](#help-identifier)

### <a name="shortcut-menus"></a>快顯功能表

系統也會提供 *快捷方式功能表*。 快捷方式功能表未附加至功能表列;它可以出現在螢幕上的任何位置。 應用程式通常會建立快捷方式功能表與視窗的一部分（例如，工作區）或特定物件（例如圖示）的關聯。 基於這個理由，這些功能表也稱為 *快顯功能表*。

在使用者啟動之前，快捷方式功能表會保持隱藏狀態，通常是以滑鼠右鍵按一下選取範圍、工具列或工作列按鈕。 功能表通常會顯示在插入號或滑鼠游標的位置。

### <a name="the-window-menu"></a>視窗功能表

[ **視窗]** 功能表 (也稱為 [ **系統** ] 功能表或 [ **控制** ] 功能表) 是由作業系統所定義和管理的快顯功能表。 使用者可以按一下標題列上的 [應用程式] 圖示，或是以滑鼠右鍵按一下標題列上的任何位置，來開啟 [視窗] 功能表。

[ **視窗]** 功能表提供一組標準的功能表項目，讓使用者可以選擇變更視窗的大小或位置，或關閉應用程式。 您可以新增、刪除及修改 [視窗] 功能表上的專案，但大部分的應用程式只會使用一組標準的功能表項目。 重迭、快顯視窗或子視窗可以有視窗功能表。 重迭或快顯視窗不會包含視窗功能表的情況很常見。

當使用者從 [ **視窗]** 功能表選擇命令時，系統會將 [**WM \_ SYSCOMMAND**](wm-syscommand.md) 訊息傳送至功能表的擁有者視窗。 在大部分的應用程式中，視窗程式都不會處理來自 [視窗] 功能表的訊息。 相反地，它只會將訊息傳遞至 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函式，以進行訊息的系統預設處理。 如果應用程式將命令新增至 [視窗] 功能表，則視窗程式必須處理命令。

應用程式可以使用 [**GetSystemMenu**](/windows/desktop/api/Winuser/nf-winuser-getsystemmenu) 函式來建立要修改之預設視窗功能表的複本。 任何未使用 **GetSystemMenu** 函式來建立它自己的視窗功能表複本的視窗，都會收到標準的視窗功能表。

### <a name="help-identifier"></a>說明識別碼

與每個功能表列、功能表、子功能表和快捷方式功能表相關聯的是說明識別碼。 如果使用者在功能表為使用中時按 F1 鍵，則會將此值傳送至擁有者視窗作為 WM 說明 [**訊息 \_**](../shell/wm-help.md) 的一部分。

## <a name="keyboard-access-to-menus"></a>鍵盤存取功能表

系統會提供功能表的標準鍵盤介面。 您可以針對功能表項目，提供助憶鍵存取金鑰和快捷方式 (加速器) 機碼，以增強這個介面。

下列主題描述標準鍵盤介面、存取金鑰和快速鍵：

-   [標準鍵盤介面](#standard-keyboard-interface)
-   [功能表存取金鑰](#menu-access-keys)
-   [功能表快速鍵](#menu-shortcut-keys)

### <a name="standard-keyboard-interface"></a>標準鍵盤介面

系統是設計來使用或不使用滑鼠或其他指標裝置。 由於系統提供標準鍵盤介面，因此使用者可以使用鍵盤來選取功能表項目。 這個鍵盤介面不需要特殊的程式碼。 應用程式會收到命令訊息，指出使用者是透過鍵盤或使用滑鼠選取功能表項目。 標準鍵盤介面會處理下列按鍵。



| 按鍵              | 動作                                                                                                                                                                                                                                   |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 字母字元 | 選取具有指定字元作為其存取金鑰的第一個功能表項目。 如果選取的專案叫用功能表，就會顯示功能表，並反白顯示第一個專案。 否則，就會選擇功能表項目。                            |
| ALT                    | 切換開啟和離開功能表列模式。                                                                                                                                                                                                     |
| ALT 鍵 + 空格鍵           | 顯示視窗功能表。                                                                                                                                                                                                                |
| ENTER                  | 啟用功能表，並選取第一個功能表項目（如果專案有相關聯的功能表項目）。 否則，此按鍵會選擇專案，就像在選取專案時，使用者放開滑鼠按鍵一樣。                              |
| ESC                    | 離開功能表模式。                                                                                                                                                                                                                         |
| 向左鍵             | 迴圈至先前的最上層功能表項目。 最上層功能表項目包括功能表名稱和 [視窗] 功能表。 如果選取的專案位於功能表中，則會選取功能表中的上一個資料行，或選取先前的最上層功能表項目。 |
| 向右鍵            | 的運作方式與向左箭號不同，但方向相反。 在功能表中，此按鍵會向前移動一個資料行;當目前選取的專案位於最右側的資料行時，就會選取下一個功能表。                              |
| 向上鍵或向下鍵      | 當您按下功能表名稱時，會啟用功能表。 在功能表中按下時，向上箭號鍵會選取前一個專案;向下鍵會選取下一個專案。                                                                  |



 

### <a name="menu-access-keys"></a>功能表存取金鑰

您可以將存取金鑰 (助憶鍵) 至功能表項目，以增強功能表的標準鍵盤介面。 存取金鑰是功能表項目文字中的加底線字母。 當功能表為使用中時，使用者可以按下對應至專案加底線字母的按鍵來選取功能表項目。 使用者會按下 ALT 鍵來反白顯示功能表列上的第一個專案，讓功能表列成為使用中狀態。 功能表在顯示時為使用中狀態。

若要建立功能表項目的存取金鑰，請在專案文字字串中的任何字元前面加上連字號。 例如，文字字串 "&Move" 會導致系統將字母 "M" 加上底線。

### <a name="menu-shortcut-keys"></a>功能表快速鍵

除了具有便捷鍵之外，功能表項目也可以有相關聯的快速鍵。 快速鍵與存取金鑰不同，因為功能表不需要使用中，快速鍵才能運作。 此外，便捷鍵 *一律* 會與功能表項目相關聯，而快速鍵 *通常* 是 (，但不需要) 與功能表項目相關聯。

識別快速鍵的文字會加入至功能表項目文字字串。 快速鍵文字會出現在功能表項目名稱右邊，反斜線和定位字元 (\\ t) 。 例如，"&Close \\ tAlt + f4" 代表 Close 命令，其中 ALT + F4 按鍵組合作為其快速鍵，並以字母 "C" 作為其存取金鑰。 如需詳細資訊，請參閱 [鍵盤快捷](keyboard-accelerators.md)。

## <a name="menu-creation"></a>功能表建立

您可以使用功能表範本或功能表建立功能來建立功能表。 功能表範本通常定義為資源。 功能表-範本資源可以明確地載入，或指派為視窗類別的預設功能表。 您也可以在記憶體中動態建立功能表範本資源。

下列主題將詳細說明功能表建立：

-   [功能表範本資源](#menu-template-resources)
-   [記憶體中的功能表範本](#menu-template-in-memory)
-   [功能表控點](#menu-handles)
-   [功能表建立功能](#menu-creation-functions)
-   [功能表顯示](#menu-display)
-   [視窗類別功能表](#window-class-menus)

### <a name="menu-template-resources"></a>功能表範本資源

大部分的應用程式會使用功能表範本資源建立功能表。 *功能表範本* 會定義功能表，包括功能表列中的專案和所有功能表。 如需建立功能表範本資源的詳細資訊，請參閱您的開發工具隨附的檔。

建立功能表範本資源並將它加入至應用程式的可執行檔 (.exe) 檔之後，您可以使用 [**LoadMenu**](/windows/desktop/api/Winuser/nf-winuser-loadmenua) 函式將資源載入至記憶體。 此函式會傳回功能表的控制碼，然後您可以使用 [**SetMenu**](/windows/desktop/api/Winuser/nf-winuser-setmenu) 函式將其指派給視窗。 您可以將功能表指派給不是子視窗的任何視窗。

將功能表實作為資源，可讓您更輕鬆地將應用程式當地語系化，以在多個國家/地區中使用。 只有資源定義檔需要針對每種語言進行當地語系化，而不是應用程式的原始程式碼。

### <a name="menu-template-in-memory"></a>記憶體中的功能表範本

您可以從在執行時間內建于記憶體中的功能表範本建立功能表。 例如，允許使用者自訂其功能表的應用程式可能會根據使用者的喜好設定，在記憶體中建立功能表範本。 然後，應用程式可以將範本儲存在檔案或登錄中，以供日後使用。 若要從記憶體中的範本建立功能表，請使用 [**LoadMenuIndirect**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta) 函數。 如需功能表範本格式的說明，請參閱 [功能表範本資源](#menu-template-resources)。

標準功能表範本包含 [**MENUITEMTEMPLATEHEADER**](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplateheader) 結構，後面接著一或多個 [**MENUITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplate) 結構。

擴充功能表範本包含 [**MENUEX \_ 範本 \_ 標頭**](menuex-template-header.md) 結構，後面接著一或多個 [**MENUEX \_ 範本 \_ 專案**](menuex-template-item.md) 結構。

### <a name="menu-handles"></a>功能表控點

系統會為每個功能表產生唯一的控制碼。 *功能表控制碼* 是 **HMENU** 類型的值。 應用程式必須在許多功能表函數中指定功能表控制碼。 當您建立功能表或載入功能表資源時，會收到功能表列的控制碼。

若要取得已建立或載入之功能表的功能表列控制碼，請使用 [**GetMenu**](/windows/desktop/api/Winuser/nf-winuser-getmenu) 函式。 若要取得與功能表項目相關聯之子功能表的控制碼，請使用 [**GetSubMenu**](/windows/desktop/api/Winuser/nf-winuser-getsubmenu) 或 [**GetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) 函數。 若要取得視窗功能表的控制碼，請使用 [**GetSystemMenu**](/windows/desktop/api/Winuser/nf-winuser-getsystemmenu) 函數。

### <a name="menu-creation-functions"></a>功能表建立功能

使用功能表建立功能時，您可以在執行時間建立功能表，或將功能表項目加入至現有的功能表。 您可以使用 [**CreateMenu**](/windows/desktop/api/Winuser/nf-winuser-createmenu) 函式來建立空白的功能表列，並使用 [**CreatePopupMenu**](/windows/desktop/api/Winuser/nf-winuser-createpopupmenu) 函式來建立空白的功能表。 您可以使用 [**MENUINFO**](/windows/win32/api/winuser/ns-winuser-menuinfo) 結構來儲存功能表的特定設定資訊。 若要取得或取得功能表的設定，請使用 [**GetMenuInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuinfo) 或 [**SetMenuInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuinfo)。 若要將專案加入至功能表，請使用 [**InsertMenuItem**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema) 函數。 仍然支援較舊的 [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua) 和 [**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua) 函式，但 **InsertMenuItem** 應該用於新的應用程式。

### <a name="menu-display"></a>功能表顯示

載入或建立功能表之後，必須先將它指派給視窗，系統才能顯示該功能表。 您可以藉由定義類別功能表來指派功能表。 如需詳細資訊，請參閱 [視窗類別功能表](#window-class-menus)。 您也可以藉由將功能表的控制碼指定為 [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa)或 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)函數的 *hMenu* 參數，或藉由呼叫 [**SetMenu**](/windows/desktop/api/Winuser/nf-winuser-setmenu)函式，將功能表指派給視窗。

若要顯示快捷方式功能表，請使用 [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) 函數。 處理 [**WM \_ CONTEXTMENU**](wm-contextmenu.md) 訊息時，通常會顯示快捷方式功能表（也稱為浮動快顯功能表或快顯功能表）。

您可以將功能表指派給不是子視窗的任何視窗。

仍然支援較舊的 [**trackpopupmenu 讓**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) 函式，但新的應用程式應該使用 [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) 函數。

### <a name="window-class-menus"></a>視窗類別功能表

當您註冊視窗類別時，可以指定預設功能表，稱為 *類別功能表* 。 若要這樣做，請將功能表範本資源的名稱指派給用來註冊類別的 [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa)結構的 **lpszMenuName** 成員。

預設會為每個視窗指派其視窗類別的 [類別] 功能表，因此您不需要明確地載入功能表並將它指派給每個視窗。 您可以藉由在 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 函式的呼叫中指定不同的功能表控制碼，來覆寫 [類別] 功能表。 您也可以在使用 [**SetMenu**](/windows/desktop/api/Winuser/nf-winuser-setmenu) 函式建立之後，變更視窗的功能表。 如需詳細資訊，請參閱 [視窗類別](/windows/desktop/winmsg/window-classes)。

## <a name="menu-items"></a>功能表項目

下列主題討論當使用者選擇功能表項目時，系統執行的動作，以及應用程式可以控制專案外觀和功能的方式：

-   [開啟子功能表的命令專案和專案](#command-items-and-items-that-open-submenus)
-   [功能表項目識別碼](#menu-item-identifier)
-   [功能表項目位置](#menu-item-position)
-   [以程式設計方式存取功能表項目](#accessing-menu-items-programmatically)
-   [預設功能表項目](#default-menu-items)
-   [選取和清除功能表項目](#selected-and-clear-menu-items)
-   [啟用、灰色和停用的功能表項目](#enabled-grayed-and-disabled-menu-items)
-   [反白顯示的功能表項目](#highlighted-menu-items)
-   [擁有者繪製的功能表項目](#owner-drawn-menu-items)
-   [功能表項目分隔符號和分行符號號](#menu-item-separators-and-line-breaks)

### <a name="command-items-and-items-that-open-submenus"></a>開啟子功能表的命令專案和專案

當使用者選擇命令專案時，系統會將命令訊息傳送至擁有功能表的視窗。 如果命令專案位於 [視窗] 功能表上，系統會傳送 [**WM \_ SYSCOMMAND**](wm-syscommand.md) 訊息。 否則，它會傳送 [**WM \_ 命令**](wm-command.md) 訊息。

與開啟子功能表的每個功能表項目相關聯，是對應子功能表的控制碼。 當使用者指向這類專案時，系統會開啟子功能表。 沒有任何命令訊息會傳送至主控視窗。 不過，系統會先將 [**WM \_ INITMENUPOPUP**](wm-initmenupopup.md) 訊息傳送給擁有者視窗，然後才顯示子功能表。 您可以使用 [**GetSubMenu**](/windows/desktop/api/Winuser/nf-winuser-getsubmenu) 或 [**GetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) 函數，取得與專案相關聯的子功能表控制碼。

功能表列通常包含功能表名稱，但也可以包含命令專案。 子功能表通常包含命令專案，但也可以包含開啟嵌套子功能表的專案。 藉由將這類專案加入至子功能表，您可以將功能表嵌套到任何深度。 為了提供視覺提示給使用者，系統會自動在開啟子功能表的功能表項目文字右邊顯示一個小箭號。

### <a name="menu-item-identifier"></a>Menu-Item 識別碼

與每個功能表項目相關聯的是一個唯一的應用程式定義整數，稱為 *功能表項目識別碼*。 當使用者從功能表中選擇命令專案時，系統會將專案的識別碼傳送至擁有者視窗，作為 [**WM \_ 命令**](wm-command.md) 訊息的一部分。 視窗程式會檢查識別碼，以判斷訊息的來源，並據以處理訊息。 此外，您可以在呼叫功能表函式時，使用其識別碼指定功能表項目;例如，啟用或停用功能表項目。

開啟子功能表的功能表項目具有識別碼，就像命令專案一樣。 不過，從功能表中選取這類專案時，系統不會傳送命令訊息。 相反地，系統會開啟與功能表項目相關聯的子功能表。

若要在指定位置取出功能表項目的識別碼，請使用 [**GetMenuItemID**](/windows/desktop/api/Winuser/nf-winuser-getmenuitemid) 或 [**GetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) 函數。

### <a name="menu-item-position"></a>Menu-Item 位置

除了具有唯一識別碼之外，功能表列或功能表中的每個功能表項目都具有唯一的位置值。 功能表列中最左邊的專案或功能表中的最上層專案，都有位置零。 後續功能表項目的位置值會遞增。 系統會將位置值指派給功能表中的所有專案，包括分隔符號。 下圖顯示功能表列和功能表中專案的位置值。

![功能表列和功能表](images/csemn-01.png)

當呼叫修改或抓取特定功能表項目相關資訊的功能表函式時，您可以使用它的識別碼或其位置來指定專案。 如需詳細資訊，請參閱下一節。

### <a name="accessing-menu-items-programmatically"></a>以程式設計方式存取功能表項目

大部分的功能表功能都可讓您依位置或命令指定功能表項目。 有些函式會使用 **mf \_ BYPOSITION** 和 **mf \_ BYCOMMAND** 旗標來表示搜尋演算法，有些則具有明確的 *fByPosition* 參數。 如果您依位置指定功能表項目，則專案編號是以零為基底的索引，在功能表中。 如果您依命令指定功能表項目，則會在功能表識別碼等於所提供專案編號的專案中搜尋功能表和其子功能表。 如果功能表階層中有多個專案符合專案編號，則不會指定使用哪一個專案。 如果您的功能表包含重複的功能表識別碼，您應該使用以位置為基礎的功能表作業來避免這種混淆。

### <a name="default-menu-items"></a>預設功能表項目

子功能表可以包含一個預設功能表項目。 當使用者按兩下來開啟子功能表時，系統會將命令訊息傳送至功能表的擁有者視窗，並關閉功能表，如同已選擇預設的命令專案一樣。 如果沒有預設的命令專案，子功能表會保持開啟。 若要抓取並設定子功能表的預設專案，請使用 [**GetMenuDefaultItem**](/windows/desktop/api/Winuser/nf-winuser-getmenudefaultitem) 和 [**SetMenuDefaultItem**](/windows/desktop/api/Winuser/nf-winuser-setmenudefaultitem) 函數。

### <a name="selected-and-clear-menu-items"></a>選取和清除功能表項目

功能表項目可以是 [已選取] 或 [清除]。 系統會在選取的功能表項目旁邊顯示點陣圖，以指出其選取的狀態。 除非指定了應用程式定義的「清除」點陣圖，否則系統不會在清除專案旁顯示點陣圖。 您只能選取功能表中的功能表項目;無法選取功能表列中的專案。

應用程式通常會檢查或清除功能表項目，以指出選項是否作用中。 例如，假設應用程式有一個工具列，可讓使用者使用功能表上的 **工具列** 命令來顯示或隱藏。 隱藏工具列時， **工具列** 功能表項目會很清楚。 當使用者選擇此命令時，應用程式會檢查功能表項目，並顯示工具列。

核取記號屬性會控制是否已選取功能表項目。 您可以使用 [**CheckMenuItem**](/windows/desktop/api/Winuser/nf-winuser-checkmenuitem) 函數來設定功能表項目的核取記號屬性。 您可以使用 [**GetMenuState**](/windows/desktop/api/Winuser/nf-winuser-getmenustate) 函式來判斷是否目前已選取或清除功能表項目。

您可以使用 [**GetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa)和 [**SetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa)函式來取得和設定功能表項目的檢查狀態，而不是 [**CheckMenuItem**](/windows/desktop/api/Winuser/nf-winuser-checkmenuitem)和 [**GetMenuState**](/windows/desktop/api/Winuser/nf-winuser-getmenustate)。

有時候，一組功能表項目會對應到一組互斥的選項。 在這種情況下，您可以使用選取的 [選項按鈕] 功能表項目， (類似選項按鈕控制項) 來指出選取的選項。 選取的選項按鈕會以專案符號點陣圖而非核取記號點陣圖顯示。 若要檢查功能表項目並將其設為選項按鈕，請使用 [**CheckMenuRadioItem**](/windows/desktop/api/Winuser/nf-winuser-checkmenuradioitem) 函數。

根據預設，系統會在選取的功能表項目旁邊顯示核取記號或專案符號點陣圖，並在清除的功能表項目旁邊顯示任何點陣圖。 不過，您可以使用 [**SetMenuItemBitmaps**](/windows/desktop/api/Winuser/nf-winuser-setmenuitembitmaps) 函式，將應用程式定義的選取和清除點陣圖與功能表項目產生關聯。 系統接著會使用指定的點陣圖來指出功能表項目的選取或清除狀態。

與功能表項目相關聯的應用程式定義點陣圖必須與預設的核取記號點陣圖大小相同，其尺寸可能會依螢幕解析度而有所不同。 若要取得正確的維度，請使用 [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) 函數。 您可以針對不同的螢幕解析度建立多個點陣圖資源;如有必要，請建立一個點陣圖資源並調整其大小。或在執行時間建立點陣圖，並在其中繪製影像。 點陣圖可能是單色或彩色。 不過，由於功能表項目會在反白顯示時反轉，因此可能不需要某些反轉色彩點陣圖的外觀。 如需詳細資訊，請參閱 [點陣圖](/windows/desktop/gdi/bitmaps)。

### <a name="enabled-grayed-and-disabled-menu-items"></a>啟用、灰色和停用的功能表項目

您可以啟用、呈現灰色或停用功能表項目。 依預設，會啟用功能表項目。 當使用者選擇 [已啟用] 功能表項目時，系統會將命令訊息傳送至主控視窗，或根據功能表項目的類型，顯示對應的子功能表。

當使用者無法使用功能表項目時，這些專案應該呈現灰色或停用。 無法選擇灰色和停用的功能表項目。 已停用的專案看起來就像已啟用的專案一樣。 當使用者按一下已停用的專案時，就不會選取該專案，也不會發生任何事。 例如，已停用的專案可能會在顯示顯示為使用中但未顯示之功能表的教學課程中有用。

應用程式會將無法使用的功能表項目設為灰色，以提供不提供命令給使用者的視覺提示。 當動作不適用時，您可以使用灰色的專案 (例如，當系統沒有安裝印表機) 時，[檔案 **] 功能表中的 [** **列印**] 命令會變成灰色。

[**EnableMenuItem**](/windows/desktop/api/Winuser/nf-winuser-enablemenuitem)函式會啟用、停用或停用功能表項目。 若要判斷是否已啟用、灰色或停用功能表項目，請使用 [**GetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) 函數。

除了 [**GetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa)之外，您也可以使用 [**GetMenuState**](/windows/desktop/api/Winuser/nf-winuser-getmenustate) 函式來判斷功能表項目是已啟用、灰色還是停用。

### <a name="highlighted-menu-items"></a>反白顯示的功能表項目

當使用者選取功能表項目時，系統會自動反白顯示功能表上的功能表項目。 不過，您可以使用 [**HiliteMenuItem**](/windows/desktop/api/Winuser/nf-winuser-hilitemenuitem) 函式，在功能表列上的功能表名稱中明確地加入或移除反白顯示。 此函式不會影響功能表上的功能表項目。 不過，當 **HiliteMenuItem** 用來反白顯示功能表名稱時，此名稱只會顯示為已選取。 如果使用者按下 ENTER 鍵，則不會選擇反白顯示的專案。 例如，這項功能在示範功能表使用方式的訓練應用程式中可能很有用。

### <a name="owner-drawn-menu-items"></a>Owner-Drawn 功能表項目

應用程式可以使用主控描繪 *專案* 來完全控制功能表項目的外觀。 擁有者繪製的專案需要應用程式，才能將選取的 (醒目提示) 、選取和清除的狀態。 例如，如果應用程式提供了字型功能表，則可以使用對應的字型繪製每個功能表項目;羅馬字的專案會以羅馬繪製，斜體的專案會以斜體繪製，依此類推。 如需詳細資訊，請參閱 [建立 Owner-Drawn 功能表項目](using-menus.md)。

### <a name="menu-item-separators-and-line-breaks"></a>功能表項目分隔符號和分行符號號

系統會提供一種特殊類型的功能表項目（稱為 *分隔符號*），以水平線顯示。 您可以使用分隔符號將功能表分割成相關專案的群組。 無法在功能表列中使用分隔符號，使用者也無法選取分隔符號。

當功能表列包含的功能表名稱超過一行所容納的數目時，系統會自動將它分成兩行或多行，以包裝功能表列。 您可以藉由將 [ **MFT \_ MENUBREAK** 類型] 旗標指派給專案，在功能表列上的特定專案上產生分行符號。 系統會將該專案和所有後續專案放在新行上。

當功能表所包含的專案數目超過一個資料行時，功能表將會被截斷。 您可以藉由將 **MFT \_ MENUBREAK** 類型旗標指派給專案，或使用 [MENUITEM](/windows/desktop/menurc/menuitem-statement) 語句中的 MENUBREAK 選項，讓資料行出現在功能表中的特定專案上。 系統會將該專案和所有後續專案放在新的資料行中。 [ **MFT \_ MENUBARBREAK** 類型] 旗標具有相同的效果，不同之處在于新的資料行與舊的資料行之間會出現垂直線。

如果您使用 [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua)、 [**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua)或 [**ModifyMenu**](/windows/desktop/api/Winuser/nf-winuser-modifymenua) 函式來指派分行符號，則應指派類型旗標 **mf \_ MENUBREAK** 或 **mf \_ MENUBARBREAK**。

## <a name="messages-used-with-menus"></a>搭配功能表使用的訊息

系統會將訊息傳送至擁有功能表之視窗的視窗程式，以報告功能表相關活動。 當使用者在功能表列上選取專案或按一下滑鼠右鍵以顯示快捷方式功能表時，系統會傳送一連串的訊息。

當使用者在功能表列上啟動專案時，擁有者視窗會先收到 [**WM \_ SYSCOMMAND**](wm-syscommand.md) 訊息。 此訊息包含一個旗標，指出使用者是否使用鍵盤 (SC \_ KEYMENU) 或滑鼠 (SC MOUSEMENU) 來啟用功能表 \_ 。 如需詳細資訊，請參閱 [鍵盤存取功能表](#keyboard-access-to-menus)。

接下來，在顯示任何功能表之前，系統會將 [**WM \_ INITMENU**](wm-initmenu.md) 訊息傳送至視窗程式，讓應用程式可以在使用者看到功能表之前修改功能表。 系統只會針對每個功能表啟用傳送一次 **WM 的 \_ INITMENU** 訊息。

當使用者指向開啟子功能表的功能表項目時，系統會在顯示子功能表之前，先將 [**WM \_ INITMENUPOPUP**](wm-initmenupopup.md) 訊息傳送給擁有者視窗。 這則訊息會讓應用程式有機會在子功能表顯示前加以修改。

每次使用者將醒目提示從某個專案移到另一個專案時，系統就會將 [**WM \_ MENUSELECT**](wm-menuselect.md) 訊息傳送至功能表的擁有者視窗的視窗程式。 此訊息會識別目前選取的功能表項目。 許多應用程式會在其主視窗的底部提供資訊區域，並使用此訊息來顯示有關選取之功能表項目的其他資訊。

當使用者從功能表中選擇命令專案時，系統會將 [**WM \_ 命令**](wm-command.md) 訊息傳送至視窗程式。 **WM \_ 命令** 訊息的 *wParam* 參數的低序位文字包含所選項目的識別碼。 視窗程式應檢查識別碼，並據以處理訊息。

您可以使用 [**MENUINFO**](/windows/win32/api/winuser/ns-winuser-menuinfo) 結構來儲存功能表的資訊。 如果功能表是以 **MENUINFO** 定義。**dwStyle** 的 MNS \_ NOTIFYBYPOS 值，當選取專案時，系統會傳送 [**Wm \_ MENUCOMMAND**](wm-menucommand.md) 而非 [**wm \_ 命令**](wm-command.md) 。 這可讓您存取 **MENUINFO** 結構中的資訊，也可直接提供所選取專案的索引。

並非所有功能表都可透過視窗的功能表列來存取。 當使用者按一下特定位置的滑鼠右鍵時，許多應用程式會顯示快捷方式功能表。 這類應用程式應該處理 [**WM \_ CONTEXTMENU**](wm-contextmenu.md) 訊息，並在適當的情況下顯示快捷方式功能表。 如果應用程式未顯示快捷方式功能表，則應該將 **WM \_ CONTEXTMENU** 訊息傳遞至 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函式，以進行預設處理。

當使用者放開滑鼠右鍵，而游標位於功能表項目上時，就會傳送 [**WM \_ MENURBUTTONUP**](wm-menurbuttonup.md) 訊息。 提供此訊息，讓應用程式可以顯示功能表項目的內容相關或快捷方式功能表。

有幾個訊息只牽涉到拖放功能表。 當滑鼠游標進入功能表項目，或從專案的中央移動至專案的頂端或底部時，會將 [**WM \_ MENUGETOBJECT**](wm-menugetobject.md) 傳送至拖放功能表的擁有者。 當使用者實際拖曳功能表項目時，會傳送 [**WM \_ MENUDRAG**](wm-menudrag.md) 訊息。

當下拉功能表或子功能表損毀時，系統會傳送 [**WM \_ UNINITMENUPOPUP**](wm-uninitmenupopup.md) 訊息。

## <a name="menu-destruction"></a>功能表損毀

如果已將功能表指派給視窗，且該視窗已終結，系統會自動終結功能表及其子功能表，釋出功能表的控制碼和功能表所佔用的記憶體。 系統不會自動摧毀未指派給視窗的功能表。 應用程式必須藉由呼叫 [**DestroyMenu**](/windows/desktop/api/Winuser/nf-winuser-destroymenu) 函數來終結未指派的功能表。 否則，即使應用程式關閉，功能表仍會繼續存在於記憶體中。 若要結束呼叫執行緒的現用功能表，請使用 [**EndMenu**](/windows/desktop/api/Winuser/nf-winuser-endmenu)。 如果平臺不支援 **EndMenu**，請將動態功能表的擁有者傳送至 [**WM \_ CANCELMODE**](/windows/desktop/winmsg/wm-cancelmode) 訊息。

 

 