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
# <a name="whats-new-in-system-monitor"></a><span data-ttu-id="41a8c-103">系統監視器中的新功能</span><span class="sxs-lookup"><span data-stu-id="41a8c-103">What's New in System Monitor</span></span>

<span data-ttu-id="41a8c-104">下表指出每個版本的系統監視器 (SYSMON) 的新功能。</span><span class="sxs-lookup"><span data-stu-id="41a8c-104">The following table identifies what is new for each release of System Monitor (SYSMON).</span></span>



| <span data-ttu-id="41a8c-105">版本</span><span class="sxs-lookup"><span data-stu-id="41a8c-105">Version</span></span>     | <span data-ttu-id="41a8c-106">功能描述</span><span class="sxs-lookup"><span data-stu-id="41a8c-106">Description of features</span></span>                                                                                                                                                                                                                                                                                                                              |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41a8c-107">版本3。7</span><span class="sxs-lookup"><span data-stu-id="41a8c-107">Version 3.7</span></span> | <span data-ttu-id="41a8c-108">此版本會新增新的圖表類型、可選取多個計數器、從圖形上的某個點抓取計數器值、將圖表計數器值儲存至記錄檔，以及讓折線圖持續在圖形視窗中移動，而不是在其本身換行的選項。包含在 Windows Server 2008 和 Windows Vista 中。</span><span class="sxs-lookup"><span data-stu-id="41a8c-108">This version adds new graph types, the ability to select multiple counters, retrieve counter values from a point on the graph, save graphed counter values to a log file, and the option to have a line graph continuously scroll in the graph window instead of wrap-around on itself.Included in Windows Server 2008 and Windows Vista.</span></span><br/> |



 

## <a name="version-37"></a><span data-ttu-id="41a8c-109">版本3。7</span><span class="sxs-lookup"><span data-stu-id="41a8c-109">Version 3.7</span></span>

<span data-ttu-id="41a8c-110">新增至 [**CounterItem**](counteritem.md)的新屬性和方法。</span><span class="sxs-lookup"><span data-stu-id="41a8c-110">New properties and methods that were added to [**CounterItem**](counteritem.md).</span></span>

-   [<span data-ttu-id="41a8c-111">**GetDataAt**</span><span class="sxs-lookup"><span data-stu-id="41a8c-111">**GetDataAt**</span></span>](counteritem-getdataat.md)
-   [<span data-ttu-id="41a8c-112">**已選取**</span><span class="sxs-lookup"><span data-stu-id="41a8c-112">**Selected**</span></span>](counteritem-selected.md)
-   [<span data-ttu-id="41a8c-113">**可見**</span><span class="sxs-lookup"><span data-stu-id="41a8c-113">**Visible**</span></span>](counteritem-visible.md)
-   <span data-ttu-id="41a8c-114">CounterItem 的有效值範圍已變更 [ **。寬度**](counteritem-width.md)</span><span class="sxs-lookup"><span data-stu-id="41a8c-114">Range of valid values changed for [**CounterItem.Width**](counteritem-width.md)</span></span>

<span data-ttu-id="41a8c-115">新增至 [**SystemMonitor**](systemmonitor.md)的新屬性和方法。</span><span class="sxs-lookup"><span data-stu-id="41a8c-115">New properties and methods that were added to [**SystemMonitor**](systemmonitor.md).</span></span>

