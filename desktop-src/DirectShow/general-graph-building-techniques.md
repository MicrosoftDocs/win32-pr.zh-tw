---
description: 一般 Graph-Building 技術
ms.assetid: 66d93305-175c-4549-b825-2f3d7fd6bf09
title: 一般 Graph-Building 技術
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73c73a005f1fbf7af0a53f11d44d600852f88752
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104187394"
---
# <a name="general-graph-building-techniques"></a><span data-ttu-id="9dccb-103">一般 Graph-Building 技術</span><span class="sxs-lookup"><span data-stu-id="9dccb-103">General Graph-Building Techniques</span></span>

<span data-ttu-id="9dccb-104">每個 DirectShow 應用程式一開始都會建立篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="9dccb-104">Every DirectShow application starts by building a filter graph.</span></span> <span data-ttu-id="9dccb-105">當您閱讀 DirectShow 檔中的「總覽」主題時，您會發現最重要的是，它會說明所需的篩選圖形種類。</span><span class="sxs-lookup"><span data-stu-id="9dccb-105">As you read the overview topics in the DirectShow documentation, you will find that most start by describing what kind of filter graph you need.</span></span> <span data-ttu-id="9dccb-106">在某些情況下，有一種方法或協助程式物件專門設計來建立該類型的圖形。</span><span class="sxs-lookup"><span data-stu-id="9dccb-106">In some cases, there is a method or a helper object specifically designed for building that type of graph.</span></span> <span data-ttu-id="9dccb-107">例如， [Dvd 圖形](dvd-graph-builder.md) 產生器物件會建立 dvd 播放圖形。</span><span class="sxs-lookup"><span data-stu-id="9dccb-107">For example, the [DVD Graph Builder](dvd-graph-builder.md) object builds DVD playback graphs.</span></span> <span data-ttu-id="9dccb-108">在其他情況下，應用程式必須藉由新增篩選並加以連接來建立圖形。</span><span class="sxs-lookup"><span data-stu-id="9dccb-108">In other cases, the application must construct the graph by adding filters and connecting them.</span></span>

<span data-ttu-id="9dccb-109">本節提供一些協助程式函式，這些函式會執行基本的圖形組建作業。</span><span class="sxs-lookup"><span data-stu-id="9dccb-109">This section presents some helper functions that implement basic graph-building operations.</span></span> <span data-ttu-id="9dccb-110">任何需要建立或修改篩選圖形的 DirectShow 應用程式都可以使用這些應用程式。</span><span class="sxs-lookup"><span data-stu-id="9dccb-110">They can be used by any DirectShow application that needs to build or modify a filter graph.</span></span> <span data-ttu-id="9dccb-111">本節包含下列主題：</span><span class="sxs-lookup"><span data-stu-id="9dccb-111">This section contains the following topics:</span></span>

-   [<span data-ttu-id="9dccb-112">依 CLSID 新增篩選</span><span class="sxs-lookup"><span data-stu-id="9dccb-112">Add a Filter by CLSID</span></span>](add-a-filter-by-clsid.md)
-   [<span data-ttu-id="9dccb-113">在篩選器上尋找未連接的 Pin</span><span class="sxs-lookup"><span data-stu-id="9dccb-113">Find an Unconnected Pin on a Filter</span></span>](find-an-unconnected-pin-on-a-filter.md)
-   [<span data-ttu-id="9dccb-114">連接兩個篩選器</span><span class="sxs-lookup"><span data-stu-id="9dccb-114">Connect Two Filters</span></span>](connect-two-filters.md)
-   [<span data-ttu-id="9dccb-115">尋找篩選或釘選上的介面</span><span class="sxs-lookup"><span data-stu-id="9dccb-115">Find an Interface on a Filter or Pin</span></span>](find-an-interface-on-a-filter-or-pin.md)
-   [<span data-ttu-id="9dccb-116">尋找篩選準則的對等</span><span class="sxs-lookup"><span data-stu-id="9dccb-116">Find a Filter's Peer</span></span>](find-a-filters-peer.md)
-   [<span data-ttu-id="9dccb-117">移除圖形中的所有篩選</span><span class="sxs-lookup"><span data-stu-id="9dccb-117">Remove All the Filters in the Graph</span></span>](remove-all-the-filters-in-the-graph.md)
-   [<span data-ttu-id="9dccb-118">使用 Capture Graph Builder 建立圖形</span><span class="sxs-lookup"><span data-stu-id="9dccb-118">Building Graphs with the Capture Graph Builder</span></span>](building-graphs-with-the-capture-graph-builder.md)

## <a name="related-topics"></a><span data-ttu-id="9dccb-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="9dccb-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9dccb-120">基本的 DirectShow 工作</span><span class="sxs-lookup"><span data-stu-id="9dccb-120">Basic DirectShow Tasks</span></span>](basic-directshow-tasks.md)
</dt> <dt>

[<span data-ttu-id="9dccb-121">列舉裝置和篩選器</span><span class="sxs-lookup"><span data-stu-id="9dccb-121">Enumerating Devices and Filters</span></span>](enumerating-devices-and-filters.md)
</dt> <dt>

[<span data-ttu-id="9dccb-122">列舉篩選圖形中的物件</span><span class="sxs-lookup"><span data-stu-id="9dccb-122">Enumerating Objects in a Filter Graph</span></span>](enumerating-objects-in-a-filter-graph.md)
</dt> <dt>

[<span data-ttu-id="9dccb-123">智慧型連接</span><span class="sxs-lookup"><span data-stu-id="9dccb-123">Intelligent Connect</span></span>](intelligent-connect.md)
</dt> </dl>

 

 



