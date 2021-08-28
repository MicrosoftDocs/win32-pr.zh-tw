---
title: '索引標籤 (Windows 控制項) '
description: 本章節包含與索引標籤控制項搭配使用之程式設計項目的相關資訊。
ms.assetid: vs|controls|~\controls\tab\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85c4da2f0aeb05aea6bb671c395b151c7d69e2596d10a3564b8bbd8557c39877
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119696378"
---
# <a name="tab-windows-controls"></a>索引標籤 (Windows 控制項) 

本章節包含與索引標籤控制項搭配使用之程式設計項目的相關資訊。

### <a name="overviews"></a>概觀



| 主題                                        | 目錄                                                                                                                                                                                                           |
|----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [關於索引標籤控制項](tab-controls.md)       | 「索引標籤控制項」類似於筆記本裡的分隔頁或檔案櫃中的標籤。 藉由使用索引標籤控制項，應用程式可以定義視窗或對話方塊中同一個區域的多個頁面。<br/> |
| [使用索引標籤控制項](using-tab-controls.md) | 本主題包含兩個使用索引標籤控制項的範例。<br/>                                                                                                                                                 |



 

### <a name="macros"></a>巨集



| 主題                                                         | 目錄                                                                                                                                                                                                                                                                                                          |
|---------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TabCtrl \_ AdjustRect**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_adjustrect)             | 在指定視窗矩形的情況下，計算索引標籤控制項的顯示區域，或計算對應至指定之顯示區域的視窗矩形。 您可以使用這個宏，或明確地傳送 [**TCM \_ ADJUSTRECT**](tcm-adjustrect.md) 訊息。 <br/>                                              |
| [**TabCtrl \_ DeleteAllItems**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_deleteallitems)     | 從索引標籤控制項移除所有專案。 您可以使用這個宏，或明確地傳送 [**TCM \_ DELETEALLITEMS**](tcm-deleteallitems.md) 訊息。 <br/>                                                                                                                                                        |
| [**TabCtrl \_ DeleteItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_deleteitem)             | 從索引標籤控制項移除專案。 您可以使用這個宏，或明確地傳送 [**TCM \_ DELETEITEM**](tcm-deleteitem.md) 訊息。 <br/>                                                                                                                                                                  |
| [**TabCtrl \_ DeselectAll**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_deselectall)           | 重設索引標籤控制項中的專案，清除任何已設定為 [**TCIS \_ BUTTONPRESSED**](tab-control-item-states.md) 狀態的專案。 您可以使用這個宏，或明確地傳送 [**TCM \_ DESELECTALL**](tcm-deselectall.md) 訊息。 <br/>                                                  |
| [**TabCtrl \_ GetCurFocus**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getcurfocus)           | 傳回在索引標籤控制項中具有焦點之專案的索引。 您可以使用這個宏，或明確地傳送 [**TCM \_ GETCURFOCUS**](tcm-getcurfocus.md) 訊息。 <br/>                                                                                                                                 |
| [**TabCtrl \_ GetCurSel**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getcursel)               | 決定目前在索引標籤控制項中選取的索引標籤。 您可以使用這個宏，或明確地傳送 [**TCM \_ GETCURSEL**](tcm-getcursel.md) 訊息。 <br/>                                                                                                                                                |
| [**TabCtrl \_ GetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getextendedstyle) | 抓取目前用於索引標籤控制項的延伸樣式。 您可以使用這個宏，或明確地傳送 [**TCM \_ GETEXTENDEDSTYLE**](tcm-getextendedstyle.md) 訊息。 <br/>                                                                                                             |
| [**TabCtrl \_ GetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getimagelist)         | 抓取與索引標籤控制項相關聯的影像清單。 您可以使用這個宏，或明確地傳送 [**TCM \_ GETIMAGELIST**](tcm-getimagelist.md) 訊息。 <br/>                                                                                                                                          |
| [**TabCtrl \_ GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getitem)                   | 抓取索引標籤控制項中索引標籤的相關資訊。 您可以使用這個宏，或明確地傳送 [**TCM \_ GETITEM**](tcm-getitem.md) 訊息。<br/>                                                                                                                                                         |
| [**TabCtrl \_ GetItemCount**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getitemcount)         | 抓取索引標籤控制項中的索引標籤數目。 您可以使用這個宏，或明確地傳送 [**TCM \_ GETITEMCOUNT**](tcm-getitemcount.md) 訊息。 <br/>                                                                                                                                                 |
| [**TabCtrl \_ GetItemRect**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getitemrect)           | 抓取索引標籤控制項中索引標籤的周框。 您可以使用這個宏，或明確地傳送 [**TCM \_ GETITEMRECT**](tcm-getitemrect.md) 訊息。 <br/>                                                                                                                                       |
| [**TabCtrl \_ GetRowCount**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getrowcount)           | 抓取索引標籤控制項中目前的索引標籤數目。 您可以使用這個宏，或明確地傳送 [**TCM \_ GETROWCOUNT**](tcm-getrowcount.md) 訊息。 <br/>                                                                                                                                     |
| [**TabCtrl \_ GetToolTips**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_gettooltips)           | 抓取與索引標籤控制項相關聯的工具提示控制項控點。 您可以使用這個宏，或明確地傳送 [**TCM \_ GETTOOLTIPS**](tcm-gettooltips.md) 訊息。 <br/>                                                                                                                         |
| [**TabCtrl \_ GetUnicodeFormat**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getunicodeformat) | 抓取控制項的 UNICODE 字元格式旗標。 您可以使用這個宏，或明確地傳送 [**TCM \_ GETUNICODEFORMAT**](tcm-getunicodeformat.md) 訊息。 <br/>                                                                                                                             |
| [**TabCtrl \_ HighlightItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_highlightitem)       | 設定索引標籤專案的醒目提示狀態。 您可以使用這個宏，或明確地傳送 [**TCM \_ HIGHLIGHTITEM**](tcm-highlightitem.md) 訊息。 <br/>                                                                                                                                                        |
| [**TabCtrl \_ system.windows.media.visualtreehelper.hittest**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_hittest)                   | 判斷哪一個索引標籤（如果有的話）位於指定的畫面位置上。 您可以使用這個宏，或明確地傳送 [**TCM \_ system.windows.media.visualtreehelper.hittest**](tcm-hittest.md) 訊息。 <br/>                                                                                                                                           |
| [**TabCtrl \_ InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_insertitem)             | 在索引標籤控制項中插入新的索引標籤。 您可以使用這個宏，或明確地傳送 [**TCM \_ INSERTITEM**](tcm-insertitem.md) 訊息。 <br/>                                                                                                                                                                  |
| [**TabCtrl \_ RemoveImage**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_removeimage)           | 從索引標籤控制項的影像清單中移除影像。 您可以使用這個宏，或明確地傳送 [**TCM \_ REMOVEIMAGE**](tcm-removeimage.md) 訊息。 <br/>                                                                                                                                                  |
| [**TabCtrl \_ SetCurFocus**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setcurfocus)           | 將焦點設定至索引標籤控制項中的指定索引標籤。 您可以使用這個宏，或明確地傳送 [**TCM \_ SETCURFOCUS**](tcm-setcurfocus.md) 訊息。 <br/>                                                                                                                                                |
| [**TabCtrl \_ SetCurSel**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setcursel)               | 在索引標籤控制項中選取索引標籤。 您可以使用這個宏，或明確地傳送 [**TCM \_ SETCURSEL**](tcm-setcursel.md) 訊息。 <br/>                                                                                                                                                                        |
| [**TabCtrl \_ SetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setextendedstyle) | 設定索引標籤控制項將使用的擴充樣式。 您可以使用這個宏，或明確地傳送 [**TCM \_ SETEXTENDEDSTYLE**](tcm-setextendedstyle.md) 訊息。 <br/>                                                                                                                                  |
| [**TabCtrl \_ SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setimagelist)         | 將影像清單指派給索引標籤控制項。 您可以使用這個宏，或明確地傳送 [**TCM \_ SETIMAGELIST**](tcm-setimagelist.md) 訊息。 <br/>                                                                                                                                                          |
| [**TabCtrl \_ SetItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setitem)                   | 設定部分或全部索引標籤的屬性。 您可以使用這個宏，或明確地傳送 [**TCM \_ SETITEM**](tcm-setitem.md) 訊息。 <br/>                                                                                                                                                                    |
| [**TabCtrl \_ SetItemExtra**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setitemextra)         | 設定在索引標籤控制項中，為應用程式定義資料保留的每個索引標籤的位元組數目。 您可以使用這個宏，或明確地傳送 [**TCM \_ SETITEMEXTRA**](tcm-setitemextra.md) 訊息。 <br/>                                                                                                         |
| [**TabCtrl \_ SetItemSize**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setitemsize)           | 在固定寬度或主控描繪的索引標籤控制項中，設定索引標籤的寬度和高度。 您可以使用這個宏，或明確地傳送 [**TCM \_ SETITEMSIZE**](tcm-setitemsize.md) 訊息。 <br/>                                                                                                                     |
| [**TabCtrl \_ SetMinTabWidth**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setmintabwidth)     | 設定索引標籤控制項中專案的最小寬度。 您可以使用這個宏，或明確地傳送 [**TCM \_ SETMINTABWIDTH**](tcm-setmintabwidth.md) 訊息。 <br/>                                                                                                                                            |
| [**TabCtrl \_ SetPadding**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setpadding)             | 設定在索引標籤控制項中每個索引標籤的圖示和標籤周圍的空間 (填補) 。 您可以使用這個宏，或明確地傳送 [**TCM \_ SETPADDING**](tcm-setpadding.md) 訊息。 <br/>                                                                                                                |
| [**TabCtrl \_ SetToolTips**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_settooltips)           | 將工具提示控制項指派給索引標籤控制項。 您可以使用這個宏，或明確地傳送 [**TCM \_ SETTOOLTIPS**](tcm-settooltips.md) 訊息。 <br/>                                                                                                                                                        |
| [**TabCtrl \_ SetUnicodeFormat**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setunicodeformat) | 設定控制項的 Unicode 字元格式旗標。 此訊息可讓您變更控制項在執行時間所使用的字元集，而不需要重新建立控制項。 您可以使用這個宏，或明確地傳送 [**TCM \_ SETUNICODEFORMAT**](tcm-setunicodeformat.md) 訊息。 <br/> |



 

