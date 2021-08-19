---
title: 'SystemMonitor 物件 (Isysmon) '
description: 這個類別包含用來設定 [系統監視器] 控制項的方法和屬性。
ms.assetid: 5a6195ee-ed89-4f5d-85dd-88cf4a9b5155
keywords:
- SystemMonitor 物件 SysMon
- SystemMonitor 物件 SysMon，描述
topic_type:
- apiref
api_name:
- SystemMonitor
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88b9489c2e966abdf3c329d952a76bd30de487cca99a3e00c8ff46431a163ec9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117954503"
---
# <a name="systemmonitor-object"></a>SystemMonitor 物件

這個類別包含用來設定 [系統監視器] 控制項的方法和屬性。

## <a name="members"></a>成員

**SystemMonitor** 物件具有下列類型的成員：

-   [事件](#events)
-   [方法](#methods)
-   [屬性](#properties)

### <a name="events"></a>事件

**SystemMonitor** 物件具有這些事件。



| 事件                                                         | 描述                                                                                                                 |
|:--------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [**OnCounterAdded**](systemmonitor-oncounteradded.md)        | 當計數器新增至 [**計數器**](counters.md) 集合時通知您。<br/>                             |
| [**OnCounterDeleted**](-systemmonitor-oncounterdeleted.md)   | 從 [**計數器**](counters.md) 集合刪除計數器之前通知您。<br/>                       |
| [**OnCounterSelected**](-systemmonitor-oncounterselected.md) | 在選取計數器時通知您。<br/>                                                                         |
| [**OnDblClick**](-systemmonitor-ondblclick.md)               | 當使用者以滑鼠左鍵按兩下圖形線條、長條圖列或報表專案時，就會通知您。<br/> |
| [**OnSampleCollected**](-systemmonitor-onsamplecollected.md) | 在收集到計數器的取樣值時通知您。<br/>                                            |



 

### <a name="methods"></a>方法

**SystemMonitor** 物件有這些方法。



| 方法                                                       | 描述                                                                                                                                                              |
|:-------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BatchLocking**](systemmonitor-batchinglock.md)           | 鎖定系統監視器，以防止它從新加入的計數器或記錄檔取樣計數器資料。<br/>                                                   |
| [**BrowseCounters**](systemmonitor-browsecounters.md)       | 顯示 [ **加入計數器** ] 對話方塊。<br/>                                                                                                                      |
| [**ClearData**](systemmonitor-cleardata.md)                 | 清除控制項中的所有資料欄位。<br/>                                                                                                                        |
| [**CollectSample**](systemmonitor-collectsample.md)         | 為 **計數器** 集合物件中的每個計數器取樣一個值。<br/>                                                                                       |
| [**複製**](systemmonitor-copy.md)                           | 將控制項的屬性設定、計數器清單和計數器資料複製到剪貼簿，以做為 HTML 物件。<br/>                                                |
| [**DisplayProperties**](systemmonitor-displayproperties.md) | 顯示 [ **Graph 屬性**] 對話方塊。<br/>                                                                                                                 |
| [**GetLogViewRange**](systemmonitor-getlogviewrange.md)     | 抓取用來從記錄檔中取出計數器值的開始日期。<br/>                                                                               |
| [**LoadSettings**](systemmonitor-loadsettings.md)           | 將 HTML 範本檔案中的計數器加入至系統監視器。<br/>                                                                                            |
| [**貼上**](systemmonitor-paste.md)                         | 將複製到剪貼簿的計數器清單附加至目前的計數器集合。 <br/>                                                        |
| [**重新記錄**](systemmonitor-relog.md)                         | 將計數器資料 Relogs 至新的檔案。 您也可以使用這個方法來指定新的檔案類型，並減少記錄檔中包含的樣本數目。<br/> |
| [**重設**](systemmonitor-reset.md)                         | 從 **計數器** 集合物件中移除所有 [**CounterItem**](counteritem.md)物件。<br/>                                                               |
| [**SaveAs**](systemmonitor-saveas.md)                       | 將圖形視圖中的計數器值儲存至記錄檔。<br/>                                                                                                     |
| [**ScaleToFit**](systemmonitor-scaletofit.md)               | 調整計數器值以納入圖形中。<br/>                                                                                                                     |
| [**SetLogViewRange**](systemmonitor-setlogviewrange.md)     | 設定用來從記錄檔中取出計數器值的開始日期。<br/>                                                                                    |
| [**UpdateGraph**](systemmonitor-updategraph.md)             | 重新整理系統監視器視窗的內容。<br/>                                                                                                         |



 

### <a name="properties"></a>屬性

**SystemMonitor** 物件具有這些屬性。



| 屬性                                                                                | 描述                                                                                                                                                                                                                             |
|:----------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**外觀**](systemmonitor-appearance.md)<br/>                               | 抓取或設定控制項的外觀，以包含或省略三維顯示效果。<br/>                                                                                                                        |
| [**顏色**](systemmonitor-backcolor.md)<br/>                                 | 抓取或設定圖形和報表檢視的背景色彩。<br/>                                                                                                                                                        |
| [**BackColorCtl**](systemmonitor-backcolorctl.md)<br/>                           | 抓取或設定控制項的背景色彩。<br/>                                                                                                                                                                       |
| [**BorderStyle**](systemmonitor-borderstyle.md)<br/>                             | 抓取或設定控制項的框線樣式。<br/>                                                                                                                                                                           |
| [**ChartScroll**](systemmonitor-chartscroll.md)<br/>                             | 抓取或設定值，這個值會決定折線圖是否會在視圖中滾動。<br/>                                                                                                                                             |
| [**計數器**](systemmonitor-counters.md)<br/>                                   | 捕獲 [**CounterItem**](counteritem.md) 物件的集合。<br/>                                                                                                                                                      |
| [**DataPointCount**](systemmonitor-datapointcount.md)<br/>                       | 抓取或設定線條圖形中顯示的資料點數目。<br/>                                                                                                                                                       |
| [**DataSourceType**](systemmonitor-datasourcetype.md)<br/>                       | 抓取或設定效能計數器資料的來源。<br/>                                                                                                                                                                |
| [**DisplayType**](systemmonitor-displaytype.md)<br/>                             | 抓取或設定用來繪製效能計數器資料圖形的圖表類型。<br/>                                                                                                                                              |
| [**EnableDigitGrouping**](systemmonitor-enabledigitgrouping.md)<br/>             | 抓取或設定值，這個值會決定 SYSMON 是否在顯示數值時使用數位群組。<br/>                                                                                                                      |
| [**EnableToolTips**](systemmonitor-enabletooltips.md)<br/>                       | 抓取或設定值，這個值會決定當滑鼠停留在其中一個圖形瀏覽器的計數器上方時，是否要顯示工具提示。<br/>                                                                                             |
| [**Font**](systemmonitor-font.md)<br/>                                           | 抓取或設定控制項中所使用的字型。<br/>                                                                                                                                                                              |
| [**ForeColor**](systemmonitor-forecolor.md)<br/>                                 | 抓取或設定顯示在控制項中的文字色彩。<br/>                                                                                                                                                         |
| [**GraphTitle**](systemmonitor-graphtitle.md)<br/>                               | 抓取或設定圖形的標題。<br/>                                                                                                                                                                                    |
| [**GridColor**](systemmonitor-gridcolor.md)<br/>                                 | 抓取或設定圖形中所使用之格線的色彩。<br/>                                                                                                                                                             |
| [**反白顯示**](systemmonitor-highlight.md)<br/>                                 | 抓取或設定值，指出在圖形中是否反白顯示所選計數器的值。<br/>                                                                                                               |
| [**LogFileName**](systemmonitor-logfilename.md)<br/>                             | 已過時。 抓取或設定要做為系統監視器中顯示的計數器值來源之記錄檔的名稱。<br/>                                                                                                   |
| [**LogFiles**](systemmonitor-logfilename.md)<br/>                                | 收集一或多個要作為系統監視器中顯示的計數器值來源的記錄檔。<br/>                                                                                                                  |
| [**LogSourceStartTime**](systemmonitor-logsourcestarttime.md)<br/>               | 從已記錄在記錄檔中的計數器集合中的計數器，抓取最早計數器值的時間戳記。<br/>                                                                                           |
| [**LogSourceStopTime**](systemmonitor-logsourcestoptime.md)<br/>                 | 從計數器集合中記錄在記錄檔中的計數器，抓取最新計數器值的時間戳記。<br/>                                                                                             |
| [**LogViewStart**](systemmonitor-logviewstart.md)<br/>                           | 取得或設定用來從記錄檔抓取計數器值的開始日期。<br/>                                                                                                                                      |
| [**LogViewStop**](systemmonitor-logviewstop.md)<br/>                             | 取得或設定用來從記錄檔抓取計數器值的結束日期。<br/>                                                                                                                                        |
| [**ManualUpdate**](systemmonitor-manualupdate.md)<br/>                           | 抓取或設定值，指出系統監視器的內容將會以手動方式更新，還是在指定的間隔自動更新。<br/>                                                                           |
| [**MaximumScale**](systemmonitor-maximumscale.md)<br/>                           | 抓取或設定圖形垂直 (Y) 軸的最大值。<br/>                                                                                                                                                   |
| [**MinimumScale**](systemmonitor-minimumscale.md)<br/>                           | 抓取或設定圖形垂直 (Y) 軸的最小值。<br/>                                                                                                                                                   |
| [**MonitorDuplicateInstances**](systemmonitor-monitorduplicateinstances.md)<br/> | 抓取或設定值，這個值會決定是否可以監視計數器的多個實例。<br/>                                                                                                                          |
| [**ReadOnly**](systemmonitor-readonly.md)<br/>                                   | 抓取或設定值，這個值會決定使用者是否可以修改控制項的屬性值。<br/>                                                                                                                      |
| [**ReportValueType**](systemmonitor-reportvaluetype.md)<br/>                     | 抓取或設定值，這個值會決定長條圖和報表檢視是否會圖形化取樣間隔期間所取樣的最後一個值，或取樣中的計算值，例如平均或最小計數器值。<br/> |
| [**ShowHorizontalGrid**](systemmonitor-showhorizontalgrid.md)<br/>               | 抓取或設定值，這個值會決定是否要在圖形中顯示水準格線。<br/>                                                                                                                          |
| [**ShowLegend**](systemmonitor-showlegend.md)<br/>                               | 抓取或設定值，這個值會決定是否要顯示圖例。<br/>                                                                                                                                                   |
| [**ShowScaleLabels**](systemmonitor-showscalelabels.md)<br/>                     | 抓取或設定值，這個值會決定尺規標籤是否會顯示在圖形的垂直軸上。<br/>                                                                                                          |
| [**ShowTimeAxisLabels**](systemmonitor-showtimeaxislabels.md)<br/>               | 抓取或設定值，這個值會判斷圖形視圖的水準 (X) 軸是否包含標籤。<br/>                                                                                                                      |
| [**ShowToolbar**](systemmonitor-showtoolbar.md)<br/>                             | 抓取或設定值，這個值會決定是否要在控制項上顯示工具列。<br/>                                                                                                                                   |
| [**ShowValueBar**](systemmonitor-showvaluebar.md)<br/>                           | 抓取或設定值，這個值會決定是否要在控制項上顯示值列 (圖形) 下方的統計值集。<br/>                                                                                 |
| [**ShowVerticalGrid**](systemmonitor-showverticalgrid.md)<br/>                   | 抓取或設定值，這個值會決定是否要在圖形中顯示垂直格線。<br/>                                                                                                                            |
| [**SqlDsnName**](systemmonitor-sqldsnname.md)<br/>                               | 抓取或設定 ODBC 資料來源名稱。<br/>                                                                                                                                                                                 |
| [**SqlLogSetName**](systemmonitor-sqllogsetname.md)<br/>                         | 抓取或設定記錄集的易記名稱。<br/>                                                                                                                                                                          |
| [**TimeBarColor**](systemmonitor-timebarcolor.md)<br/>                           | 抓取或設定狀態列的色彩， (在圖形視窗間移動的垂直列，以指出折線圖) 中每個取樣間隔的段。<br/>                                                  |
| [**UpdateInterval**](systemmonitor-updateinterval.md)<br/>                       | 抓取或設定 SYSMON 在下一次更新圖表或報表之前等候的時間長度。<br/>                                                                                                                  |
| [**YAxisLabel**](systemmonitor-yaxislabel.md)<br/>                               | 抓取或設定圖形垂直 (Y) 軸的標籤。<br/>                                                                                                                                                           |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                            |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Isysmon。h</dt> </dl>  |
| DLL<br/>                      | <dl> <dt>Sysmon .ocx</dt> </dl> |



 

 





