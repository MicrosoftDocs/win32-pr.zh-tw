---
description: 轉換方向
ms.assetid: d18525de-bb75-4c5e-b387-cfec7ba03df7
title: 轉換方向
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01d43ec4258d2f23c8b8961e3e1b8fd3d554b057
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104562436"
---
# <a name="transition-direction"></a><span data-ttu-id="44fb4-103">轉換方向</span><span class="sxs-lookup"><span data-stu-id="44fb4-103">Transition Direction</span></span>

<span data-ttu-id="44fb4-104">\[此 API 不受支援，而且可能會在未來變更或無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="44fb4-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="44fb4-105">轉換會從輸入 A 移至輸入 B，並從時間 t ₀至 t ₁。</span><span class="sxs-lookup"><span data-stu-id="44fb4-105">A transition goes from input A to input B, and from time t₀ to t₁.</span></span> <span data-ttu-id="44fb4-106">因此，轉換的 *方向* 可能表示下列其中一種情況：</span><span class="sxs-lookup"><span data-stu-id="44fb4-106">Therefore, the *direction* of a transition can mean one of two things:</span></span>

-   <span data-ttu-id="44fb4-107">時間軸圖層與輸入的對應。</span><span class="sxs-lookup"><span data-stu-id="44fb4-107">The mapping of timeline layers to inputs.</span></span>
-   <span data-ttu-id="44fb4-108">經過一段時間的進展。</span><span class="sxs-lookup"><span data-stu-id="44fb4-108">The progression over time.</span></span>

<span data-ttu-id="44fb4-109">第一個是 *輸入方向*，而第二個則是 *進度方向*。</span><span class="sxs-lookup"><span data-stu-id="44fb4-109">The first is the *input direction*, and the second is the *progress direction*.</span></span> <span data-ttu-id="44fb4-110">您可以控制兩個方向。</span><span class="sxs-lookup"><span data-stu-id="44fb4-110">You can control both directions.</span></span>

-   <span data-ttu-id="44fb4-111">輸入方向：根據預設，轉換會從較低優先順序層級的複合層移至包含轉換的圖層。</span><span class="sxs-lookup"><span data-stu-id="44fb4-111">Input direction: By default, a transition goes from the composite of the lower-priority layers to the layer that contains the transition.</span></span> <span data-ttu-id="44fb4-112">若要反轉此方向，請呼叫 [**IAMTimelineTrans：： SetSwapInputs**](iamtimelinetrans-setswapinputs.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="44fb4-112">To reverse this direction, call the [**IAMTimelineTrans::SetSwapInputs**](iamtimelinetrans-setswapinputs.md) method.</span></span>
-   <span data-ttu-id="44fb4-113">進度方向：大部分的轉換都支援標準 **進度** 屬性，以指定在指定的時間內，輸出中會反映的轉換百分比。</span><span class="sxs-lookup"><span data-stu-id="44fb4-113">Progress direction: Most transitions support a standard **Progress** property, which specifies what percentage of the transition is reflected in the output at a given moment.</span></span> <span data-ttu-id="44fb4-114">根據預設，在轉換期間， **進度** 屬性的值會從0.0 到1.0。</span><span class="sxs-lookup"><span data-stu-id="44fb4-114">By default, the value of the **Progress** property goes from 0.0 to 1.0 over the duration of the transition.</span></span> <span data-ttu-id="44fb4-115">若要反轉進度，請將 **進度** 屬性設定為從1.0 移至0.0。</span><span class="sxs-lookup"><span data-stu-id="44fb4-115">To reverse the progress, set the **Progress** property to go from 1.0 to 0.0.</span></span>

<span data-ttu-id="44fb4-116">下圖說明輸入方向和進度方向之間的差異。</span><span class="sxs-lookup"><span data-stu-id="44fb4-116">The following diagram illustrates the difference between input direction and progress direction.</span></span> <span data-ttu-id="44fb4-117">它會顯示標準 [SMPTE](smpte-wipe-transition.md) 抹除轉換的四個變化。</span><span class="sxs-lookup"><span data-stu-id="44fb4-117">It shows four variations on a standard [SMPTE Wipe](smpte-wipe-transition.md) transition.</span></span>

![抹除方向](images/wipedirections.png)

<span data-ttu-id="44fb4-119">轉換位於曲目1上。</span><span class="sxs-lookup"><span data-stu-id="44fb4-119">The transition resides on track 1.</span></span> <span data-ttu-id="44fb4-120">依預設，抹除會從左至右，以及從「曲目0」到「追蹤1」。</span><span class="sxs-lookup"><span data-stu-id="44fb4-120">By default, the wipe goes from left to right and from track 0 to track 1.</span></span> <span data-ttu-id="44fb4-121">交換輸入會導致抹除從曲目1移至追蹤0，但仍由左至右。</span><span class="sxs-lookup"><span data-stu-id="44fb4-121">Swapping inputs causes the wipe to go from track 1 to track 0, but still from left to right.</span></span> <span data-ttu-id="44fb4-122">反轉進度可讓轉換從右至左。</span><span class="sxs-lookup"><span data-stu-id="44fb4-122">Reversing the progress makes the transition go from right to left.</span></span> <span data-ttu-id="44fb4-123">您可以結合這兩個，如最左邊的顯示。</span><span class="sxs-lookup"><span data-stu-id="44fb4-123">You can combine both, as shown on the far left.</span></span>

<span data-ttu-id="44fb4-124">如需 DES 如何轉譯轉換的詳細資訊，請參閱 [時間軸模型](the-timeline-model.md)。</span><span class="sxs-lookup"><span data-stu-id="44fb4-124">For more information about how DES renders transitions, see [The Timeline Model](the-timeline-model.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="44fb4-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="44fb4-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="44fb4-126">使用效果和轉換</span><span class="sxs-lookup"><span data-stu-id="44fb4-126">Working with Effects and Transitions</span></span>](working-with-effects-and-transitions.md)
</dt> </dl>

 

 



