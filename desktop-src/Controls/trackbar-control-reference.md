---
title: 跟蹤
description: 本章節包含與 [資料段] 控制項搭配使用之程式設計項目的相關資訊。
ms.assetid: vs|controls|~\controls\trackbar\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f56c5a483340a8e77ef0df6503481d3cbc50e51a85bd07258cdf283dd563c6a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060538"
---
# <a name="trackbar"></a>跟蹤

本章節包含與 [資料段] 控制項搭配使用之程式設計項目的相關資訊。

### <a name="overviews"></a>概觀



| 主題                                                  | 目錄                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [關於資料說明控制項](trackbar-controls.md)       | [點擊線] 是一種視窗，其中包含滑杆 (有時也稱為頻道中) 的捲動方塊，以及選擇性的刻度標記。 當使用者使用滑鼠或方向按鍵移動滑杆時，會傳送通知訊息以指出變更。<br/> |
| [使用 [使用] 控制項](using-trackbar-controls.md) | 本章節提供適用于區段控制項的執行詳細資料和範例。<br/>                                                                                                                                                                               |



 

### <a name="messages"></a>訊息



| 主題                                                 | 目錄                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TBM \_ CLEARSEL**](tbm-clearsel.md)                 | 清除目前選取範圍中的選取範圍。 <br/>                                                                                                                                                                                                                                                      |
| [**TBM \_ CLEARTICS**](tbm-cleartics.md)               | 從跟蹤條中移除目前的刻度標記。 此訊息不會移除第一個和最後一個刻度，這些刻度會由 [並排顯示] 自動建立。 <br/>                                                                                                                                           |
| [**TBM \_ GETBUDDY**](tbm-getbuddy.md)                 | 抓取指定位置上的 [查看點] 控制項好友視窗控制碼。 指定的位置是相對於控制項的方向 (水準或垂直) 。 <br/>                                                                                                                                 |
| [**TBM \_ GETCHANNELRECT**](tbm-getchannelrect.md)     | 抓取的區域框之頻道的大小與位置。  (通道是滑杆移動的區域。 它包含選取範圍時的醒目提示。 )  <br/>                                                                                                         |
| [**TBM \_ GETLINESIZE**](tbm-getlinesize.md)           | 抓取捲軸滑動軸移動以回應鍵盤輸入的邏輯位置數目，例如，或索引鍵。 邏輯位置是捲軸的最小值與最大滑杆位置之間的整數增量。 <br/>                                         |
| [**TBM \_ GETNUMTICS**](tbm-getnumtics.md)             | 抓取在一個標記中的刻度數目。 <br/>                                                                                                                                                                                                                                                      |
| [**TBM \_ GETPAGESIZE**](tbm-getpagesize.md)           | 抓取捲軸的滑杆為了回應鍵盤輸入（例如或按鍵）或滑鼠輸入而移動的邏輯位置數目，例如在並排條的通道中按一下。 邏輯位置是捲軸的最小值與最大滑杆位置之間的整數增量。 <br/>   |
| [**TBM \_ GETPOS**](tbm-getpos.md)                     | 抓取捲軸中滑杆的目前邏輯位置。 邏輯位置是在最小至最大滑杆位置的 [最大值] 範圍內的整數值。 <br/>                                                                                                                       |
| [**TBM \_ GETPTICS**](tbm-getptics.md)                 | 抓取陣列的位址，這個陣列包含了刻度的刻度位置。 <br/>                                                                                                                                                                                                        |
| [**TBM \_ GETRANGEMAX**](tbm-getrangemax.md)           | 抓取捲軸中滑杆的最大位置。 <br/>                                                                                                                                                                                                                                           |
| [**TBM \_ GETRANGEMIN**](tbm-getrangemin.md)           | 抓取捲軸中滑杆的最小位置。 <br/>                                                                                                                                                                                                                                           |
| [**TBM \_ GETSELEND**](tbm-getselend.md)               | 抓取目前選取範圍的結束位置。 <br/>                                                                                                                                                                                                                            |
| [**TBM \_ GETSELSTART**](tbm-getselstart.md)           | 抓取目前選取範圍在 [選取範圍] 中的開始位置。 <br/>                                                                                                                                                                                                                          |
| [**TBM \_ GETTHUMBLENGTH**](tbm-getthumblength.md)     | 抓取捲軸中滑杆的長度。 <br/>                                                                                                                                                                                                                                                      |
| [**TBM \_ GETTHUMBRECT**](tbm-getthumbrect.md)         | 抓取捲軸中滑杆的周框大小和位置。 <br/>                                                                                                                                                                                                                |
| [**TBM \_ GETTIC**](tbm-gettic.md)                     | 捕獲刻度中刻度標記的邏輯位置。 邏輯位置可以是 [最小值] 和 [最大值] 滑杆位置範圍中的任何整數值。 <br/>                                                                                                                     |
| [**TBM \_ GETTICPOS**](tbm-getticpos.md)               | 抓取刻度中刻度標記目前的實體位置。<br/>                                                                                                                                                                                                                                   |
| [**TBM \_ GETTOOLTIPS**](tbm-gettooltips.md)           | 抓取指派給的提示（如果有的話）之工具提示控制項的控制碼。 <br/>                                                                                                                                                                                                                          |
| [**TBM \_ GETUNICODEFORMAT**](tbm-getunicodeformat.md) | 抓取控制項的 Unicode 字元格式旗標。 <br/>                                                                                                                                                                                                                                           |
| [**TBM \_ SETBUDDY**](tbm-setbuddy.md)                 | 將視窗指派為 [查看] 控制項的合作者視窗。 [並排顯示] 視窗會自動顯示在相對於控制項方向 (水準或垂直) 的位置。 <br/>                                                                                                          |
| [**TBM \_ SETLINESIZE**](tbm-setlinesize.md)           | 設定從箭號按鍵（例如，或按鍵）回應鍵盤輸入時，會將這些捲軸滑杆移動的邏輯位置數目。 邏輯位置是捲軸的最小值與最大滑杆位置之間的整數增量。 <br/>                                              |
| [**TBM \_ >SETPAGESIZE METHOD**](tbm-setpagesize.md)           | 設定捲軸的滑杆為了回應鍵盤輸入而移動的邏輯位置數目，例如或按鍵，或滑鼠輸入，例如在並排條通道中按一下。 邏輯位置是捲軸的最小值與最大滑杆位置之間的整數增量。 <br/>        |
| [**TBM \_ SETPOS**](tbm-setpos.md)                     | 設定捲軸中滑杆的目前邏輯位置。 <br/>                                                                                                                                                                                                                                         |
| [**TBM \_ SETPOSNOTIFY**](tbm-setposnotify.md)         | 設定捲軸中滑杆的目前邏輯位置。 <br/>                                                                                                                                                                                                                                         |
| [**TBM \_ SETRANGE**](tbm-setrange.md)                 | 設定捲軸中滑杆的最小和最大邏輯位置的範圍。 <br/>                                                                                                                                                                                                                  |
| [**TBM \_ SETRANGEMAX**](tbm-setrangemax.md)           | 設定捲軸中滑杆的最大邏輯位置。 <br/>                                                                                                                                                                                                                                        |
| [**TBM \_ SETRANGEMIN**](tbm-setrangemin.md)           | 設定捲軸中滑杆的最小邏輯位置。 <br/>                                                                                                                                                                                                                                        |
| [**TBM \_ SETSEL**](tbm-setsel.md)                     | 設定在 [選取區] 中可用選取範圍的開始和結束位置。 <br/>                                                                                                                                                                                                                |
| [**TBM \_ SETSELEND**](tbm-setselend.md)               | 在 [選取區] 中設定目前選取範圍的結束邏輯位置。 如果 [ENABLESELRANGE] 沒有 [ [**tb] \_**](trackbar-control-styles.md) 樣式，則會忽略此訊息。 <br/>                                                                              |
| [**TBM \_ SETSELSTART**](tbm-setselstart.md)           | 在 [選取區] 中設定目前選取範圍的開始邏輯位置。 如果 [ENABLESELRANGE] 沒有 [ [**tb] \_**](trackbar-control-styles.md) 樣式，則會忽略此訊息。 <br/>                                                                            |
| [**TBM \_ SETTHUMBLENGTH**](tbm-setthumblength.md)     | 設定捲軸中滑杆的長度。 如果 [FIXEDLENGTH] 沒有 [ [**tb] \_**](trackbar-control-styles.md) 樣式，則會忽略此訊息。 <br/>                                                                                                                      |
| [**TBM \_ SETTIC**](tbm-settic.md)                     | 在指定的邏輯位置的 [查看] 中設定刻度。 <br/>                                                                                                                                                                                                                                      |
| [**TBM \_ SETTICFREQ**](tbm-setticfreq.md)             | 設定在 [標記] 中刻度的間隔頻率。 例如，如果 [頻率] 設定為 [二]，則會在 [顯示區] 範圍中顯示每個其他增量的刻度。 頻率的預設設定為 1;亦即，範圍中的每個遞增都會與刻度相關聯。 <br/> |
| [**TBM \_ SETTIPSIDE**](tbm-settipside.md)             | 放置 [提示] 控制項所使用的工具提示控制項。 使用 [ [**TBS \_ 工具提示**](trackbar-control-styles.md) ] 樣式的 [顯示工具提示] 控制項。 <br/>                                                                                                                           |
| [**TBM \_ SETTOOLTIPS**](tbm-settooltips.md)           | 將工具提示控制項指派給 [對等] 控制項。 <br/>                                                                                                                                                                                                                                                       |
| [**TBM \_ SETUNICODEFORMAT**](tbm-setunicodeformat.md) | 設定控制項的 Unicode 字元格式旗標。 此訊息可讓您變更控制項在執行時間所使用的字元集，而不需要重新建立控制項。 <br/>                                                                                                               |



 

### <a name="notifications"></a>通知



| 主題                                                              | 目錄                                                                                                                                                                                      |
|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [NM \_ CUSTOMDRAW (的) ](nm-customdraw-trackbar.md)            | 由 [資料提示] 控制項傳送，以通知其父視窗關於繪圖作業。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。 <br/>        |
| [NM \_ RELEASEDCAPTURE (的) ](nm-releasedcapture-trackbar-.md) | 通知字幕控制項的父視窗，控制項正在放開滑鼠捕捉。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。 <br/> |
| [TRBN \_ THUMBPOSCHANGING](trbn-thumbposchanging.md)                | 通知正在進行的捲軸位置變更。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。<br/>                               |



 

### <a name="constants"></a>常數



| 主題                                                  | 目錄                                                                                    |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [自訂繪製值](custom-draw-values.md)           | 此區段會列出用來識別資料列控制群組件的值。 <br/>      |
| [[控制項] 控制項樣式](trackbar-control-styles.md) | 本章節包含與 [資料] 控制項搭配使用之樣式的相關資訊。 <br/> |



 

 

 





