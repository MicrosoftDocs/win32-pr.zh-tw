---
title: 標題控制項
description: 本章節包含與標題控制項搭配使用之程式設計項目的相關資訊。
ms.assetid: vs|controls|~\controls\header\header_header.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3de60403165b666d9d323a38baffb926889d7946
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104463732"
---
# <a name="header-control"></a>標題控制項

本章節包含與標題控制項搭配使用之程式設計項目的相關資訊。

### <a name="overviews"></a>概觀



| 主題                                              | 目錄                                                                                                                                                                    |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [關於標題控制項](header-controls.md)       | 標題控制項是通常位於文字或數位資料行上方的視窗。 它包含每個資料行的標題，而且可以分成幾個部分。<br/> |
| [使用標題控制項](using-header-controls.md) | 本主題提供標題控制項的執行詳細資料和程式碼範例。<br/>                                                                                   |



 

### <a name="macros"></a>巨集



| 主題                                                                   | 目錄                                                                                                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**標頭 \_ ClearAllFilters**](/windows/desktop/api/Commctrl/nf-commctrl-header_clearallfilters)               | 清除指定標題控制項的所有篩選準則。 您可以使用這個宏，或明確地傳送 [**HDM \_ CLEARFILTER**](hdm-clearfilter.md) 訊息。 <br/>                                                                                                                                              |
| [**標頭 \_ ClearFilter**](/windows/desktop/api/Commctrl/nf-commctrl-header_clearfilter)                       | 清除指定標題控制項的篩選。 您可以使用這個宏，或明確地傳送 [**HDM \_ CLEARFILTER**](hdm-clearfilter.md) 訊息。 <br/>                                                                                                                                                      |
| [**標頭 \_ CreateDragImage**](/windows/desktop/api/Commctrl/nf-commctrl-header_createdragimage)               | 在現有的標題控制項內建立專案影像的透明版本。 您可以使用這個宏，或明確地傳送 [**HDM \_ CREATEDRAGIMAGE**](hdm-createdragimage.md) 訊息。 <br/>                                                                                                          |
| [**標頭 \_ DeleteItem**](/windows/desktop/api/Commctrl/nf-commctrl-header_deleteitem)                         | 從標題控制項刪除專案。 您可以使用這個宏，或明確地傳送 [**HDM \_ DELETEITEM**](hdm-deleteitem.md) 訊息。 <br/>                                                                                                                                                               |
| [**標頭 \_ EditFilter**](/windows/desktop/api/Commctrl/nf-commctrl-header_editfilter)                         | 當篩選按鈕具有焦點時，將輸入焦點移至編輯方塊。<br/>                                                                                                                                                                                                                              |
| [**標頭 \_ GetBitmapMargin**](/windows/desktop/api/Commctrl/nf-commctrl-header_getbitmapmargin)               | 取得現有標題控制項中點陣圖的邊界 (寬度（以圖元) 為單位）。 您可以使用這個宏，或明確地傳送 [**HDM \_ GETBITMAPMARGIN**](hdm-getbitmapmargin.md) 訊息。 <br/>                                                                                                        |
| [**標頭 \_ GetFocusedItem**](/windows/desktop/api/Commctrl/nf-commctrl-header_getfocuseditem)                 | 取得標題控制項中具有焦點的專案。 使用這個宏或明確地傳送 [**HDM \_ GETFOCUSEDITEM**](hdm-getfocuseditem.md) 訊息。<br/>                                                                                                                                                 |
| [**標頭 \_ GetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-header_getimagelist)                     | 取得已針對現有標題控制項設定之影像清單的控制碼。 您可以使用這個宏，或明確地傳送 [**HDM \_ GETIMAGELIST**](hdm-getimagelist.md) 訊息。 <br/>                                                                                                              |
| [**標頭 \_ GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitem)                               | 取得標題控制項中的專案相關資訊。 您可以使用這個宏，或明確地傳送 [**HDM \_ GETITEM**](hdm-getitem.md) 訊息。 <br/>                                                                                                                                                        |
| [**標頭 \_ GetItemCount**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitemcount)                     | 取得標題控制項中的專案計數。 您可以使用這個宏，或明確地傳送 [**HDM \_ GETITEMCOUNT**](hdm-getitemcount.md) 訊息。 <br/>                                                                                                                                                   |
| [**標頭 \_ GetItemDropDownRect**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitemdropdownrect)       | 取得標題控制項中指定專案之下拉式按鈕的座標。 標題控制項的類型必須是 HDF \_ SPLITBUTTON。 使用這個宏或明確地傳送 [**HDM \_ GETITEMDROPDOWNRECT**](hdm-getitemdropdownrect.md) 訊息。<br/>                                                 |
| [**標頭 \_ GetItemRect**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitemrect)                       | 取得標題控制項中指定專案的周框。 您可以使用這個宏，或明確地傳送 [**HDM \_ GETITEMRECT**](hdm-getitemrect.md) 訊息。 <br/>                                                                                                                                  |
| [**標頭 \_ GetOrderArray**](/windows/desktop/api/Commctrl/nf-commctrl-header_getorderarray)                   | 取得標題控制項中專案的目前由左到右的順序。 您可以使用這個宏，或明確地傳送 [**HDM \_ GETORDERARRAY**](hdm-getorderarray.md) 訊息。 <br/>                                                                                                                             |
| [**標頭 \_ GetOverflowRect**](/windows/desktop/api/Commctrl/nf-commctrl-header_getoverflowrect)               | 取得所指定標題控制項之下拉式溢位區域域的座標。 標題控制項的類型必須是 HDF \_ SPLITBUTTON。 使用這個宏或明確地傳送 [**HDM \_ GETOVERFLOWRECT**](hdm-getoverflowrect.md) 訊息。<br/>                                                            |
| [**標頭 \_ GetStateImageList**](/windows/desktop/api/Commctrl/nf-commctrl-header_getstateimagelist)           | 取得已針對現有標題控制項狀態設定之影像清單的控制碼。<br/>                                                                                                                                                                                                              |
| [**標頭 \_ GetUnicodeFormat**](/windows/desktop/api/Commctrl/nf-commctrl-header_getunicodeformat)             | 取得控制項的 Unicode 字元格式旗標。 您可以使用這個宏，或明確地傳送 [**HDM \_ GETUNICODEFORMAT**](hdm-getunicodeformat.md) 訊息。 <br/>                                                                                                                                  |
| [**標頭 \_ InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-header_insertitem)                         | 將新的專案插入至標題控制項。 您可以使用這個宏，或明確地傳送 [**HDM \_ INSERTITEM**](hdm-insertitem.md) 訊息。 <br/>                                                                                                                                                            |
| [**標頭 \_ 版面配置**](/windows/desktop/api/Commctrl/nf-commctrl-header_layout)                                 | 抓取父視窗內標題控制項的正確大小和位置。 您可以使用這個宏，或明確地傳送 [**HDM \_**](hdm-layout.md) 配置訊息。 <br/>                                                                                                                        |
| [**標頭 \_ OrderToIndex**](/windows/desktop/api/Commctrl/nf-commctrl-header_ordertoindex)                     | 根據標題控制項中的順序，抓取專案的索引值。 您可以使用這個宏，或明確地傳送 [**HDM \_ ORDERTOINDEX**](hdm-ordertoindex.md) 訊息。 <br/>                                                                                                                   |
| [**標頭 \_ SetBitmapMargin**](/windows/desktop/api/Commctrl/nf-commctrl-header_setbitmapmargin)               | 在現有的標題控制項中，設定點陣圖邊界的寬度。 您可以使用這個宏，或明確地傳送 [**HDM \_ SETBITMAPMARGIN**](hdm-setbitmapmargin.md) 訊息。 <br/>                                                                                                                   |
| [**標頭 \_ SetFilterChangeTimeout**](/windows/desktop/api/Commctrl/nf-commctrl-header_setfilterchangetimeout) | 設定篩選屬性中發生變更和張貼 [HDN \_ FILTERCHANGE](hdn-filterchange.md) 通知之間的逾時間隔。 您可以使用這個宏，或明確地傳送 [**HDM \_ SETFILTERCHANGETIMEOUT**](hdm-setfilterchangetimeout.md) 訊息。 <br/>       |
| [**標頭 \_ SetFocusedItem**](/windows/desktop/api/Commctrl/nf-commctrl-header_setfocuseditem)                 | 將焦點設定為標題控制項中的指定專案。 使用這個宏或明確地傳送 [**HDM \_ SETFOCUSEDITEM**](hdm-setfocuseditem.md) 訊息。<br/>                                                                                                                                               |
| [**標頭 \_ SetHotDivider**](/windows/desktop/api/Commctrl/nf-commctrl-header_sethotdivider)                   | 變更標題專案之間的分隔線色彩，以表示外部拖放作業的目的地。 您可以使用這個宏，或明確地傳送 [**HDM \_ SETHOTDIVIDER**](hdm-sethotdivider.md) 訊息。 <br/>                                                                        |
| [**標頭 \_ SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-header_setimagelist)                     | 將影像清單指派給現有的標題控制項。 您可以使用這個宏，或明確地傳送 [**HDM \_ SETIMAGELIST**](hdm-setimagelist.md) 訊息。 <br/>                                                                                                                                             |
| [**標頭 \_ SetItem**](/windows/desktop/api/Commctrl/nf-commctrl-header_setitem)                               | 在標題控制項中設定指定專案的屬性。 您可以使用這個宏，或明確地傳送 [**HDM \_ SETITEM**](hdm-setitem.md) 訊息。 <br/>                                                                                                                                             |
| [**標頭 \_ SetOrderArray**](/windows/desktop/api/Commctrl/nf-commctrl-header_setorderarray)                   | 設定標頭專案的由左到右順序。 您可以使用這個宏，或明確地傳送 [**HDM \_ SETORDERARRAY**](hdm-setorderarray.md) 訊息。 <br/>                                                                                                                                                  |
| [**標頭 \_ SetStateImageList**](/windows/desktop/api/Commctrl/nf-commctrl-header_setstateimagelist)           | 將影像清單指派給現有的標題控制項狀態。<br/>                                                                                                                                                                                                                                             |
| [**標頭 \_ SetUnicodeFormat**](/windows/desktop/api/Commctrl/nf-commctrl-header_setunicodeformat)             | 設定控制項的 UNICODE 字元格式旗標。 此訊息可讓您變更控制項在執行時間所使用的字元集，而不需要重新建立控制項。 您可以使用這個宏，或明確地傳送 [**HDM \_ SETUNICODEFORMAT**](hdm-setunicodeformat.md) 訊息。 <br/> |



 

