---
title: 系統監視器中的新功能
description: 下表指出每個版本的系統監視器 (SYSMON) 的新功能。
ms.assetid: 9cb0e0db-0933-4993-a995-74a36a24eccb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b3662e83954630232e3fe30c26a3f6d94aa9cc7
ms.sourcegitcommit: 780d4b1601c45658ef0b799b80d13f45a53d808d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/26/2020
ms.locfileid: "104374669"
---
# <a name="whats-new-in-system-monitor"></a>系統監視器中的新功能

下表指出每個版本的系統監視器 (SYSMON) 的新功能。



| 版本     | 功能描述                                                                                                                                                                                                                                                                                                                              |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本3。7 | 此版本會新增新的圖表類型、可選取多個計數器、從圖形上的某個點抓取計數器值、將圖表計數器值儲存至記錄檔，以及讓折線圖持續在圖形視窗中移動，而不是在其本身換行的選項。包含在 Windows Server 2008 和 Windows Vista 中。<br/> |



 

## <a name="version-37"></a>版本3。7

新增至 [**CounterItem**](counteritem.md)的新屬性和方法。

-   [**GetDataAt**](counteritem-getdataat.md)
-   [**已選取**](counteritem-selected.md)
-   [**可見**](counteritem-visible.md)
-   CounterItem 的有效值範圍已變更 [ **。寬度**](counteritem-width.md)

新增至 [**SystemMonitor**](systemmonitor.md)的新屬性和方法。

-   [**BatchingLock**](systemmonitor-batchinglock.md)
-   [**ChartScroll**](systemmonitor-chartscroll.md)
-   [**ClearData**](systemmonitor-cleardata.md)
-   [**DataPointCount**](systemmonitor-datapointcount.md)
-   [**EnableDigitGrouping**](systemmonitor-enabledigitgrouping.md)
-   [**EnableToolTips**](systemmonitor-enabletooltips.md)
-   [**GetLogViewRange**](systemmonitor-getlogviewrange.md)
-   [**LoadSettings**](systemmonitor-loadsettings.md)
-   [**LogSourceStartTime**](systemmonitor-logsourcestarttime.md)
-   [**LogSourceStopTime**](systemmonitor-logsourcestoptime.md)
-   [**重新記錄**](systemmonitor-relog.md)
-   [**SaveAs**](systemmonitor-saveas.md)
-   [**ScaleToFit**](systemmonitor-scaletofit.md)
-   [**SetLogViewRange**](systemmonitor-setlogviewrange.md)
-   [**ShowTimeAxisLables**](systemmonitor-showtimeaxislabels.md)

新增的列舉。

-   [**SysmonDataType**](/windows/win32/api/isysmon/ne-isysmon-sysmondatatype)
-   [**SysmonFileType**](/windows/win32/api/isysmon/ne-isysmon-sysmonfiletype)
-   新的顯示類型值已新增至 [ **DisplayTypeConstants**](/windows/win32/api/isysmon/ne-isysmon-displaytypeconstants)

 

 





