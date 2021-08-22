---
title: '物件角色 (Oleacc .h) '
description: 本主題說明用來描述應用程式中各種 UI 物件角色的常數值。
ms.assetid: f015252a-c0df-4a21-a995-ff2f6cafbab8
topic_type:
- apiref
api_name:
- ROLE_SYSTEM_ALERT
- ROLE_SYSTEM_ANIMATION
- ROLE_SYSTEM_APPLICATION
- ROLE_SYSTEM_BORDER
- ROLE_SYSTEM_BUTTONDROPDOWN
- ROLE_SYSTEM_BUTTONDROPDOWNGRID
- ROLE_SYSTEM_BUTTONMENU
- ROLE_SYSTEM_CARET
- ROLE_SYSTEM_CELL
- ROLE_SYSTEM_CHARACTER
- ROLE_SYSTEM_CHART
- ROLE_SYSTEM_CHECKBUTTON
- ROLE_SYSTEM_CLIENT
- ROLE_SYSTEM_CLOCK
- ROLE_SYSTEM_COLUMN
- ROLE_SYSTEM_COLUMNHEADER
- ROLE_SYSTEM_COMBOBOX
- ROLE_SYSTEM_CURSOR
- ROLE_SYSTEM_DIAGRAM
- ROLE_SYSTEM_DIAL
- ROLE_SYSTEM_DIALOG
- ROLE_SYSTEM_DOCUMENT
- ROLE_SYSTEM_DROPLIST
- ROLE_SYSTEM_EQUATION
- ROLE_SYSTEM_GRAPHIC
- ROLE_SYSTEM_GRIP
- ROLE_SYSTEM_GROUPING
- ROLE_SYSTEM_HELPBALLOON
- ROLE_SYSTEM_HOTKEYFIELD
- ROLE_SYSTEM_INDICATOR
- ROLE_SYSTEM_IPADDRESS
- ROLE_SYSTEM_LINK
- ROLE_SYSTEM_LIST
- ROLE_SYSTEM_LISTITEM
- ROLE_SYSTEM_MENUBAR
- ROLE_SYSTEM_MENUITEM
- ROLE_SYSTEM_MENUPOPUP
- ROLE_SYSTEM_OUTLINE
- ROLE_SYSTEM_OUTLINEBUTTON
- ROLE_SYSTEM_OUTLINEITEM
- ROLE_SYSTEM_PAGETAB
- ROLE_SYSTEM_PAGETABLIST
- ROLE_SYSTEM_PANE
- ROLE_SYSTEM_PROGRESSBAR
- ROLE_SYSTEM_PROPERTYPAGE
- ROLE_SYSTEM_PUSHBUTTON
- ROLE_SYSTEM_RADIOBUTTON
- ROLE_SYSTEM_ROW
- ROLE_SYSTEM_ROWHEADER
- ROLE_SYSTEM_SCROLLBAR
- ROLE_SYSTEM_SEPARATOR
- ROLE_SYSTEM_SLIDER
- ROLE_SYSTEM_SOUND
- ROLE_SYSTEM_SPINBUTTON
- ROLE_SYSTEM_SPLITBUTTON
- ROLE_SYSTEM_STATICTEXT
- ROLE_SYSTEM_STATUSBAR
- ROLE_SYSTEM_TABLE
- ROLE_SYSTEM_TEXT
- ROLE_SYSTEM_TITLEBAR
- ROLE_SYSTEM_TOOLBAR
- ROLE_SYSTEM_TOOLTIP
- ROLE_SYSTEM_WHITESPACE
- ROLE_SYSTEM_WINDOW
api_location:
- Oleacc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03ec3eb9574dbed208a7c38714c838e567990fc76af137fca563de65142ac5f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119614658"
---
# <a name="object-roles"></a>物件角色

本主題說明用來描述應用程式中各種 UI 物件角色的常數值。 角色常數定義于 Oleacc .h 檔案中。

您應該只使用此處列出的列出角色常數;請勿新增自訂角色或未預先定義的角色。

使用這些物件角色之前，用戶端應用程式的開發人員必須使用 [檢查](inspect-objects.md) 工具來確認 UI 元素正在使用物件角色。

若要取得物件的角色，用戶端會呼叫 [**IAccessible：： get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole) 方法，此方法必須傳回資料表中所述的其中一個值。 為了取得描述物件角色的當地語系化字串，用戶端會以角色值呼叫 [**GetRoleText**](/windows/desktop/api/Oleacc/nf-oleacc-getroletexta) 函式。 角色值的當地語系化字串位於 oleaccrc.dll 檔案中。



