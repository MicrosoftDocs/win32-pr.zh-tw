---
title: '功能表 (功能表和其他資源) '
description: 本節討論功能表。
ms.assetid: vs|winui|~\winui\windowsuserinterface\resources\menus.htm
keywords:
- 資源、功能表
- 功能表，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c376aa1d2f55fa482ca7a2f98f57ae15236bf26b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104383522"
---
# <a name="menus-menus-and-other-resources"></a>功能表 (功能表和其他資源) 

本節說明功能表並說明其使用方式。

### <a name="in-this-section"></a>本節內容



| Name                                 | 描述                                                  |
|--------------------------------------|--------------------------------------------------------------|
| [關於功能表](about-menus.md)       | 討論功能表。<br/>                                  |
| [使用功能表](using-menus.md)       | 提供與功能表相關之工作的程式碼範例。<br/> |
| [功能表參考](menu-reference.md) | 包含 API 參考。<br/>                       |



 

### <a name="menu-functions"></a>功能表函數



| Name                                                             | 描述                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua)                                 | 將新專案附加至指定功能表列、下拉式功能表、子功能表或快捷方式功能表的結尾。 您可以使用這個函數來指定功能表項目的內容、外觀和行為。 <br/>                                                                                                                                                                                                  |
| [**CheckMenuItem**](/windows/desktop/api/Winuser/nf-winuser-checkmenuitem)                           | 將指定之功能表項目的核取記號屬性狀態設定為 [已選取] 或 [清除]。<br/>                                                                                                                                                                                                                                                                                                      |
| [**CheckMenuRadioItem**](/windows/desktop/api/Winuser/nf-winuser-checkmenuradioitem)                 | 檢查指定的功能表項目，並使其成為單選項目。 同時，此函式會清除相關聯群組中的所有其他功能表項目，並清除這些專案的選項按鈕類型旗標。<br/>                                                                                                                                                                                                    |
| [**CreateMenu**](/windows/desktop/api/Winuser/nf-winuser-createmenu)                                 | 建立功能表。 此功能表一開始是空的，但您可以使用 [**InsertMenuItem**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema)、 [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua)和 [**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua) 函數來填入功能表項目。 <br/>                                                                                                                                                                        |
| [**CreatePopupMenu**](/windows/desktop/api/Winuser/nf-winuser-createpopupmenu)                       | 建立下拉式選單、子功能表或快捷方式功能表。 此功能表一開始是空的。 您可以使用 [**InsertMenuItem**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema) 函數來插入或附加功能表項目。 您也可以使用 [**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua) 函式來插入功能表項目，並使用 [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua) 函數來附加功能表項目。<br/>                                                  |
| [**DeleteMenu**](/windows/desktop/api/Winuser/nf-winuser-deletemenu)                                 | 從指定的功能表中刪除專案。 如果功能表項目開啟功能表或子功能表，此函式會終結功能表或子功能表的控制碼，並釋出功能表或子功能表所使用的記憶體。 <br/>                                                                                                                                                                                                     |
| [**DestroyMenu**](/windows/desktop/api/Winuser/nf-winuser-destroymenu)                               | 終結指定的功能表，並釋出功能表所佔用的任何記憶體。 <br/>                                                                                                                                                                                                                                                                                                                          |
| [**DrawMenuBar**](/windows/desktop/api/Winuser/nf-winuser-drawmenubar)                               | 重新繪製指定之視窗的功能表列。 如果功能表列在系統建立視窗之後變更，則必須呼叫此函式來繪製已變更的功能表列。 <br/>                                                                                                                                                                                                                         |
| [**EnableMenuItem**](/windows/desktop/api/Winuser/nf-winuser-enablemenuitem)                         | 啟用、停用或停用指定功能表項目的灰色。 <br/>                                                                                                                                                                                                                                                                                                                                              |
| [**EndMenu**](/windows/desktop/api/Winuser/nf-winuser-endmenu)                                       | 結束呼叫執行緒的現用功能表。<br/>                                                                                                                                                                                                                                                                                                                                                             |
| [**GetMenu**](/windows/desktop/api/Winuser/nf-winuser-getmenu)                                       | 抓取指派給指定視窗之功能表的控制碼。 <br/>                                                                                                                                                                                                                                                                                                                                  |
| [**GetMenuBarInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenubarinfo)                         | 抓取指定功能表列的相關資訊。<br/>                                                                                                                                                                                                                                                                                                                                                |
| [**GetMenuCheckMarkDimensions**](/windows/desktop/api/Winuser/nf-winuser-getmenucheckmarkdimensions) | 抓取預設核取記號點陣圖的維度。 系統會在選取的功能表項目旁邊顯示此點陣圖。 在呼叫 [**SetMenuItemBitmaps**](/windows/desktop/api/Winuser/nf-winuser-setmenuitembitmaps) 函式來取代功能表項目的預設核取記號點陣圖之前，應用程式必須藉由呼叫 [**GetMenuCheckMarkDimensions**](/windows/desktop/api/Winuser/nf-winuser-getmenucheckmarkdimensions)來判斷正確的點陣圖大小。 <br/> |
| [**GetMenuDefaultItem**](/windows/desktop/api/Winuser/nf-winuser-getmenudefaultitem)                 | 決定指定功能表上的預設功能表項目。<br/>                                                                                                                                                                                                                                                                                                                                            |
| [**GetMenuInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuinfo)                               | 抓取指定功能表的相關資訊。<br/>                                                                                                                                                                                                                                                                                                                                                      |
| [**GetMenuItemCount**](/windows/desktop/api/Winuser/nf-winuser-getmenuitemcount)                     | 抓取指定功能表中的專案數。 <br/>                                                                                                                                                                                                                                                                                                                                              |
| [**GetMenuItemID**](/windows/desktop/api/Winuser/nf-winuser-getmenuitemid)                           | 抓取功能表中位於指定位置之功能表項目的功能表項目識別碼。 <br/>                                                                                                                                                                                                                                                                                                    |
| [**GetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa)                       | 抓取功能表項目的相關資訊。<br/>                                                                                                                                                                                                                                                                                                                                                           |
| [**GetMenuItemRect**](/windows/desktop/api/Winuser/nf-winuser-getmenuitemrect)                       | 抓取指定功能表項目的周框。<br/>                                                                                                                                                                                                                                                                                                                                      |
| [**GetMenuState**](/windows/desktop/api/Winuser/nf-winuser-getmenustate)                             | 抓取與指定的功能表項目相關聯的功能表旗標。 如果功能表項目開啟子功能表，此函數也會傳回子功能表中的專案數。 <br/>                                                                                                                                                                                                                                |
| [**GetMenuString**](/windows/desktop/api/Winuser/nf-winuser-getmenustringa)                           | 將指定之功能表項目的文字字串複製到指定的緩衝區。 <br/>                                                                                                                                                                                                                                                                                                                      |
| [**GetSubMenu**](/windows/desktop/api/Winuser/nf-winuser-getsubmenu)                                 | 抓取由指定功能表項目啟動的下拉式功能表或子功能表的控制碼。 <br/>                                                                                                                                                                                                                                                                                                         |
| [**GetSystemMenu**](/windows/desktop/api/Winuser/nf-winuser-getsystemmenu)                           | 讓應用程式存取視窗功能表 (也稱為 [系統] 功能表或 [控制] 功能表) 進行複製和修改。 <br/>                                                                                                                                                                                                                                                                  |
| [**HiliteMenuItem**](/windows/desktop/api/Winuser/nf-winuser-hilitemenuitem)                         | 從功能表列中的專案反白顯示或移除反白顯示。 <br/>                                                                                                                                                                                                                                                                                                                                |
| [**InsertMenuItem**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema)                         | 在功能表中的指定位置插入新的功能表項目。<br/>                                                                                                                                                                                                                                                                                                                                       |
| [**IsMenu**](/windows/desktop/api/Winuser/nf-winuser-ismenu)                                         | 判斷控制碼是否為功能表控制碼。 <br/>                                                                                                                                                                                                                                                                                                                                                     |
| [**LoadMenu**](/windows/desktop/api/Winuser/nf-winuser-loadmenua)                                     | 從與應用程式實例相關聯的可執行檔 ( .exe) 檔案載入指定的功能表資源。 <br/>                                                                                                                                                                                                                                                                                        |
| [**LoadMenuIndirect**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta)                     | 將指定的功能表範本載入記憶體中。 <br/>                                                                                                                                                                                                                                                                                                                                                      |
| [**MenuItemFromPoint**](/windows/desktop/api/Winuser/nf-winuser-menuitemfrompoint)                   | 判斷哪個功能表項目（如果有的話）位於指定的位置。<br/>                                                                                                                                                                                                                                                                                                                                  |
| [**ModifyMenu**](/windows/desktop/api/Winuser/nf-winuser-modifymenua)                                 | 變更現有的功能表項目。 這個函式是用來指定功能表項目的內容、外觀和行為。 <br/>                                                                                                                                                                                                                                                                           |
| [**RemoveMenu**](/windows/desktop/api/Winuser/nf-winuser-removemenu)                                 | 從指定的功能表刪除功能表項目或卸離子功能表。 如果功能表項目開啟下拉式功能表或子功能表， [**RemoveMenu**](/windows/desktop/api/Winuser/nf-winuser-removemenu) 就不會摧毀功能表或其控點，讓功能表可以重複使用。 在呼叫此函式之前， [**GetSubMenu**](/windows/desktop/api/Winuser/nf-winuser-getsubmenu) 函式應該取得下拉式功能表或子功能表的控制碼。 <br/>                         |
| [**SetMenu**](/windows/desktop/api/Winuser/nf-winuser-setmenu)                                       | 將新的功能表指派給指定的視窗。 <br/>                                                                                                                                                                                                                                                                                                                                                       |
| [**SetMenuDefaultItem**](/windows/desktop/api/Winuser/nf-winuser-setmenudefaultitem)                 | 設定指定功能表的預設功能表項目。<br/>                                                                                                                                                                                                                                                                                                                                                 |
| [**SetMenuInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuinfo)                               | 設定指定之功能表的資訊。<br/>                                                                                                                                                                                                                                                                                                                                                             |
| [**SetMenuItemBitmaps**](/windows/desktop/api/Winuser/nf-winuser-setmenuitembitmaps)                 | 將指定的點陣圖與功能表項目產生關聯。 無論是選取或清除功能表項目，系統都會在功能表項目旁邊顯示適當的點陣圖。 <br/>                                                                                                                                                                                                                                   |
| [**SetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa)                       | 變更功能表項目的相關資訊。<br/>                                                                                                                                                                                                                                                                                                                                                             |
| [**Trackpopupmenu 讓**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu)                         | 在指定的位置顯示快捷方式功能表，並追蹤功能表上的專案選取專案。 快捷方式功能表可以出現在螢幕上的任何位置。<br/>                                                                                                                                                                                                                                             |
| [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex)                     | 在指定的位置顯示快捷方式功能表，並在快捷方式功能表上追蹤選取的專案。 快捷方式功能表可以出現在螢幕上的任何位置。<br/>                                                                                                                                                                                                                                    |



 

