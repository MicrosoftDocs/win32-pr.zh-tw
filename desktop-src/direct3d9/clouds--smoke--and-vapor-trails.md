---
description: 雲端、冒煙和蒸氣軌跡都可以透過 billboarding 技術的延伸模組來建立。
ms.assetid: c5607327-de46-4241-a01a-4adfe0bbf6fb
title: " (Direct3D 9) 的雲端、冒煙和蒸氣軌跡"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f60bce89e23b2b2aab7affbb6947cab4d11c33ed
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104555726"
---
# <a name="clouds-smoke-and-vapor-trails-direct3d-9"></a><span data-ttu-id="10467-103"> (Direct3D 9) 的雲端、冒煙和蒸氣軌跡</span><span class="sxs-lookup"><span data-stu-id="10467-103">Clouds, Smoke, and Vapor Trails (Direct3D 9)</span></span>

<span data-ttu-id="10467-104">雲端、冒煙和蒸氣軌跡都可以透過 billboarding 技術的延伸模組來建立。</span><span class="sxs-lookup"><span data-stu-id="10467-104">Clouds, smoke, and vapor trails can all be created by an extension of the billboarding technique.</span></span> <span data-ttu-id="10467-105">請參閱 [Billboarding (Direct3D 9) ](billboarding.md)。</span><span class="sxs-lookup"><span data-stu-id="10467-105">See [Billboarding (Direct3D 9)](billboarding.md).</span></span> <span data-ttu-id="10467-106">藉由在兩個軸（而不是一個）上旋轉佈告欄，您的應用程式可以讓使用者從任何角度觀看佈告欄。</span><span class="sxs-lookup"><span data-stu-id="10467-106">By rotating the billboard on two axes instead of one, your application can enable the user to view a billboard from any angle.</span></span> <span data-ttu-id="10467-107">一般而言，應用程式會在水準和垂直軸上旋轉佈告欄。</span><span class="sxs-lookup"><span data-stu-id="10467-107">Typically, an application rotates the billboard on the horizontal and vertical axes.</span></span>

<span data-ttu-id="10467-108">若要建立簡單的雲端，您的應用程式可以在一或兩個軸上旋轉矩形基本型別，讓基本物件面對使用者。</span><span class="sxs-lookup"><span data-stu-id="10467-108">To make a simple cloud, your application can rotate a rectangular primitive on one or two axes so that the primitive faces the user.</span></span> <span data-ttu-id="10467-109">然後可以將類似雲端的材質套用至具有透明度的基本物件。</span><span class="sxs-lookup"><span data-stu-id="10467-109">A cloud-like texture can then be applied to the primitive with transparency.</span></span> <span data-ttu-id="10467-110">如需將透明材質套用至基本專案的詳細資訊，請參閱 [ (Direct3D 9) 的材質混色 ](texture-blending.md)。</span><span class="sxs-lookup"><span data-stu-id="10467-110">For details on applying transparent textures to primitives, see [Texture Blending (Direct3D 9)](texture-blending.md).</span></span> <span data-ttu-id="10467-111">您可以在一段時間內套用一連串的紋理，以建立雲端的動畫。</span><span class="sxs-lookup"><span data-stu-id="10467-111">You can animate the cloud by applying a series of textures over time.</span></span>

<span data-ttu-id="10467-112">應用程式可以建立更複雜的雲端，方法是從一組基本專案形成它們。</span><span class="sxs-lookup"><span data-stu-id="10467-112">An application can create more complex clouds by forming them from a group of primitives.</span></span> <span data-ttu-id="10467-113">雲端的每個部分都是矩形的基本元件。</span><span class="sxs-lookup"><span data-stu-id="10467-113">Each part of the cloud is a rectangular primitive.</span></span> <span data-ttu-id="10467-114">您可以在一段時間內獨立移動基本專案，以提供動態薄霧的外觀。</span><span class="sxs-lookup"><span data-stu-id="10467-114">The primitives can be moved independently over time to give the appearance of a dynamic mist.</span></span> <span data-ttu-id="10467-115">下圖顯示這個概念。</span><span class="sxs-lookup"><span data-stu-id="10467-115">The following illustration shows this concept.</span></span>

![形成更複雜雲端之基本專案的圖例](images/cloud.png)

<span data-ttu-id="10467-117">冒煙的外觀會以類似于雲端的方式來顯示。</span><span class="sxs-lookup"><span data-stu-id="10467-117">The appearance of smoke is displayed in a manner similar to clouds.</span></span> <span data-ttu-id="10467-118">它通常需要多個公告欄，例如複雜的雲端。</span><span class="sxs-lookup"><span data-stu-id="10467-118">It typically requires multiple billboards, like complex clouds.</span></span> <span data-ttu-id="10467-119">冒煙通常會隨著時間而 billows 並上升，因此構成冒煙 plume 的公告欄需要據以移動。</span><span class="sxs-lookup"><span data-stu-id="10467-119">Smoke usually billows and rises over time, so the billboards that make up the smoke plume need to move accordingly.</span></span> <span data-ttu-id="10467-120">當 plume 上升和 disperses 時，您可能需要新增更多公告欄。</span><span class="sxs-lookup"><span data-stu-id="10467-120">You may need to add more billboards as the plume rises and disperses.</span></span>

<span data-ttu-id="10467-121">蒸氣記錄是一種不會增加的冒煙 plume。</span><span class="sxs-lookup"><span data-stu-id="10467-121">A vapor trail is a smoke plume that doesn't rise.</span></span> <span data-ttu-id="10467-122">不過，就像冒煙 plume，它會在一段時間內 disperses。</span><span class="sxs-lookup"><span data-stu-id="10467-122">However, like a smoke plume, it disperses over time.</span></span> <span data-ttu-id="10467-123">下圖顯示使用公告欄來模擬蒸氣記錄的技巧。</span><span class="sxs-lookup"><span data-stu-id="10467-123">The following illustration shows the technique of using billboards to simulate a vapor trail.</span></span>

![模擬蒸氣記錄的公告欄圖例](images/vapor.png)

## <a name="related-topics"></a><span data-ttu-id="10467-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="10467-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="10467-126">Alpha 範例</span><span class="sxs-lookup"><span data-stu-id="10467-126">Alpha Examples</span></span>](alpha-examples.md)
</dt> </dl>

 

 



