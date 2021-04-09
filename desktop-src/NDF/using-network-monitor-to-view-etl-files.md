---
title: 使用網路監視器來查看 ETL 檔案
description: 網路監視器3.3 可讓使用者使用 Windows Vista 或更新版本) 來剖析、篩選和查看 ETL 檔案 (。
ms.assetid: 932be193-70f9-48f9-95d8-18916d3b7064
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04120f860654f4859aa930f32a4711999682eaf8
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/03/2021
ms.locfileid: "103945537"
---
# <a name="using-network-monitor-to-view-etl-files"></a><span data-ttu-id="1f7e0-103">使用網路監視器來查看 ETL 檔案</span><span class="sxs-lookup"><span data-stu-id="1f7e0-103">Using Network Monitor to View ETL Files</span></span>

<span data-ttu-id="1f7e0-104">[網路監視器 3.3](https://connect.microsoft.com/site/sitehome.aspx?SiteID=216) 可讓使用者使用 Windows Vista 或更新版本) 來剖析、篩選和查看 ETL 檔案 (。</span><span class="sxs-lookup"><span data-stu-id="1f7e0-104">[Network Monitor 3.3](https://connect.microsoft.com/site/sitehome.aspx?SiteID=216) enables users to parse, filter, and view an ETL file (using Windows Vista or later).</span></span> <span data-ttu-id="1f7e0-105"> (如果使用網路監視器3.2，您將需要從 [CodePlex](https://www.codeplex.com/NMParsers) 下載並安裝其他剖析器，才能轉譯網路追蹤事件。 ) </span><span class="sxs-lookup"><span data-stu-id="1f7e0-105">(If using Network Monitor 3.2, you will need to download and install additional parsers from [CodePlex](https://www.codeplex.com/NMParsers) in order to render the network tracing events.)</span></span>

<span data-ttu-id="1f7e0-106">相互關聯的 ETL 檔案會將相關的事件群組在一起。</span><span class="sxs-lookup"><span data-stu-id="1f7e0-106">Correlated ETL files group the relevant events together.</span></span> <span data-ttu-id="1f7e0-107">下列圖例顯示在網路監視器中開啟的相互關聯檔案，並啟用交談。</span><span class="sxs-lookup"><span data-stu-id="1f7e0-107">The illlustration below shows a correlated file opened in Network Monitor, with conversation enabled.</span></span>

![顯示網路監視器的螢幕擷取畫面，其中已醒目提示左側視窗中的相互關聯事件，並從下拉式清單中反白顯示 UTEvent。](images/ut-netmon1.png)

<span data-ttu-id="1f7e0-109">相互關聯事件會依左窗格中的活動分組。</span><span class="sxs-lookup"><span data-stu-id="1f7e0-109">Correlated events are grouped by activity in the left pane.</span></span> <span data-ttu-id="1f7e0-110">您可以在 [框架摘要] 窗格中選取事件，然後以滑鼠右鍵按一下以選取網路事件層級的交談。</span><span class="sxs-lookup"><span data-stu-id="1f7e0-110">You can select an event in the Frame Summary pane, then right-click to select the conversation at the network event level.</span></span> <span data-ttu-id="1f7e0-111">這將會在左窗格中顯示相關的活動。</span><span class="sxs-lookup"><span data-stu-id="1f7e0-111">This will display a related activity in the left pane.</span></span>

<span data-ttu-id="1f7e0-112">從左窗格中選取特定活動並展開，將會顯示相互關聯事件的提供者清單。</span><span class="sxs-lookup"><span data-stu-id="1f7e0-112">Selecting a particular activity from the left pane and expanding it will show the list of providers for the correlated events.</span></span>

![顯示網路監視器的螢幕擷取畫面，其中包含從左窗格選取的活動，以及右窗格中對應至該事件的事件。](images/ut-netmon2.png)

<span data-ttu-id="1f7e0-114">當您在左窗格中選取特定提供者時，將會在 [框架摘要] 窗格中顯示該提供者和活動特定的事件清單。</span><span class="sxs-lookup"><span data-stu-id="1f7e0-114">When you select a specific provider in the left pane, a list of events specific to that provider and activity will be displayed in the Frame Summary pane.</span></span>

![顯示在左窗格中選取之特定提供者的螢幕擷取畫面，以及右上方窗格中反白顯示的提供者特定事件清單。](images/ut-netmon3.png)

<span data-ttu-id="1f7e0-116">篩選準則可以在網路監視器中套用，讓您更輕鬆地查看並尋找正確的事件或封包。</span><span class="sxs-lookup"><span data-stu-id="1f7e0-116">Filters can be applied in Network Monitor to make it easier to view and find the right events or packet.</span></span> <span data-ttu-id="1f7e0-117">例如，您可以將篩選套用至選取的錯誤事件 (例如， **UTEvent。 Level = = 2**) 以特定色彩顯示。</span><span class="sxs-lookup"><span data-stu-id="1f7e0-117">For example, you can apply a filter to selected error events (for example, **UTEvent.Header.Descriptor.Level == 2**) to display them in a certain color.</span></span>

![顯示 [編輯色彩篩選器] 對話方塊的螢幕擷取畫面。](images/ut-netmon4.png)

<span data-ttu-id="1f7e0-119">您也可以套用篩選，以不同的色彩標示不同的提供者，以便更輕鬆地查看結果。</span><span class="sxs-lookup"><span data-stu-id="1f7e0-119">Filters can also be applied to mark different providers in different colors so that the results are easier to view.</span></span>

![顯示以不同色彩標示的不同提供者範例的螢幕擷取畫面。](images/ut-netmon5.png)

<span data-ttu-id="1f7e0-121">若要套用篩選，請按一下 [**篩選**] 功能表上的 [ **ColorFilters** ]。</span><span class="sxs-lookup"><span data-stu-id="1f7e0-121">To apply a filter, click **ColorFilters** on the **Filters** menu.</span></span>

<span data-ttu-id="1f7e0-122">下表顯示實用篩選準則的一些範例。</span><span class="sxs-lookup"><span data-stu-id="1f7e0-122">The following table shows some examples of useful filters.</span></span>



| <span data-ttu-id="1f7e0-123">篩選</span><span class="sxs-lookup"><span data-stu-id="1f7e0-123">Filter</span></span>                                                                        | <span data-ttu-id="1f7e0-124">Description</span><span class="sxs-lookup"><span data-stu-id="1f7e0-124">Description</span></span>                                                       |
|-------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="1f7e0-125">UTEvent。 Level = = 2</span><span class="sxs-lookup"><span data-stu-id="1f7e0-125">UTEvent.Header.Descriptor.Level == 2</span></span>                                          | <span data-ttu-id="1f7e0-126">只篩選錯誤事件。</span><span class="sxs-lookup"><span data-stu-id="1f7e0-126">Filters only error events.</span></span>                                        |
| <span data-ttu-id="1f7e0-127">UTEvent。 Level = = 3</span><span class="sxs-lookup"><span data-stu-id="1f7e0-127">UTEvent.Header.Descriptor.Level == 3</span></span>                                          | <span data-ttu-id="1f7e0-128">只篩選警告事件。</span><span class="sxs-lookup"><span data-stu-id="1f7e0-128">Filters only warning events.</span></span>                                      |
| <span data-ttu-id="1f7e0-129">UTEvent.Header.Descriptor.Id = = 2001</span><span class="sxs-lookup"><span data-stu-id="1f7e0-129">UTEvent.Header.Descriptor.Id == 2001</span></span>                                          | <span data-ttu-id="1f7e0-130">只篩選事件識別碼為2001的事件。</span><span class="sxs-lookup"><span data-stu-id="1f7e0-130">Filters only events with event ID 2001.</span></span>                           |
| <span data-ttu-id="1f7e0-131">WLAN \_ MicrosoftWindowsWLANAutoConfig</span><span class="sxs-lookup"><span data-stu-id="1f7e0-131">WLAN\_MicrosoftWindowsWLANAutoConfig</span></span>                                          | <span data-ttu-id="1f7e0-132">只篩選來自 WLAN 服務的事件。</span><span class="sxs-lookup"><span data-stu-id="1f7e0-132">Filters only events from WLAN service.</span></span>                            |
| <span data-ttu-id="1f7e0-133">N802 \_ MicrosoftWindowsNWiFi</span><span class="sxs-lookup"><span data-stu-id="1f7e0-133">N802\_MicrosoftWindowsNWiFi</span></span>                                                   | <span data-ttu-id="1f7e0-134">只篩選來自原生 Wifi 驅動程式的事件。</span><span class="sxs-lookup"><span data-stu-id="1f7e0-134">Filters only events from the Native Wifi driver.</span></span>                  |
| <span data-ttu-id="1f7e0-135">WLAN \_ MICROSOFTWINDOWSWLANAUTOCONFIG 和 UTEvent.Header.Descriptor.Id = = 2001</span><span class="sxs-lookup"><span data-stu-id="1f7e0-135">WLAN\_MicrosoftWindowsWLANAutoConfig AND UTEvent.Header.Descriptor.Id == 2001</span></span> | <span data-ttu-id="1f7e0-136">僅篩選從 WLAN 服務發出的事件識別碼為2001的事件。</span><span class="sxs-lookup"><span data-stu-id="1f7e0-136">Filters only events with event ID 2001 emitted from WLAN service.</span></span> |



 

 

 




