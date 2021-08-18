---
title: " 內容工作表頁"
description: 本章節包含與屬性工作表搭配使用之程式設計項目的相關資訊。
ms.assetid: f4fa9815-eab8-4b0b-ae5f-0bce4374223a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d50661ece6985c16f299b514fa59068bf06f115b49c0f0bbea783cf637c2c921
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119826028"
---
# <a name="property-sheet"></a> 內容工作表頁

本章節包含與屬性工作表搭配使用之程式設計項目的相關資訊。

### <a name="overviews"></a>概觀



| 主題                                              | 目錄                                                                                                                    |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [關於屬性工作表](property-sheets.md)       | *屬性工作表* 是一種視窗，可讓使用者查看和編輯專案的屬性。<br/>                  |
| [建立嚮導](wizards.md)                    | Wizard 是一種屬性工作表，可提供簡單且強大的方式來引導使用者完成程式。<br/> |
| [使用屬性工作表](using-property-sheets.md) | 本節提供使用屬性工作表的執行詳細資料與範例程式碼。<br/>                     |



 

### <a name="functions"></a>函式



| 主題                                                        | 目錄                                                                                                                                                                                                                                                   |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [*AddPropSheetPageProc*](/windows/desktop/api/Prsht/nc-prsht-lpfnaddpropsheetpage)           | 指定應用程式定義的回呼函式，屬性工作表擴充功能會使用此函式將頁面加入至屬性工作表。<br/>                                                                                                                      |
| [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea)   | 為屬性工作表建立新的頁面。<br/>                                                                                                                                                                                                        |
| [**DestroyPropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-destroypropertysheetpage) | 終結屬性工作表頁面。 應用程式必須針對未傳遞至 [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) 函式的頁面呼叫此函數。<br/>                                                                              |
| [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta)                       | 建立屬性工作表，並新增在指定的屬性工作表標頭結構中所定義的頁面。<br/>                                                                                                                                           |
| [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka)                 | 指定應用程式定義的回呼函式，該函式會在頁面建立時以及即將終結時呼叫。 應用程式可以使用此函式來執行頁面的初始化和清除作業。<br/> |
| [*PropSheetProc*](/windows/desktop/api/Prsht/nc-prsht-pfnpropsheetcallback)                         | 建立和初始化屬性工作表時，系統所呼叫的應用程式定義回呼函數。<br/>                                                                                                                        |



 

### <a name="messages"></a>訊息



