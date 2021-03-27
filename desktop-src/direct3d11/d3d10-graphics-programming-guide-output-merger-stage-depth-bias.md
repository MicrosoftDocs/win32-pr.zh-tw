---
title: 深度偏差
description: 在3D 空間中有共置的多邊形，會顯示為不是共置的多邊形，方法是將 z 偏差 (或深度偏差) 新增至每一個。
ms.assetid: ee904316-dc6d-48a4-bdb7-0f7dcdb9d9d6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d6f9a3850b03e033a90b358d0c6ffd1ceef830f
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "103684266"
---
# <a name="depth-bias"></a><span data-ttu-id="1ecc4-103">深度偏差</span><span class="sxs-lookup"><span data-stu-id="1ecc4-103">Depth Bias</span></span>

<span data-ttu-id="1ecc4-104">在3D 空間中有共置的多邊形，會顯示為不是共置的多邊形，方法是將 z 偏差 (或深度偏差) 新增至每一個。</span><span class="sxs-lookup"><span data-stu-id="1ecc4-104">Polygons that are coplanar in 3D space can be made to appear as if they are not coplanar by adding a z-bias (or depth bias) to each one.</span></span>

<span data-ttu-id="1ecc4-105">這項技術通常用來確保場景中的陰影正確顯示。</span><span class="sxs-lookup"><span data-stu-id="1ecc4-105">This is a technique commonly used to ensure that shadows in a scene are displayed properly.</span></span> <span data-ttu-id="1ecc4-106">例如，牆上的陰影可能會有與牆相同的深度值。</span><span class="sxs-lookup"><span data-stu-id="1ecc4-106">For instance, a shadow on a wall will likely have the same depth value as the wall.</span></span> <span data-ttu-id="1ecc4-107">如果應用程式先轉譯牆，然後再呈現陰影，則可能看不到陰影，或是可見的深度成品。</span><span class="sxs-lookup"><span data-stu-id="1ecc4-107">If an application renders a wall first and then a shadow, the shadow might not be visible, or depth artifacts might be visible.</span></span>


<span data-ttu-id="1ecc4-108">應用程式可以藉由將偏差 (從 D3D11 轉譯器) [**\_ \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1)的 **DepthBias** 成員新增到系統在轉譯共置多邊形的集合時使用的 z 值，協助確保已正確轉譯共置多邊形。</span><span class="sxs-lookup"><span data-stu-id="1ecc4-108">An application can help ensure that coplanar polygons are rendered properly by adding the bias (from the **DepthBias** member of [**D3D11\_RASTERIZER\_DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1)) to the z-values that the system uses when rendering the sets of coplanar polygons.</span></span> <span data-ttu-id="1ecc4-109">具有較大 z 值的多邊形會繪製在具有較小 z 值的多邊形前方。</span><span class="sxs-lookup"><span data-stu-id="1ecc4-109">Polygons with a larger z value will be drawn in front of polygons with a smaller z value.</span></span>

<span data-ttu-id="1ecc4-110">有兩個選項可計算深度偏差。</span><span class="sxs-lookup"><span data-stu-id="1ecc4-110">There are two options for calculating depth bias.</span></span>

1.  <span data-ttu-id="1ecc4-111">如果目前系結至輸出合併階段的深度緩衝區有 **UNORM** 格式，或沒有系結的深度緩衝區，則偏差值的計算方式如下：</span><span class="sxs-lookup"><span data-stu-id="1ecc4-111">If the depth buffer currently bound to the output-merger stage has a **UNORM** format or no depth buffer is bound, the bias value is calculated like this:</span></span>
    ```
    Bias = (float)DepthBias * r + SlopeScaledDepthBias * MaxDepthSlope;
    ```

    

    <span data-ttu-id="1ecc4-112">其中 *r* 是在深度緩衝區格式轉換為 **float32** 的最小可表示值 > 0。</span><span class="sxs-lookup"><span data-stu-id="1ecc4-112">where *r* is the minimum representable value > 0 in the depth-buffer format converted to **float32**.</span></span> <span data-ttu-id="1ecc4-113">**DepthBias** 和 **SlopeScaledDepthBias** 值是 D3D11 的轉譯器 [**\_ \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1)結構成員。</span><span class="sxs-lookup"><span data-stu-id="1ecc4-113">The **DepthBias** and **SlopeScaledDepthBias** values are [**D3D11\_RASTERIZER\_DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1) structure members.</span></span> <span data-ttu-id="1ecc4-114">**MaxDepthSlope** 值是圖元深度值水準和垂直傾斜的最大值。</span><span class="sxs-lookup"><span data-stu-id="1ecc4-114">The **MaxDepthSlope** value is the maximum of the horizontal and vertical slopes of the depth value at the pixel.</span></span>
2.  <span data-ttu-id="1ecc4-115">如果浮點深度緩衝區系結至輸出合併階段，偏差值的計算方式如下：</span><span class="sxs-lookup"><span data-stu-id="1ecc4-115">If a floating-point depth buffer is bound to the output-merger stage the bias value is calculated like this:</span></span>
    ```
    Bias = (float)DepthBias * 2**(exponent(max z in primitive) - r) +
                SlopeScaledDepthBias * MaxDepthSlope;
    ```

    

    <span data-ttu-id="1ecc4-116">其中 *r* 是浮點數標記法中的尾數位數目 (不包括隱藏的位) ;例如，針對 **float32** 的23。</span><span class="sxs-lookup"><span data-stu-id="1ecc4-116">where *r* is the number of mantissa bits in the floating point representation (excluding the hidden bit); for example, 23 for **float32**.</span></span>

