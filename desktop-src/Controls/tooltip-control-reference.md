---
title: 工具提示
description: 本章節包含與工具提示控制項搭配使用之程式設計項目的相關資訊。
ms.assetid: vs|controls|~\controls\tooltip\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b30ebe66569ede133c311168d3f3f2870dc3aeabe8eaeaa3e15d6584be2d6873
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046038"
---
# <a name="tooltip"></a>工具提示

本章節包含與工具提示控制項搭配使用之程式設計項目的相關資訊。

### <a name="overviews"></a>概觀



| 主題                                              | 目錄                                                                                                                          |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [關於工具提示控制項](tooltip-controls.md)     | 當使用者將滑鼠指標暫停在工具或其他 UI 元素上方時，工具提示會自動出現或快顯。<br/> |
| [使用工具提示控制項](using-tooltip-contro.md) | 本章節包含的範例會示範如何建立不同類型的工具提示。<br/>                             |



 

### <a name="messages"></a>訊息



| 主題                                               | 目錄                                                                                                                                                                                                          |
|-----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TTM \_ 啟用**](ttm-activate.md)               | 啟用或停用工具提示控制項。 <br/>                                                                                                                                                           |
| [**TTM \_ ADDTOOL**](ttm-addtool.md)                 | 使用工具提示控制項註冊工具。 <br/>                                                                                                                                                              |
| [**TTM \_ ADJUSTRECT**](ttm-adjustrect.md)           | 從視窗矩形計算工具提示控制項的文字顯示矩形，或從顯示指定的文字顯示矩形所需的工具提示視窗矩形。 <br/>                                |
| [**TTM \_ DELTOOL**](ttm-deltool.md)                 | 從工具提示控制項移除工具。 <br/>                                                                                                                                                                |
| [**TTM \_ ENUMTOOLS**](ttm-enumtools.md)             | 抓取工具提示控制項針對目前工具所維護的資訊，也就是工具提示目前顯示文字的工具。 <br/>                                               |
| [**TTM \_ GETBUBBLESIZE**](ttm-getbubblesize.md)     | 傳回工具提示控制項的寬度和高度。<br/>                                                                                                                                                     |
| [**TTM \_ GETCURRENTTOOL**](ttm-getcurrenttool.md)   | 抓取工具提示控制項中目前工具的資訊。 <br/>                                                                                                                                  |
| [**TTM \_ GETDELAYTIME**](ttm-getdelaytime.md)       | 抓取目前針對工具提示控制項設定的初始、快顯和 reshow 持續時間。<br/>                                                                                                               |
| [**TTM \_ GETMARGIN**](ttm-getmargin.md)             | 抓取工具提示視窗的頂端、左方、底端和右邊界設定。 邊界是工具提示視窗框線和工具提示視窗內所含文字之間的距離（以圖元為單位）。 <br/> |
| [**TTM \_ GETMAXTIPWIDTH**](ttm-getmaxtipwidth.md)   | 抓取工具提示視窗的最大寬度。 <br/>                                                                                                                                                     |
| [**TTM \_ GETTEXT**](ttm-gettext.md)                 | 抓取工具提示控制項維護工具的相關資訊。 <br/>                                                                                                                                   |
| [**TTM \_ GETTIPBKCOLOR**](ttm-gettipbkcolor.md)     | 抓取工具提示視窗中的背景色彩。 <br/>                                                                                                                                                   |
| [**TTM \_ GETTIPTEXTCOLOR**](ttm-gettiptextcolor.md) | 抓取工具提示視窗中的文字色彩。 <br/>                                                                                                                                                         |
| [**TTM \_ GETTITLE**](ttm-gettitle.md)               | 取得工具提示控制項標題的相關資訊。<br/>                                                                                                                                        |
| [**TTM \_ GETTOOLCOUNT**](ttm-gettoolcount.md)       | 捕獲工具提示控制項所維護的工具計數。 <br/>                                                                                                                                       |
| [**TTM \_ GETTOOLINFO**](ttm-gettoolinfo.md)         | 抓取工具提示控制項維護的工具相關資訊。 <br/>                                                                                                                              |
| [**TTM \_ SYSTEM.WINDOWS.MEDIA.VISUALTREEHELPER.HITTEST**](ttm-hittest.md)                 | 測試點以判斷它是否在指定之工具的周框矩形內，如果是，則會抓取工具的相關資訊。 <br/>                                                     |
| [**TTM \_ NEWTOOLRECT**](ttm-newtoolrect.md)         | 設定工具的新周框矩形。 <br/>                                                                                                                                                             |
| [**TTM \_ POP**](ttm-pop.md)                         | 從 view 中移除顯示的工具提示視窗。 <br/>                                                                                                                                                         |
| [**TTM \_ 快顯視窗**](ttm-popup.md)                     | 使工具提示顯示于最後一個滑鼠訊息的座標上。<br/>                                                                                                                            |
| [**TTM \_ RELAYEVENT**](ttm-relayevent.md)           | 將滑鼠訊息傳遞至工具提示控制項以進行處理。 <br/>                                                                                                                                           |
| [**TTM \_ SETDELAYTIME**](ttm-setdelaytime.md)       | 設定工具提示控制項的初始、彈出和 reshow 持續期間。<br/>                                                                                                                                  |
| [**TTM \_ SETMARGIN**](ttm-setmargin.md)             | 設定工具提示視窗的頂端、左方、下邊界和右邊界。 邊界是工具提示視窗框線和工具提示視窗內所含文字之間的距離（以圖元為單位）。 <br/>          |
| [**TTM \_ SETMAXTIPWIDTH**](ttm-setmaxtipwidth.md)   | 設定工具提示視窗的最大寬度。 <br/>                                                                                                                                                          |
| [**TTM \_ SETTIPBKCOLOR**](ttm-settipbkcolor.md)     | 設定工具提示視窗中的背景色彩。 <br/>                                                                                                                                                        |
| [**TTM \_ SETTIPTEXTCOLOR**](ttm-settiptextcolor.md) | 設定工具提示視窗中的文字色彩。 <br/>                                                                                                                                                              |
| [**TTM \_ SETTITLE**](ttm-settitle.md)               | 將標準圖示和標題字串新增至工具提示。<br/>                                                                                                                                                    |
| [**TTM \_ SETTOOLINFO**](ttm-settoolinfo.md)         | 設定工具提示控制項為工具維護的資訊。 <br/>                                                                                                                                     |
| [**TTM \_ SETWINDOWTHEME**](ttm-setwindowtheme.md)   | 設定工具提示控制項的視覺化樣式。<br/>                                                                                                                                                            |
| [**TTM \_ TRACKACTI加值稅E**](ttm-trackactivate.md)     | 啟用或停用追蹤工具提示。<br/>                                                                                                                                                           |
| [**TTM \_ TRACKPOSITION**](ttm-trackposition.md)     | 設定追蹤工具提示的位置。<br/>                                                                                                                                                               |
| [**TTM \_ 更新**](ttm-update.md)                   | 強制重新繪製目前的工具提示。 <br/>                                                                                                                                                             |
| [**TTM \_ UPDATETIPTEXT**](ttm-updatetiptext.md)     | 設定工具的工具提示文字。 <br/>                                                                                                                                                                     |
| [**TTM \_ WINDOWFROMPOINT**](ttm-windowfrompoint.md) | 允許子類別程式使工具提示顯示滑鼠游標下方以外的視窗文字。 <br/>                                                                              |



 

