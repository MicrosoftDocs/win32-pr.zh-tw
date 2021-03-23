---
title: 範例根簽章
description: 下一節顯示從空白到完全完整的根目錄簽章變化。
ms.assetid: 493D35C9-2A90-4688-BD7E-74B9EB2B4E72
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19d09d355cc1c96d77670c5536400f0b3f93c097
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103785"
---
# <a name="example-root-signatures"></a><span data-ttu-id="576bd-103">範例根簽章</span><span class="sxs-lookup"><span data-stu-id="576bd-103">Example Root Signatures</span></span>

<span data-ttu-id="576bd-104">下一節顯示從空白到完全完整的根目錄簽章變化。</span><span class="sxs-lookup"><span data-stu-id="576bd-104">The following section shows root signatures varying in complexity from empty to completely full.</span></span>

-   [<span data-ttu-id="576bd-105">空白的根簽章</span><span class="sxs-lookup"><span data-stu-id="576bd-105">An empty root signature</span></span>](#an-empty-root-signature)
-   [<span data-ttu-id="576bd-106">一個常數</span><span class="sxs-lookup"><span data-stu-id="576bd-106">One constant</span></span>](#one-constant)
-   [<span data-ttu-id="576bd-107">加入根常數緩衝區視圖</span><span class="sxs-lookup"><span data-stu-id="576bd-107">Adding a root Constant Buffer View</span></span>](#adding-a-root-constant-buffer-view)
-   [<span data-ttu-id="576bd-108">系結描述中繼資料表</span><span class="sxs-lookup"><span data-stu-id="576bd-108">Binding descriptor tables</span></span>](#binding-descriptor-tables)
-   [<span data-ttu-id="576bd-109">更複雜的根簽章</span><span class="sxs-lookup"><span data-stu-id="576bd-109">A more complex root signature</span></span>](#a-more-complex-root-signature)
-   [<span data-ttu-id="576bd-110">串流著色器資源檢視</span><span class="sxs-lookup"><span data-stu-id="576bd-110">Streaming Shader Resource Views</span></span>](#streaming-shader-resource-views)
-   [<span data-ttu-id="576bd-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="576bd-111">Related topics</span></span>](#related-topics)

## <a name="an-empty-root-signature"></a><span data-ttu-id="576bd-112">空白的根簽章</span><span class="sxs-lookup"><span data-stu-id="576bd-112">An empty root signature</span></span>

![空白的根簽章沒有系結](images/root-tables-0.png)

<span data-ttu-id="576bd-114">空白的根簽章不太可能有用，但可用於只使用輸入組合語言的簡單轉譯階段，以及不會存取任何描述項的最小頂點和圖元著色器。</span><span class="sxs-lookup"><span data-stu-id="576bd-114">An empty root signature is unlikely to be useful, but could be used in a trivial rendering pass with use of only the input assembler, and minimal vertex and pixel shaders that do not access any descriptors.</span></span> <span data-ttu-id="576bd-115">此外，也可以使用 blend 階段、轉譯目標和深度樣板階段，即使是空的根簽章也是一樣。</span><span class="sxs-lookup"><span data-stu-id="576bd-115">Also the blend stage, render target and depth-stencil stages are available, even with an empty root signature.</span></span>

## <a name="one-constant"></a><span data-ttu-id="576bd-116">一個常數</span><span class="sxs-lookup"><span data-stu-id="576bd-116">One constant</span></span>

![單一根常數](images/root-tables-constant.png)

<span data-ttu-id="576bd-118">API 系結位置是此參數的根引數會在命令清單記錄時間進行系結。</span><span class="sxs-lookup"><span data-stu-id="576bd-118">The API bind slot is where the root argument for this parameter will be bound at command list record time.</span></span> <span data-ttu-id="576bd-119">API 系結位置的數目是隱含的，根據根簽章中的參數順序 (第一個一律為零) 。</span><span class="sxs-lookup"><span data-stu-id="576bd-119">The number of the API bind slots is implicit, based on the order of the parameters in the root signature (the first is always zero).</span></span> <span data-ttu-id="576bd-120">HLSL 系結位置是著色器會看到根參數顯示的位置。</span><span class="sxs-lookup"><span data-stu-id="576bd-120">The HLSL bind slot is where the shader will see the root parameter show up.</span></span> <span data-ttu-id="576bd-121">上述) 範例中的 "uint" ( 類型對硬體而言是未知的，但只是映射中的批註，而硬體只會看到單一 DWORD 作為內容。</span><span class="sxs-lookup"><span data-stu-id="576bd-121">The type ("uint" in the above example) is not known to the hardware but is just a comment in the image, the hardware will simply see the single DWORD as the contents.</span></span>

<span data-ttu-id="576bd-122">若要在命令清單記錄時間系結常數，請使用類似下列的命令：</span><span class="sxs-lookup"><span data-stu-id="576bd-122">To bind a constant at command-list record time, a command similar to the following would be used:</span></span>

``` syntax
pCmdList->SetComputeRoot32BitConstant(0,seed); // 0 is the parameter index, seed is used by the shaders
```

## <a name="adding-a-root-constant-buffer-view"></a><span data-ttu-id="576bd-123">加入根常數緩衝區視圖</span><span class="sxs-lookup"><span data-stu-id="576bd-123">Adding a root Constant Buffer View</span></span>

![將常數緩衝區視圖新增至根簽章](images/root-tables-cbv.png)

<span data-ttu-id="576bd-125">此範例顯示兩個根常數，而根常數緩衝區視圖 (CBV 成本為兩個 DWORD 位置的) 。</span><span class="sxs-lookup"><span data-stu-id="576bd-125">This example shows two root constants, and a root Constant Buffer View (CBV) that costs two DWORD slots.</span></span>

<span data-ttu-id="576bd-126">若要系結常數緩衝區視圖，請使用下列命令：</span><span class="sxs-lookup"><span data-stu-id="576bd-126">To bind a constant buffer view use a command such as the following.</span></span> <span data-ttu-id="576bd-127">請注意，第一個參數 (2) 是影像中所顯示的位置。</span><span class="sxs-lookup"><span data-stu-id="576bd-127">Note the first parameter (2) is the slot shown in the image.</span></span> <span data-ttu-id="576bd-128">通常會設定常數陣列，然後以 CBV 形式提供給 b0 的著色器。</span><span class="sxs-lookup"><span data-stu-id="576bd-128">Typically an array of constants will be set up and then made available to the shaders at b0 as a CBV.</span></span>

``` syntax
pCmdList->SetGraphicsRootConstantBufferView(2,GPUVAForCurrDynamicConstants);
```

## <a name="binding-descriptor-tables"></a><span data-ttu-id="576bd-129">系結描述中繼資料表</span><span class="sxs-lookup"><span data-stu-id="576bd-129">Binding descriptor tables</span></span>

![將描述中繼資料表新增至根簽章](images/root-tables-2.png)

<span data-ttu-id="576bd-131">此範例示範如何使用兩個描述中繼資料表;其中一個宣告可在執行時間于 CBV SRV UAV 描述元堆積中使用的五個描述項的資料表 \_ \_ ，以及另一個宣告兩個描述項的資料表，這些描述項將在執行時間于取樣器描述元堆積中顯示。</span><span class="sxs-lookup"><span data-stu-id="576bd-131">This example shows the use of two descriptor tables; one declaring a table of five descriptors that will be available at execution time in a CBV\_SRV\_UAV descriptor heap, and another declaring a table of two descriptors that will show up at execution time in a sampler descriptor heap.</span></span>

<span data-ttu-id="576bd-132">在記錄命令清單時系結描述項資料表。</span><span class="sxs-lookup"><span data-stu-id="576bd-132">To bind descriptor tables when recording a command list.</span></span>

``` syntax
pCmdList->SetComputeRootDescriptorTable(1, handleToCurrentMaterialDataInHeap);
pCmdList->SetComputeRootDescriptorTable(2, handleToCurrentMaterialDataInSamplerHeap);
```

<span data-ttu-id="576bd-133">根簽章的另一項功能是 float4 的根常數，大小為四個 DWORD。</span><span class="sxs-lookup"><span data-stu-id="576bd-133">Another feature of the root signature is the float4 root constant that is four DWORDS in size.</span></span> <span data-ttu-id="576bd-134">下列命令只會系結四的中間兩個 DWORD。</span><span class="sxs-lookup"><span data-stu-id="576bd-134">The following command binds just the middle two DWORDS of the four.</span></span>

``` syntax
pCmdList->SetComputeRoot32BitConstants(0,2,myFloat2Array,1);  // 2 constants starting at offset 1 (middle 2 values in float4)
```

## <a name="a-more-complex-root-signature"></a><span data-ttu-id="576bd-135">更複雜的根簽章</span><span class="sxs-lookup"><span data-stu-id="576bd-135">A more complex root signature</span></span>

![具有許多元素的複雜根簽章](images/root-tables-3.png)

<span data-ttu-id="576bd-137">此範例顯示具有大部分專案類型的密集根簽章。</span><span class="sxs-lookup"><span data-stu-id="576bd-137">This example shows a dense root signature with most types of entries.</span></span> <span data-ttu-id="576bd-138">兩個描述項資料表 (在插槽3和 6) 包含未系結的大小陣列。</span><span class="sxs-lookup"><span data-stu-id="576bd-138">Two of the descriptor tables (at slots 3 and 6) include unbounded size arrays.</span></span> <span data-ttu-id="576bd-139">這裡的負擔在於應用程式只能在堆積中接觸有效的描述項。</span><span class="sxs-lookup"><span data-stu-id="576bd-139">The burden here is on the application to only touch valid descriptors in a heap.</span></span> <span data-ttu-id="576bd-140">無限制或非常大型的陣列，需要硬體層 2 + 資源系結支援。</span><span class="sxs-lookup"><span data-stu-id="576bd-140">Unbounded, or very large arrays, require hardware tier 2+ of resource binding support.</span></span>

<span data-ttu-id="576bd-141">有兩個靜態取樣器 (系結，而不需要) 的根簽章位置。</span><span class="sxs-lookup"><span data-stu-id="576bd-141">There are two static samplers (bound without requiring root signature slots).</span></span>

<span data-ttu-id="576bd-142">在插槽9，UAV u4 和 UAV u5 是在相同的描述項資料表位移中宣告。</span><span class="sxs-lookup"><span data-stu-id="576bd-142">At slot 9, UAV u4 and UAV u5 are declared at the same descriptor table offset.</span></span> <span data-ttu-id="576bd-143">這是使用別名描述項，記憶體中的一個描述項在 HLSL 著色器中會顯示為 u4 和 u5。</span><span class="sxs-lookup"><span data-stu-id="576bd-143">This is use of an aliased descriptor, one descriptor in memory will show up as both u4 and u5 in the HLSL shaders.</span></span> <span data-ttu-id="576bd-144">在此情況下，必須使用 D3D10 \_ 著色器資源的 \_ \_ \_ 別名選項或 `/res_may_alias` fxc.exe 中的或選項來編譯著色器。</span><span class="sxs-lookup"><span data-stu-id="576bd-144">In this case the shader must be compiled with the D3D10\_SHADER\_RESOURCES\_MAY\_ALIAS option, or the or `/res_may_alias` option in FXC.</span></span> <span data-ttu-id="576bd-145">別名描述項可讓一個描述元系結至多個系結點，而不需要對著色器進行任何變更。</span><span class="sxs-lookup"><span data-stu-id="576bd-145">Aliased descriptors enable one descriptor to be bound to multiple bind points, without having to make any changes to the shaders.</span></span>

## <a name="streaming-shader-resource-views"></a><span data-ttu-id="576bd-146">串流著色器資源檢視</span><span class="sxs-lookup"><span data-stu-id="576bd-146">Streaming Shader Resource Views</span></span>

![此根簽章中的串流著色器資源瀏覽器](images/root-tables-4.png)

<span data-ttu-id="576bd-148">此根簽章說明將所有 SRVs 流入和移出一個大型陣列的案例。</span><span class="sxs-lookup"><span data-stu-id="576bd-148">This root signature illustrates a scenario where all SRVs are streamed in and out of one large array.</span></span> <span data-ttu-id="576bd-149">在執行時間，當設定根簽章時，可以設定描述中繼資料表一次。</span><span class="sxs-lookup"><span data-stu-id="576bd-149">At execution time, a descriptor table can be set once when the root signature is set.</span></span> <span data-ttu-id="576bd-150">然後透過前幾個根引數所送出的常數，在陣列中編制所有材質讀取的功能。</span><span class="sxs-lookup"><span data-stu-id="576bd-150">Then all texture reads are done by indexing into the array via constants fed via the first few root arguments.</span></span> <span data-ttu-id="576bd-151">只需要單一描述元堆積，而且只會在有可用的描述項位置或流出紋理時進行更新。</span><span class="sxs-lookup"><span data-stu-id="576bd-151">Only a single descriptor heap is needed, and is only updated as textures are streamed in or out of free descriptor slots.</span></span>

<span data-ttu-id="576bd-152">大型堆積中的描述項位移是使用常數緩衝區視圖中的常數，以著色器來識別。</span><span class="sxs-lookup"><span data-stu-id="576bd-152">The descriptor offsets in the large heap are identified by shaders using the constants in the Constant Buffer Views.</span></span> <span data-ttu-id="576bd-153">例如，如果為著色器指定了材質識別碼，它可以使用常數來索引至一個大型陣列，以存取所需的描述項 (參考所需的材質) 。</span><span class="sxs-lookup"><span data-stu-id="576bd-153">For example, if a shader is given a material ID, it can index into the one large array using the constant to access the required descriptor (which references the required texture).</span></span>

<span data-ttu-id="576bd-154">此案例需要具有資源系結第2層 + 的硬體。</span><span class="sxs-lookup"><span data-stu-id="576bd-154">This scenario requires hardware with resource binding tier2+.</span></span>

## <a name="related-topics"></a><span data-ttu-id="576bd-155">相關主題</span><span class="sxs-lookup"><span data-stu-id="576bd-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="576bd-156">資源系結硬體層</span><span class="sxs-lookup"><span data-stu-id="576bd-156">Resource Binding Hardware Tiers</span></span>](hardware-support.md)
</dt> <dt>

[<span data-ttu-id="576bd-157">HLSL 中的資源系結</span><span class="sxs-lookup"><span data-stu-id="576bd-157">Resource Binding in HLSL</span></span>](resource-binding-in-hlsl.md)
</dt> <dt>

[<span data-ttu-id="576bd-158">根簽章</span><span class="sxs-lookup"><span data-stu-id="576bd-158">Root Signatures</span></span>](root-signatures.md)
</dt> </dl>

 

 