### <a name="messages"></a>訊息



| 主題                                                 | 目錄                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TCM \_ ADJUSTRECT**](tcm-adjustrect.md)             | 在指定視窗矩形的情況下，計算索引標籤控制項的顯示區域，或計算對應至指定之顯示區域的視窗矩形。 您可以使用 [**TabCtrl \_ AdjustRect**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_adjustrect) 宏明確地傳送此訊息。<br/>                                          |
| [**TCM \_ DELETEALLITEMS**](tcm-deleteallitems.md)     | 從索引標籤控制項移除所有專案。 您可以使用 [**TabCtrl \_ DeleteAllItems**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_deleteallitems) 宏明確地傳送此訊息。 <br/>                                                                                                                                                   |
| [**TCM \_ DELETEITEM**](tcm-deleteitem.md)             | 從索引標籤控制項移除專案。 您可以使用 [**TabCtrl \_ DeleteItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_deleteitem) 宏明確地傳送此訊息。 <br/>                                                                                                                                                             |
| [**TCM \_ DESELECTALL**](tcm-deselectall.md)           | 重設索引標籤控制項中的專案，清除任何已設定為 [**TCIS \_ BUTTONPRESSED**](tab-control-item-states.md) 狀態的專案。 您可以使用 [**TabCtrl \_ DeselectAll**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_deselectall) 宏明確地傳送此訊息。 <br/>                                             |
| [**TCM \_ GETCURFOCUS**](tcm-getcurfocus.md)           | 傳回在索引標籤控制項中具有焦點之專案的索引。 您可以使用 [**TabCtrl \_ GetCurFocus**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getcurfocus) 宏明確地傳送此訊息。 <br/>                                                                                                                            |
| [**TCM \_ GETCURSEL**](tcm-getcursel.md)               | 決定目前在索引標籤控制項中選取的索引標籤。 您可以使用 [**TabCtrl \_ GetCurSel**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getcursel) 宏明確地傳送此訊息。 <br/>                                                                                                                                           |
| [**TCM \_ GETEXTENDEDSTYLE**](tcm-getextendedstyle.md) | 抓取目前用於索引標籤控制項的延伸樣式。 您可以使用 [**TabCtrl \_ GetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getextendedstyle) 宏明確地傳送此訊息。 <br/>                                                                                                        |
| [**TCM \_ GETIMAGELIST**](tcm-getimagelist.md)         | 抓取與索引標籤控制項相關聯的影像清單。 您可以使用 [**TabCtrl \_ GetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getimagelist) 宏明確地傳送此訊息。 <br/>                                                                                                                                     |
| [**TCM \_ GETITEM**](tcm-getitem.md)                   | 抓取索引標籤控制項中索引標籤的相關資訊。 您可以使用 [**TabCtrl \_ GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getitem) 宏明確地傳送此訊息。<br/>                                                                                                                                                    |
| [**TCM \_ GETITEMCOUNT**](tcm-getitemcount.md)         | 抓取索引標籤控制項中的索引標籤數目。 您可以使用 [**TabCtrl \_ GetItemCount**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getitemcount) 宏明確地傳送此訊息。 <br/>                                                                                                                                            |
| [**TCM \_ GETITEMRECT**](tcm-getitemrect.md)           | 抓取索引標籤控制項中索引標籤的周框。 您可以使用 [**TabCtrl \_ GetItemRect**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getitemrect) 宏明確地傳送此訊息。 <br/>                                                                                                                                  |
| [**TCM \_ GETROWCOUNT**](tcm-getrowcount.md)           | 抓取索引標籤控制項中目前的索引標籤數目。 您可以使用 [**TabCtrl \_ GetRowCount**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getrowcount) 宏明確地傳送此訊息。 <br/>                                                                                                                                |
| [**TCM \_ GETTOOLTIPS**](tcm-gettooltips.md)           | 抓取與索引標籤控制項相關聯的工具提示控制項控點。 您可以使用 [**TabCtrl \_ GetToolTips**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_gettooltips) 宏明確地傳送此訊息。 <br/>                                                                                                                    |
| [**TCM \_ GETUNICODEFORMAT**](tcm-getunicodeformat.md) | 抓取控制項的 Unicode 字元格式旗標。 您可以明確地傳送此訊息，或使用 [**TabCtrl \_ GetUnicodeFormat**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getunicodeformat) 宏。 <br/>                                                                                                                             |
| [**TCM \_ HIGHLIGHTITEM**](tcm-highlightitem.md)       | 設定索引標籤專案的醒目提示狀態。 您可以使用 [**TabCtrl \_ HighlightItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_highlightitem) 宏明確地傳送此訊息。<br/>                                                                                                                                                    |
| [**TCM \_ SYSTEM.WINDOWS.MEDIA.VISUALTREEHELPER.HITTEST**](tcm-hittest.md)                   | 判斷哪一個索引標籤（如果有的話）位於指定的畫面位置上。 您可以使用 [**TabCtrl \_ system.windows.media.visualtreehelper.hittest**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_hittest) 宏明確地傳送此訊息。 <br/>                                                                                                                                      |
| [**TCM \_ INSERTITEM**](tcm-insertitem.md)             | 在索引標籤控制項中插入新的索引標籤。 您可以使用 [**TabCtrl \_ InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_insertitem) 宏明確地傳送此訊息。 <br/>                                                                                                                                                             |
| [**TCM \_ REMOVEIMAGE**](tcm-removeimage.md)           | 從索引標籤控制項的影像清單中移除影像。 您可以使用 [**TabCtrl \_ RemoveImage**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_removeimage) 宏明確地傳送此訊息。 <br/>                                                                                                                                             |
| [**TCM \_ SETCURFOCUS**](tcm-setcurfocus.md)           | 將焦點設定至索引標籤控制項中的指定索引標籤。 您可以使用 [**TabCtrl \_ SetCurFocus**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setcurfocus) 宏明確地傳送此訊息。 <br/>                                                                                                                                           |
| [**TCM \_ SETCURSEL**](tcm-setcursel.md)               | 在索引標籤控制項中選取索引標籤。 您可以使用 [**TabCtrl \_ SetCurSel**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setcursel) 宏明確地傳送此訊息。 <br/>                                                                                                                                                                   |
| [**TCM \_ SETEXTENDEDSTYLE**](tcm-setextendedstyle.md) | 設定索引標籤控制項將使用的擴充樣式。 您可以使用 [**TabCtrl \_ SetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setextendedstyle) 宏明確地傳送此訊息。 <br/>                                                                                                                             |
| [**TCM \_ SETIMAGELIST**](tcm-setimagelist.md)         | 將影像清單指派給索引標籤控制項。 您可以使用 [**TabCtrl \_ SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setimagelist) 宏明確地傳送此訊息。 <br/>                                                                                                                                                     |
| [**TCM \_ SETITEM**](tcm-setitem.md)                   | 設定部分或全部索引標籤的屬性。 您可以使用 [**TabCtrl \_ SetItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setitem) 宏明確地傳送此訊息。 <br/>                                                                                                                                                               |
| [**TCM \_ SETITEMEXTRA**](tcm-setitemextra.md)         | 設定在索引標籤控制項中，為應用程式定義資料保留的每個索引標籤的位元組數目。 您可以使用 [**TabCtrl \_ SetItemExtra**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setitemextra) 宏明確地傳送此訊息。 <br/>                                                                                                    |
| [**TCM \_ SETITEMSIZE**](tcm-setitemsize.md)           | 在固定寬度或主控描繪的索引標籤控制項中，設定索引標籤的寬度和高度。 您可以使用 [**TabCtrl \_ SetItemSize**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setitemsize) 宏明確地傳送此訊息。<br/>                                                                                                                 |
| [**TCM \_ SETMINTABWIDTH**](tcm-setmintabwidth.md)     | 設定索引標籤控制項中專案的最小寬度。 您可以使用 [**TabCtrl \_ SetMinTabWidth**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setmintabwidth) 宏明確地傳送此訊息。 <br/>                                                                                                                                       |
| [**TCM \_ SETPADDING**](tcm-setpadding.md)             | 設定在索引標籤控制項中每個索引標籤的圖示和標籤周圍的空間 (填補) 。 您可以使用 [**TabCtrl \_ SetPadding**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setpadding) 宏明確地傳送此訊息。<br/>                                                                                                            |
| [**TCM \_ SETTOOLTIPS**](tcm-settooltips.md)           | 將工具提示控制項指派給索引標籤控制項。 您可以使用 [**TabCtrl \_ SetToolTips**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_settooltips) 宏明確地傳送此訊息。 <br/>                                                                                                                                                   |
| [**TCM \_ SETUNICODEFORMAT**](tcm-setunicodeformat.md) | 設定控制項的 Unicode 字元格式旗標。 此訊息可讓您變更控制項在執行時間所使用的字元集，而不需要重新建立控制項。 您可以明確地傳送此訊息，或使用 [**TabCtrl \_ SetUnicodeFormat**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setunicodeformat) 宏。 <br/> |



 