下列函式已過時。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Name</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-insertmenua"><strong>InsertMenu</strong></a></td>
<td>在功能表中插入新的功能表項目，然後在功能表中移動其他專案。
<blockquote>
[!Note]<br />
<a href="/windows/desktop/api/Winuser/nf-winuser-insertmenua"><strong>InsertMenu</strong></a>函式已被<a href="/windows/desktop/api/Winuser/nf-winuser-insertmenuitema"><strong>InsertMenuItem</strong></a>函數取代。 但是，如果您不需要<strong>InsertMenuItem</strong>的任何擴充功能，仍然可以使用<strong>InsertMenu</strong>。
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

### <a name="menu-notifications"></a>功能表通知



| Name                                                  | 描述                                                                                                                                                                          |
|-------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ 命令**](wm-command.md)                     | 當使用者從功能表中選取命令專案時、控制項將通知訊息傳送至其父視窗，或翻譯快速鍵按鍵時傳送。 <br/> |
| [**WM \_ CONTEXTMENU**](wm-contextmenu.md)             | 通知視窗，使用者按一下滑鼠右鍵， (在視窗中以 *滑鼠右鍵按一下*) 。<br/>                                                                            |
| [**WM \_ ENTERMENULOOP**](wm-entermenuloop.md)         | 通知應用程式的主視窗程式，表示已輸入功能表強制回應迴圈。 <br/>                                                                                  |
| [**WM \_ EXITMENULOOP**](wm-exitmenuloop.md)           | 通知應用程式的主視窗程式，表示已結束功能表強制回應迴圈。 <br/>                                                                                   |
| [**WM \_ GETTITLEBARINFOEX**](wm-gettitlebarinfoex.md) | 傳送至要求延伸的標題列資訊。 視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。<br/>                                  |
| [**WM \_ MENUCOMMAND**](wm-menucommand.md)             | 當使用者從功能表進行選取時傳送。 <br/>                                                                                                                        |
| [**WM \_ MENUDRAG**](wm-menudrag.md)                   | 當使用者拖曳功能表項目時，傳送至拖放功能表的擁有者。 <br/>                                                                                               |
| [**WM \_ MENUGETOBJECT**](wm-menugetobject.md)         | 當滑鼠游標進入功能表項目，或從專案的中央移至專案的頂端或底部時，傳送至拖放功能表的擁有者。 <br/>                |
| [**WM \_ MENURBUTTONUP**](wm-menurbuttonup.md)         | 當使用者放開滑鼠右鍵，而游標位於功能表項目上時傳送。 <br/>                                                                                   |
| [**WM \_ NEXTMENU**](wm-nextmenu.md)                   | 當使用向右鍵或向左鍵切換至功能表列和系統功能表時，傳送至應用程式。 <br/>                                                      |
| [**WM \_ UNINITMENUPOPUP**](wm-uninitmenupopup.md)     | 當下拉式選單或子功能表已終結時傳送。 <br/>                                                                                                                |



 