### <a name="notifications"></a>通知



| 主題                                                 | 目錄                                                                                                                                                                                                                                                              |
|-------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [NM \_ CUSTOMDRAW (工具提示) ](nm-customdraw-tooltip.md) | 由工具提示控制項傳送，以通知其父視窗關於繪圖作業。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。 <br/>                                                                                 |
| [TTN \_ GETDISPINFO](ttn-getdispinfo.md)               | 由工具提示控制項傳送，以取得顯示工具提示視窗所需的資訊。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。 <br/>                                                                            |
| [TTN \_ LINKCLICK](ttn-linkclick.md)                   | 按一下氣球工具提示內的文字連結時傳送。 <br/>                                                                                                                                                                                                |
| [TTN \_ NEEDTEXT](ttn-needtext.md)                     | 由工具提示控制項傳送，以取得顯示工具提示視窗所需的資訊。 此通知等同于 [TTN \_ GETDISPINFO](ttn-getdispinfo.md)。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。 <br/> |
| [TTN \_ POP](ttn-pop.md)                               | 通知擁有者視窗即將隱藏工具提示。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。 <br/>                                                                                                  |
| [TTN \_ SHOW](ttn-show.md)                             | 通知擁有者視窗即將顯示工具提示控制項。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。 <br/>                                                                                       |



 

### <a name="structures"></a>結構



| 主題                                    | 目錄                                                                                                                                                                                                                           |
|------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NMTTCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmttcustomdraw) | 包含工具提示控制項所傳送的 [NM \_ CUSTOMDRAW](nm-customdraw-tooltip.md) 通知碼特定資訊。 <br/>                                                                                           |
| [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa)     | 包含用來處理 [TTN \_ GETDISPINFO](ttn-getdispinfo.md) 通知碼的資訊。 此結構會取代 **TOOLTIPTEXT** 結構。 <br/>                                                          |
| [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa)             | [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa)結構包含工具提示控制項中工具的相關資訊。<br/>                                                                                                                      |
| [**TTGETTITLE**](/windows/desktop/api/Commctrl/ns-commctrl-ttgettitle)         | 提供工具提示控制項標題的相關資訊。 <br/>                                                                                                                                                             |
| [**TTHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-tthittestinfoa)   | 包含工具提示控制項用來判斷某個點是否在指定工具的周框中的資訊。 如果此點位於矩形中，則結構會接收工具的相關資訊。 <br/> |



 

### <a name="constants"></a>常數



| 主題                                | 目錄                                                                     |
|--------------------------------------|------------------------------------------------------------------------------|
| [工具提示樣式](tooltip-styles.md) | 此區段會列出與工具提示控制項搭配使用的控制項樣式。<br/> |



 

 

 