### <a name="notifications"></a>通知



| 主題                                                    | 目錄                                                                                                                                                                                                                                                                                            |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [選擇 [NM] (索引標籤 \_) ](nm-click-tab.md)                      | 通知索引標籤控制項的父視窗，使用者在控制項內按一下滑鼠左鍵。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。<br/>                                                                                 |
| [NM \_ DBLCLK (] 索引標籤) ](nm-dblclk-tab.md)                    | 通知索引標籤控制項的父視窗，使用者在控制項內按兩下滑鼠左鍵。 此通知會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。<br/>                                                                                 |
| [NM \_ RCLICK (] 索引標籤) ](nm-rclick-tab.md)                    | 通知索引標籤控制項的父視窗，使用者在控制項內按一下滑鼠右鍵。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。<br/>                                                                                |
| [NM \_ RDBLCLK (] 索引標籤) ](nm-rdblclk-tab.md)                  | 通知索引標籤控制項的父視窗，使用者在控制項內按兩下滑鼠右鍵。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。<br/>                                                                         |
| [NM \_ RELEASEDCAPTURE (] 索引標籤) ](nm-releasedcapture-tab-.md) | 通知索引標籤控制項的父視窗，控制項正在放開滑鼠捕捉。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。 <br/>                                                                                                            |
| [TCN \_ FOCUSCHANGE](tcn-focuschange.md)                  | 通知索引標籤控制項的父視窗，按鈕焦點已變更。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。 <br/>                                                                                                                      |
| [TCN \_ GETOBJECT](tcn-getobject.md)                      | 當索引標籤控制項具有 [**TCS \_ EX \_ REGISTERDROP**](tab-control-extended-styles.md) 擴充樣式，且將物件拖曳至控制項中的索引標籤專案上方時，便會傳送此控制項。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。 <br/> |
| [TCN \_ KEYDOWN](tcn-keydown.md)                          | 通知索引標籤控制項的父視窗已按下按鍵。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。 <br/>                                                                                                                            |
| [TCN \_ SELCHANGE](tcn-selchange.md)                      | 通知索引標籤控制項的父視窗，指出目前選取的索引標籤已變更。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。 <br/>                                                                                                            |
| [TCN \_ SELCHANGING](tcn-selchanging.md)                  | 通知索引標籤控制項的父視窗，指出目前選取的索引標籤即將變更。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。 <br/>                                                                                                     |



 