<span data-ttu-id="1ecc4-117">然後，偏差值會壓制如下：</span><span class="sxs-lookup"><span data-stu-id="1ecc4-117">The bias value is then clamped like this:</span></span>


```
if(DepthBiasClamp > 0)
    Bias = min(DepthBiasClamp, Bias)
else if(DepthBiasClamp < 0)
    Bias = max(DepthBiasClamp, Bias)
```



<span data-ttu-id="1ecc4-118">然後，會使用偏差值來計算圖元深度。</span><span class="sxs-lookup"><span data-stu-id="1ecc4-118">The bias value is then used to calculate the pixel depth.</span></span>


```
if ( (DepthBias != 0) || (SlopeScaledDepthBias != 0) )
    z = z + Bias
```



<span data-ttu-id="1ecc4-119">深度偏差作業會在剪切之後頂點上發生，因此深度偏差不會影響幾何裁剪。</span><span class="sxs-lookup"><span data-stu-id="1ecc4-119">Depth-bias operations occur on vertices after clipping, therefore, depth-bias has no effect on geometric clipping.</span></span> <span data-ttu-id="1ecc4-120">針對給定的基本值，偏差值是常數，而且會在插即置設定之前加入每個頂點的 z 值。</span><span class="sxs-lookup"><span data-stu-id="1ecc4-120">The bias value is constant for a given primitive and is added to the z value for each vertex before interpolator setup.</span></span> <span data-ttu-id="1ecc4-121">當您使用 [功能層級](overviews-direct3d-11-devices-downlevel-intro.md) 10.0 和更高版本時，會使用32位浮點算術來執行所有偏差計算。</span><span class="sxs-lookup"><span data-stu-id="1ecc4-121">When you use [feature levels](overviews-direct3d-11-devices-downlevel-intro.md) 10.0 and higher, all bias calculations are performed using 32-bit floating-point arithmetic.</span></span> <span data-ttu-id="1ecc4-122">偏差不會套用到任何點或線條基本專案，但以線框模式繪製的線條除外。</span><span class="sxs-lookup"><span data-stu-id="1ecc4-122">Bias is not applied to any point or line primitives, except for lines drawn in wireframe mode.</span></span>

<span data-ttu-id="1ecc4-123">具有陰影緩衝區型陰影的其中一個成品是陰影 acne，或是表面遮蔽本身，因為著色器中的深度計算和陰影緩衝區中的深度計算有些許差異。</span><span class="sxs-lookup"><span data-stu-id="1ecc4-123">One of the artifacts with shadow buffer based shadows is shadow acne, or a surface shadowing itself due to minor differences between the depth computation in a shader, and the depth of the same surface in the shadow buffer.</span></span> <span data-ttu-id="1ecc4-124">解決這種情況的一種方法是在轉譯陰影緩衝區時使用 **DepthBias** 和 **SlopeScaledDepthBias** 。</span><span class="sxs-lookup"><span data-stu-id="1ecc4-124">One way to alleviate this is to use **DepthBias** and **SlopeScaledDepthBias** when rendering a shadow buffer.</span></span> <span data-ttu-id="1ecc4-125">其構想是在轉譯陰影緩衝區時，將表面推出足夠的範圍，讓陰影緩衝區 z 與著色器 z) 之間的比較結果 (一致，並避免本機自我遮蔽。</span><span class="sxs-lookup"><span data-stu-id="1ecc4-125">The idea is to push surfaces out enough while rendering a shadow buffer so that the comparison result (between the shadow buffer z and the shader z) is consistent across the surface, and avoid local self-shadowing.</span></span>

<span data-ttu-id="1ecc4-126">不過，使用 **DepthBias** 和 **SlopeScaledDepthBias** 時，可能會在以極銳利的角度查看的多邊形產生新的轉譯問題，而造成偏差方程式產生非常大的 z 值。</span><span class="sxs-lookup"><span data-stu-id="1ecc4-126">However, using **DepthBias** and **SlopeScaledDepthBias** can introduce new rendering problems when a polygon viewed at an extremely sharp angle causes the bias equation to generate a very large z value.</span></span> <span data-ttu-id="1ecc4-127">這實際上會從陰影地圖中的原始表面，將多邊形推播得相當遠。</span><span class="sxs-lookup"><span data-stu-id="1ecc4-127">This in effect pushes the polygon extremely far away from the original surface in the shadow map.</span></span> <span data-ttu-id="1ecc4-128">解決此特定問題的其中一種方法是使用 **DepthBiasClamp**，它會在計算的 z 偏差範圍上提供上限 (正面或負面) 。</span><span class="sxs-lookup"><span data-stu-id="1ecc4-128">One way to help alleviate this particular problem is to use **DepthBiasClamp**, which provides an upper bound (positive or negative) on the magnitude of the z bias calculated.</span></span>

> [!Note]  
> <span data-ttu-id="1ecc4-129">若為 [功能層級](overviews-direct3d-11-devices-downlevel-intro.md) 9.1、9.2、9.3、 **DepthBiasClamp** ，則不受支援。</span><span class="sxs-lookup"><span data-stu-id="1ecc4-129">For [feature levels](overviews-direct3d-11-devices-downlevel-intro.md) 9.1, 9.2, 9.3, **DepthBiasClamp** is not supported.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="1ecc4-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="1ecc4-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1ecc4-131">輸出合併階段</span><span class="sxs-lookup"><span data-stu-id="1ecc4-131">Output-Merger Stage</span></span>](d3d10-graphics-programming-guide-output-merger-stage.md)
</dt> </dl>

 

 




