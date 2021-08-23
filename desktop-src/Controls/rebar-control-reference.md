---
title: 鋼筋
description: 本章節包含與 Rebar 控制項搭配使用之程式設計項目的相關資訊。
ms.assetid: vs|controls|~\controls\rebar\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14ac71ea71b5e0b0bd1e222d46c070a62512f0f5ff3b885fe13b19fad10f7bf7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119434838"
---
# <a name="rebar"></a>鋼筋

本章節包含與 Rebar 控制項搭配使用之程式設計項目的相關資訊。

### <a name="overviews"></a>概觀



| 主題                                            | 目錄                                                                               |
|--------------------------------------------------|----------------------------------------------------------------------------------------|
| [Rebar 控制項](rebar-controls.md)             | *Rebar 控制項* 可作為子視窗的容器。<br/>                       |
| [使用 Rebar 控制項](using-rebar-controls.md) | 本章節包含範例程式碼，示範如何執行 Rebar 控制項。<br/> |



 

### <a name="messages"></a>訊息



| 主題                                               | 目錄                                                                                                                                                                                             |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**RB \_ BEGINDRAG**](rb-begindrag.md)               | 將 Rebar 控制項放在拖放模式中。 此訊息不會造成 [RBN \_ BEGINDRAG](rbn-begindrag.md) 通知傳送。 <br/>                                                 |
| [**RB \_ DELETEBAND**](rb-deleteband.md)             | 從 Rebar 控制項刪除頻外。 <br/>                                                                                                                                                     |
| [**RB \_ DRAGMOVE**](rb-dragmove.md)                 | 更新在上一個 [**RB \_ BEGINDRAG**](rb-begindrag.md) 訊息之後，Rebar 控制項中的拖曳位置。 <br/>                                                                           |
| [**RB \_ ENDDRAG**](rb-enddrag.md)                   | 終止 Rebar 控制項的拖放作業。 此訊息不會造成 [RBN \_ ENDDRAG](rbn-enddrag.md) 通知傳送。 <br/>                                          |
| [**RB \_ GETBANDBORDERS**](rb-getbandborders.md)     | 抓取寬線的框線。 此訊息的結果可以用來計算頻外的可用區域。 <br/>                                                                          |
| [**RB \_ GETBANDCOUNT**](rb-getbandcount.md)         | 抓取目前在 Rebar 控制項中的條紋計數。 <br/>                                                                                                                             |
| [**RB \_ GETBANDINFO**](rb-getbandinfo.md)           | 抓取 Rebar 控制項中指定之頻外的相關資訊。 <br/>                                                                                                                         |
| [**RB \_ GETBANDMARGINS**](rb-getbandmargins.md)     | 抓取寬線的邊界。<br/>                                                                                                                                                          |
| [**RB \_ GETBARHEIGHT**](rb-getbarheight.md)         | 抓取 Rebar 控制項的高度。 <br/>                                                                                                                                               |
| [**RB \_ GETBARINFO**](rb-getbarinfo.md)             | 抓取 Rebar 控制項及其所使用影像清單的相關資訊。 <br/>                                                                                                                |
| [**RB \_ GETBKCOLOR**](rb-getbkcolor.md)             | 抓取 Rebar 控制項的預設背景色彩。 <br/>                                                                                                                                    |
| [**RB \_ GETCOLORSCHEME**](rb-getcolorscheme.md)     | 從 Rebar 控制項抓取色彩配置資訊。 <br/>                                                                                                                           |
| [**RB \_ GETDROPTARGET**](rb-getdroptarget.md)       | 抓取 Rebar 控制項的 [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) 介面指標。 <br/>                                                                                                        |
| [**RB \_ GETEXTENDEDSTYLE**](rb-getextendedstyle.md) | 取得延伸樣式。 <br/>                                                                                                                                                                 |
| [**RB \_ GETPALETTE**](rb-getpalette.md)             | 抓取 Rebar 控制項的目前調色板。 <br/>                                                                                                                                           |
| [**RB \_ GETRECT**](rb-getrect.md)                   | 抓取 Rebar 控制項中指定範圍的周框。 <br/>                                                                                                                    |
| [**RB \_ GETROWCOUNT**](rb-getrowcount.md)           | 抓取 Rebar 控制項中的資料列數。 <br/>                                                                                                                                |
| [**RB \_ GETROWHEIGHT**](rb-getrowheight.md)         | 抓取 Rebar 控制項中指定之資料列的高度。 <br/>                                                                                                                              |
| [**RB \_ GETTEXTCOLOR**](rb-gettextcolor.md)         | 抓取 Rebar 控制項的預設文字色彩。 <br/>                                                                                                                                          |
| [**RB \_ GETTOOLTIPS**](rb-gettooltips.md)           | 抓取與 Rebar 控制項相關聯之任何工具提示控制項的控制碼。 <br/>                                                                                                           |
| [**RB \_ GETUNICODEFORMAT**](rb-getunicodeformat.md) | 抓取控制項的 Unicode 字元格式旗標。 <br/>                                                                                                                             |
| [**RB \_ SYSTEM.WINDOWS.MEDIA.VISUALTREEHELPER.HITTEST**](rb-hittest.md)                   | 判斷如果在該點上存在 Rebar 帶，則在螢幕上的某個點上，Rebar 區的哪個部分是在指定的點上。 <br/>                                                                        |
| [**RB \_ IDTOINDEX**](rb-idtoindex.md)               | 將帶狀識別碼轉換為 Rebar 控制項中的寬線索引。 <br/>                                                                                                                           |
| [**RB \_ INSERTBAND**](rb-insertband.md)             | 在 Rebar 控制項中插入新的波段。 <br/>                                                                                                                                                   |
| [**RB \_ MAXIMIZEBAND**](rb-maximizeband.md)         | 將 Rebar 控制項中的寬線大小調整為理想或最大的大小。 <br/>                                                                                                                   |
| [**RB \_ MINIMIZEBAND**](rb-minimizeband.md)         | 將 Rebar 控制項中的寬線大小調整為最小的大小。 <br/>                                                                                                                                  |
| [**RB \_ MOVEBAND**](rb-moveband.md)                 | 將一個索引區從一個索引移至另一個索引。 <br/>                                                                                                                                                  |
| [**RB \_ PUSHCHEVRON**](rb-pushchevron.md)           | 傳送至 Rebar 控制項以程式設計方式推送燕形。<br/>                                                                                                                               |
| [**RB \_ SETBANDINFO**](rb-setbandinfo.md)           | 在 Rebar 控制項中設定現有波段的特性。 <br/>                                                                                                                             |
| [**RB \_ SETBANDWIDTH**](rb-setbandwidth.md)         | 設定停駐區的寬度。<br/>                                                                                                                                                         |
| [**RB \_ SETBARINFO**](rb-setbarinfo.md)             | 設定 Rebar 控制項的特性。 <br/>                                                                                                                                             |
| [**RB \_ SETBKCOLOR**](rb-setbkcolor.md)             | 設定 Rebar 控制項的預設背景色彩。 <br/>                                                                                                                                         |
| [**RB \_ SETCOLORSCHEME**](rb-setcolorscheme.md)     | 設定 Rebar 控制項的色彩配置資訊。 <br/>                                                                                                                                 |
| [**RB \_ SETEXTENDEDSTYLE**](rb-setextendedstyle.md) | 設定延伸樣式。 此訊息不會執行。<br/>                                                                                                                                 |
| [**RB \_ SETPALETTE**](rb-setpalette.md)             | 設定 Rebar 控制項的目前調色板。 <br/>                                                                                                                                                |
| [**RB \_ SETPARENT**](rb-setparent.md)               | 設定 Rebar 控制項的父視窗。 <br/>                                                                                                                                                    |
| [**RB \_ SETTEXTCOLOR**](rb-settextcolor.md)         | 設定 Rebar 控制項的預設文字色彩。 <br/>                                                                                                                                               |
| [**RB \_ SETTOOLTIPS**](rb-settooltips.md)           | 將工具提示控制項與 Rebar 控制項產生關聯。 <br/>                                                                                                                                     |
| [**RB \_ SETUNICODEFORMAT**](rb-setunicodeformat.md) | 設定控制項的 Unicode 字元格式旗標。 此訊息可讓您變更控制項在執行時間所使用的字元集，而不需要重新建立控制項。 <br/> |
| [**RB \_ SETWINDOWTHEME**](rb-setwindowtheme.md)     | 設定 Rebar 控制項的視覺化樣式。<br/>                                                                                                                                                 |
| [**RB \_ SHOWBAND**](rb-showband.md)                 | 顯示或隱藏 Rebar 控制項中的指定頻。 <br/>                                                                                                                                          |
| [**RB \_ SIZETORECT**](rb-sizetorect.md)             | 嘗試找出指定矩形之區段的最佳版面配置。 <br/>                                                                                                                   |



 