| 主題                                                               | 目錄                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PSM \_ ADDPAGE**](psm-addpage.md)                                 | 將新頁面加入現有屬性工作表的結尾。 您可以使用 [**PropSheet \_ AddPage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_addpage) 宏明確地傳送此訊息。<br/>                                                                                                |
| [**適用的 PSM \_**](psm-apply.md)                                     | 模擬 **[套用] 按鈕的** 選取專案，表示一或多個頁面已變更，而且需要驗證和記錄變更。<br/>                                                                                                                   |
| [**PSM \_ CANCELTOCLOSE**](psm-canceltoclose.md)                     | 當應用程式在最近的 PSN 套用無法取消的通知之後 [， \_ ](psn-apply.md) 由應用程式傳送。 您可以使用 [**PropSheet \_ CancelToClose**](/windows/desktop/api/Prsht/nf-prsht-propsheet_canceltoclose) 宏明確地傳送此訊息。<br/> |
| [**\_已變更 PSM**](psm-changed.md)                                 | 通知屬性工作表，頁面中的資訊已變更。 您可以使用 [**PropSheet \_ Changed**](/windows/desktop/api/Prsht/nf-prsht-propsheet_changed) 宏明確地傳送此訊息。<br/>                                                                                         |
| [**PSM \_ ENABLEWIZBUTTONS**](psm-enablewizbuttons.md)               | 啟用或停用 Aero wizard 中的任何標準按鈕。 您可以明確地傳送此訊息，或使用 [**PropSheet \_ EnableWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_enablewizbuttons) 宏。<br/>                                                                          |
| [**PSM \_ GETCURRENTPAGEHWND**](psm-getcurrentpagehwnd.md)           | 抓取屬性工作表目前頁面的視窗控制碼。 您可以使用 [**PropSheet \_ GetCurrentPageHwnd**](/windows/desktop/api/Prsht/nf-prsht-propsheet_getcurrentpagehwnd) 宏明確地傳送此訊息。<br/>                                                          |
| [**PSM \_ GETRESULT**](psm-getresult.md)                             | 由非強制回應屬性工作表用來取出 [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta)傳回的強制回應屬性工作表資訊。 您可以明確地傳送此訊息，或使用 [**PropSheet \_ GetResult**](/windows/desktop/api/Prsht/nf-prsht-propsheet_getresult) 宏。<br/>                 |
| [**PSM \_ GETTABCONTROL**](psm-gettabcontrol.md)                     | 抓取屬性工作表之索引標籤控制項的控制碼。 您可以使用 [**PropSheet \_ GetTabControl**](/windows/desktop/api/Prsht/nf-prsht-propsheet_gettabcontrol) 宏明確地傳送此訊息。<br/>                                                                                 |
| [**PSM \_ HWNDTOINDEX**](psm-hwndtoindex.md)                         | 採用屬性工作表頁面的視窗控制碼，並傳回其以零為基底的索引。 您可以明確地傳送此訊息，或使用 [**PropSheet \_ HwndToIndex**](/windows/desktop/api/Prsht/nf-prsht-propsheet_hwndtoindex) 宏。<br/>                                                                  |
| [**PSM \_ IDTOINDEX**](psm-idtoindex.md)                             | 取得屬性工作表頁面的資源識別碼，並傳回其以零為基底的索引。 您可以明確地傳送此訊息，或使用 [**PropSheet \_ IdToIndex**](/windows/desktop/api/Prsht/nf-prsht-propsheet_idtoindex) 宏。<br/>                                                                          |
| [**PSM \_ INDEXTOHWND**](psm-indextohwnd.md)                         | 取得屬性工作表頁面的索引，並傳回其視窗控制碼。 您可以明確地傳送此訊息，或使用 [**PropSheet \_ IndexToHwnd**](/windows/desktop/api/Prsht/nf-prsht-propsheet_indextohwnd) 宏。<br/>                                                                               |
| [**PSM \_ INDEXTOID**](psm-indextoid.md)                             | 取得屬性工作表頁面的索引，並傳回其資源識別碼。 您可以明確地傳送此訊息，或使用 [**PropSheet \_ IndexToId**](/windows/desktop/api/Prsht/nf-prsht-propsheet_indextoid) 宏。<br/>                                                                                     |
| [**PSM \_ INDEXTOPAGE**](psm-indextopage.md)                         | 取得屬性工作表頁面的索引，並傳回其 HPROPSHEETPAGE 控制碼。 您可以明確地傳送此訊息，或使用 [**PropSheet \_ IndexToPage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_indextopage) 宏。<br/>                                                                       |
| [**PSM \_ INSERTPAGE**](psm-insertpage.md)                           | 將新頁面插入現有的屬性工作表中。 頁面可以插入指定的索引或指定的頁面之後。 您可以使用 [**PropSheet \_ InsertPage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_insertpage) 宏明確地傳送此訊息。<br/>                |
| [**PSM \_ ISDIALOGMESSAGE**](psm-isdialogmessage.md)                 | 將訊息傳遞至屬性工作表對話方塊，並指出對話方塊是否已處理訊息。 您可以使用 [**PropSheet \_ IsDialogMessage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_isdialogmessage) 宏明確地傳送此訊息。<br/>                              |
| [**PSM \_ PAGETOINDEX**](psm-pagetoindex.md)                         | 取得屬性工作表頁面的 HPROPSHEETPAGE 控制碼，並傳回其以零為基底的索引。 您可以明確地傳送此訊息，或使用 [**PropSheet \_ PageToIndex**](/windows/desktop/api/Prsht/nf-prsht-propsheet_pagetoindex) 宏。<br/>                                                          |
| [**PSM \_ PRESSBUTTON**](psm-pressbutton.md)                         | 模擬屬性工作表按鈕的選取專案。 您可以使用 [**PropSheet \_ PressButton**](/windows/desktop/api/Prsht/nf-prsht-propsheet_pressbutton) 宏明確地傳送此訊息。<br/>                                                                                              |
| [**PSM \_ QUERYSIBLINGS**](psm-querysiblings.md)                     | 傳送至屬性工作表，然後將訊息轉送到其每個頁面。 您可以使用 [**PropSheet \_ QuerySiblings**](/windows/desktop/api/Prsht/nf-prsht-propsheet_querysiblings) 宏明確地傳送此訊息。<br/>                                                              |
| [**PSM \_ REBOOTSYSTEM**](psm-rebootsystem.md)                       | 指出需要重新開機系統，變更才會生效。 您可以明確地傳送 [**PSM \_ REBOOTSYSTEM**](psm-rebootsystem.md) 訊息或使用 [**PropSheet \_ REBOOTSYSTEM**](/windows/desktop/api/Prsht/nf-prsht-propsheet_rebootsystem) 宏。<br/>                        |
| [**PSM \_ RECALCPAGESIZES**](psm-recalcpagesizes.md)                 | 新增或移除頁面之後，重新計算標準或 wizard 屬性工作表的頁面大小。 您可以明確地傳送此訊息，或使用 [**PropSheet \_ RecalcPageSizes**](/windows/desktop/api/Prsht/nf-prsht-propsheet_recalcpagesizes) 宏。<br/>                                     |
| [**PSM \_ REMOVEPAGE**](psm-removepage.md)                           | 從屬性工作表移除頁面。 您可以使用 [**PropSheet \_ RemovePage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_removepage) 宏明確地傳送此訊息。<br/>                                                                                                              |
| [**PSM \_ RESTARTWINDOWS**](psm-restartwindows.md)                   | 指出 Windows 需要重新開機，變更才會生效。<br/>                                                                                                                                                                                         |
| [**PSM \_ SETBUTTONTEXT**](psm-setbuttontext.md)                     | 設定 Aero wizard 中按鈕的文字。 您可以使用 [**PropSheet \_ SetButtonText**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setbuttontext) 宏明確地傳送此訊息。<br/>                                                                                                 |
| [**PSM \_ SETCURSEL**](psm-setcursel.md)                             | 啟用屬性工作表中的指定頁面。 您可以使用 [**PropSheet \_ SetCurSel**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setcursel) 宏明確地傳送此訊息。<br/>                                                                                                    |
| [**PSM \_ SETCURSELID**](psm-setcurselid.md)                         | 根據頁面的資源識別碼，啟用屬性工作表中的指定頁面。 您可以使用 [**PropSheet \_ SetCurSelByID**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setcurselbyid) 宏明確地傳送此訊息。<br/>                                                   |
| [**PSM \_ SETFINISHTEXT**](psm-setfinishtext.md)                     | 設定 wizard 中 [ **完成]** 按鈕的文字、顯示並啟用按鈕，以及隱藏 [ **下一步]** 和 [ **上一頁** ] 按鈕。 您可以使用 [**PropSheet \_ SetFinishText**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setfinishtext) 宏明確地傳送此訊息。<br/>               |
| [**PSM \_ SETHEADERBITMAP**](psm-setheaderbitmap.md)                 | 此訊息不會執行。<br/>                                                                                                                                                                                                                                     |
| [**PSM \_ SETHEADERBITMAPRESOURCE**](psm-setheaderbitmapresource.md) | 此訊息不會執行。<br/>                                                                                                                                                                                                                                     |
| [**PSM \_ SETHEADERSUBTITLE**](psm-setheadersubtitle.md)             | 設定 wizard 內部頁面標頭的子標題文字。 您可以明確地傳送此訊息，或使用 [**PropSheet \_ SetHeaderSubTitle**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setheadersubtitle) 宏。<br/>                                                                        |
| [**PSM \_ SETHEADERTITLE**](psm-setheadertitle.md)                   | 設定 wizard 內部頁面標頭的標題文字。 您可以明確地傳送此訊息，或使用 [**PropSheet \_ SetHeaderTitle**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setheadertitle) 宏。<br/>                                                                                 |
| [**PSM \_ SETNEXTTEXT**](psm-setnexttext.md)                         | 設定 wizard 中 [ **下一步** ] 按鈕的文字。 您可以使用 [**PropSheet \_ SetNextText**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setnexttext) 宏明確地傳送此訊息。<br/>                                                                                                |
| [**PSM \_ SETTITLE**](psm-settitle.md)                               | 設定屬性工作表的標題。 您可以使用 [**PropSheet \_ SetTitle**](/windows/desktop/api/Prsht/nf-prsht-propsheet_settitle) 宏明確地傳送此訊息。<br/>                                                                                                                    |
| [**PSM \_ SETWIZBUTTONS**](psm-setwizbuttons.md)                     | 啟用或停用 wizard 中的 [ **上一頁**]、 **[下一頁**] 和 **[完成** ] 按鈕。 您也可以使用 [**PropSheet \_ SetWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setwizbuttons) 宏來張貼訊息。<br/>                                                                          |
| [**PSM \_ SHOWWIZBUTTONS**](psm-showwizbuttons.md)                   | 顯示或隱藏嚮導中的按鈕。 您可以使用 [**PropSheet \_ ShowWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_showwizbuttons) 宏明確地傳送此訊息。<br/>                                                                                                        |
| [**PSM \_ 未變更**](psm-unchanged.md)                             | 通知屬性工作表，頁面中的資訊已還原為先前儲存的狀態。 您可以明確地傳送此訊息，或使用 [**PropSheet \_ 未**](/windows/desktop/api/Prsht/nf-prsht-propsheet_unchanged) 變更宏。<br/>                                                      |



 

