---
description: C + + 應用程式可以藉由變更 Microsoft Direct3D 如何計算與距離之間的霧化效果，來控制霧化如何影響場景中的物件色彩。
ms.assetid: b7148ae8-45c7-4dbe-8295-0335c7fdeff0
title: " (Direct3D 9) 的霧化公式"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75150a00d491f1e3fc1ea1444209449c1c2a825d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846175"
---
# <a name="fog-formulas-direct3d-9"></a><span data-ttu-id="e6785-103"> (Direct3D 9) 的霧化公式</span><span class="sxs-lookup"><span data-stu-id="e6785-103">Fog Formulas (Direct3D 9)</span></span>

<span data-ttu-id="e6785-104">C + + 應用程式可以藉由變更 Microsoft Direct3D 如何計算與距離之間的霧化效果，來控制霧化如何影響場景中的物件色彩。</span><span class="sxs-lookup"><span data-stu-id="e6785-104">C++ applications can control how fog affects the color of objects in a scene by changing how Microsoft Direct3D computes fog effects over distance.</span></span> <span data-ttu-id="e6785-105">[**D3DFOGMODE**](./d3dfogmode.md)列舉型別包含可識別三個霧化公式的成員。</span><span class="sxs-lookup"><span data-stu-id="e6785-105">The [**D3DFOGMODE**](./d3dfogmode.md) enumerated type contains members that identify the three fog formulas.</span></span> <span data-ttu-id="e6785-106">所有公式都會將一個霧化因數計算為距離的函式，並指定您的應用程式所設定的參數。</span><span class="sxs-lookup"><span data-stu-id="e6785-106">All formulas calculate a fog factor as a function of distance, given parameters that your application sets.</span></span>

## <a name="linear-fog"></a><span data-ttu-id="e6785-107">線性霧化</span><span class="sxs-lookup"><span data-stu-id="e6785-107">Linear Fog</span></span>

<span data-ttu-id="e6785-108">這會以下列 D3DFOG 線性方程序來設定 \_ 。</span><span class="sxs-lookup"><span data-stu-id="e6785-108">This is set with the following D3DFOG\_LINEAR equation.</span></span>

![direct3d 線性模糊的方程式](images/fogliner.png)

<span data-ttu-id="e6785-110">其中</span><span class="sxs-lookup"><span data-stu-id="e6785-110">where</span></span>

-   <span data-ttu-id="e6785-111">start 是霧化效果開始的距離。</span><span class="sxs-lookup"><span data-stu-id="e6785-111">start is the distance at which fog effects begin.</span></span>
-   <span data-ttu-id="e6785-112">end 是不會再增加霧化效果的距離。</span><span class="sxs-lookup"><span data-stu-id="e6785-112">end is the distance at which fog effects no longer increase.</span></span>
-   <span data-ttu-id="e6785-113">d 表示深度，或從觀點來看距離。</span><span class="sxs-lookup"><span data-stu-id="e6785-113">d represents depth, or the distance from the viewpoint.</span></span> <span data-ttu-id="e6785-114">針對以範圍為基礎的霧化，d 的值是相機位置與頂點之間的距離。</span><span class="sxs-lookup"><span data-stu-id="e6785-114">For range based fog, the value for d is the distance between the camera position and a vertex.</span></span> <span data-ttu-id="e6785-115">針對非範圍的霧化，d 的值是相機空間中 Z 座標的絕對值。</span><span class="sxs-lookup"><span data-stu-id="e6785-115">For non-range based fog, the value for d is the absolute value of the Z-coordinate in camera space.</span></span>

## <a name="exponential-fog"></a><span data-ttu-id="e6785-116">指數霧化</span><span class="sxs-lookup"><span data-stu-id="e6785-116">Exponential Fog</span></span>

<span data-ttu-id="e6785-117">線性和指數公式都支援圖元霧化和頂點霧化。</span><span class="sxs-lookup"><span data-stu-id="e6785-117">Linear and exponential formulas are supported for both pixel fog and vertex fog.</span></span>

<span data-ttu-id="e6785-118">這會使用下列 D3DFOG EXP 方程式來設定 \_ 。</span><span class="sxs-lookup"><span data-stu-id="e6785-118">This is set with the following D3DFOG\_EXP equation.</span></span>

![direct3d 指數霧化的方程式](images/fogexp.png)

<span data-ttu-id="e6785-120">其中</span><span class="sxs-lookup"><span data-stu-id="e6785-120">where</span></span>

-   <span data-ttu-id="e6785-121">e 是自然對數的基底， (大約 2.71828) 。</span><span class="sxs-lookup"><span data-stu-id="e6785-121">e is the base of natural logarithms (approximately 2.71828).</span></span>
-   <span data-ttu-id="e6785-122">密度是任意的霧化密度，範圍從0.0 到1.0。</span><span class="sxs-lookup"><span data-stu-id="e6785-122">density is an arbitrary fog density that can range from 0.0 to 1.0.</span></span>
-   <span data-ttu-id="e6785-123">d 表示深度，或與視點之間的距離（如先前所述）。</span><span class="sxs-lookup"><span data-stu-id="e6785-123">d represents depth, or the distance from the viewpoint, as stated earlier.</span></span>

