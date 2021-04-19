---
description: 將霧化新增至3D 場景可以增強逼真、提供 ambiance 或設定調式，以及在較遠的幾何進入視野時，有時會造成隱匿的構件。
ms.assetid: 42045e96-43aa-4cec-82b5-0b46a7d5097b
title: " (Direct3D 9) 的霧化"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44b9ed234bef0f3dea76baa98390f25e9b2003a6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106972101"
---
# <a name="fog-direct3d-9"></a><span data-ttu-id="23652-103"> (Direct3D 9) 的霧化</span><span class="sxs-lookup"><span data-stu-id="23652-103">Fog (Direct3D 9)</span></span>

<span data-ttu-id="23652-104">將霧化新增至3D 場景可以增強逼真、提供 ambiance 或設定調式，以及在較遠的幾何進入視野時，有時會造成隱匿的構件。</span><span class="sxs-lookup"><span data-stu-id="23652-104">Adding fog to a 3D scene can enhance realism, provide ambiance or set a mood, and obscure artifacts sometimes caused when distant geometry comes into view.</span></span> <span data-ttu-id="23652-105">Direct3D 支援兩種霧化模型：圖元霧化和頂點霧化，各有自己的功能和程式設計介面。</span><span class="sxs-lookup"><span data-stu-id="23652-105">Direct3D supports two fog models, pixel fog and vertex fog, each with its own features and programming interface.</span></span>

<span data-ttu-id="23652-106">基本上，會根據場景中物件的深度或與視點之間的距離，將場景中的物件色彩與所選擇的霧化色彩混合，來實行霧化。</span><span class="sxs-lookup"><span data-stu-id="23652-106">Essentially, fog is implemented by blending the color of objects in a scene with a chosen fog color based on the depth of an object in a scene or its distance from the viewpoint.</span></span> <span data-ttu-id="23652-107">隨著物件的成長較遠，其原始色彩會以所選的霧化色彩更多及更高的色彩，建立物件在場景中浮動浮動的微小物件。</span><span class="sxs-lookup"><span data-stu-id="23652-107">As objects grow more distant, their original color blends more and more with the chosen fog color, creating the illusion that the object is being increasingly obscured by tiny particles floating in the scene.</span></span> <span data-ttu-id="23652-108">下圖顯示在沒有霧化的情況下呈現的場景，以及已啟用霧化的類似場景。</span><span class="sxs-lookup"><span data-stu-id="23652-108">The following illustration shows a scene rendered without fog, and a similar scene rendered with fog enabled.</span></span>

![具有和不具有霧化之相同場景的圖例](images/fogcomp.png)

<span data-ttu-id="23652-110">在此圖中，左邊的場景具有明確的範圍，但不會顯示任何景象，即使它會顯示在真實世界中也一樣。</span><span class="sxs-lookup"><span data-stu-id="23652-110">In this illustration, the scene on the left has a clear horizon, beyond which no scenery is visible, even though it would be visible in the real world.</span></span> <span data-ttu-id="23652-111">右邊的場景會使用與背景色彩相同的霧化色彩來遮蔽範圍，讓多邊形出現淡入距離。</span><span class="sxs-lookup"><span data-stu-id="23652-111">The scene on the right obscures the horizon by using a fog color identical to the background color, making polygons appear to fade into the distance.</span></span> <span data-ttu-id="23652-112">藉由結合離散的霧化效果與創意場景設計，您可以在場景中新增調式和柔化物件的色彩。</span><span class="sxs-lookup"><span data-stu-id="23652-112">By combining discrete fog effects with creative scene design you can add mood and soften the color of objects in a scene.</span></span>