### <a name="notifications"></a>通知



| 主題                                                        | 目錄                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [NM \_ CUSTOMDRAW (Rebar) ](nm-customdraw-rebar.md)            | 由 Rebar 控制項傳送，以通知其父視窗有關繪製作業。 此通知會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。<br/>                                                                                               |
| [NM \_ NCHITTEST (Rebar) ](nm-nchittest-rebar.md)              | 當控制項收到 [**WM \_ NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) 訊息時，由 Rebar 控制項傳送。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。 <br/>                                                                 |
| [NM \_ RELEASEDCAPTURE (Rebar) ](nm-releasedcapture-rebar-.md) | 通知 Rebar 控制項的父視窗，控制項正在放開滑鼠捕捉。 此通知會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。 <br/>                                                                                        |
| [RBN \_ AUTOBREAK](rbn-autobreak.md)                          | 通知 [Rebar 的](rebar-controls.md) 父系，將會在橫條中顯示中斷。 父代會決定是否要進行中斷。 <br/>                                                                                                                            |
| [RBN \_ AUTOSIZE](rbn-autosize.md)                            | 當 Rebar 自動調整大小時，以 [**RBS \_ AUTOSIZE**](rebar-control-styles.md) 樣式建立的 Rebar 控制項傳送。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。 <br/>                  |
| [RBN \_ BEGINDRAG](rbn-begindrag.md)                          | 當使用者開始拖曳寬線時，由 Rebar 控制項傳送。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。 <br/>                                                                                                           |
| [RBN \_ CHEVRONPUSHED](rbn-chevronpushed.md)                  | 當推送燕形時由 Rebar 控制項傳送。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。<br/>                                                                                                                        |
| [RBN \_ CHILDSIZE](rbn-childsize.md)                          | 當調整寬線的子視窗大小時，由 Rebar 控制項傳送。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。 <br/>                                                                                                          |
| [RBN \_ DELETEDBAND](rbn-deletedband.md)                      | 在刪除帶狀之後，由 Rebar 控制項傳送。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。 <br/>                                                                                                                  |
| [RBN \_ DELETINGBAND](rbn-deletingband.md)                    | 當您即將刪除內區時，由 Rebar 控制項傳送。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。 <br/>                                                                                                             |
| [RBN \_ ENDDRAG](rbn-enddrag.md)                              | 當使用者停止拖曳寬線時，由 Rebar 控制項傳送。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。 <br/>                                                                                                            |
| [RBN \_ GETOBJECT](rbn-getobject.md)                          | 當物件拖曳至控制項中的範圍時，以 [**RBS \_ REGISTERDROP**](rebar-control-styles.md) 樣式建立的 Rebar 控制項所傳送。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。 <br/> |
| [RBN \_ HEIGHTCHANGE](rbn-heightchange.md)                    | 當 Rebar 控制項的高度變更時傳送。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。 <br/>                                                                                                                    |
| [RBN \_ LAYOUTCHANGED](rbn-layoutchanged.md)                  | 當使用者變更控制列紋的版面配置時，由 Rebar 控制項傳送。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。 <br/>                                                                                        |
| [RBN \_ MINMAX](rbn-minmax.md)                                | 在最大化或最小化寬線之前，由 Rebar 控制項傳送。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。 <br/>                                                                                                       |
| [RBN \_ SPLITTERDRAG](rbn-splitterdrag.md)                    | 由 Rebar 控制項在使用者拖曳分隔器時傳送。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。 <br/>                                                                                                                 |



 

