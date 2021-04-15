---
description: 使用 GraphEdit 模擬圖表建立
ms.assetid: 3f7d3079-3d3d-4b93-9ab7-4c03def7c4be
title: 使用 GraphEdit 模擬圖表建立
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f76878997c873c74d454979ccda689a9c241489d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467753"
---
# <a name="simulating-graph-building-with-graphedit"></a><span data-ttu-id="e393d-103">使用 GraphEdit 模擬圖表建立</span><span class="sxs-lookup"><span data-stu-id="e393d-103">Simulating Graph Building with GraphEdit</span></span>

<span data-ttu-id="e393d-104">DirectShow 提供一個稱為 GraphEdit 的偵錯工具，可讓您用來建立及測試篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="e393d-104">DirectShow provides a debugging utility called GraphEdit, which you can use to create and test filter graphs.</span></span>

<span data-ttu-id="e393d-105">GraphEdit 是用來建立篩選圖形的視覺化檢視。</span><span class="sxs-lookup"><span data-stu-id="e393d-105">GraphEdit is a visual tool for building filter graphs.</span></span> <span data-ttu-id="e393d-106">透過 GraphEdit，您可以在撰寫任何應用程式程式碼之前，先實驗篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="e393d-106">With GraphEdit, you can experiment with a filter graph before you write any application code.</span></span> <span data-ttu-id="e393d-107">您也可以載入應用程式所建立的篩選圖形，以確認您的應用程式正在建立正確的圖形。</span><span class="sxs-lookup"><span data-stu-id="e393d-107">You can also load a filter graph that your application creates, to verify that your application is building the correct graph.</span></span> <span data-ttu-id="e393d-108">如果您開發自訂篩選器，GraphEdit 會提供快速測試的方法：只要使用您的自訂篩選載入圖形，並嘗試執行圖形即可。</span><span class="sxs-lookup"><span data-stu-id="e393d-108">If you develop a custom filter, GraphEdit provides a quick way to test it: Simply load a graph with your custom filter and try running the graph.</span></span> <span data-ttu-id="e393d-109">如果您是新的 DirectShow，GraphEdit 是熟悉篩選圖形和 DirectShow 架構的好方法。</span><span class="sxs-lookup"><span data-stu-id="e393d-109">If you are new to DirectShow, GraphEdit is a good way to become familiar with filter graphs and the DirectShow architecture.</span></span>

<span data-ttu-id="e393d-110">下圖顯示 GraphEdit 如何代表簡單的篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="e393d-110">The following illustration shows how GraphEdit represents a simple filter graph.</span></span>

![graphedit 中的簡單篩選圖形](images/gedit09.png)

<span data-ttu-id="e393d-112">每個篩選都會以矩形表示。</span><span class="sxs-lookup"><span data-stu-id="e393d-112">Each filter is represented as a rectangle.</span></span> <span data-ttu-id="e393d-113">沿著篩選邊緣的較小平方表示圖釘。</span><span class="sxs-lookup"><span data-stu-id="e393d-113">Smaller squares along the edges of the filters represent pins.</span></span> <span data-ttu-id="e393d-114">輸入圖釘位於篩選器的左側，輸出則是在右邊。</span><span class="sxs-lookup"><span data-stu-id="e393d-114">Input pins are on the left side of the filter, and output pins are on the right side.</span></span> <span data-ttu-id="e393d-115">箭號代表圖釘之間的連接。</span><span class="sxs-lookup"><span data-stu-id="e393d-115">The arrows represent the connections between pins.</span></span>

<span data-ttu-id="e393d-116">透過 GraphEdit，您可以：</span><span class="sxs-lookup"><span data-stu-id="e393d-116">With GraphEdit, you can:</span></span>

-   <span data-ttu-id="e393d-117">使用視覺效果拖放介面建立和修改篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="e393d-117">Create and modify filter graphs using a visual, drag-and-drop interface.</span></span>
-   <span data-ttu-id="e393d-118">模擬以程式設計方式呼叫來建立圖形。</span><span class="sxs-lookup"><span data-stu-id="e393d-118">Simulate programmatic calls to build a graph.</span></span>
-   <span data-ttu-id="e393d-119">執行、暫停、停止和搜尋圖形。</span><span class="sxs-lookup"><span data-stu-id="e393d-119">Run, pause, stop, and seek a graph.</span></span>
-   <span data-ttu-id="e393d-120">查看電腦上已註冊的篩選器，並查看每個篩選器的登錄資訊。</span><span class="sxs-lookup"><span data-stu-id="e393d-120">See what filters are registered on your computer, and view registry information for each filter.</span></span>
-   <span data-ttu-id="e393d-121">視圖篩選屬性頁。</span><span class="sxs-lookup"><span data-stu-id="e393d-121">View filter property pages.</span></span>
-   <span data-ttu-id="e393d-122">查看 pin 連接的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="e393d-122">View the media types of pin connections.</span></span>

<span data-ttu-id="e393d-123">本節包含下列主題：</span><span class="sxs-lookup"><span data-stu-id="e393d-123">This section contains the following topics:</span></span>

-   [<span data-ttu-id="e393d-124">使用 GraphEdit</span><span class="sxs-lookup"><span data-stu-id="e393d-124">Using GraphEdit</span></span>](using-graphedit.md)
-   [<span data-ttu-id="e393d-125">從外部進程載入圖形</span><span class="sxs-lookup"><span data-stu-id="e393d-125">Loading a Graph From an External Process</span></span>](loading-a-graph-from-an-external-process.md)
-   [<span data-ttu-id="e393d-126">將篩選圖形儲存至 GraphEdit 檔案</span><span class="sxs-lookup"><span data-stu-id="e393d-126">Saving a Filter Graph to a GraphEdit File</span></span>](saving-a-filter-graph-to-a-graphedit-file.md)
-   [<span data-ttu-id="e393d-127">以程式設計方式載入 GraphEdit 檔案</span><span class="sxs-lookup"><span data-stu-id="e393d-127">Loading a GraphEdit File Programmatically</span></span>](loading-a-graphedit-file-programmatically.md)
-   [<span data-ttu-id="e393d-128">GraphEdit 檔案格式</span><span class="sxs-lookup"><span data-stu-id="e393d-128">GraphEdit File Format</span></span>](graphedit-file-format.md)

## <a name="related-topics"></a><span data-ttu-id="e393d-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="e393d-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e393d-130">使用 DirectShow</span><span class="sxs-lookup"><span data-stu-id="e393d-130">Using DirectShow</span></span>](using-directshow.md)
</dt> </dl>

 

 



