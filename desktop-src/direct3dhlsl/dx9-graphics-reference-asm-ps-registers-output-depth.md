---
title: 輸出深度註冊
description: 圖元著色器輸出深度暫存器 (oDepth) 是僅限寫入的純量暫存器，其範圍為 \ 0. 1 \，可針對深度樣板緩衝區傳回深度測試的新深度值。
ms.assetid: 47b9afd9-4520-480d-b4a2-3d9a5569defb
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9be825d6117cf1cc14464973146dbe176d696d25
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311481"
---
# <a name="output-depth-register"></a><span data-ttu-id="95479-103">輸出深度註冊</span><span class="sxs-lookup"><span data-stu-id="95479-103">Output Depth Register</span></span>

<span data-ttu-id="95479-104">圖元著色器輸出深度暫存器 (oDepth) 是僅限寫入的純量暫存器，其範圍為 \[ 0 ..1 \] ，可針對深度樣板緩衝區傳回深度測試的新深度值。</span><span class="sxs-lookup"><span data-stu-id="95479-104">The pixel shader output depth register (oDepth) is a write-only scalar register with the range \[0..1\] that returns a new depth value for a depth test against the depth-stencil buffer.</span></span>

<span data-ttu-id="95479-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="95479-105">Syntax</span></span>



| <span data-ttu-id="95479-106">oDepth</span><span class="sxs-lookup"><span data-stu-id="95479-106">oDepth</span></span> |
|--------|



 

<span data-ttu-id="95479-107">其中：</span><span class="sxs-lookup"><span data-stu-id="95479-107">Where:</span></span>



| <span data-ttu-id="95479-108">Name</span><span class="sxs-lookup"><span data-stu-id="95479-108">Name</span></span>   | <span data-ttu-id="95479-109">描述</span><span class="sxs-lookup"><span data-stu-id="95479-109">Description</span></span>                                                       |
|--------|-------------------------------------------------------------------|
| <span data-ttu-id="95479-110">oDepth</span><span class="sxs-lookup"><span data-stu-id="95479-110">oDepth</span></span> | <span data-ttu-id="95479-111">深度測試的新深度值-樣板緩衝區</span><span class="sxs-lookup"><span data-stu-id="95479-111">New depth value for a depth test against the depth-stencil buffer</span></span> |



 

<span data-ttu-id="95479-112">要注意的是，寫入 oDepth 會導致遺失任何硬體特定深度緩衝區優化演算法 (亦即階層式 Z) ，可加快深度測試效能。</span><span class="sxs-lookup"><span data-stu-id="95479-112">It is important to be aware that writing to oDepth causes the loss of any hardware-specific depth buffer optimization algorithms (i.e. hierarchical Z) which accelerate depth test performance.</span></span>

<span data-ttu-id="95479-113">\| \| 寫入至 oDepth 時，需要複寫來源 swizzle (. x. y. z. \| w) 。</span><span class="sxs-lookup"><span data-stu-id="95479-113">Replicate source swizzle (.x \| .y \| .z \| .w) is required when writing to oDepth.</span></span> <span data-ttu-id="95479-114">不允許明確的寫入遮罩。</span><span class="sxs-lookup"><span data-stu-id="95479-114">Explicit write masks are not allowed.</span></span>

<span data-ttu-id="95479-115">寫入至 oDepth 註冊會取代插補深度值 (，並忽略任何深度偏差/slopescale renderstates) 。</span><span class="sxs-lookup"><span data-stu-id="95479-115">Writing to the oDepth register replaces the interpolated depth value (and ignores any depth bias/slopescale renderstates).</span></span> <span data-ttu-id="95479-116">如果未建立任何深度緩衝區或將其附加至裝置，則會忽略寫入 oDepth。</span><span class="sxs-lookup"><span data-stu-id="95479-116">If no depth buffer has been created or attached to the device, then write to oDepth is ignored.</span></span>

<span data-ttu-id="95479-117">如果您要進行取樣並寫入至 oDepth，因為圖元著色器每圖元只會執行一次，所以會針對所有涵蓋的子樣本位置複寫您的深度值。</span><span class="sxs-lookup"><span data-stu-id="95479-117">If you are multisampling and write to oDepth, since the pixel shader only runs once per pixel, your depth value is replicated for all covered sub-sample locations.</span></span> <span data-ttu-id="95479-118">深度測試仍會在每個範例中進行，但您不會有每個取樣的深度值與圖元著色器的比較，就像您未撰寫 oDepth 一樣。</span><span class="sxs-lookup"><span data-stu-id="95479-118">The depth test still happens per-sample, but you don't have a per-sample depth value going into the comparison from the pixel shader like you would have if you didn't write oDepth.</span></span>

