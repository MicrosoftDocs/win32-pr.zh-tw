---
description: 列舉篩選圖形中的物件
ms.assetid: 04a3dbc8-33c4-4b70-930e-686be2f8301f
title: 列舉篩選圖形中的物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2369cd3400d3b7fc9944662ed6d32fd67234af90
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109105"
---
# <a name="enumerating-objects-in-a-filter-graph"></a><span data-ttu-id="3d26e-103">列舉篩選圖形中的物件</span><span class="sxs-lookup"><span data-stu-id="3d26e-103">Enumerating Objects in a Filter Graph</span></span>

<span data-ttu-id="3d26e-104">應用程式可能需要在篩選圖形中找出特定的篩選，甚至在篩選器上找出特定的釘選。</span><span class="sxs-lookup"><span data-stu-id="3d26e-104">An application might need to locate a particular filter in the filter graph, or even a particular pin on a filter.</span></span> <span data-ttu-id="3d26e-105">例如，它可能會使用特定篩選器所公開的介面。</span><span class="sxs-lookup"><span data-stu-id="3d26e-105">For example, it might use an interface that a particular filter exposes.</span></span> <span data-ttu-id="3d26e-106">或者，它可能會建立特製化的篩選圖形，而且需要在個別的 pin 上呼叫方法來連接篩選。</span><span class="sxs-lookup"><span data-stu-id="3d26e-106">Or, it might construct a specialized filter graph and need to call methods on individual pins to connect the filters.</span></span> <span data-ttu-id="3d26e-107">基於這個目的，DirectShow 提供數種方法來列舉篩選圖形中的物件。</span><span class="sxs-lookup"><span data-stu-id="3d26e-107">For this purpose, DirectShow provides several methods for enumerating objects in a filter graph.</span></span>

<span data-ttu-id="3d26e-108">本節中所討論的列舉值會遵循 COM 列舉介面所使用的標準格式。</span><span class="sxs-lookup"><span data-stu-id="3d26e-108">The enumerators discussed in this section follow the standard form used by COM enumeration interfaces.</span></span> <span data-ttu-id="3d26e-109">如需詳細資訊，請參閱 Platform SDK 中的「IEnumXXXX」主題。</span><span class="sxs-lookup"><span data-stu-id="3d26e-109">For more information, see the "IEnumXXXX" topic in the Platform SDK.</span></span> <span data-ttu-id="3d26e-110">如需列舉使用者電腦上已註冊但尚未在篩選圖形中之篩選準則的相關資訊，請參閱 [列舉裝置和篩選器](enumerating-devices-and-filters.md)。</span><span class="sxs-lookup"><span data-stu-id="3d26e-110">For information on enumerating filters that are registered on the user's computer, but aren't yet in the filter graph, see [Enumerating Devices and Filters](enumerating-devices-and-filters.md).</span></span>

<span data-ttu-id="3d26e-111">本文包含下列主題：</span><span class="sxs-lookup"><span data-stu-id="3d26e-111">This article contains the following topics:</span></span>

-   [<span data-ttu-id="3d26e-112">列舉篩選</span><span class="sxs-lookup"><span data-stu-id="3d26e-112">Enumerating Filters</span></span>](enumerating-filters.md)
-   [<span data-ttu-id="3d26e-113">列舉釘選</span><span class="sxs-lookup"><span data-stu-id="3d26e-113">Enumerating Pins</span></span>](enumerating-pins.md)
-   [<span data-ttu-id="3d26e-114">列舉媒體類型</span><span class="sxs-lookup"><span data-stu-id="3d26e-114">Enumerating Media Types</span></span>](enumerating-media-types.md)

## <a name="related-topics"></a><span data-ttu-id="3d26e-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="3d26e-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3d26e-116">基本的 DirectShow 工作</span><span class="sxs-lookup"><span data-stu-id="3d26e-116">Basic DirectShow Tasks</span></span>](basic-directshow-tasks.md)
</dt> </dl>

 

 



