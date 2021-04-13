---
description: 畫面格緩衝區 blender 現在可以混合 Alpha 通道，而不會與呈現目標上的色頻混合。 此控制項已啟用新的轉譯狀態 D3DRS \_ SEPARATEALPHABLENDENABLE。
ms.assetid: 6d30b13e-f4c6-4bc4-8735-15c398c099f1
title: '轉譯目標 Alpha (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b70f395406559782172448b5555daff056ffd54c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104509780"
---
# <a name="render-target-alpha-direct3d-9"></a><span data-ttu-id="eea04-104">轉譯目標 Alpha (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="eea04-104">Render Target Alpha (Direct3D 9)</span></span>

<span data-ttu-id="eea04-105">畫面格緩衝區 blender 現在可以混合 Alpha 通道，而不會與呈現目標上的色頻混合。</span><span class="sxs-lookup"><span data-stu-id="eea04-105">The frame buffer blender can now blend alpha channels independent from color-channel blending on render targets.</span></span> <span data-ttu-id="eea04-106">此控制項已啟用新的轉譯狀態 D3DRS \_ SEPARATEALPHABLENDENABLE。</span><span class="sxs-lookup"><span data-stu-id="eea04-106">This control is enabled with a new render state, D3DRS\_SEPARATEALPHABLENDENABLE.</span></span>

<span data-ttu-id="eea04-107">當 D3DRS \_ SEPARATEALPHABLENDENABLE 設定為 **FALSE** (預設條件為) 時，套用至 Alpha 的轉譯目標混色因數和作業與針對混色色頻所定義的不同。</span><span class="sxs-lookup"><span data-stu-id="eea04-107">When D3DRS\_SEPARATEALPHABLENDENABLE is set to **FALSE** (which is the default condition), the render-target blending factors and operations applied to alpha are the same as those defined for blending color channels.</span></span> <span data-ttu-id="eea04-108">驅動程式必須設定 D3DPMISCCAPS \_ SEPARATEALPHABLEND cap，以指出它可以支援轉譯目標 Alpha 混合。</span><span class="sxs-lookup"><span data-stu-id="eea04-108">A driver needs to set the D3DPMISCCAPS\_SEPARATEALPHABLEND cap to indicate that it can support render-target alpha blending.</span></span> <span data-ttu-id="eea04-109">請務必啟用 D3DRS \_ ALPHABLEND，告知管線需要進行 Alpha 混色。</span><span class="sxs-lookup"><span data-stu-id="eea04-109">Be sure to enable D3DRS\_ALPHABLEND to tell the pipeline that alpha blending is needed.</span></span>

<span data-ttu-id="eea04-110">若要控制轉譯目標 blenders 之 Alpha 通道中的因素，會定義兩個新的轉譯狀態，如下所示：</span><span class="sxs-lookup"><span data-stu-id="eea04-110">To control the factors in the alpha channel of the render-target blenders, two new render states are defined as follows:</span></span>


```
D3DRS_SRCBLENDALPHA 
D3DRS_DESTBLENDALPHA 
```



<span data-ttu-id="eea04-111">如同 D3DRS \_ SRCBLEND 和 D3DRS \_ DESTBLEND，這些都可以設定為 [**D3DBLEND**](./d3dblend.md) 列舉中的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="eea04-111">Like the D3DRS\_SRCBLEND and D3DRS\_DESTBLEND, these can be set to one of the values in the [**D3DBLEND**](./d3dblend.md) enumeration.</span></span> <span data-ttu-id="eea04-112">來源和目的地 blend 設定可以用數種方式結合，視 [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)的 SrcBlendCaps 和 DestBlendCaps 成員中的設定而定。</span><span class="sxs-lookup"><span data-stu-id="eea04-112">The source and destination blend settings can be combined in several ways, depending on the settings in the SrcBlendCaps and DestBlendCaps members of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

<span data-ttu-id="eea04-113">Alpha 混合的完成方式如下：</span><span class="sxs-lookup"><span data-stu-id="eea04-113">The alpha blending is done as follows:</span></span>

<span data-ttu-id="eea04-114">renderTargetAlpha = 在 srcBlendOp<sub>中</sub> (Alpha \*) BlendOp (Alpha<sub>rt</sub> \* destBlendOp) </span><span class="sxs-lookup"><span data-stu-id="eea04-114">renderTargetAlpha = (alpha<sub>in</sub> \* srcBlendOp) BlendOp (alpha<sub>rt</sub> \* destBlendOp)</span></span>

<span data-ttu-id="eea04-115">其中：</span><span class="sxs-lookup"><span data-stu-id="eea04-115">Where:</span></span>

-   <span data-ttu-id="eea04-116"><sub>中</sub>的 Alpha 是輸入 Alpha 值。</span><span class="sxs-lookup"><span data-stu-id="eea04-116">alpha<sub>in</sub> is the input alpha value.</span></span>
-   <span data-ttu-id="eea04-117">srcBlendOp 是 [**D3DBLEND**](./d3dblend.md)中的其中一個 blend 因素。</span><span class="sxs-lookup"><span data-stu-id="eea04-117">srcBlendOp is one of the blend factors in [**D3DBLEND**](./d3dblend.md).</span></span>
-   <span data-ttu-id="eea04-118">BlendOp 是 [**D3DBLENDOP**](./d3dblendop.md)中的其中一個 blend 因素。</span><span class="sxs-lookup"><span data-stu-id="eea04-118">BlendOp is one of the blend factors in [**D3DBLENDOP**](./d3dblendop.md).</span></span>
-   <span data-ttu-id="eea04-119">Alpha<sub>rt</sub> 是呈現目標的 Alpha 值。</span><span class="sxs-lookup"><span data-stu-id="eea04-119">alpha<sub>rt</sub> is the render-target alpha value.</span></span>
-   <span data-ttu-id="eea04-120">destBlendOp 是 [**D3DBLEND**](./d3dblend.md)中的其中一個 blend 因素。</span><span class="sxs-lookup"><span data-stu-id="eea04-120">destBlendOp is one of the blend factors in [**D3DBLEND**](./d3dblend.md).</span></span>
-   <span data-ttu-id="eea04-121">renderTargetAlpha 是最終的混合 Alpha 值。</span><span class="sxs-lookup"><span data-stu-id="eea04-121">renderTargetAlpha is the final blended alpha value.</span></span>

## <a name="related-topics"></a><span data-ttu-id="eea04-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="eea04-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eea04-123">Alpha 混色</span><span class="sxs-lookup"><span data-stu-id="eea04-123">Alpha Blending</span></span>](alpha-blending.md)
</dt> </dl>

 

 