<span data-ttu-id="95479-119">如果應用程式將 w 緩衝區設定為其深度緩衝區，則在寫入至 oDepth 時，必須將該應用程式納入考慮。</span><span class="sxs-lookup"><span data-stu-id="95479-119">If an application has a w-buffer set as its depth buffer, then it needs to take that into account while writing to oDepth.</span></span> <span data-ttu-id="95479-120">它可能需要將 w 範圍資訊傳送給圖元著色器，並計算 w 範圍，以將寫出的 w 值調整為 oDepth。</span><span class="sxs-lookup"><span data-stu-id="95479-120">It potentially needs to send w-range information to the pixel shader and compute the w-range to scale the w-values written out to oDepth.</span></span>

### <a name="ps_2_0-and-ps_2_x-restrictions"></a><span data-ttu-id="95479-121">ps \_ 2 \_ 0 和 ps \_ 2 \_ x 限制</span><span class="sxs-lookup"><span data-stu-id="95479-121">ps\_2\_0 and ps\_2\_x Restrictions</span></span>

-   <span data-ttu-id="95479-122">oDepth 只能以 [mov-ps](mov---ps.md) 指令撰寫，而且只能執行一次。</span><span class="sxs-lookup"><span data-stu-id="95479-122">oDepth can only be written with the [mov - ps](mov---ps.md) instruction and can only be done once.</span></span>
-   <span data-ttu-id="95479-123">寫入 oDepth 時，不允許來源修飾詞。</span><span class="sxs-lookup"><span data-stu-id="95479-123">No source modifier is allowed when writing to oDepth.</span></span>
-   <span data-ttu-id="95479-124">寫入至 oDepth 時，不允許使用指令修飾詞。</span><span class="sxs-lookup"><span data-stu-id="95479-124">No instruction modifier is allowed when writing to oDepth.</span></span>
-   <span data-ttu-id="95479-125">從流程式控制制結構內或使用 predication 時，不會寫入至 oDepth。</span><span class="sxs-lookup"><span data-stu-id="95479-125">No writing to oDepth from within a flow control construct, or when using predication.</span></span>

### <a name="ps_3_0-restrictions"></a><span data-ttu-id="95479-126">ps \_ 3 \_ 0 限制</span><span class="sxs-lookup"><span data-stu-id="95479-126">ps\_3\_0 Restrictions</span></span>

-   <span data-ttu-id="95479-127">針對 ps \_ 3 \_ 0，輸出會將 oC # 和 oD \# 寫入任意次數。</span><span class="sxs-lookup"><span data-stu-id="95479-127">For ps\_3\_0, output registers oC# and oD\# can be written any number of times.</span></span> <span data-ttu-id="95479-128">圖元著色器的輸出來自于著色器執行結束時的輸出暫存器內容。</span><span class="sxs-lookup"><span data-stu-id="95479-128">The output of the pixel shader comes from the contents of the output registers at the end of shader execution.</span></span> <span data-ttu-id="95479-129">如果未進行寫入至輸出暫存器（可能是因為流量控制），或是著色器剛剛未寫入，則也不會更新對應的呈現目標。</span><span class="sxs-lookup"><span data-stu-id="95479-129">If a write to an output register does not happen, perhaps due to flow control or if the shader just did not write it, the corresponding render target is also not updated.</span></span> <span data-ttu-id="95479-130">如果寫入輸出暫存器中的通道子集，則會將未定義的值寫入其餘的通道。</span><span class="sxs-lookup"><span data-stu-id="95479-130">If a subset of the channels in an output register are written, then undefined values will be written to the remaining channels.</span></span>
-   <span data-ttu-id="95479-131">您可以在流量控制或 predication 中寫入 oDepth，只要所有可能的路徑最後寫入註冊即可。</span><span class="sxs-lookup"><span data-stu-id="95479-131">You can write to oDepth within flow control or predication as long as all possible paths eventually write into the register.</span></span>
-   <span data-ttu-id="95479-132">您可能不會執行任何漸層計算 (或隱含叫用漸層計算的作業（例如 [texld-ps \_ 2 \_ 0 和 up](texld---ps-2-0.md)、 [texldb-ps](texldb---ps.md)、 [texldp-ps](texldp---ps.md)) 在流程式控制制語句內，其分支條件會因每個基準而異 (例如：動態流程式控制制指示) 。</span><span class="sxs-lookup"><span data-stu-id="95479-132">You may not perform any gradient calculations (or operations that implicitly invoke gradient calculations such as [texld - ps\_2\_0 and up](texld---ps-2-0.md), [texldb - ps](texldb---ps.md), [texldp - ps](texldp---ps.md)) inside of flow control statements whose branching conditions vary on a per-primitive basis (ie: dynamic flow control instructions).</span></span> <span data-ttu-id="95479-133">指令 predication 不會被視為動態流量控制。</span><span class="sxs-lookup"><span data-stu-id="95479-133">Instruction predication is not considered dynamic flow control.</span></span>

## <a name="related-topics"></a><span data-ttu-id="95479-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="95479-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="95479-135">寄存 器</span><span class="sxs-lookup"><span data-stu-id="95479-135">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