<span data-ttu-id="23652-113">Direct3D 提供兩種方式來將霧化新增至場景：圖元霧化和頂點霧化，名為會如何套用霧化效果。</span><span class="sxs-lookup"><span data-stu-id="23652-113">Direct3D provides two ways to add fog to a scene: pixel fog and vertex fog, named for how the fog effects are applied.</span></span> <span data-ttu-id="23652-114">如需詳細資訊，請參閱 [ (direct3d 9 的圖元霧化) ](pixel-fog.md) 和 [ (direct3d 9) 的頂點霧化 ](vertex-fog.md)。</span><span class="sxs-lookup"><span data-stu-id="23652-114">For details, see [Pixel Fog (Direct3D 9)](pixel-fog.md) and [Vertex Fog (Direct3D 9)](vertex-fog.md).</span></span> <span data-ttu-id="23652-115">簡言之，圖元霧化（也稱為資料表霧化）會在設備磁碟機中執行，並在 Direct3D 光源引擎中實作為頂點霧化。</span><span class="sxs-lookup"><span data-stu-id="23652-115">In short, pixel fog - also called table fog - is implemented in the device driver and vertex fog is implemented in the Direct3D lighting engine.</span></span> <span data-ttu-id="23652-116">應用程式可以使用頂點著色器和圖元霧化（如有需要）來執行霧化。</span><span class="sxs-lookup"><span data-stu-id="23652-116">An application can implement fog with a vertex shader, and pixel fog simultaneously if desired.</span></span>

> [!Note]  
> <span data-ttu-id="23652-117">無論您是使用圖元或頂點霧化，您的應用程式都必須提供符合規範的投射矩陣，以確保已正確套用霧化效果。</span><span class="sxs-lookup"><span data-stu-id="23652-117">Regardless of whether you use pixel or vertex fog, your application must provide a compliant projection matrix to ensure that fog effects are properly applied.</span></span> <span data-ttu-id="23652-118">這種限制甚至適用于未使用 Direct3D 轉換和光源引擎的應用程式。</span><span class="sxs-lookup"><span data-stu-id="23652-118">This restriction applies even to applications that do not use the Direct3D transformation and lighting engine.</span></span> <span data-ttu-id="23652-119">如需如何提供適當矩陣的其他詳細資料，請參閱 [ (Direct3D 9) 的投射轉換 ](projection-transform.md)。</span><span class="sxs-lookup"><span data-stu-id="23652-119">For additional details about how you can provide an appropriate matrix, see [Projection Transform (Direct3D 9)](projection-transform.md).</span></span>

 

<span data-ttu-id="23652-120">下列主題介紹在 Direct3D 應用程式中使用各種霧化功能的霧化和展示資訊。</span><span class="sxs-lookup"><span data-stu-id="23652-120">The following topics introduce fog and present information about using various fog features in Direct3D applications.</span></span>

-   [<span data-ttu-id="23652-121"> (Direct3D 9) 的霧化公式 </span><span class="sxs-lookup"><span data-stu-id="23652-121">Fog Formulas (Direct3D 9)</span></span>](fog-formulas.md)
-   [<span data-ttu-id="23652-122"> (Direct3D 9) 的霧化參數 </span><span class="sxs-lookup"><span data-stu-id="23652-122">Fog Parameters (Direct3D 9)</span></span>](fog-parameters.md)
-   [<span data-ttu-id="23652-123"> (Direct3D 9) 的霧化混色 </span><span class="sxs-lookup"><span data-stu-id="23652-123">Fog Blending (Direct3D 9)</span></span>](fog-blending.md)
-   [<span data-ttu-id="23652-124"> (Direct3D 9) 的霧化色彩 </span><span class="sxs-lookup"><span data-stu-id="23652-124">Fog Color (Direct3D 9)</span></span>](fog-color.md)
-   [<span data-ttu-id="23652-125"> (Direct3D 9) 的頂點霧化 </span><span class="sxs-lookup"><span data-stu-id="23652-125">Vertex Fog (Direct3D 9)</span></span>](vertex-fog.md)
-   [<span data-ttu-id="23652-126"> (Direct3D 9) 的圖元霧化 </span><span class="sxs-lookup"><span data-stu-id="23652-126">Pixel Fog (Direct3D 9)</span></span>](pixel-fog.md)

<span data-ttu-id="23652-127">霧化混色由轉譯狀態控制;它不是可程式化的圖元管線的一部分。</span><span class="sxs-lookup"><span data-stu-id="23652-127">Fog blending is controlled by render states; it is not part of the programmable pixel pipeline.</span></span>

## <a name="related-topics"></a><span data-ttu-id="23652-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="23652-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23652-129">Direct3D 轉譯</span><span class="sxs-lookup"><span data-stu-id="23652-129">Direct3D Rendering</span></span>](direct3d-rendering.md)
</dt> </dl>

 

 