### <a name="structures"></a>結構



| 主題                                  | 目錄                                                                                                                                                                                                                                                                     |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NMTCKEYDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmtckeydown)     | 包含在索引標籤控制項中按下按鍵的相關資訊。 它會與 [**TCN \_ KEYDOWN**](tcn-keydown.md) 通知程式碼搭配使用。 此結構取代了 **TC \_ KEYDOWN** 結構。 <br/>                                                                     |
| [**TCHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-tchittestinfo) | 包含點擊測試的相關資訊。 此結構取代了 **TC \_ HITTESTINFO** 結構。 <br/>                                                                                                                                                              |
| [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema)               | 指定或接收索引標籤專案的屬性。 它適用于 [**tcm \_ INSERTITEM**](tcm-insertitem.md)、 [**tcm \_ GETITEM**](tcm-getitem.md)和 [**tcm \_ SETITEM**](tcm-setitem.md) 訊息。 此結構取代了 **TC \_ 專案** 結構。 <br/>  |
| [**TCITEMHEADER**](/windows/win32/api/commctrl/ns-commctrl-tcitemheadera)   | 指定或接收索引標籤的屬性。它適用于 [**tcm \_ INSERTITEM**](tcm-insertitem.md)、 [**tcm \_ GETITEM**](tcm-getitem.md)和 [**tcm \_ SETITEM**](tcm-setitem.md) 訊息。 此結構取代了 **TC \_ ITEMHEADER** 結構。 <br/> |



 

### <a name="constants"></a>常數



| 主題                                                          | 目錄                                                                                                                                                                                                                                                                                                                                         |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [索引標籤控制項擴充樣式](tab-control-extended-styles.md) | 索引標籤控制項現在支援擴充樣式。 這些樣式是使用 [**tcm \_ GETEXTENDEDSTYLE**](tcm-getextendedstyle.md) 和 [**tcm \_ SETEXTENDEDSTYLE**](tcm-setextendedstyle.md) 訊息來操作，不應該與傳遞給 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)的延伸視窗樣式混淆。 <br/> |
| [Tab 控制項專案狀態](tab-control-item-states.md)         | 索引標籤控制項現在支援支援 [**TCM \_ DESELECTALL**](tcm-deselectall.md) 訊息的專案狀態。 此外， [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) 結構支援專案狀態值。 <br/>                                                                                                                                     |
| [索引標籤控制項樣式](tab-control-styles.md)                   | 本節列出支援的索引標籤控制項樣式。<br/>                                                                                                                                                                                                                                                                                      |



 

 