### <a name="menu-structures"></a>功能表結構



| Name                                                       | 描述                                                                                                                                                     |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MDINEXTMENU**](/windows/win32/api/winuser/ns-winuser-mdinextmenu)                         | 包含要啟用之功能表的相關資訊。 <br/>                                                                                                |
| [**MENUBARINFO**](/windows/win32/api/winuser/ns-winuser-menubarinfo)                         | 包含功能表列資訊。<br/>                                                                                                                       |
| [**MENUEX \_ 範本 \_ 標頭**](menuex-template-header.md) | 定義擴充功能表範本的標頭。 此結構定義僅供說明之用;它不會出現在任何標準標頭檔中。 <br/> |
| [**MENUEX \_ 範本 \_ 專案**](menuex-template-item.md)     | 定義擴充功能表範本中的功能表項目。 此結構定義僅供說明之用;它不會出現在任何標準標頭檔中。<br/>  |
| [**MENUGETOBJECTINFO**](/windows/win32/api/winuser/ns-winuser-menugetobjectinfo)             | 包含滑鼠游標所在功能表的相關資訊。<br/>                                                                                     |
| [**MENUINFO**](/windows/win32/api/winuser/ns-winuser-menuinfo)                               | 包含功能表的相關資訊。<br/>                                                                                                                   |
| [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa)                       | 包含功能表項目的相關資訊。 <br/>                                                                                                             |
| [**MENUITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplate)               | 在功能表範本中定義功能表項目。 <br/>                                                                                                             |
| [**MENUITEMTEMPLATEHEADER**](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplateheader)   | 定義功能表範本的標頭。 完整的功能表範本是由標頭和一或多個功能表項目清單所組成。 <br/>                              |
| [**TPMPARAMS**](/windows/win32/api/winuser/ns-winuser-tpmparams)                             | 包含 [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) 函數的擴充參數。<br/>                                                          |



 

 