| 常數                                                                                                                                                                                                          | 描述                                                                                                                                                                                                                                                                                                                                                                                                                              |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ROLE_SYSTEM_ALERT"></span><span id="role_system_alert"></span><dl> <dt>**角色 \_ 系統 \_ 警示**</dt> </dl>                                        | 物件代表應通知使用者的警示或條件。 這個角色只適用于體現警示但未與另一個使用者介面專案（例如訊息方塊、圖形、文字或音效）相關聯的物件。<br/>                                                                                                                                                                       |
| <span id="ROLE_SYSTEM_ANIMATION"></span><span id="role_system_animation"></span><dl> <dt>**角色 \_ 系統 \_ 動畫**</dt> </dl>                            | 物件代表動畫控制項，其內容會隨著時間而變更，例如顯示一系列點陣圖框架的控制項。 複製檔案時，或在執行其他耗時的工作時，會顯示動畫控制項。<br/>                                                                                                                                                                            |
| <span id="ROLE_SYSTEM_APPLICATION"></span><span id="role_system_application"></span><dl> <dt>**角色 \_ 系統 \_ 應用程式**</dt> </dl>                      | 物件表示應用程式的主視窗。<br/>                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="ROLE_SYSTEM_BORDER"></span><span id="role_system_border"></span><dl> <dt>**角色 \_ 系統 \_ 框線**</dt> </dl>                                     | 物件代表視窗框線。 整個框線都會以單一物件表示，而不是每個邊個別的物件。<br/>                                                                                                                                                                                                                                                                                     |
| <span id="ROLE_SYSTEM_BUTTONDROPDOWN"></span><span id="role_system_buttondropdown"></span><dl> <dt>**角色 \_ 系統 \_ BUTTONDROPDOWN**</dt> </dl>             | 物件表示展開專案清單的按鈕。<br/>                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="ROLE_SYSTEM_BUTTONDROPDOWNGRID"></span><span id="role_system_buttondropdowngrid"></span><dl> <dt>**角色 \_ 系統 \_ BUTTONDROPDOWNGRID**</dt> </dl> | 物件代表展開方格的按鈕。<br/>                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="ROLE_SYSTEM_BUTTONMENU"></span><span id="role_system_buttonmenu"></span><dl> <dt>**角色 \_ 系統 \_ BUTTONMENU**</dt> </dl>                         | 物件代表展開功能表的按鈕。<br/>                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="ROLE_SYSTEM_CARET"></span><span id="role_system_caret"></span><dl> <dt>**角色 \_ 系統 \_ 插入號**</dt> </dl>                                        | 物件表示系統插入號。<br/>                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="ROLE_SYSTEM_CELL"></span><span id="role_system_cell"></span><dl> <dt>**角色 \_ 系統 \_ 儲存格**</dt> </dl>                                           | 物件代表資料表內的資料格。<br/>                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="ROLE_SYSTEM_CHARACTER"></span><span id="role_system_character"></span><dl> <dt>**角色 \_ 系統 \_ 字元**</dt> </dl>                            | 物件代表類似卡通的繪圖物件，例如 Microsoft Office Assistant，會顯示以提供應用程式使用者的協助。<br/>                                                                                                                                                                                                                                                                       |
| <span id="ROLE_SYSTEM_CHART"></span><span id="role_system_chart"></span><dl> <dt>**角色 \_ 系統 \_ 圖表**</dt> </dl>                                        | 物件代表用來繪製資料的圖形影像。<br/>                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="ROLE_SYSTEM_CHECKBUTTON"></span><span id="role_system_checkbutton"></span><dl> <dt>**角色 \_ 系統 \_ CHECKBUTTON**</dt> </dl>                      | 物件表示核取方塊控制項：選取或清除的選項會與其他選項無關。<br/>                                                                                                                                                                                                                                                                                                              |
| <span id="ROLE_SYSTEM_CLIENT"></span><span id="role_system_client"></span><dl> <dt>**角色 \_ 系統 \_ 用戶端**</dt> </dl>                                     | 物件代表視窗的工作區。 如果 UI 元素的角色有問題，Microsoft Active Accessibility 會使用此角色作為預設值。<br/>                                                                                                                                                                                                                                                               |
| <span id="ROLE_SYSTEM_CLOCK"></span><span id="role_system_clock"></span><dl> <dt>**角色 \_ 系統 \_ 時鐘**</dt> </dl>                                        | 物件表示顯示時間的控制項。<br/>                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="ROLE_SYSTEM_COLUMN"></span><span id="role_system_column"></span><dl> <dt>**角色 \_ 系統資料 \_ 行**</dt> </dl>                                     | 物件代表資料表內資料格的資料行。<br/>                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="ROLE_SYSTEM_COLUMNHEADER"></span><span id="role_system_columnheader"></span><dl> <dt>**角色 \_ 系統 \_ COLUMNHEADER**</dt> </dl>                   | 物件表示資料行標頭，為數據表中的資料行提供視覺標籤。<br/>                                                                                                                                                                                                                                                                                                                                      |
| <span id="ROLE_SYSTEM_COMBOBOX"></span><span id="role_system_combobox"></span><dl> <dt>**角色 \_ 系統 \_ COMBOBOX**</dt> </dl>                               | 物件代表下拉式方塊：具有相關聯清單方塊的編輯控制項，可提供一組預先定義的選項。<br/>                                                                                                                                                                                                                                                                                                     |
| <span id="ROLE_SYSTEM_CURSOR"></span><span id="role_system_cursor"></span><dl> <dt>**角色 \_ 系統資料 \_ 指標**</dt> </dl>                                     | 物件代表系統的滑鼠指標。<br/>                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="ROLE_SYSTEM_DIAGRAM"></span><span id="role_system_diagram"></span><dl> <dt>**角色 \_ 系統 \_ 圖表**</dt> </dl>                                  | 物件代表用來圖表資料的圖形影像。<br/>                                                                                                                                                                                                                                                                                                                                                         |
| <span id="ROLE_SYSTEM_DIAL"></span><span id="role_system_dial"></span><dl> <dt>**角色 \_ 系統 \_ 撥號**</dt> </dl>                                           | 物件代表撥號或旋鈕。<br/>                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="ROLE_SYSTEM_DIALOG"></span><span id="role_system_dialog"></span><dl> <dt>**角色 \_ 系統 \_ 對話方塊**</dt> </dl>                                     | 物件代表對話方塊或訊息方塊。<br/>                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="ROLE_SYSTEM_DOCUMENT"></span><span id="role_system_document"></span><dl> <dt>**角色 \_ 系統 \_ 檔**</dt> </dl>                               | 物件代表文件視窗。 文件視窗一律包含在應用程式視窗中。 這個角色只適用于 MDI 視窗，而且會參考包含 MDI 標題列的物件。<br/>                                                                                                                                                                                                                  |
| <span id="ROLE_SYSTEM_DROPLIST"></span><span id="role_system_droplist"></span><dl> <dt>**角色 \_ 系統 \_ DROPLIST**</dt> </dl>                               | 物件代表行事曆控制項 SysDateTimePick32。 Microsoft Active Accessibility 執行時間元件會使用此角色來表示已找到日期或行事曆控制項。<br/>                                                                                                                                                                                                                       |
| <span id="ROLE_SYSTEM_EQUATION"></span><span id="role_system_equation"></span><dl> <dt>**角色 \_ 系統方程式 \_**</dt> </dl>                               | 物件代表數學方程式。<br/>                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="ROLE_SYSTEM_GRAPHIC"></span><span id="role_system_graphic"></span><dl> <dt>**角色 \_ 系統 \_ 圖形**</dt> </dl>                                  | 物件代表圖片。<br/>                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="ROLE_SYSTEM_GRIP"></span><span id="role_system_grip"></span><dl> <dt>**角色 \_ 系統 \_ 抓住**</dt> </dl>                                           | 物件代表特殊的滑鼠指標，可讓使用者操作使用者介面元素（例如 windows）。 其中一個範例牽涉到將視窗的右下角拖曳來調整視窗大小。<br/>                                                                                                                                                                                                                    |
| <span id="ROLE_SYSTEM_GROUPING"></span><span id="role_system_grouping"></span><dl> <dt>**角色 \_ 系統 \_ 群組**</dt> </dl>                               | 物件會以邏輯方式將其他物件分組。 群組物件與其包含的物件之間不一定會有父子式關聯性。<br/>                                                                                                                                                                                                                                                                           |
| <span id="ROLE_SYSTEM_HELPBALLOON"></span><span id="role_system_helpballoon"></span><dl> <dt>**角色 \_ 系統 \_ HELPBALLOON**</dt> </dl>                      | 物件會以工具提示或說明氣球的形式來顯示說明主題。<br/>                                                                                                                                                                                                                                                                                                                                                    |
| <span id="ROLE_SYSTEM_HOTKEYFIELD"></span><span id="role_system_hotkeyfield"></span><dl> <dt>**角色 \_ 系統 \_ HOTKEYFIELD**</dt> </dl>                      | 物件代表鍵盤快速鍵欄位，可讓使用者輸入組合或按鍵順序。<br/>                                                                                                                                                                                                                                                                                                        |
| <span id="ROLE_SYSTEM_INDICATOR"></span><span id="role_system_indicator"></span><dl> <dt>**角色 \_ 系統 \_ 指標**</dt> </dl>                            | 物件代表指向目前專案的指標，例如指標圖形。<br/>                                                                                                                                                                                                                                                                                                                               |
| <span id="ROLE_SYSTEM_IPADDRESS"></span><span id="role_system_ipaddress"></span><dl> <dt>**角色 \_ 系統 \_ IPADDRESS**</dt> </dl>                            | 物件代表針對 IP 位址所設計的編輯控制項。 編輯控制項分為各區段，而每個區段都是 IP 位址的特定部分。<br/>                                                                                                                                                                                                                                                              |
| <span id="ROLE_SYSTEM_LINK"></span><span id="role_system_link"></span><dl> <dt>**角色 \_ 系統 \_ 連結**</dt> </dl>                                           | 物件代表其他內容的連結。 這個物件看起來像是文字或圖形，但動作卻像是按鈕。<br/>                                                                                                                                                                                                                                                                                                     |
| <span id="ROLE_SYSTEM_LIST"></span><span id="role_system_list"></span><dl> <dt>**角色 \_ 系統 \_ 清單**</dt> </dl>                                           | 物件代表清單方塊，可讓使用者選取一或多個專案。<br/>                                                                                                                                                                                                                                                                                                                                              |
| <span id="ROLE_SYSTEM_LISTITEM"></span><span id="role_system_listitem"></span><dl> <dt>**角色 \_ 系統 \_**</dt> </dl>                               | 物件代表清單方塊中的專案，或下拉式方塊、下拉式清單方塊或下拉式方塊的清單部分中的專案。<br/>                                                                                                                                                                                                                                                                                                |
| <span id="ROLE_SYSTEM_MENUBAR"></span><span id="role_system_menubar"></span><dl> <dt>**角色 \_ 系統 \_ 功能表列**</dt> </dl>                                  | 物件表示功能表列 (位於視窗) 的標題列下方，使用者會從中選取功能表。<br/>                                                                                                                                                                                                                                                                                                              |
| <span id="ROLE_SYSTEM_MENUITEM"></span><span id="role_system_menuitem"></span><dl> <dt>**角色 \_ 系統 \_ MENUITEM**</dt> </dl>                               | 物件代表功能表項目：使用者可以選擇執行命令的功能表項目、選取選項，或顯示其他功能表。 在功能上，功能表項目相當於按鈕、選項按鈕、核取方塊或功能表。<br/>                                                                                                                                                                                |
| <span id="ROLE_SYSTEM_MENUPOPUP"></span><span id="role_system_menupopup"></span><dl> <dt>**角色 \_ 系統 \_ MENUPOPUP**</dt> </dl>                            | 物件表示功能表：選項清單，各有特定的動作。 所有功能表類型都必須有角色，包括從功能表列選取時所顯示的下拉式功能表;然後按一下滑鼠右鍵，即可顯示快捷方式功能表。<br/>                                                                                                                                                     |
| <span id="ROLE_SYSTEM_OUTLINE"></span><span id="role_system_outline"></span><dl> <dt>**角色 \_ 系統 \_ 大綱**</dt> </dl>                                  | 物件代表大綱或樹狀結構，例如樹狀檢視控制項，它會顯示階層式清單，並允許使用者展開和折迭分支。<br/>                                                                                                                                                                                                                                                     |
| <span id="ROLE_SYSTEM_OUTLINEBUTTON"></span><span id="role_system_outlinebutton"></span><dl> <dt>**角色 \_ 系統 \_ OUTLINEBUTTON**</dt> </dl>                | 物件代表導覽的專案，例如大綱專案。 向上鍵和向下鍵可用來導覽大綱。 不過，當按下左右箭號時，這些功能表會展開或折迭，而不是按下空格鍵或 ENTER 鍵，且專案具有焦點。 <br/>                                                                                          |
| <span id="ROLE_SYSTEM_OUTLINEITEM"></span><span id="role_system_outlineitem"></span><dl> <dt>**角色 \_ 系統 \_ OUTLINEITEM**</dt> </dl>                      | 物件代表大綱或樹狀結構中的專案。<br/>                                                                                                                                                                                                                                                                                                                                                                |
| <span id="ROLE_SYSTEM_PAGETAB"></span><span id="role_system_pagetab"></span><dl> <dt>**角色 \_ 系統 \_ PAGETAB**</dt> </dl>                                  | 物件代表頁面索引標籤。頁面索引標籤控制項的唯一子系是角色 \_ 系統 \_ 群組物件，其中包含相關頁面的內容。<br/>                                                                                                                                                                                                                                                                       |
| <span id="ROLE_SYSTEM_PAGETABLIST"></span><span id="role_system_pagetablist"></span><dl> <dt>**角色 \_ 系統 \_ PAGETABLIST**</dt> </dl>                      | 物件代表頁面索引標籤控制項的容器。<br/>                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="ROLE_SYSTEM_PANE"></span><span id="role_system_pane"></span><dl> <dt>**角色 \_ 系統 \_ 窗格**</dt> </dl>                                           | 物件表示框架或文件視窗內的窗格。 使用者可在窗格之間和目前窗格的內容之內巡覽，但無法在不同窗格內的項目之間巡覽。 因此，窗格代表比框架或文件視窗還低的群組層級，但比個別控制項更高。 使用者在窗格之間巡覽的方式是依照內容而定，可按下 TAB、F6 或 CTRL+TAB 鍵。<br/> |
| <span id="ROLE_SYSTEM_PROGRESSBAR"></span><span id="role_system_progressbar"></span><dl> <dt>**角色 \_ 系統 \_ PROGRESSBAR**</dt> </dl>                      | 物件代表進度列，它會動態顯示正在進行的作業中有多少已完成。 此控制項不需要使用者輸入。<br/>                                                                                                                                                                                                                                                                           |
| <span id="ROLE_SYSTEM_PROPERTYPAGE"></span><span id="role_system_propertypage"></span><dl> <dt>**角色 \_ 系統 \_ PROPERTYPAGE**</dt> </dl>                   | 物件代表屬性工作表。<br/>                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="ROLE_SYSTEM_PUSHBUTTON"></span><span id="role_system_pushbutton"></span><dl> <dt>**角色 \_ 系統 \_ 按鍵**</dt> </dl>                         | 物件代表按鈕控制項。<br/>                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="ROLE_SYSTEM_RADIOBUTTON"></span><span id="role_system_radiobutton"></span><dl> <dt>**角色 \_ 系統 \_ 選項按鈕**</dt> </dl>                      | 物件表示選項按鈕 (先前為選項按鈕) 。 它是一組互斥選項的其中一個。 共用相同父系並具有這個屬性的所有物件，都會假設為單一互斥群組的一部分。 若要將這些物件分成不同的群組，請使用角色 \_ 系統 \_ 群組物件。<br/>                                                                                     |
| <span id="ROLE_SYSTEM_ROW"></span><span id="role_system_row"></span><dl> <dt>**角色 \_ 系統資料 \_ 列**</dt> </dl>                                              | 物件代表資料表內的資料列。<br/>                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="ROLE_SYSTEM_ROWHEADER"></span><span id="role_system_rowheader"></span><dl> <dt>**角色 \_ 系統 \_ ROWHEADER**</dt> </dl>                            | 物件表示資料列標頭，此標頭會提供資料表資料列的視覺標籤。<br/>                                                                                                                                                                                                                                                                                                                                            |
| <span id="ROLE_SYSTEM_SCROLLBAR"></span><span id="role_system_scrollbar"></span><dl> <dt>**角色 \_ 系統 \_ 捲軸**</dt> </dl>                            | 物件代表垂直或水準捲軸，其為工作區的一部分或用於控制項。<br/>                                                                                                                                                                                                                                                                                                          |
| <span id="ROLE_SYSTEM_SEPARATOR"></span><span id="role_system_separator"></span><dl> <dt>**角色 \_ 系統 \_ 分隔符號**</dt> </dl>                            | 物件是用來以視覺方式將空間分割成兩個區域。 分隔符號物件的範例包括分隔符號功能表項目，以及在視窗內分割分割窗格的橫條。<br/>                                                                                                                                                                                                                                              |
| <span id="ROLE_SYSTEM_SLIDER"></span><span id="role_system_slider"></span><dl> <dt>**角色 \_ 系統 \_ 滑杆**</dt> </dl>                                     | 物件代表滑杆，可讓使用者在最小值與最大值之間，以特別遞增的方式調整設定。<br/>                                                                                                                                                                                                                                                                                        |
| <span id="ROLE_SYSTEM_SOUND"></span><span id="role_system_sound"></span><dl> <dt>**角色 \_ 系統 \_ 音效**</dt> </dl>                                        | 物件代表與各種系統事件相關聯的系統音效。<br/>                                                                                                                                                                                                                                                                                                                                         |
| <span id="ROLE_SYSTEM_SPINBUTTON"></span><span id="role_system_spinbutton"></span><dl> <dt>**角色系統已進行數值 \_ \_ 調節**</dt> </dl>                         | 物件表示微調方塊，這是一個控制項，可讓使用者遞增或遞減與微調方塊相關聯之個別「合作者」控制項中所顯示的值。<br/>                                                                                                                                                                                                                                   |
| <span id="ROLE_SYSTEM_SPLITBUTTON"></span><span id="role_system_splitbutton"></span><dl> <dt>**角色 \_ 系統 \_ SPLITBUTTON**</dt> </dl>                      | 物件代表工具列上的按鈕，該按鈕的下拉式清單圖示會直接與按鈕相鄰。<br/>                                                                                                                                                                                                                                                                                                           |
| <span id="ROLE_SYSTEM_STATICTEXT"></span><span id="role_system_statictext"></span><dl> <dt>**角色 \_ 系統 \_ STATICTEXT**</dt> </dl>                         | 物件代表唯讀文字，例如，其他控制項的標籤或對話方塊中的指示。 靜態文字不能修改或者選取。<br/>                                                                                                                                                                                                                                                                          |
| <span id="ROLE_SYSTEM_STATUSBAR"></span><span id="role_system_statusbar"></span><dl> <dt>**角色 \_ 系統 \_ 狀態列**</dt> </dl>                            | 物件代表狀態列，也就是視窗底部的區域，顯示目前作業的相關資訊、應用程式的狀態，或選取的物件。 狀態列有多個欄位，會顯示不同類型的資訊。<br/>                                                                                                                                                    |
| <span id="ROLE_SYSTEM_TABLE"></span><span id="role_system_table"></span><dl> <dt>**角色 \_ 系統 \_ 資料表**</dt> </dl>                                        | 物件表示包含資料列和資料行的資料表，以及選擇性的資料列標頭和資料行標頭。<br/>                                                                                                                                                                                                                                                                                                       |
| <span id="ROLE_SYSTEM_TEXT"></span><span id="role_system_text"></span><dl> <dt>**角色 \_ 系統 \_ 文字**</dt> </dl>                                           | 物件表示允許編輯或指定為唯讀的可選取文字。<br/>                                                                                                                                                                                                                                                                                                                                        |
| <span id="ROLE_SYSTEM_TITLEBAR"></span><span id="role_system_titlebar"></span><dl> <dt>**角色 \_ 系統 \_ 標題列**</dt> </dl>                               | 物件代表視窗的標題或標題列。<br/>                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="ROLE_SYSTEM_TOOLBAR"></span><span id="role_system_toolbar"></span><dl> <dt>**角色 \_ 系統 \_ 工具列**</dt> </dl>                                  | 物件代表工具列，這是可讓您輕鬆存取常用功能的控制項群組。<br/>                                                                                                                                                                                                                                                                                                       |
| <span id="ROLE_SYSTEM_TOOLTIP"></span><span id="role_system_tooltip"></span><dl> <dt>**角色 \_ 系統 \_ 工具提示**</dt> </dl>                                  | 物件表示提供實用提示的工具提示。<br/>                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="ROLE_SYSTEM_WHITESPACE"></span><span id="role_system_whitespace"></span><dl> <dt>**角色 \_ 系統 \_ 空白字元**</dt> </dl>                         | 物件代表其他物件之間的空格。<br/>                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="ROLE_SYSTEM_WINDOW"></span><span id="role_system_window"></span><dl> <dt>**角色 \_ 系統 \_ 視窗**</dt> </dl>                                     | 物件代表視窗框架，其中包含子物件，例如標題列、用戶端，以及視窗的其他物件。<br/>                                                                                                                                                                                                                                                                                              |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Oleacc。h</dt> </dl> |



 

 





