---
title: 著色器常數 (HLSL)
description: 在著色器模型4中，著色器常數會儲存在記憶體中的一或多個緩衝區資源中。
ms.assetid: 89fe874a-8009-4901-bebe-2d9e45f894bb
keywords:
- cbuffer
- tbuffer
- 常數緩衝區
- 材質緩衝區
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a1b78da747a248bf4bb5774add1bf97f14f048c4
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "103685390"
---
# <a name="shader-constants-hlsl"></a><span data-ttu-id="e1423-107">著色器常數 (HLSL)</span><span class="sxs-lookup"><span data-stu-id="e1423-107">Shader Constants (HLSL)</span></span>

<span data-ttu-id="e1423-108">在著色器模型4中，著色器常數會儲存在記憶體中的一或多個緩衝區資源中。</span><span class="sxs-lookup"><span data-stu-id="e1423-108">In Shader Model 4, shader constants are stored in one or more buffer resources in memory.</span></span> <span data-ttu-id="e1423-109">它們可以組織成兩種類型的緩衝區：常數緩衝區 (cbuffers) 和材質緩衝區 (tbuffers) 。</span><span class="sxs-lookup"><span data-stu-id="e1423-109">They can be organized into two types of buffers: constant buffers (cbuffers) and texture buffers (tbuffers).</span></span> <span data-ttu-id="e1423-110">常數緩衝區最適合用於常數變數的使用方式，其以較低延遲的存取和 CPU 較頻繁的更新為特徵。</span><span class="sxs-lookup"><span data-stu-id="e1423-110">Constant buffers are optimized for constant-variable usage, which is characterized by lower-latency access and more frequent update from the CPU.</span></span> <span data-ttu-id="e1423-111">基於這個理由，其他大小、配置和存取限制適用于這些資源。</span><span class="sxs-lookup"><span data-stu-id="e1423-111">For this reason, additional size, layout, and access restrictions apply to these resources.</span></span> <span data-ttu-id="e1423-112">紋理緩衝區會像材質一樣存取，並針對任意索引的資料執行得更好。</span><span class="sxs-lookup"><span data-stu-id="e1423-112">Texture buffers are accessed like textures and perform better for arbitrarily indexed data.</span></span> <span data-ttu-id="e1423-113">無論您使用哪種類型的資源，應用程式可以建立的常數緩衝區或紋理緩衝區數目沒有任何限制。</span><span class="sxs-lookup"><span data-stu-id="e1423-113">Regardless of which type of resource you use, there is no limit to the number of constant buffers or texture buffers an application can create.</span></span>

<span data-ttu-id="e1423-114">宣告常數緩衝區或紋理緩衝區看起來很像 C 中的結構宣告，而是新增 **register** 和 **packoffset** 關鍵字以手動指派暫存器或封裝資料。</span><span class="sxs-lookup"><span data-stu-id="e1423-114">Declaring a constant buffer or a texture buffer looks very much like a structure declaration in C, with the addition of the **register** and **packoffset** keywords for manually assigning registers or packing data.</span></span>



|                                                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1423-115">*BufferType* \[*名稱* \]\[： **register** (b \#) \] { *VariableDeclaration* \[ ： **packoffset** (c. \# xyzw) \] ;     ... };</span><span class="sxs-lookup"><span data-stu-id="e1423-115">*BufferType* \[*Name*\] \[: **register**(b\#)\] {     *VariableDeclaration* \[: **packoffset**(c\#.xyzw)\];      ... };</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="e1423-116">參數</span><span class="sxs-lookup"><span data-stu-id="e1423-116">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1423-117"><span id="BufferType"></span><span id="buffertype"></span><span id="BUFFERTYPE"></span>*BufferType*</span><span class="sxs-lookup"><span data-stu-id="e1423-117"><span id="BufferType"></span><span id="buffertype"></span><span id="BUFFERTYPE"></span>*BufferType*</span></span>
</dt> <dd>

<span data-ttu-id="e1423-118">\[在 \] 緩衝區類型中。</span><span class="sxs-lookup"><span data-stu-id="e1423-118">\[in\] The buffer type.</span></span>