### <a name="messages"></a>訊息



| 主題                                                             | 目錄                                                                                                                                                                                                                                                                                                                |
|-------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**HDM \_ CLEARFILTER**](hdm-clearfilter.md)                       | 清除指定標題控制項的篩選。 您可以明確地傳送此訊息，或使用 [**標頭 \_ ClearFilter**](/windows/desktop/api/Commctrl/nf-commctrl-header_clearfilter) 宏。 <br/>                                                                                                                                                      |
| [**HDM \_ CREATEDRAGIMAGE**](hdm-createdragimage.md)               | 建立專案影像的半透明版本，作為拖曳影像使用。 您可以明確地傳送此訊息，或使用 [**標頭 \_ CreateDragImage**](/windows/desktop/api/Commctrl/nf-commctrl-header_createdragimage) 宏。 <br/>                                                                                                         |
| [**HDM \_ DELETEITEM**](hdm-deleteitem.md)                         | 從標題控制項刪除專案。 您可以明確地傳送此訊息，或使用 [**標頭 \_ DeleteItem**](/windows/desktop/api/Commctrl/nf-commctrl-header_deleteitem) 宏。 <br/>                                                                                                                                                               |
| [**HDM \_ EDITFILTER**](hdm-editfilter.md)                         | 當篩選按鈕具有焦點時，將輸入焦點移至編輯方塊。<br/>                                                                                                                                                                                                                                    |
| [**HDM \_ GETBITMAPMARGIN**](hdm-getbitmapmargin.md)               | 取得標題控制項之點陣圖邊界的寬度。 您可以明確地傳送此訊息，或使用 [**標頭 \_ GetBitmapMargin**](/windows/desktop/api/Commctrl/nf-commctrl-header_getbitmapmargin) 宏。 <br/>                                                                                                                                  |
| [**HDM \_ GETFOCUSEDITEM**](hdm-getfocuseditem.md)                 | 取得標題控制項中具有焦點的專案。 明確地傳送此訊息，或使用 [**標頭 \_ GetFocusedItem**](/windows/desktop/api/Commctrl/nf-commctrl-header_getfocuseditem) 宏。 視窗會透過其 [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。<br/>                                                     |
| [**HDM \_ GETIMAGELIST**](hdm-getimagelist.md)                     | 取得已針對現有標題控制項設定之影像清單的控制碼。 您可以明確地傳送此訊息，或使用 [**標頭 \_ GetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-header_getimagelist) 或 [**標頭 \_ GetStateImageList**](/windows/desktop/api/Commctrl/nf-commctrl-header_getstateimagelist) 宏。 <br/>                                             |
| [**HDM \_ GETITEM**](hdm-getitem.md)                               | 取得標題控制項中的專案相關資訊。 您可以明確地傳送此訊息，或使用 [**標頭 \_ GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitem) 宏。<br/>                                                                                                                                                         |
| [**HDM \_ GETITEMCOUNT**](hdm-getitemcount.md)                     | 取得標題控制項中的專案計數。 您可以明確地傳送此訊息，或使用 [**標頭 \_ GetItemCount**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitemcount) 宏。 <br/>                                                                                                                                                   |
| [**HDM \_ GETITEMDROPDOWNRECT**](hdm-getitemdropdownrect.md)       | 取得具有樣式 HDF SPLITBUTTON 的標頭專案之分割按鈕的周框 \_ 。 明確地傳送此訊息，或使用 [**標頭 \_ GetItemDropDownRect**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitemdropdownrect)宏。<br/>                                                                                           |
| [**HDM \_ GETITEMRECT**](hdm-getitemrect.md)                       | 取得標題控制項中指定專案的周框。 您可以明確地傳送此訊息，或使用 [**標頭 \_ GetItemRect**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitemrect) 宏。 <br/>                                                                                                                                  |
| [**HDM \_ GETORDERARRAY**](hdm-getorderarray.md)                   | 取得標題控制項中專案的目前由左到右的順序。 您可以明確地傳送此訊息，或使用 [**標頭 \_ GetOrderArray**](/windows/desktop/api/Commctrl/nf-commctrl-header_getorderarray) 宏。 <br/>                                                                                                                             |
| [**HDM \_ GETOVERFLOWRECT**](hdm-getoverflowrect.md)               | 當在標題控制項上設定 [**HDS \_ 溢**](header-control-styles.md) 位樣式，且顯示溢位按鈕時，取得溢位按鈕的周框。 明確地傳送此訊息，或使用 [**標頭 \_ GetOverflowRect**](/windows/desktop/api/Commctrl/nf-commctrl-header_getoverflowrect)宏。<br/>   |
| [**HDM \_ GETUNICODEFORMAT**](hdm-getunicodeformat.md)             | 取得控制項的 Unicode 字元格式旗標。 您可以明確地傳送此訊息，或使用 [**標頭 \_ GetUnicodeFormat**](/windows/desktop/api/Commctrl/nf-commctrl-header_getunicodeformat) 宏。 <br/>                                                                                                                                  |
| [**HDM \_ SYSTEM.WINDOWS.MEDIA.VISUALTREEHELPER.HITTEST**](hdm-hittest.md)                               | 測試點以判斷哪個標頭專案（如果有的話）位於指定的點。 <br/>                                                                                                                                                                                                                            |
| [**HDM \_ INSERTITEM**](hdm-insertitem.md)                         | 將新的專案插入至標題控制項。 您可以明確地傳送此訊息，或使用 [**標頭 \_ InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-header_insertitem) 宏。 <br/>                                                                                                                                                            |
| [**HDM \_ 版面配置**](hdm-layout.md)                                 | 抓取用來在父視窗的目標矩形內設定標題控制項大小和位置的資訊。 您可以明確地傳送此訊息，或使用 [**標頭 \_ 版面**](/windows/desktop/api/Commctrl/nf-commctrl-header_layout) 配置宏。 <br/>                                                                              |
| [**HDM \_ ORDERTOINDEX**](hdm-ordertoindex.md)                     | 根據標題控制項中的順序，抓取專案的索引值。 您可以明確地傳送此訊息，或使用 [**標頭 \_ OrderToIndex**](/windows/desktop/api/Commctrl/nf-commctrl-header_ordertoindex) 宏。 <br/>                                                                                                                   |
| [**HDM \_ SETBITMAPMARGIN**](hdm-setbitmapmargin.md)               | 在現有的標題控制項中，設定點陣圖的邊界寬度（以圖元為單位）。 您可以明確地傳送此訊息，或使用 [**標頭 \_ SetBitmapMargin**](/windows/desktop/api/Commctrl/nf-commctrl-header_setbitmapmargin) 宏。 <br/>                                                                                              |
| [**HDM \_ SETFILTERCHANGETIMEOUT**](hdm-setfilterchangetimeout.md) | 設定篩選屬性中發生變更和張貼 [**HDN \_ FILTERCHANGE**](hdn-filterchange.md) 通知之間的逾時間隔。 您可以明確地傳送此訊息，或使用 [**標頭 \_ SetFilterChangeTimeout**](/windows/desktop/api/Commctrl/nf-commctrl-header_setfilterchangetimeout) 宏。 <br/>   |
| [**HDM \_ SETFOCUSEDITEM**](hdm-setfocuseditem.md)                 | 將焦點設定為標題控制項中的指定專案。 明確地傳送此訊息，或使用 [**標頭 \_ SetFocusedItem**](/windows/desktop/api/Commctrl/nf-commctrl-header_setfocuseditem) 宏。<br/>                                                                                                                                          |
| [**HDM \_ SETHOTDIVIDER**](hdm-sethotdivider.md)                   | 變更標題專案之間的分隔線色彩，以表示外部拖放作業的目的地。 您可以明確地傳送此訊息，或使用 [**標頭 \_ SetHotDivider**](/windows/desktop/api/Commctrl/nf-commctrl-header_sethotdivider) 宏。 <br/>                                                                        |
| [**HDM \_ SETIMAGELIST**](hdm-setimagelist.md)                     | 將影像清單指派給現有的標題控制項。 您可以明確地傳送此訊息，或使用 [**標頭 \_ SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-header_setimagelist) 或 [**標頭 \_ SetStateImageList**](/windows/desktop/api/Commctrl/nf-commctrl-header_setstateimagelist) 宏。 <br/>                                                                            |
| [**HDM \_ SETITEM**](hdm-setitem.md)                               | 在標題控制項中設定指定專案的屬性。 您可以明確地傳送此訊息，或使用 [**標頭 \_ SetItem**](/windows/desktop/api/Commctrl/nf-commctrl-header_setitem) 宏。 <br/>                                                                                                                                             |
| [**HDM \_ SETORDERARRAY**](hdm-setorderarray.md)                   | 設定標頭專案的由左到右順序。 您可以明確地傳送此訊息，或使用 [**標頭 \_ SetOrderArray**](/windows/desktop/api/Commctrl/nf-commctrl-header_setorderarray) 宏。 <br/>                                                                                                                                                  |
| [**HDM \_ SETUNICODEFORMAT**](hdm-setunicodeformat.md)             | 設定控制項的 UNICODE 字元格式旗標。 此訊息可讓您變更控制項在執行時間所使用的字元集，而不需要重新建立控制項。 您可以明確地傳送此訊息，或使用 [**標頭 \_ SetUnicodeFormat**](/windows/desktop/api/Commctrl/nf-commctrl-header_setunicodeformat) 宏。 <br/> |
| [**HDM \_ TRANSLATEACCELERATOR**](hdm-translateaccelerator.md)     | 未實作。<br/>                                                                                                                                                                                                                                                                                             |



 

### <a name="notifications"></a>通知



| 主題                                                          | 目錄                                                                                                                                                                                                                                                                                                                         |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [HDN \_ BEGINDRAG](hdn-begindrag.md)                            | 當拖曳作業在其中一個專案上開始時，由標題控制項所傳送。 只有設定為 [**HDS \_ system.windows.dragdrop.drop>**](header-control-styles.md) 樣式的標題控制項才會傳送此通知碼。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。 <br/> |
| [HDN \_ BEGINFILTEREDIT](hdn-beginfilteredit.md)                | 通知標題控制項的父視窗，篩選編輯已開始。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。<br/>                                                                                                                                                      |
| [HDN \_ BEGINTRACK](hdn-begintrack.md)                          | 通知標題控制項的父視窗，使用者已開始拖曳控制項中的分隔線 (也就是說，當滑鼠游標位於標題控制項) 的分隔線上時，使用者按下滑鼠左鍵。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。 <br/>     |
| [HDN \_ DIVIDERDBLCLICK](hdn-dividerdblclick.md)                | 通知標題控制項的父視窗，使用者按兩下控制項的 [分割區] 區域。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。 <br/>                                                                                                                     |
| [HDN \_ 下拉式清單](hdn-dropdown.md)                              | 當按一下標題控制項上的下拉箭號時，由標題控制項傳送至其父代。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。<br/>                                                                                                                            |
| [HDN \_ ENDDRAG](hdn-enddrag.md)                                | 當拖曳作業在其中一個專案上結束時，由標題控制項所傳送。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。 只有設定為 [**HDS \_ system.windows.dragdrop.drop>**](header-control-styles.md) 樣式的標題控制項才會傳送此通知。 <br/>                        |
| [HDN \_ ENDFILTEREDIT](hdn-endfilteredit.md)                    | 通知標題控制項的父視窗，篩選編輯已結束。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。<br/>                                                                                                                                                      |
| [HDN \_ ENDTRACK](hdn-endtrack.md)                              | 通知標題控制項的父視窗，指出使用者已完成拖曳分隔線。 此通知碼以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。 <br/>                                                                                                                                       |
| [HDN \_ FILTERBTNCLICK](hdn-filterbtnclick.md)                  | 當按一下 [篩選] 按鈕或回應 [**HDM \_ SETITEM**](hdm-setitem.md) 訊息時，通知標題控制項的父視窗。 <br/>                                                                                                                                                                      |
| [HDN \_ FILTERCHANGE](hdn-filterchange.md)                      | 通知標題控制項的父視窗，標題控制項篩選的屬性正在變更或編輯。 <br/>                                                                                                                                                                                              |
| [HDN \_ GETDISPINFO](hdn-getdispinfo.md)                        | 當控制項需要回呼標頭專案的相關資訊時，傳送至標題控制項的擁有者。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。 <br/>                                                                                                                                  |
| [HDN \_ ITEMCHANGED](hdn-itemchanged.md)                        | 通知標題控制項的父視窗，標題專案的屬性已變更。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。 <br/>                                                                                                                                |
| [HDN \_ ITEMCHANGING](hdn-itemchanging.md)                      | 通知標題控制項的父視窗，標題專案的屬性即將變更。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。 <br/>                                                                                                                         |
| [HDN \_ ITEMCLICK](hdn-itemclick.md)                            | 通知標題控制項的父視窗，指出使用者已按一下控制項。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。 <br/>                                                                                                                                                |
| [HDN \_ ITEMDBLCLICK](hdn-itemdblclick.md)                      | 通知標題控制項的父視窗，使用者按兩下控制項。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。 只有設定為 [**HDS \_ 按鈕**](header-control-styles.md) 樣式的標題控制項才會傳送此通知。 <br/>        |
| [HDN \_ ITEMKEYDOWN](hdn-itemkeydown.md)                        | 通知標題控制項的父視窗，已選取某個專案的按鍵。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。<br/>                                                                                                                                 |
| [HDN \_ ITEMSTATEICONCLICK](hdn-itemstateiconclick.md)          | 通知標題控制項的父視窗，使用者按一下專案的狀態圖示。<br/>                                                                                                                                                                                                                                 |
| [HDN \_ OVERFLOWCLICK](hdn-overflowclick.md)                    | 按一下標頭的溢位按鈕時，由標題控制項傳送到其父系。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。<br/>                                                                                                                                        |
| [HDN \_ TRACK](hdn-track.md)                                    | 通知標題控制項的父視窗，表示使用者正在拖曳標題控制項中的分隔線。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。 <br/>                                                                                                                        |
| [NM \_ CUSTOMDRAW (標頭) ](nm-customdraw-header.md)            | 由標題控制項傳送，以通知其父視窗有關繪製作業。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。<br/>                                                                                                                                               |
| [NM \_ RCLICK (標頭) ](nm-rclick-header.md)                    | 通知樹狀檢視控制項的父視窗，使用者在控制項內按一下滑鼠右鍵。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。 <br/>                                                                                                           |
| [NM \_ RELEASEDCAPTURE (標頭) ](nm-releasedcapture-header-.md) | 通知標題控制項的父視窗，控制項正在放開滑鼠捕捉。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。 <br/>                                                                                                                                      |



 

### <a name="constants"></a>常數



| 主題                                              | 目錄                                                                                                                                                                                            |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [標題控制項樣式](header-control-styles.md) | 標題控制項有許多樣式（如本節所述），可決定控制項的外觀和行為。 當您建立標題控制項時，會設定初始樣式。<br/> |



 

 