-   [<span data-ttu-id="41a8c-116">**BatchingLock**</span><span class="sxs-lookup"><span data-stu-id="41a8c-116">**BatchingLock**</span></span>](systemmonitor-batchinglock.md)
-   [<span data-ttu-id="41a8c-117">**ChartScroll**</span><span class="sxs-lookup"><span data-stu-id="41a8c-117">**ChartScroll**</span></span>](systemmonitor-chartscroll.md)
-   [<span data-ttu-id="41a8c-118">**ClearData**</span><span class="sxs-lookup"><span data-stu-id="41a8c-118">**ClearData**</span></span>](systemmonitor-cleardata.md)
-   [<span data-ttu-id="41a8c-119">**DataPointCount**</span><span class="sxs-lookup"><span data-stu-id="41a8c-119">**DataPointCount**</span></span>](systemmonitor-datapointcount.md)
-   [<span data-ttu-id="41a8c-120">**EnableDigitGrouping**</span><span class="sxs-lookup"><span data-stu-id="41a8c-120">**EnableDigitGrouping**</span></span>](systemmonitor-enabledigitgrouping.md)
-   [<span data-ttu-id="41a8c-121">**EnableToolTips**</span><span class="sxs-lookup"><span data-stu-id="41a8c-121">**EnableToolTips**</span></span>](systemmonitor-enabletooltips.md)
-   [<span data-ttu-id="41a8c-122">**GetLogViewRange**</span><span class="sxs-lookup"><span data-stu-id="41a8c-122">**GetLogViewRange**</span></span>](systemmonitor-getlogviewrange.md)
-   [<span data-ttu-id="41a8c-123">**LoadSettings**</span><span class="sxs-lookup"><span data-stu-id="41a8c-123">**LoadSettings**</span></span>](systemmonitor-loadsettings.md)
-   [<span data-ttu-id="41a8c-124">**LogSourceStartTime**</span><span class="sxs-lookup"><span data-stu-id="41a8c-124">**LogSourceStartTime**</span></span>](systemmonitor-logsourcestarttime.md)
-   [<span data-ttu-id="41a8c-125">**LogSourceStopTime**</span><span class="sxs-lookup"><span data-stu-id="41a8c-125">**LogSourceStopTime**</span></span>](systemmonitor-logsourcestoptime.md)
-   [<span data-ttu-id="41a8c-126">**重新記錄**</span><span class="sxs-lookup"><span data-stu-id="41a8c-126">**Relog**</span></span>](systemmonitor-relog.md)
-   [<span data-ttu-id="41a8c-127">**SaveAs**</span><span class="sxs-lookup"><span data-stu-id="41a8c-127">**SaveAs**</span></span>](systemmonitor-saveas.md)
-   [<span data-ttu-id="41a8c-128">**ScaleToFit**</span><span class="sxs-lookup"><span data-stu-id="41a8c-128">**ScaleToFit**</span></span>](systemmonitor-scaletofit.md)
-   [<span data-ttu-id="41a8c-129">**SetLogViewRange**</span><span class="sxs-lookup"><span data-stu-id="41a8c-129">**SetLogViewRange**</span></span>](systemmonitor-setlogviewrange.md)
-   [<span data-ttu-id="41a8c-130">**ShowTimeAxisLables**</span><span class="sxs-lookup"><span data-stu-id="41a8c-130">**ShowTimeAxisLables**</span></span>](systemmonitor-showtimeaxislabels.md)

<span data-ttu-id="41a8c-131">新增的列舉。</span><span class="sxs-lookup"><span data-stu-id="41a8c-131">New enumerations that were added.</span></span>

-   [<span data-ttu-id="41a8c-132">**SysmonDataType**</span><span class="sxs-lookup"><span data-stu-id="41a8c-132">**SysmonDataType**</span></span>](/windows/win32/api/isysmon/ne-isysmon-sysmondatatype)
-   [<span data-ttu-id="41a8c-133">**SysmonFileType**</span><span class="sxs-lookup"><span data-stu-id="41a8c-133">**SysmonFileType**</span></span>](/windows/win32/api/isysmon/ne-isysmon-sysmonfiletype)
-   <span data-ttu-id="41a8c-134">新的顯示類型值已新增至 [ **DisplayTypeConstants**](/windows/win32/api/isysmon/ne-isysmon-displaytypeconstants)</span><span class="sxs-lookup"><span data-stu-id="41a8c-134">New display type values were added to [**DisplayTypeConstants**](/windows/win32/api/isysmon/ne-isysmon-displaytypeconstants)</span></span>

 

 