| <span data-ttu-id="e1423-119">BufferType</span><span class="sxs-lookup"><span data-stu-id="e1423-119">BufferType</span></span> | <span data-ttu-id="e1423-120">Description</span><span class="sxs-lookup"><span data-stu-id="e1423-120">Description</span></span>     |
|------------|-----------------|
| <span data-ttu-id="e1423-121">cbuffer</span><span class="sxs-lookup"><span data-stu-id="e1423-121">cbuffer</span></span>    | <span data-ttu-id="e1423-122">常數緩衝區</span><span class="sxs-lookup"><span data-stu-id="e1423-122">constant buffer</span></span> |
| <span data-ttu-id="e1423-123">tbuffer</span><span class="sxs-lookup"><span data-stu-id="e1423-123">tbuffer</span></span>    | <span data-ttu-id="e1423-124">材質緩衝區</span><span class="sxs-lookup"><span data-stu-id="e1423-124">texture buffer</span></span>  |



 

</dd> <dt>

<span data-ttu-id="e1423-125"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*名字*</span><span class="sxs-lookup"><span data-stu-id="e1423-125"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Name*</span></span>
</dt> <dd>

<span data-ttu-id="e1423-126">\[\]（選擇性）包含唯一緩衝區名稱的 ASCII 字串。</span><span class="sxs-lookup"><span data-stu-id="e1423-126">\[in\] Optional, ASCII string containing a unique buffer name.</span></span>

</dd> <dt>