### <a name="structures"></a>結構



| 主題                                        | 目錄                                                                                                                                      |
|----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**NMRBAUTOSIZE**](/windows/win32/api/commctrl/ns-commctrl-nmrbautosize)         | 包含用來處理 RBN 自動 [ \_ 調整](rbn-autosize.md) 通知碼的資訊。 <br/>                                   |
| [**NMREBAR**](/windows/win32/api/commctrl/ns-commctrl-nmrebar)                   | 包含用來處理各種 Rebar 通知碼的資訊。 <br/>                                                           |
| [**NMREBARAUTOBREAK**](/windows/win32/api/commctrl/ns-commctrl-nmrebarautobreak) | 包含 [RBN \_ AUTOBREAK](rbn-autobreak.md) 通知所使用的資訊。<br/>                                               |
| [**NMREBARCHEVRON**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchevron)     | 包含用來處理 [RBN \_ CHEVRONPUSHED](rbn-chevronpushed.md) 通知碼的資訊。 <br/>                          |
| [**NMREBARCHILDSIZE**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchildsize) | 包含用來處理 [RBN \_ CHILDSIZE](rbn-childsize.md) 通知碼的資訊。 <br/>                                  |
| [**NMREBARSPLITTER**](/windows/win32/api/commctrl/ns-commctrl-nmrebarsplitter)   | 包含用來處理 [RBN \_ SPLITTERDRAG](rbn-splitterdrag.md) 通知碼的資訊。<br/>                                |
| [**RBHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-rbhittestinfo)       | 包含點擊測試作業的特定資訊。 此結構會搭配 [**RB \_ system.windows.media.visualtreehelper.hittest**](rb-hittest.md) 訊息使用。 <br/> |
| [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa)       | 包含在 Rebar 控制項中定義寬線的資訊。 <br/>                                                                      |
| [**REBARINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarinfo)               | 包含描述 Rebar 控制項特性的資訊。 <br/>                                                                |



 

### <a name="constants"></a>常數



| 主題                                            | 目錄                                                                                              |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [Rebar 控制項樣式](rebar-control-styles.md) | 除了標準視窗樣式之外，Rebar 控制項還支援各種控制項樣式。 <br/> |



 

 