### <a name="notifications"></a>通知



| 主題                                                     | 目錄                                                                                                                                                                                                                                                |
|-----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [PSN \_ APPLY](psn-apply.md)                               | 傳送至屬性工作表中的每個頁面，表示使用者已按下 [確定]、[關閉] 或 [套用] 按鈕，並想要讓所有變更生效。 此通知會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。<br/>      |
| [PSN \_ GETOBJECT](psn-getobject.md)                       | 由屬性工作表傳送，以在游標通過其中一個索引標籤控制項按鈕時，要求放置目標物件。<br/>                                                                                                                       |
| [PSN \_ 說明](psn-help.md)                                 | 通知頁面，表示使用者已按一下 [說明] 按鈕。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。<br/>                                                                                          |
| [PSN \_ KILLACTIVE](psn-killactive.md)                     | 通知頁面，因為正在啟用另一個頁面，或使用者已按下 [ **確定]** 按鈕，所以即將遺失啟用。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。<br/>       |
| [PSN \_ QUERYCANCEL](psn-querycancel.md)                   | 指出使用者已取消屬性工作表。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。<br/>                                                                                            |
| [PSN \_ QUERYINITIALFOCUS](psn-queryinitialfocus.md)       | 由屬性工作表傳送以提供屬性工作表頁面，有機會指定哪個對話方塊控制項應該接收初始焦點。 此通知會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。<br/>           |
| [PSN \_ 重設](psn-reset.md)                               | 通知頁面：即將終結屬性工作表。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。<br/>                                                                                   |
| [PSN \_ ADVANCED.FIELD.SETACTIVE](psn-setactive.md)                       | 通知頁面，指出即將啟用。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。<br/>                                                                                                   |
| [PSN \_ TRANSLATEACCELERATOR](psn-translateaccelerator.md) | 通知屬性工作表已收到鍵盤訊息。 它讓頁面有機會進行私用鍵盤快速鍵轉譯。 此通知會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。<br/> |
| [PSN \_ WIZBACK](psn-wizback.md)                           | 通知頁面，使用者已按一下嚮導中的 [ **上一頁** ] 按鈕。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。<br/>                                                                          |
| [PSN \_ WIZFINISH](psn-wizfinish.md)                       | 通知頁面，表示使用者已按一下嚮導中的 [ **完成]** 按鈕。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。<br/>                                                                        |
| [PSN \_ WIZNEXT](psn-wiznext.md)                           | 通知頁面，表示使用者已按下 wizard 中的 [ **下一步** ] 按鈕。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。<br/>                                                                          |



 

### <a name="structures"></a>結構



| 主題                                      | 目錄                                                                   |
|--------------------------------------------|----------------------------------------------------------------------------|
| [**PROPSHEETHEADER**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2) | 定義屬性工作表的框架和頁面。<br/>                |
| [**PROPSHEETPAGE**](/windows/desktop/api/Prsht/ns-prsht-propsheetpagea_v2)     | 定義屬性工作表中的頁面。<br/>                             |
| [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify)             | 包含屬性工作表通知碼的資訊。<br/> |



 

 