<span data-ttu-id="e1423-127"><span id="register_b__"></span><span id="REGISTER_B__"></span>**註冊** (b \#) </span><span class="sxs-lookup"><span data-stu-id="e1423-127"><span id="register_b__"></span><span id="REGISTER_B__"></span>**register**(b\#)</span></span>
</dt> <dd>

<span data-ttu-id="e1423-128">\[\]使用選擇性的關鍵字，用來手動封裝常數資料。</span><span class="sxs-lookup"><span data-stu-id="e1423-128">\[in\] Optional keyword, used to manually pack constant data.</span></span> <span data-ttu-id="e1423-129">常數只能在常數緩衝區中封裝于暫存器中，而在此情況下， () 的暫存器編號會提供開始登錄 *\#* 。</span><span class="sxs-lookup"><span data-stu-id="e1423-129">Constants can be packed in a register only in a constant buffer, where the starting register is given by the register number (*\#*).</span></span>

</dd> <dt>

<span data-ttu-id="e1423-130"><span id="VariableDeclaration"></span><span id="variabledeclaration"></span><span id="VARIABLEDECLARATION"></span>*VariableDeclaration*</span><span class="sxs-lookup"><span data-stu-id="e1423-130"><span id="VariableDeclaration"></span><span id="variabledeclaration"></span><span id="VARIABLEDECLARATION"></span>*VariableDeclaration*</span></span>
</dt> <dd>

<span data-ttu-id="e1423-131">\[在 \] 變數宣告中，類似于結構成員宣告。</span><span class="sxs-lookup"><span data-stu-id="e1423-131">\[in\] Variable declaration, similar to a structure member declaration.</span></span> <span data-ttu-id="e1423-132">這可以是任何 HLSL 類型或效果物件 (但) 的材質或取樣器物件除外。</span><span class="sxs-lookup"><span data-stu-id="e1423-132">This can be any HLSL type or effect object (except a texture or a sampler object).</span></span>

</dd> <dt>

<span data-ttu-id="e1423-133"><span id="packoffset_c_.xyzw_"></span><span id="PACKOFFSET_C_.XYZW_"></span>**packoffset** (c. \# xyzw) </span><span class="sxs-lookup"><span data-stu-id="e1423-133"><span id="packoffset_c_.xyzw_"></span><span id="PACKOFFSET_C_.XYZW_"></span>**packoffset**(c\#.xyzw)</span></span>
</dt> <dd>

<span data-ttu-id="e1423-134">\[\]使用選擇性的關鍵字，用來手動封裝常數資料。</span><span class="sxs-lookup"><span data-stu-id="e1423-134">\[in\] Optional keyword, used to manually pack constant data.</span></span> <span data-ttu-id="e1423-135">常數可以封裝在任何常數緩衝區中，其中的暫存器編號是由 (*\#*) 指定。</span><span class="sxs-lookup"><span data-stu-id="e1423-135">Constants can be packed in any constant buffer, where the register number is given by (*\#*).</span></span> <span data-ttu-id="e1423-136">使用 xyzw swizzling) 的子元件封裝 (可用於大小符合單一登入 (不會跨越暫存器界限) 的常數。</span><span class="sxs-lookup"><span data-stu-id="e1423-136">Sub-component packing (using xyzw swizzling) is available for constants whose size fit within a single register (do not cross a register boundary).</span></span> <span data-ttu-id="e1423-137">比方說，float4 無法封裝在開頭為 y 元件的單一登入中，因為它無法容納在四個元件的暫存器中。</span><span class="sxs-lookup"><span data-stu-id="e1423-137">For instance, a float4 could not be packed in a single register starting with the y-component because it would not fit in a four-component register.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e1423-138">備註</span><span class="sxs-lookup"><span data-stu-id="e1423-138">Remarks</span></span>

<span data-ttu-id="e1423-139">常數緩衝區透過允許著色器常數群組在一起並且同時認可，而不是進行個別呼叫以分別認可每一個常數，來減少更新著色器常數所需的頻寬。</span><span class="sxs-lookup"><span data-stu-id="e1423-139">Constant buffers reduce the bandwidth required to update shader constants by allowing shader constants to be grouped together and committed at the same time rather than making individual calls to commit each constant separately.</span></span>

<span data-ttu-id="e1423-140">常數緩衝區是像緩衝區一樣存取的特製化緩衝區資源。</span><span class="sxs-lookup"><span data-stu-id="e1423-140">A constant buffer is a specialized buffer resource that is accessed like a buffer.</span></span> <span data-ttu-id="e1423-141">每個常數緩衝區最多可容納4096個 [向量](dx-graphics-hlsl-vector.md);每個向量最多包含 4 32 位值。</span><span class="sxs-lookup"><span data-stu-id="e1423-141">Each constant buffer can hold up to 4096 [vectors](dx-graphics-hlsl-vector.md); each vector contains up to four 32-bit values.</span></span> <span data-ttu-id="e1423-142">您最多可以在每個管線階段系結14個常數緩衝區 (2 個額外的插槽保留供內部使用) 。</span><span class="sxs-lookup"><span data-stu-id="e1423-142">You can bind up to 14 constant buffers per pipeline stage (2 additional slots are reserved for internal use).</span></span>

<span data-ttu-id="e1423-143">材質緩衝區是以材質形式存取的特製化緩衝區資源。</span><span class="sxs-lookup"><span data-stu-id="e1423-143">A texture buffer is a specialized buffer resource that is accessed like a texture.</span></span> <span data-ttu-id="e1423-144">材質存取 (相較于緩衝區存取，) 可為任意索引的資料提供更好的效能。</span><span class="sxs-lookup"><span data-stu-id="e1423-144">Texture access (as compared with buffer access) can have better performance for arbitrarily indexed data.</span></span> <span data-ttu-id="e1423-145">您最多可以為每個管線階段系結128紋理緩衝區。</span><span class="sxs-lookup"><span data-stu-id="e1423-145">You can bind up to 128 texture buffers per pipeline stage.</span></span>

<span data-ttu-id="e1423-146">緩衝區資源的設計目的是要將設定著色器常數的額外負荷降到最低。</span><span class="sxs-lookup"><span data-stu-id="e1423-146">A buffer resource is designed to minimize the overhead of setting shader constants.</span></span> <span data-ttu-id="e1423-147">效果架構 (查看 [**ID3D10Effect 介面**](/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effect)) 將會管理更新常數和材質緩衝區，或您可以使用 direct3d API 來更新緩衝區 (如需資訊) ，請參閱 [複製和存取資源資料 (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-mapping) 。</span><span class="sxs-lookup"><span data-stu-id="e1423-147">The effect framework (see [**ID3D10Effect Interface**](/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effect)) will manage updating constant and texture buffers, or you can use the Direct3D API to update buffers (see [Copying and Accessing Resource Data (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-mapping) for information).</span></span> <span data-ttu-id="e1423-148">應用程式也可以將資料從另一個緩衝區 (例如轉譯目標或資料流程輸出目標) 複製到常數緩衝區。</span><span class="sxs-lookup"><span data-stu-id="e1423-148">An application can also copy data from another buffer (such as a render target or a stream-output target) into a constant buffer.</span></span>

<span data-ttu-id="e1423-149">如需在 D3D10 應用程式中使用常數緩衝區的詳細資訊，請參閱 [ (direct3d 10) 的資源類型 ](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) ，以及 [ (Direct3d 10) 建立緩衝區資源 ](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-creating)。</span><span class="sxs-lookup"><span data-stu-id="e1423-149">For more info on using constant buffers in a D3D10 application, see [Resource Types (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) and [Creating Buffer Resources (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-creating).</span></span>

<span data-ttu-id="e1423-150">如需在 D3D11 應用程式中使用常數緩衝區的 morel 資訊，請參閱 [Direct3D 11 中的緩衝區簡介](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-intro) 和 [如何：建立常數緩衝區](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-constant-how-to)。</span><span class="sxs-lookup"><span data-stu-id="e1423-150">For morel info on using constant buffers in a D3D11 application, see [Introduction to Buffers in Direct3D 11](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-intro) and [How to: Create a Constant Buffer](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-constant-how-to).</span></span>

<span data-ttu-id="e1423-151">常數緩衝區不需要將 [view](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-access-views) 系結至管線。</span><span class="sxs-lookup"><span data-stu-id="e1423-151">A constant buffer does not require a [view](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-access-views) to be bound to the pipeline.</span></span> <span data-ttu-id="e1423-152">不過，材質緩衝區需要一個視圖，而且必須系結至材質位置 (或在使用效果) 時必須與 [**SetTextureBuffer**](/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effectconstantbuffer-settexturebuffer) 系結。</span><span class="sxs-lookup"><span data-stu-id="e1423-152">A texture buffer, however, requires a view and must be bound to a texture slot (or must be bound with [**SetTextureBuffer**](/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effectconstantbuffer-settexturebuffer) when using an effect).</span></span>

<span data-ttu-id="e1423-153">有兩種方式可以封裝常數資料：使用 [register (DIRECTX HLSL) ](dx-graphics-hlsl-variable-register.md) 和 [PACKOFFSET (directx HLSL) ](dx-graphics-hlsl-variable-packoffset.md) 關鍵字。</span><span class="sxs-lookup"><span data-stu-id="e1423-153">There are two ways to pack constants data: using the [register (DirectX HLSL)](dx-graphics-hlsl-variable-register.md) and [packoffset (DirectX HLSL)](dx-graphics-hlsl-variable-packoffset.md) keywords.</span></span>



|                                                                                                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1423-154">Direct3D 9 與 Direct3D 10 和11之間的差異：</span><span class="sxs-lookup"><span data-stu-id="e1423-154">Differences between Direct3D 9 and Direct3D 10 and 11:</span></span><br/> <span data-ttu-id="e1423-155">不同于 Direct3D 9 中未執行封裝，而改為將每個變數指派給一組 float4 暫存器的常數的自動設定，HLSL 常數變數在 Direct3D 10 和11中遵循封裝規則。</span><span class="sxs-lookup"><span data-stu-id="e1423-155">Unlike the auto-allocation of constants in Direct3D 9, which did not perform packing and instead assigned each variable to a set of float4 registers, HLSL constant variables follow packing rules in Direct3D 10 and 11.</span></span><br/> |



 

### <a name="organizing-constant-buffers"></a><span data-ttu-id="e1423-156">組織常數緩衝區</span><span class="sxs-lookup"><span data-stu-id="e1423-156">Organizing constant buffers</span></span>

<span data-ttu-id="e1423-157">常數緩衝區透過允許著色器常數群組在一起並且同時認可，而不是進行個別呼叫以分別認可每一個常數，來減少更新著色器常數所需的頻寬。</span><span class="sxs-lookup"><span data-stu-id="e1423-157">Constant buffers reduce the bandwidth required to update shader constants by allowing shader constants to be grouped together and committed at the same time rather than making individual calls to commit each constant separately.</span></span>

<span data-ttu-id="e1423-158">有效使用常數緩衝區的最佳方法是根據它們的更新頻率，將著色器變數組織到常數緩衝區。</span><span class="sxs-lookup"><span data-stu-id="e1423-158">The best way to efficiently use constant buffers is to organize shader variables into constant buffers based on their frequency of update.</span></span> <span data-ttu-id="e1423-159">這可讓應用程式將更新著色器常數所需的頻寬降至最低。</span><span class="sxs-lookup"><span data-stu-id="e1423-159">This allows an application to minimize the bandwidth required for updating shader constants.</span></span> <span data-ttu-id="e1423-160">例如，著色器可能會宣告兩個常數緩衝區，並根據更新的頻率來組織每個常數的資料：需要針對每個物件更新的資料 (例如世界矩陣) 會分組到可針對每個物件更新的常數緩衝區。</span><span class="sxs-lookup"><span data-stu-id="e1423-160">For example, a shader might declare two constant buffers and organize the data in each based on their frequency of update: data that needs to be updated on a per-object basis (like a world matrix) is grouped into a constant buffer which could be updated for each object.</span></span> <span data-ttu-id="e1423-161">這與場景的特性不同，因此可能會在場景變更) 時較不常更新 (。</span><span class="sxs-lookup"><span data-stu-id="e1423-161">This is separate from data that characterizes a scene and is therefore likely to be updated much less often (when the scene changes).</span></span>


```
cbuffer myObject
{       
    float4x4 matWorld;
    float3   vObjectPosition;
    int      arrayIndex;
}
 
cbuffer myScene
{
    float3   vSunPosition;
    float4x4 matView;
}
        
```



### <a name="default-constant-buffers"></a><span data-ttu-id="e1423-162">預設常數緩衝區</span><span class="sxs-lookup"><span data-stu-id="e1423-162">Default constant buffers</span></span>

<span data-ttu-id="e1423-163">有兩個預設的常數緩衝區可用，$Global 和 $Param。</span><span class="sxs-lookup"><span data-stu-id="e1423-163">There are two default constant buffers available, $Global and $Param.</span></span> <span data-ttu-id="e1423-164">放在全域範圍中的變數，會使用用於 cbuffers 的相同封裝方法，隱含地新增至 $Global cbuffer。</span><span class="sxs-lookup"><span data-stu-id="e1423-164">Variables that are placed in the global scope are added implicitly to the $Global cbuffer, using the same packing method that is used for cbuffers.</span></span> <span data-ttu-id="e1423-165">當著色器在效果架構之外編譯時，函式參數清單中的統一參數會出現在 $Param 常數緩衝區中。</span><span class="sxs-lookup"><span data-stu-id="e1423-165">Uniform parameters in the parameter list of a function appear in the $Param constant buffer when a shader is compiled outside of the effects framework.</span></span> <span data-ttu-id="e1423-166">在效果架構內進行編譯時，所有 uniforms 都必須解析為全域範圍中定義的變數。</span><span class="sxs-lookup"><span data-stu-id="e1423-166">When compiled inside the effects framework, all uniforms must resolve to variables defined in the global scope.</span></span>

## <a name="examples"></a><span data-ttu-id="e1423-167">範例</span><span class="sxs-lookup"><span data-stu-id="e1423-167">Examples</span></span>

<span data-ttu-id="e1423-168">以下是來自 [Skinning10 範例](https://msdn.microsoft.com/library/Ee416429(v=VS.85).aspx) 的範例，此範例是由矩陣陣列組成的材質緩衝區。</span><span class="sxs-lookup"><span data-stu-id="e1423-168">Here is an example from [Skinning10 Sample](https://msdn.microsoft.com/library/Ee416429(v=VS.85).aspx) that is a texture buffer made up of an array of matrices.</span></span>


```
tbuffer tbAnimMatrices
{
    matrix g_mTexBoneWorld[MAX_BONE_MATRICES];
};
      
```



<span data-ttu-id="e1423-169">這個範例宣告會手動指派常數緩衝區以從特定的暫存器開始，也會依子元件封裝特定的元素。</span><span class="sxs-lookup"><span data-stu-id="e1423-169">This example declaration manually assigns a constant buffer to start at a particular register, and also packs particular elements by subcomponents.</span></span>


```
cbuffer MyBuffer : register(b3)
{
    float4 Element1 : packoffset(c0);
    float1 Element2 : packoffset(c1);
    float1 Element3 : packoffset(c1.y);
}
      
```



## <a name="related-topics"></a><span data-ttu-id="e1423-170">相關主題</span><span class="sxs-lookup"><span data-stu-id="e1423-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1423-171">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="e1423-171">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