<span data-ttu-id="e6785-124">這會使用下列 D3DFOG EXP2 方程式來設定 \_ 。</span><span class="sxs-lookup"><span data-stu-id="e6785-124">This is set with the following D3DFOG\_EXP2 equation.</span></span>

![direct3d 指數2霧化的方程式](images/fogexp2.png)

<span data-ttu-id="e6785-126">其中</span><span class="sxs-lookup"><span data-stu-id="e6785-126">where</span></span>

-   <span data-ttu-id="e6785-127">e 是自然對數的基底，如上所述。</span><span class="sxs-lookup"><span data-stu-id="e6785-127">e is the base of natural logarithms as stated above.</span></span>
-   <span data-ttu-id="e6785-128">密度是任意的霧化密度，其範圍從0.0 到1.0，如上所述。</span><span class="sxs-lookup"><span data-stu-id="e6785-128">density is an arbitrary fog density that can range from 0.0 to 1.0 as stated above.</span></span>
-   <span data-ttu-id="e6785-129">d 表示深度，或與觀點的距離，如上所述。</span><span class="sxs-lookup"><span data-stu-id="e6785-129">d represents depth, or the distance from the viewpoint, as stated above.</span></span>

> [!Note]  
> <span data-ttu-id="e6785-130">系統會在頂點的反射色彩 Alpha 元件中儲存霧化因數。</span><span class="sxs-lookup"><span data-stu-id="e6785-130">The system stores the fog factor in the alpha component of the specular color for a vertex.</span></span> <span data-ttu-id="e6785-131">如果您的應用程式執行自己的轉換和光源，您可以手動插入霧化因數值，以在轉譯期間由系統套用。</span><span class="sxs-lookup"><span data-stu-id="e6785-131">If your application performs its own transformation and lighting, you can insert fog factor values manually, to be applied by the system during rendering.</span></span>

 

<span data-ttu-id="e6785-132">下圖顯示這些公式，並使用公式參數中的一般值。</span><span class="sxs-lookup"><span data-stu-id="e6785-132">The following graph shows these formulas, using common values as in the formula parameters.</span></span>

![在距離和色彩量之間的霧化公式圖表](images/foggraph.png)

<span data-ttu-id="e6785-134">D3DFOG \_ 線性在開始和0.0 結束時為1.0。</span><span class="sxs-lookup"><span data-stu-id="e6785-134">D3DFOG\_LINEAR is 1.0 at start and 0.0 at end.</span></span> <span data-ttu-id="e6785-135">它不會相對於接近或遠的平面來測量。</span><span class="sxs-lookup"><span data-stu-id="e6785-135">It is not measured relative to the near or far planes.</span></span>

<span data-ttu-id="e6785-136">當 Direct3D 計算霧化效果時，它會使用下列混合方程式中上述其中一個方程式的霧化係數。</span><span class="sxs-lookup"><span data-stu-id="e6785-136">When Direct3D calculates fog effects, it uses the fog factor from one of the preceding equations in the following blending equation.</span></span>

![direct3d 的霧化效果方程式](images/fogcalc.png)

<span data-ttu-id="e6785-138">此公式會有效地以霧因數 f 來調整目前多邊形 C 的色彩，並將產品加入至霧色 C，並以霧化因數的位反向進行縮放。</span><span class="sxs-lookup"><span data-stu-id="e6785-138">This formula effectively scales the color of the current polygon C by the fog factor f, and adds the product to the fog color C, scaled by the bitwise inverse of the fog factor.</span></span> <span data-ttu-id="e6785-139">產生的色彩值是霧化色彩和原始色彩的 blend，作為距離的係數。</span><span class="sxs-lookup"><span data-stu-id="e6785-139">The resulting color value is a blend of the fog color and the original color, as a factor of distance.</span></span> <span data-ttu-id="e6785-140">此公式適用于 Microsoft DirectX 7.0 和更新版本中支援的所有裝置。</span><span class="sxs-lookup"><span data-stu-id="e6785-140">The formula applies to all devices supported in Microsoft DirectX 7.0 and later.</span></span> <span data-ttu-id="e6785-141">針對舊版的遞增裝置，霧化因數會調整擴散和反射色彩元件，壓制至0.0 和1.0 （含）的範圍。</span><span class="sxs-lookup"><span data-stu-id="e6785-141">For the legacy ramp device, the fog factor scales the diffuse and specular color components, clamped to the range of 0.0 and 1.0, inclusive.</span></span> <span data-ttu-id="e6785-142">下平面的霧化因數通常會從1.0 開始，並在最遠的平面減少為0.0。</span><span class="sxs-lookup"><span data-stu-id="e6785-142">The fog factor typically starts at 1.0 for the near plane and decreases to 0.0 at the far plane.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e6785-143">相關主題</span><span class="sxs-lookup"><span data-stu-id="e6785-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e6785-144">霧化類型</span><span class="sxs-lookup"><span data-stu-id="e6785-144">Fog Types</span></span>](fog-types.md)
</dt> </dl>

 

 
