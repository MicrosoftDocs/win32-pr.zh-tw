---
title: 'dcl_interface_dynamicindexed (sm5-asm) '
description: ')  (介面宣告函數資料表指標。 |dcl_interface_dynamicindexed (sm5-asm) '
ms.assetid: 5C77EBB6-7AEC-4471-AA6E-0F6D3E215156
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f78bb0152b44f7e29b9e76221db13da0c465a434
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104992070"
---
# <a name="dcl_interface_dynamicindexed-sm5---asm"></a><span data-ttu-id="d0c62-104">dcl \_ 介面 \_ dynamicindexed (sm5-asm) </span><span class="sxs-lookup"><span data-stu-id="d0c62-104">dcl\_interface\_dynamicindexed (sm5 - asm)</span></span>

<span data-ttu-id="d0c62-105">)  (介面宣告函數資料表指標。</span><span class="sxs-lookup"><span data-stu-id="d0c62-105">Declare function table pointers (interfaces).</span></span>



| <span data-ttu-id="d0c62-106">dcl \_ 介面 \_ dynamicindexed fp \# \[ arraySize \] \[ numCallSites \] = {ft \# ，ft \# ，...}</span><span class="sxs-lookup"><span data-stu-id="d0c62-106">dcl\_interface\_dynamicindexed fp\#\[arraySize\]\[numCallSites\] = {ft\#, ft\#, ...}</span></span> |
|--------------------------------------------------------------------------------------|



 



| <span data-ttu-id="d0c62-107">項目</span><span class="sxs-lookup"><span data-stu-id="d0c62-107">Item</span></span>                                                          | <span data-ttu-id="d0c62-108">描述</span><span class="sxs-lookup"><span data-stu-id="d0c62-108">Description</span></span>                                    |
|---------------------------------------------------------------|------------------------------------------------|
| <span data-ttu-id="d0c62-109"><span id="fp_"></span><span id="FP_"></span>*Fp\#*</span><span class="sxs-lookup"><span data-stu-id="d0c62-109"><span id="fp_"></span><span id="FP_"></span>*fp\#*</span></span><br/> | <span data-ttu-id="d0c62-110">\[在 \] 函數資料表指標中。</span><span class="sxs-lookup"><span data-stu-id="d0c62-110">\[in\] The function table pointers.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d0c62-111">備註</span><span class="sxs-lookup"><span data-stu-id="d0c62-111">Remarks</span></span>

<span data-ttu-id="d0c62-112">每個介面都必須先從 API 系結，才能使用著色器。</span><span class="sxs-lookup"><span data-stu-id="d0c62-112">Each interface needs to be bound from the API before the shader is usable.</span></span> <span data-ttu-id="d0c62-113">系結會提供其中一個函式資料表的參考，以便填入方法位置。</span><span class="sxs-lookup"><span data-stu-id="d0c62-113">Binding gives a reference to one of the function tables so that the method slots can be filled in.</span></span> <span data-ttu-id="d0c62-114">編譯器不會產生未參考物件的指標。</span><span class="sxs-lookup"><span data-stu-id="d0c62-114">The compiler will not generate pointers for unreferenced objects.</span></span>

<span data-ttu-id="d0c62-115">函式資料表指標有一組完整的方法位置，可避免 c + + 指標點對點標記法需要的額外間接取值層級。</span><span class="sxs-lookup"><span data-stu-id="d0c62-115">A function table pointer has a full set of method slots to avoid the extra level of indirection that a C++ pointer-to- pointer-to-vtable representation would require.</span></span> <span data-ttu-id="d0c62-116">這也需要此指標為5元組。</span><span class="sxs-lookup"><span data-stu-id="d0c62-116">That would also require that this pointers be 5-tuples.</span></span> <span data-ttu-id="d0c62-117">在 HLSL 虛擬內嵌模型中，一律會知道用於呼叫的全域變數/輸入，因此我們可以為每個根物件設定資料表。</span><span class="sxs-lookup"><span data-stu-id="d0c62-117">In the HLSL virtual inlining model it's always known what global variable/input is used for a call so we can set up tables per root object.</span></span>

<span data-ttu-id="d0c62-118">函式指標宣告指出哪些函數資料表可搭配使用。</span><span class="sxs-lookup"><span data-stu-id="d0c62-118">Function pointer declarations indicate which function tables are legal to use with them.</span></span> <span data-ttu-id="d0c62-119">這也允許衍生方法相互關聯資訊。</span><span class="sxs-lookup"><span data-stu-id="d0c62-119">This also allows derivation of method correlation information.</span></span>

<span data-ttu-id="d0c62-120">介面宣告的第一個 \[ \] 是陣列大小。</span><span class="sxs-lookup"><span data-stu-id="d0c62-120">The first \[\] of an interface declaration is the array size.</span></span> <span data-ttu-id="d0c62-121">如果使用動態索引，宣告將會指出，如下所示。</span><span class="sxs-lookup"><span data-stu-id="d0c62-121">If dynamic indexing is used the declaration will indicate that as shown.</span></span> <span data-ttu-id="d0c62-122">介面指標的陣列也可以靜態地編制索引，而介面指標的陣列則不需要表示動態索引。</span><span class="sxs-lookup"><span data-stu-id="d0c62-122">An array of interface pointers can be indexed statically also, it is not required that arrays of interface pointers mean dynamic indexing.</span></span>

<span data-ttu-id="d0c62-123">介面指標的編號是從0開始，第一個宣告，接著將陣列大小變成帳戶，因此第一個指標在四個專案陣列 fp0 4 個專案之後， \[ \] \[ \] 就會 fp4 \[ \] \[ \] 。</span><span class="sxs-lookup"><span data-stu-id="d0c62-123">Numbering of interface pointers starts at 0 for the first declaration and subsequently takes array size into account, so the first pointer after a four entry array fp0\[4\]\[1\] would be fp4\[\]\[\].</span></span>

<span data-ttu-id="d0c62-124">介面宣告的第二個 \[ \] 是呼叫位置的數目，必須符合宣告中所參考之每個資料表內的主體數目。</span><span class="sxs-lookup"><span data-stu-id="d0c62-124">The second \[\] of an interface declaration is the number of call sites, which must match the number of bodies in each table referenced in the declaration.</span></span>

<span data-ttu-id="d0c62-125">介面宣告中可能會列出多個函式資料表 (ft \#) 選項的界限。</span><span class="sxs-lookup"><span data-stu-id="d0c62-125">There are no bounds to how many function table (ft\#) choices can be listed in an interface declaration.</span></span>

<span data-ttu-id="d0c62-126">給定的函式資料表 (ft \#) 可以在一個或多個介面宣告中出現一次以上。</span><span class="sxs-lookup"><span data-stu-id="d0c62-126">A given function table (ft\#) can appear more than once in one or more interface declarations.</span></span>

### <a name="restrictions"></a><span data-ttu-id="d0c62-127">限制</span><span class="sxs-lookup"><span data-stu-id="d0c62-127">Restrictions</span></span>

-   <span data-ttu-id="d0c62-128">著色器中的物件網站數目是其 arraySize 宣告之所有 *fp \#* 宣告的總和 \[ \] ，必須不超過253。</span><span class="sxs-lookup"><span data-stu-id="d0c62-128">The number of object sites in a shader, which is the sum across all *fp\#* declarations of their \[arraySize\] declarations, must be no more than 253.</span></span> <span data-ttu-id="d0c62-129">此數位對應到可出現 **的指標數目** 。</span><span class="sxs-lookup"><span data-stu-id="d0c62-129">This number corresponds to how many **this** pointers can be present.</span></span> <span data-ttu-id="d0c62-130">執行時間會強制執行這項253限制，以保持與 DDI 的大小系結，以傳達此指標資料。</span><span class="sxs-lookup"><span data-stu-id="d0c62-130">The runtime enforces this 253 limit to keep a bound on the size of the DDI for communicating this pointer data.</span></span>
-   <span data-ttu-id="d0c62-131">著色器中的呼叫位置數，也就是可能分支目標數目之所有 fcall 語句的總和，不得超過4096。</span><span class="sxs-lookup"><span data-stu-id="d0c62-131">The number of call sites in a shader, which is the sum across all fcall statements of the number of potential branch targets, must be no more than 4096.</span></span>

    <span data-ttu-id="d0c62-132">例如，針對第一個 *fp \[ \] \[ \]* 維度使用靜態索引的 [fcall](fcall--sm5---asm-.md)會計算為一個：</span><span class="sxs-lookup"><span data-stu-id="d0c62-132">For example, an [fcall](fcall--sm5---asm-.md) that uses a static index for the first *fp\[\]\[\]* dimension counts as one:</span></span>

    `                       fcall fp0[0][0]         // +1`

    <span data-ttu-id="d0c62-133">使用動態索引的 **fcall** 會計算為數組中的元素數目， (第一個 \[ \]) 的 **dcl \_ 介面**：</span><span class="sxs-lookup"><span data-stu-id="d0c62-133">An **fcall** that uses a dynamic index counts as the number of elements in the array (first \[\] of **dcl\_interface**):</span></span>

    `                    dcl_interface_dynamicindexed fp1[2][1] = {ft2, ft3, ft4}                      ...                     `

    `fcall fp1[r0.z + 0][1]  // +2`

    <span data-ttu-id="d0c62-134">這項限制可協助某些實作為在常數類似緩衝區的儲存體中，輕鬆地容納函式主體選取的資料表。</span><span class="sxs-lookup"><span data-stu-id="d0c62-134">This limit helps some implementations easily fit tables of function body selections in constant buffer-like storage.</span></span>

<span data-ttu-id="d0c62-135">此指示適用于下列著色器階段：</span><span class="sxs-lookup"><span data-stu-id="d0c62-135">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="d0c62-136">頂點</span><span class="sxs-lookup"><span data-stu-id="d0c62-136">Vertex</span></span> | <span data-ttu-id="d0c62-137">船體</span><span class="sxs-lookup"><span data-stu-id="d0c62-137">Hull</span></span> | <span data-ttu-id="d0c62-138">網域</span><span class="sxs-lookup"><span data-stu-id="d0c62-138">Domain</span></span> | <span data-ttu-id="d0c62-139">幾何</span><span class="sxs-lookup"><span data-stu-id="d0c62-139">Geometry</span></span> | <span data-ttu-id="d0c62-140">像素</span><span class="sxs-lookup"><span data-stu-id="d0c62-140">Pixel</span></span> | <span data-ttu-id="d0c62-141">計算</span><span class="sxs-lookup"><span data-stu-id="d0c62-141">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="d0c62-142">X</span><span class="sxs-lookup"><span data-stu-id="d0c62-142">X</span></span>      | <span data-ttu-id="d0c62-143">X</span><span class="sxs-lookup"><span data-stu-id="d0c62-143">X</span></span>    | <span data-ttu-id="d0c62-144">X</span><span class="sxs-lookup"><span data-stu-id="d0c62-144">X</span></span>      | <span data-ttu-id="d0c62-145">X</span><span class="sxs-lookup"><span data-stu-id="d0c62-145">X</span></span>        | <span data-ttu-id="d0c62-146">X</span><span class="sxs-lookup"><span data-stu-id="d0c62-146">X</span></span>     | <span data-ttu-id="d0c62-147">X</span><span class="sxs-lookup"><span data-stu-id="d0c62-147">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="d0c62-148">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="d0c62-148">Minimum Shader Model</span></span>

<span data-ttu-id="d0c62-149">下列著色器模型支援此指令：</span><span class="sxs-lookup"><span data-stu-id="d0c62-149">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="d0c62-150">著色器模型</span><span class="sxs-lookup"><span data-stu-id="d0c62-150">Shader Model</span></span>                                              | <span data-ttu-id="d0c62-151">支援</span><span class="sxs-lookup"><span data-stu-id="d0c62-151">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="d0c62-152">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="d0c62-152">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="d0c62-153">是</span><span class="sxs-lookup"><span data-stu-id="d0c62-153">yes</span></span>       |
| [<span data-ttu-id="d0c62-154">著色器模型4。1</span><span class="sxs-lookup"><span data-stu-id="d0c62-154">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="d0c62-155">不可以</span><span class="sxs-lookup"><span data-stu-id="d0c62-155">no</span></span>        |
| [<span data-ttu-id="d0c62-156">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="d0c62-156">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="d0c62-157">不可以</span><span class="sxs-lookup"><span data-stu-id="d0c62-157">no</span></span>        |
| [<span data-ttu-id="d0c62-158">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="d0c62-158">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="d0c62-159">不可以</span><span class="sxs-lookup"><span data-stu-id="d0c62-159">no</span></span>        |
| [<span data-ttu-id="d0c62-160">著色器模型 2 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="d0c62-160">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="d0c62-161">不可以</span><span class="sxs-lookup"><span data-stu-id="d0c62-161">no</span></span>        |
| [<span data-ttu-id="d0c62-162">著色器模型 1 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="d0c62-162">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="d0c62-163">不可以</span><span class="sxs-lookup"><span data-stu-id="d0c62-163">no</span></span>        |



 

<span data-ttu-id="d0c62-164">cs \_ 4 \_ 0 和 cs \_ 4 \_ 1 支援此 UAV 和 SRV 指令。</span><span class="sxs-lookup"><span data-stu-id="d0c62-164">cs\_4\_0 and cs\_4\_1 support this instruction for UAV and SRV.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d0c62-165">相關主題</span><span class="sxs-lookup"><span data-stu-id="d0c62-165">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d0c62-166">著色器模型5元件 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="d0c62-166">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





