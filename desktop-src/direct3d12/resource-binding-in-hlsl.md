---
title: HLSL 中的資源系結
description: 本主題說明使用高階著色器語言 (HLSL) 著色器模型5.1 與 Direct3D 12 的一些特定功能。
ms.assetid: 3CD4BDAD-8AE3-4DE0-B3F8-9C9F9E83BBE9
ms.localizationpriority: high
ms.topic: article
ms.date: 08/27/2019
ms.openlocfilehash: 711ccdee71ff916445be68d03b84b7621aa04cf3
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550383"
---
# <a name="resource-binding-in-hlsl"></a><span data-ttu-id="4f290-103">HLSL 中的資源系結</span><span class="sxs-lookup"><span data-stu-id="4f290-103">Resource binding in HLSL</span></span>

<span data-ttu-id="4f290-104">本主題說明使用高階著色器語言 (HLSL) [著色器模型 5.1](/windows/desktop/direct3dhlsl/shader-model-5-1) 與 Direct3D 12 的一些特定功能。</span><span class="sxs-lookup"><span data-stu-id="4f290-104">This topic describes some specific features of using High Level Shader Language (HLSL) [Shader Model 5.1](/windows/desktop/direct3dhlsl/shader-model-5-1) with Direct3D 12.</span></span> <span data-ttu-id="4f290-105">所有 Direct3D 12 硬體都支援著色器模型5.1，因此對此模型的支援不會相依于硬體功能層級。</span><span class="sxs-lookup"><span data-stu-id="4f290-105">All Direct3D 12 hardware supports Shader Model 5.1, so support for this model does not depend on what the hardware feature level is.</span></span>

## <a name="resource-types-and-arrays"></a><span data-ttu-id="4f290-106">資源類型和陣列</span><span class="sxs-lookup"><span data-stu-id="4f290-106">Resource types and arrays</span></span>

<span data-ttu-id="4f290-107">著色器模型 5 (SM 5.0) 資源語法使用 `register` 關鍵字將資源的重要資訊轉送至 HLSL 編譯器。</span><span class="sxs-lookup"><span data-stu-id="4f290-107">Shader Model 5 (SM5.0) resource syntax uses the `register` keyword to relay important information about the resource to the HLSL compiler.</span></span> <span data-ttu-id="4f290-108">例如，下列語句會宣告四個在插槽 t3、t4、t5 和 t6 系結的材質陣列。</span><span class="sxs-lookup"><span data-stu-id="4f290-108">For example, the following statement declares an array of four textures bound at slots t3, t4, t5, and t6.</span></span> <span data-ttu-id="4f290-109">t3 是出現在語句中的唯一暫存器位置，只是在四個數組中的第一個位置。</span><span class="sxs-lookup"><span data-stu-id="4f290-109">t3 is the only register slot appearing in the statement, simply being the first in the array of four.</span></span>

``` syntax
Texture2D<float4> tex1[4] : register(t3)
```

<span data-ttu-id="4f290-110">著色器模型 5.1 (SM 5.1) HLSL 中的資源語法是以現有的暫存器資源語法為基礎，可讓您更輕鬆地移植。</span><span class="sxs-lookup"><span data-stu-id="4f290-110">Shader Model 5.1 (SM5.1) resource syntax in HLSL is based on existing register resource syntax, to allow easier porting.</span></span> <span data-ttu-id="4f290-111">HLSL 中的 Direct3D 12 資源會系結至邏輯暫存器空間內的虛擬暫存器：</span><span class="sxs-lookup"><span data-stu-id="4f290-111">Direct3D 12 resources in HLSL are bound to virtual registers within logical register spaces:</span></span>

-   <span data-ttu-id="4f290-112">t –適用于著色器資源檢視 (SRV) </span><span class="sxs-lookup"><span data-stu-id="4f290-112">t – for shader resource views (SRV)</span></span>
-   <span data-ttu-id="4f290-113">s-適用于取樣器</span><span class="sxs-lookup"><span data-stu-id="4f290-113">s – for samplers</span></span>
-   <span data-ttu-id="4f290-114">u –適用于未排序的存取視圖 (UAV) </span><span class="sxs-lookup"><span data-stu-id="4f290-114">u – for unordered access views (UAV)</span></span>
-   <span data-ttu-id="4f290-115">b –適用于常數緩衝區視圖 (CBV) </span><span class="sxs-lookup"><span data-stu-id="4f290-115">b – for constant buffer views (CBV)</span></span>

<span data-ttu-id="4f290-116">參考著色器的根簽章必須與宣告的註冊位置相容。</span><span class="sxs-lookup"><span data-stu-id="4f290-116">The root signature referencing the shader must be compatible with the declared register slots.</span></span> <span data-ttu-id="4f290-117">例如，下列部分的根簽章與使用材質槽 t3 至 t6 相容，因為它描述具有位置 t0 到 t98 的描述項資料表。</span><span class="sxs-lookup"><span data-stu-id="4f290-117">For example, the following portion of a root signature would be compatible with the use of texture slots t3 through t6, as it describes a descriptor table with slots t0 through t98.</span></span>

``` syntax
DescriptorTable( CBV(b1), SRV(t0,numDescriptors=99), CBV(b2) )
```

<span data-ttu-id="4f290-118">資源宣告可以是純量、1D 陣列或多維陣列：</span><span class="sxs-lookup"><span data-stu-id="4f290-118">A resource declaration may be a scalar, a 1D array, or a multidimensional array:</span></span>

``` syntax
Texture2D<float4> tex1 : register(t3,  space0)
Texture2D<float4> tex2[4] : register(t10)
Texture2D<float4> tex3[7][5][3] : register(t20, space1)
```

<span data-ttu-id="4f290-119">SM 5.1 使用的資源類型和元素類型與 SM 5.0 相同。</span><span class="sxs-lookup"><span data-stu-id="4f290-119">SM5.1 uses the same resource types and element types as SM5.0 does.</span></span> <span data-ttu-id="4f290-120">SM 5.1 宣告限制較具彈性，且僅受限於執行時間/硬體限制。</span><span class="sxs-lookup"><span data-stu-id="4f290-120">SM5.1 declaration limits are more flexible, and constrained only by the runtime/hardware limits.</span></span> <span data-ttu-id="4f290-121">`space`關鍵字會指定所宣告變數所系結的邏輯暫存器空間。</span><span class="sxs-lookup"><span data-stu-id="4f290-121">The `space` keyword specifies to which logical register space the declared variable is bound.</span></span> <span data-ttu-id="4f290-122">如果 `space` 省略關鍵字，則預設空間索引0會隱含地指派給範圍 (，因此上方的範圍位於 `tex2` `space0`) 。</span><span class="sxs-lookup"><span data-stu-id="4f290-122">If the `space` keyword is omitted, then the default space index of 0 is implicitly assigned to the range (so the `tex2` range above resides in `space0`).</span></span> <span data-ttu-id="4f290-123">`register(t3,  space0)` 永遠不會與 `register(t3,  space1)` 另一個空間中可能包含 t3 的任何陣列發生衝突。</span><span class="sxs-lookup"><span data-stu-id="4f290-123">`register(t3,  space0)` will never conflict with `register(t3,  space1)`, nor with any array in another space that might include t3.</span></span>

<span data-ttu-id="4f290-124">陣列資源可能具有未系結的大小，其宣告方式是將第一個維度指定為空的，或0：</span><span class="sxs-lookup"><span data-stu-id="4f290-124">An array resource may have an unbounded size, which is declared by specifying the very first dimension to be empty, or 0:</span></span>

``` syntax
Texture2D<float4> tex1[] : register(t0)
```

<span data-ttu-id="4f290-125">相符的描述項資料表可以是：</span><span class="sxs-lookup"><span data-stu-id="4f290-125">The matching descriptor table could be:</span></span>

``` syntax
DescriptorTable( CBV(b1), UAV(u0, numDescriptors = 4), SRV(t0, numDescriptors=unbounded)
```

<span data-ttu-id="4f290-126">HLSL 中的未系結陣列與描述項資料表中的固定數位組相同 `numDescriptors` ，而且 HLSL 中的固定大小與描述項資料表中的未系結宣告相符。</span><span class="sxs-lookup"><span data-stu-id="4f290-126">An unbounded array in HLSL does match a fixed number set with `numDescriptors` in the descriptor table, and a fixed size in the HLSL does match an unbounded declaration in the descriptor table.</span></span>

<span data-ttu-id="4f290-127">允許多維度陣列，包括未系結的大小。</span><span class="sxs-lookup"><span data-stu-id="4f290-127">Multi-dimensional arrays are allowed, including of an unbounded size.</span></span> <span data-ttu-id="4f290-128">這些多維陣列會在暫存器空間中壓平合併。</span><span class="sxs-lookup"><span data-stu-id="4f290-128">These multidimensional arrays are flattened out in register space.</span></span>

``` syntax
Texture2D<float4> tex2[3000][10] : register(t0, space0); // t0-t29999 in space0
Texture2D<float4> tex3[0][5][3] : register(t5, space1)
```

<span data-ttu-id="4f290-129">不允許資源範圍的別名。</span><span class="sxs-lookup"><span data-stu-id="4f290-129">Aliasing of resource ranges is not allowed.</span></span> <span data-ttu-id="4f290-130">換句話說，對於每個資源類型 (t、s、u、b) ，宣告的登錄範圍不得重迭。</span><span class="sxs-lookup"><span data-stu-id="4f290-130">In other words, for each resource type (t, s, u, b), declared register ranges mustn't overlap.</span></span> <span data-ttu-id="4f290-131">這也包括未系結的範圍。</span><span class="sxs-lookup"><span data-stu-id="4f290-131">That includes unbounded ranges, too.</span></span> <span data-ttu-id="4f290-132">在不同的暫存器空間中宣告的範圍絕不會重迭。</span><span class="sxs-lookup"><span data-stu-id="4f290-132">Ranges declared in different register spaces never overlap.</span></span> <span data-ttu-id="4f290-133">請注意，上述) 的未系結 `tex2` (存在於中 `space0` ，而未系結存在 `tex3` 于中 `space1` ，因此不會重迭。</span><span class="sxs-lookup"><span data-stu-id="4f290-133">Note that unbounded `tex2` (above) resides in `space0`, while unbounded `tex3` resides in `space1`, such that they don't overlap.</span></span>

<span data-ttu-id="4f290-134">存取已經宣告為數組的資源，就像編制它們的索引一樣簡單。</span><span class="sxs-lookup"><span data-stu-id="4f290-134">Accessing resources that have been declared as arrays is as simple as indexing them.</span></span>

``` syntax
Texture2D<float4> tex1[400] : register(t3);
sampler samp[7] : register(s0);
tex1[myMaterialID].Sample(samp[samplerID], texCoords);
```

<span data-ttu-id="4f290-135">在使用索引時，有一個重要的預設限制 (在 `myMaterialID` `samplerID` 上述程式碼中) ，因為它們不允許在 [wave](../direct3dhlsl/hlsl-shader-model-6-0-features-for-direct3d-12.md#terminology)內改變。</span><span class="sxs-lookup"><span data-stu-id="4f290-135">There's an important default restriction on the use of the indices (`myMaterialID` and `samplerID` in the code above) in that they're not allowed to vary within a [wave](../direct3dhlsl/hlsl-shader-model-6-0-features-for-direct3d-12.md#terminology).</span></span> <span data-ttu-id="4f290-136">甚至變更以實例為基礎的索引也會依變化計算。</span><span class="sxs-lookup"><span data-stu-id="4f290-136">Even changing the index based on instancing counts as varying.</span></span>

<span data-ttu-id="4f290-137">如果需要改變索引 `NonUniformResourceIndex` ，請在索引上指定辨識符號，例如：</span><span class="sxs-lookup"><span data-stu-id="4f290-137">If varying the index is required then specify the `NonUniformResourceIndex` qualifier on the index, for example:</span></span>

``` syntax
tex1[NonUniformResourceIndex(myMaterialID)].Sample(samp[NonUniformResourceIndex(samplerID)], texCoords);
```

<span data-ttu-id="4f290-138">在某些硬體上，使用此限定詞會產生額外的程式碼，以強制執行正確性 (包括跨執行緒) 但以較小的效能成本。</span><span class="sxs-lookup"><span data-stu-id="4f290-138">On some hardware the use of this qualifier generates additional code to enforce correctness (including across threads) but at a minor performance cost.</span></span> <span data-ttu-id="4f290-139">如果在沒有此限定詞的情況下變更索引，並在繪製/分派內變更，則結果為未定義。</span><span class="sxs-lookup"><span data-stu-id="4f290-139">If an index is changed without this qualifier and within a draw/dispatch the results are undefined.</span></span>

## <a name="descriptor-arrays-and-texture-arrays"></a><span data-ttu-id="4f290-140">描述元陣列和材質陣列</span><span class="sxs-lookup"><span data-stu-id="4f290-140">Descriptor arrays and texture arrays</span></span>

<span data-ttu-id="4f290-141">自 DirectX 10 之後，已可使用材質陣列。</span><span class="sxs-lookup"><span data-stu-id="4f290-141">Texture arrays have been available since DirectX 10.</span></span> <span data-ttu-id="4f290-142">紋理陣列需要一個描述項，不過所有陣列配量都必須共用相同的格式、寬度、高度和 mip 計數。</span><span class="sxs-lookup"><span data-stu-id="4f290-142">Texture arrays require one descriptor, however all the array slices must share the same format, width, height and mip count.</span></span> <span data-ttu-id="4f290-143">此外，陣列必須在虛擬位址空間中佔用連續的範圍。</span><span class="sxs-lookup"><span data-stu-id="4f290-143">Also, the array must occupy a contiguous range in virtual address space.</span></span> <span data-ttu-id="4f290-144">下列程式碼顯示從著色器存取材質陣列的範例。</span><span class="sxs-lookup"><span data-stu-id="4f290-144">The following code shows an example of accessing a texture array from a shader.</span></span>

``` syntax
Texture2DArray<float4> myTex2DArray : register(t0); // t0
float3 myCoord(1.0f,1.4f,2.2f); // 2.2f is array index (rounded to int)
color = myTex2DArray.Sample(mySampler, myCoord);
```

<span data-ttu-id="4f290-145">在紋理陣列中，索引可以自由地改變，而不需要像這樣的限定詞 `NonUniformResourceIndex` 。</span><span class="sxs-lookup"><span data-stu-id="4f290-145">In a texture array, the index can be varied freely, without any need for qualifiers such as `NonUniformResourceIndex`.</span></span>

<span data-ttu-id="4f290-146">對等描述元陣列會是：</span><span class="sxs-lookup"><span data-stu-id="4f290-146">The equivalent descriptor array would be:</span></span>

``` syntax
Texture2D<float4> myArrayOfTex2D[] : register(t0); // t0+
float2 myCoord(1.0f, 1.4f);
color = myArrayOfTex2D[2].Sample(mySampler,myCoord); // 2 is index
```

<span data-ttu-id="4f290-147">請注意，陣列索引的 float 用法不難用 `myArrayOfTex2D[2]` 。</span><span class="sxs-lookup"><span data-stu-id="4f290-147">Note the awkward use of a float for the array index is replaced with `myArrayOfTex2D[2]`.</span></span> <span data-ttu-id="4f290-148">此外，描述元陣列也可提供更大的彈性給維度。</span><span class="sxs-lookup"><span data-stu-id="4f290-148">Also descriptor arrays offer more flexibility with the dimensions.</span></span> <span data-ttu-id="4f290-149">`Texture2D`這個範例中的型別不能改變，但 format、width、height 和 mip count 都可以與每個描述項不同。</span><span class="sxs-lookup"><span data-stu-id="4f290-149">The type, `Texture2D` is this example, cannot vary, but the format, width, height, and mip count can all vary with each descriptor.</span></span>

<span data-ttu-id="4f290-150">有紋理陣列的描述元陣列是合法的：</span><span class="sxs-lookup"><span data-stu-id="4f290-150">It is legitimate to have a descriptor array of texture arrays:</span></span>

``` syntax
Texture2DArray<float4> myArrayOfTex2DArrays[2] : register(t0);
```

<span data-ttu-id="4f290-151">宣告結構的陣列，每個包含描述項的結構都不合法，例如，不支援下列程式碼。</span><span class="sxs-lookup"><span data-stu-id="4f290-151">It is not legitimate to declare an array of structures, each structure containing descriptors, for example the following code is not supported.</span></span>

``` syntax
struct myStruct {
    Texture2D                    a; 
    Texture2D                    b;
    ConstantBuffer<myConstants>  c;
};
myStruct foo[10000] : register(....);
```

<span data-ttu-id="4f290-152">這會允許記憶體配置 **abcabcabc**...，但這是語言限制，不受支援。</span><span class="sxs-lookup"><span data-stu-id="4f290-152">This would have allowed the memory layout **abcabcabc....**, but is a language limitation and is not supported.</span></span> <span data-ttu-id="4f290-153">其中一個支援的方法是如下所示，雖然在此案例中的記憶體配置是 **aaa .。。Bbb。。。ccc ...**</span><span class="sxs-lookup"><span data-stu-id="4f290-153">One supported method of doing this would be as follows, though the memory layout in this case is **aaa...bbb...ccc...**.</span></span>

``` syntax
Texture2D                     a[10000] : register(t0);
Texture2D                     b[10000] : register(t10000);
ConstantBuffer<myConstants>   c[10000] : register(b0);
```

<span data-ttu-id="4f290-154">若要達到 **abcabcabc ...** 記憶體配置，請使用描述中繼資料表，而不使用 `myStruct` 結構。</span><span class="sxs-lookup"><span data-stu-id="4f290-154">To achieve the **abcabcabc....** memory layout, use a descriptor table without use of the `myStruct` structure.</span></span>

## <a name="resource-aliasing"></a><span data-ttu-id="4f290-155">資源別名</span><span class="sxs-lookup"><span data-stu-id="4f290-155">Resource aliasing</span></span>

<span data-ttu-id="4f290-156">HLSL 著色器中指定的資源範圍是邏輯範圍。</span><span class="sxs-lookup"><span data-stu-id="4f290-156">The resource ranges specified in the HLSL shaders are logical ranges.</span></span> <span data-ttu-id="4f290-157">它們會在執行時間透過根簽章機制系結至具體堆積範圍。</span><span class="sxs-lookup"><span data-stu-id="4f290-157">They are be bound to concrete heap ranges at runtime via the root signature mechanism.</span></span> <span data-ttu-id="4f290-158">一般來說，邏輯範圍會對應至不會與其他堆積範圍重迭的堆積範圍。</span><span class="sxs-lookup"><span data-stu-id="4f290-158">Normally, a logical range maps to a heap range that does not overlap with other heap ranges.</span></span> <span data-ttu-id="4f290-159">不過，根簽章機制可 (重迭) 相容類型的堆積範圍。</span><span class="sxs-lookup"><span data-stu-id="4f290-159">However, the root signature mechanism makes it possible to alias (overlap) heap ranges of compatible types.</span></span> <span data-ttu-id="4f290-160">例如， `tex2` 上述範例中的和 `tex3` 範圍可能會對應到相同的 (或重迭的) 堆積範圍，其具有在 HLSL 程式中對材質進行別名的影響。</span><span class="sxs-lookup"><span data-stu-id="4f290-160">For example, `tex2` and `tex3` ranges from the above example may be mapped to the same (or overlapping) heap range, which has the effect of aliasing textures in the HLSL program.</span></span> <span data-ttu-id="4f290-161">如果需要這類別名，您必須使用 D3D10 \_ 著色器資源的別名選項來編譯著色器 \_ ，此 \_ \_ 選項是使用 [效果編譯器工具](../direct3dtools/fxc.md) (fxc.exe) 的 [ */res] \_ 可能 \_ 別名* 選項來設定。</span><span class="sxs-lookup"><span data-stu-id="4f290-161">If such aliasing is desired, the shader must be compiled with D3D10\_SHADER\_RESOURCES\_MAY\_ALIAS option, which is set by using the */res\_may\_alias* option for the [Effect-Compiler Tool](../direct3dtools/fxc.md) (FXC).</span></span> <span data-ttu-id="4f290-162">選項讓編譯器在假設資源可能為別名的情況下，防止特定的負載/存放區優化，以產生正確的程式碼。</span><span class="sxs-lookup"><span data-stu-id="4f290-162">The option makes the compiler produce correct code by preventing certain load/store optimizations under the assumption that resources may alias.</span></span>

## <a name="divergence-and-derivatives"></a><span data-ttu-id="4f290-163">發散和衍生</span><span class="sxs-lookup"><span data-stu-id="4f290-163">Divergence and derivatives</span></span>

<span data-ttu-id="4f290-164">SM 5.1 不會限制資源索引;亦即， ` tex2[idx].Sample(…)` 索引 idx 可以是常值常數、cbuffer 常數或插入值。</span><span class="sxs-lookup"><span data-stu-id="4f290-164">SM5.1 does not impose limitations on the resource index; i.e.,` tex2[idx].Sample(…)` – the index idx can be a literal constant, a cbuffer constant, or an interpolated value.</span></span> <span data-ttu-id="4f290-165">雖然程式設計模型提供極大的彈性，但有一些問題需要注意：</span><span class="sxs-lookup"><span data-stu-id="4f290-165">While the programming model provides such great flexibility, there are issues to be aware of:</span></span>

-   <span data-ttu-id="4f290-166">如果索引分歧在四個四個，則硬體計算的衍生和衍生數量（例如」 LOD）可能會未定義。</span><span class="sxs-lookup"><span data-stu-id="4f290-166">If index diverges across a quad, the hardware-computed derivative and derived quantities such as LOD may be undefined.</span></span> <span data-ttu-id="4f290-167">在此情況下，HLSL 編譯器會盡力發出警告，但不會防止編譯著色器。</span><span class="sxs-lookup"><span data-stu-id="4f290-167">The HLSL compiler makes the best effort to issue a warning in this case, but will not prevent a shader from compiling.</span></span> <span data-ttu-id="4f290-168">此行為類似于分歧控制流程中的計算衍生。</span><span class="sxs-lookup"><span data-stu-id="4f290-168">This behavior is similar to computing derivatives in divergent control flow.</span></span>
-   <span data-ttu-id="4f290-169">如果資源索引是分歧的，則相較于統一索引的案例，效能會降低，因為硬體需要在多個資源上執行作業。</span><span class="sxs-lookup"><span data-stu-id="4f290-169">If the resource index is divergent, the performance is diminished compared to the case of a uniform index, because the hardware needs to perform operations on several resources.</span></span> <span data-ttu-id="4f290-170">在 HLSL 程式碼中，必須以函式來標記可能是分歧的資源索引 `NonUniformResourceIndex` 。</span><span class="sxs-lookup"><span data-stu-id="4f290-170">Resource indexes that may be divergent must be marked with the `NonUniformResourceIndex` function in HLSL code.</span></span> <span data-ttu-id="4f290-171">否則會產生未定義的結果。</span><span class="sxs-lookup"><span data-stu-id="4f290-171">Otherwise results are undefined.</span></span>

## <a name="uavs-in-pixel-shaders"></a><span data-ttu-id="4f290-172">圖元著色器中的 UAVs</span><span class="sxs-lookup"><span data-stu-id="4f290-172">UAVs in pixel shaders</span></span>

<span data-ttu-id="4f290-173">SM 5.1 不會限制圖元著色器中 UAV 範圍的條件約束，如同 SM 5.0 的情況。</span><span class="sxs-lookup"><span data-stu-id="4f290-173">SM5.1 does not impose constraints on UAV ranges in pixel shaders as was the case for SM5.0.</span></span>

## <a name="constant-buffers"></a><span data-ttu-id="4f290-174">常數緩衝區</span><span class="sxs-lookup"><span data-stu-id="4f290-174">Constant Buffers</span></span>

<span data-ttu-id="4f290-175">SM 5.1 常數緩衝區 (cbuffer) 語法已從 SM 5.0 變更，讓開發人員可以索引常數緩衝區。</span><span class="sxs-lookup"><span data-stu-id="4f290-175">SM5.1 constant buffers (cbuffer) syntax has changed from SM5.0 to enable developers to index constant buffers.</span></span> <span data-ttu-id="4f290-176">為了啟用可編制索引的常數緩衝區，SM 5.1 引進了「 `ConstantBuffer` 範本」結構：</span><span class="sxs-lookup"><span data-stu-id="4f290-176">To enable indexable constant buffers, SM5.1 introduces the `ConstantBuffer` “template” construct:</span></span>

``` syntax
struct Foo
{
    float4 a;
    int2 b;
};
ConstantBuffer<Foo> myCB1[2][3] : register(b2, space1);
ConstantBuffer<Foo> myCB2 : register(b0, space1);
```

<span data-ttu-id="4f290-177">上述程式碼會宣告類型和大小為6的常數緩衝區變數 `myCB1` `Foo` ，以及純量常數緩衝區變數 `myCB2` 。</span><span class="sxs-lookup"><span data-stu-id="4f290-177">The preceding code declares constant buffer variable `myCB1` of type `Foo` and size 6, and a scalar, constant buffer variable `myCB2`.</span></span> <span data-ttu-id="4f290-178">常數緩衝區變數現在可以在著色器中建立索引，如下所示：</span><span class="sxs-lookup"><span data-stu-id="4f290-178">A constant buffer variable can now be indexed in the shader as:</span></span>

``` syntax
myCB1[i][j].a.xyzw
myCB2.b.yy
```

<span data-ttu-id="4f290-179">欄位 ' a ' 和 ' b ' 不會成為全域變數，而是必須視為欄位。</span><span class="sxs-lookup"><span data-stu-id="4f290-179">Fields ‘a’ and ‘b’ do not become global variables, but rather must be treated as fields.</span></span> <span data-ttu-id="4f290-180">為了回溯相容性，SM 5.1 針對純量 cbuffers 支援舊的 cbuffer 概念。</span><span class="sxs-lookup"><span data-stu-id="4f290-180">For backward compatibility, SM5.1 supports the old cbuffer concept for scalar cbuffers.</span></span> <span data-ttu-id="4f290-181">下列語句會使 ' a ' 和 ' b ' 全域唯讀變數（如同在 SM 5.0 中一樣）。</span><span class="sxs-lookup"><span data-stu-id="4f290-181">The following statement makes ‘a’ and ‘b’ global, read-only variables as in SM5.0.</span></span> <span data-ttu-id="4f290-182">不過，這類舊樣式的 cbuffer 無法進行索引。</span><span class="sxs-lookup"><span data-stu-id="4f290-182">However, such an old-style cbuffer cannot be indexable.</span></span>

``` syntax
cbuffer : register(b1)
{
    float4 a;
    int2 b;
};
```

<span data-ttu-id="4f290-183">目前，著色器編譯器只支援 `ConstantBuffer` 使用者定義結構的範本。</span><span class="sxs-lookup"><span data-stu-id="4f290-183">Currently, the shader compiler supports the `ConstantBuffer` template for user-defined structures only.</span></span>

<span data-ttu-id="4f290-184">基於相容性的理由，HLSL 編譯器可能會自動為中宣告的範圍指派資源暫存器 `space0` 。</span><span class="sxs-lookup"><span data-stu-id="4f290-184">For compatibility reasons, the HLSL compiler may automatically assign resource registers for ranges declared in `space0`.</span></span> <span data-ttu-id="4f290-185">如果在 register 子句中省略了 ' space '，則 `space0` 會使用預設值。</span><span class="sxs-lookup"><span data-stu-id="4f290-185">If ‘space’ is omitted in the register clause, the default `space0` is used.</span></span> <span data-ttu-id="4f290-186">編譯器會使用第一個洞的啟發學習法來指派暫存器。</span><span class="sxs-lookup"><span data-stu-id="4f290-186">The compiler uses the first-hole-fits heuristic to assign the registers.</span></span> <span data-ttu-id="4f290-187">您可以透過反映 API 來抓取指派，該 API 已擴充為新增空間的 *空間* 欄位，而 *BindPoint* 欄位指出資源暫存器範圍的下限。</span><span class="sxs-lookup"><span data-stu-id="4f290-187">The assignment can be retrieved via the reflection API, which has been extended to add the *Space* field for space, while the *BindPoint* field indicates the lower bound of the resource register range.</span></span>

## <a name="bytecode-changes-in-sm51"></a><span data-ttu-id="4f290-188">SM 5.1 的位元組位元組變更</span><span class="sxs-lookup"><span data-stu-id="4f290-188">Bytecode changes in SM5.1</span></span>

<span data-ttu-id="4f290-189">SM 5.1 變更如何在指示中宣告和參考資源暫存器。</span><span class="sxs-lookup"><span data-stu-id="4f290-189">SM5.1 changes how resource registers are declared and referenced in instructions.</span></span> <span data-ttu-id="4f290-190">語法包含宣告暫存器「變數」，類似于針對群組共用記憶體暫存器進行的作業：</span><span class="sxs-lookup"><span data-stu-id="4f290-190">The syntax involves declaring a register “variable”, similar to how it is done for group shared memory registers:</span></span>

``` syntax
Texture2D<float4> tex0          : register(t5,  space0);
Texture2D<float4> tex1[][5][3]  : register(t10, space0);
Texture2D<float4> tex2[8]       : register(t0,  space1);
SamplerState samp0              : register(s5, space0);

float4 main(float4 coord : COORD) : SV_TARGET
{
    float4 r = coord;
    r += tex0.Sample(samp0, r.xy);
    r += tex2[r.x].Sample(samp0, r.xy);
    r += tex1[r.x][r.y][r.z].Sample(samp0, r.xy);
    return r;
}
```

<span data-ttu-id="4f290-191">這會將它分解為：</span><span class="sxs-lookup"><span data-stu-id="4f290-191">This will disassemble to:</span></span>

``` syntax
// Resource Bindings:
//
// Name                                 Type  Format         Dim    ID   HLSL Bind     Count
// ------------------------------ ---------- ------- ----------- -----   --------- ---------
// samp0                             sampler      NA          NA     S0    a5            1
// tex0                              texture  float4          2d     T0    t5            1
// tex1[0][5][3]                     texture  float4          2d     T1   t10        unbounded
// tex2[8]                           texture  float4          2d     T2    t0.space1     8
//
//
//
// Input signature:
//
// Name                 Index   Mask Register SysValue  Format   Used
// -------------------- ----- ------ -------- -------- ------- ------
// COORD                    0   xyzw        0     NONE   float   xyzw
//
//
// Output signature:
//
// Name                 Index   Mask Register SysValue  Format   Used
// -------------------- ----- ------ -------- -------- ------- ------
// SV_TARGET                0   xyzw        0   TARGET   float   xyzw
//
ps_5_1
dcl_globalFlags refactoringAllowed
dcl_sampler s0[5:5], mode_default, space=0
dcl_resource_texture2d (float,float,float,float) t0[5:5], space=0
dcl_resource_texture2d (float,float,float,float) t1[10:*], space=0
dcl_resource_texture2d (float,float,float,float) t2[0:7], space=1
dcl_input_ps linear v0.xyzw
dcl_output o0.xyzw
dcl_temps 2
sample r0.xyzw, v0.xyxx, t0[0].xyzw, s0[5]
add r0.xyzw, r0.xyzw, v0.xyzw
ftou r1.x, r0.x
sample r1.xyzw, r0.xyxx, t2[r1.x + 0].xyzw, s0[5]
add r0.xyzw, r0.xyzw, r1.xyzw
ftou r1.xyz, r0.zyxz
imul null, r1.yz, r1.zzyz, l(0, 15, 3, 0)
iadd r1.y, r1.z, r1.y
iadd r1.x, r1.x, r1.y
sample r1.xyzw, r0.xyxx, t1[r1.x + 10].xyzw, s0[5]
add o0.xyzw, r0.xyzw, r1.xyzw
ret
// Approximately 12 instruction slots are used.
```

<span data-ttu-id="4f290-192">每個著色器資源範圍現在都有一個識別碼， (著色器位元組程式碼的唯一) 名稱。</span><span class="sxs-lookup"><span data-stu-id="4f290-192">Each shader resource range now has an ID (a name) that is unique to the shader bytecode.</span></span> <span data-ttu-id="4f290-193">例如，在著色器位元組程式碼中，tex1 (t10) 材質陣列變成不是 1 '。</span><span class="sxs-lookup"><span data-stu-id="4f290-193">For example, tex1 (t10) texture array becomes ‘T1’ in the shader bytecode.</span></span> <span data-ttu-id="4f290-194">將唯一識別碼提供給每個資源範圍，可提供兩個專案：</span><span class="sxs-lookup"><span data-stu-id="4f290-194">Giving unique IDs to each resource range allows two things:</span></span>

-   <span data-ttu-id="4f290-195">明確識別哪些資源範圍 (請參閱 \_ \_) 的指令索引 (查看範例指示) 。</span><span class="sxs-lookup"><span data-stu-id="4f290-195">Unambiguously identify which resource range (see dcl\_resource\_texture2d) is being indexed in an instruction (see sample instruction).</span></span>
-   <span data-ttu-id="4f290-196">將一組屬性附加至宣告，例如元素類型、跨距大小、點陣作業模式等。</span><span class="sxs-lookup"><span data-stu-id="4f290-196">Attaching a set of attributes to the declaration, e.g., element type, stride size, raster operation mode, etc.</span></span>

<span data-ttu-id="4f290-197">請注意，範圍的識別碼與 HLSL 下限宣告沒有關聯。</span><span class="sxs-lookup"><span data-stu-id="4f290-197">Note that the ID of the range is not related to the HLSL lower bound declaration.</span></span>

<span data-ttu-id="4f290-198">反映資源系結的順序 (在頂端的) 和著色器宣告指示 (\_ \*) 相同，以協助識別 HLSL 變數和位元組程式碼識別碼之間的對應。</span><span class="sxs-lookup"><span data-stu-id="4f290-198">The order of reflection resource bindings (listing at the top) and shader declaration instructions (dcl\_\*) is the same to aid in identifying the correspondence between HLSL variables and bytecode IDs.</span></span>

<span data-ttu-id="4f290-199">SM 5.1 中的每個宣告指令都使用3D 運算元來定義：範圍識別碼、下限和上限。</span><span class="sxs-lookup"><span data-stu-id="4f290-199">Each declaration instruction in SM5.1 uses a 3D operand to define: range ID, lower and upper bounds.</span></span> <span data-ttu-id="4f290-200">發出額外的權杖來指定註冊空間。</span><span class="sxs-lookup"><span data-stu-id="4f290-200">An additional token is emitted to specify the register space.</span></span> <span data-ttu-id="4f290-201">可能也會發出其他標記，以傳達範圍的其他屬性，例如，cbuffer 或結構化的緩衝區宣告指令會發出 cbuffer 或結構的大小。</span><span class="sxs-lookup"><span data-stu-id="4f290-201">Other tokens may be emitted as well to convey additional properties of the range, e.g., cbuffer or structured buffer declaration instruction emits the size of the cbuffer or structure.</span></span> <span data-ttu-id="4f290-202">您可以在 d3d12TokenizedProgramFormat 和 **D3D10ShaderBinary：： CShaderCodeParser** 中找到編碼的確切詳細資料。</span><span class="sxs-lookup"><span data-stu-id="4f290-202">The exact details of encoding can be found in d3d12TokenizedProgramFormat.h and **D3D10ShaderBinary::CShaderCodeParser**.</span></span>

<span data-ttu-id="4f290-203">SM 5.1 指示將不會發出額外的資源運算元資訊做為指令 (的一部分，如同 SM 5.0) 。</span><span class="sxs-lookup"><span data-stu-id="4f290-203">SM5.1 instructions will not emit additional resource operand information as part of the instruction (as in SM5.0).</span></span> <span data-ttu-id="4f290-204">這項資訊現在位於宣告指示中。</span><span class="sxs-lookup"><span data-stu-id="4f290-204">This information is now in the declaration instructions.</span></span> <span data-ttu-id="4f290-205">在 SM 5.0 中，為資源編制索引所需的資源屬性必須在擴充的 opcode 權杖中描述，因為索引將關聯性模糊至宣告。</span><span class="sxs-lookup"><span data-stu-id="4f290-205">In SM5.0, instructions indexing resources required resource attributes to be described in extended opcode tokens, since indexing obfuscated the association to the declaration.</span></span> <span data-ttu-id="4f290-206">在 SM 5.1 中，每個識別碼 (例如 ' t 1 ' ) 明確地與單一宣告相關聯，以描述所需的資源資訊。</span><span class="sxs-lookup"><span data-stu-id="4f290-206">In SM5.1, each ID (such as ‘t1’) is unambiguously associated with a single declaration that describes the required resource information.</span></span> <span data-ttu-id="4f290-207">因此，不會再發出用來描述資源資訊之指示的延伸操作碼權杖。</span><span class="sxs-lookup"><span data-stu-id="4f290-207">Therefore, the extended opcode tokens used on instructions to describe resource information are no longer emitted.</span></span>

<span data-ttu-id="4f290-208">在非宣告的指示中，取樣器、SRVs 和 UAVs 的資源運算元是2D 運算元。</span><span class="sxs-lookup"><span data-stu-id="4f290-208">In non-declaration instructions, a resource operand for samplers, SRVs, and UAVs is a 2D operand.</span></span> <span data-ttu-id="4f290-209">第一個索引是指定範圍識別碼的常值常數。</span><span class="sxs-lookup"><span data-stu-id="4f290-209">The first index is a literal constant that specifies the range ID.</span></span> <span data-ttu-id="4f290-210">第二個索引代表索引的 linearized 值。</span><span class="sxs-lookup"><span data-stu-id="4f290-210">The second index represents the linearized value of the index.</span></span> <span data-ttu-id="4f290-211">相對於對應的登錄空間的開頭，會計算此值， (不是相對於邏輯範圍的開頭) 為了讓與根簽章更好的相互關聯，以及降低調整索引的驅動程式編譯器負擔。</span><span class="sxs-lookup"><span data-stu-id="4f290-211">The value is computed relative to the beginning of the corresponding register space (not relative to the beginning of the logical range) to better correlate with the root signature and to reduce the driver compiler burden of adjusting the index.</span></span>

<span data-ttu-id="4f290-212">CBVs 的資源運算元是一種3D 運算元，包含：範圍的常值識別碼、常數緩衝區的索引，以及常數緩衝區特定實例中的位移。</span><span class="sxs-lookup"><span data-stu-id="4f290-212">A resource operand for CBVs is a 3D operand, containing: literal ID of the range, index of the constant buffer, offset into the particular instance of constant buffer.</span></span>

## <a name="example-hlsl-declarations"></a><span data-ttu-id="4f290-213">範例 HLSL 宣告</span><span class="sxs-lookup"><span data-stu-id="4f290-213">Example HLSL Declarations</span></span>

<span data-ttu-id="4f290-214">HLSL 程式不需要知道根簽章的任何相關資訊。</span><span class="sxs-lookup"><span data-stu-id="4f290-214">HLSL programs do not need to know anything about root signatures.</span></span> <span data-ttu-id="4f290-215">他們可以將系結指派給虛擬「註冊」系結空間、t \# For SRVs、u \# for UAVs、b \# for CBVs、s \# 進行取樣器，或是依賴編譯器來挑選指派 (，然後在) 之後使用著色器反映來查詢產生的對應。</span><span class="sxs-lookup"><span data-stu-id="4f290-215">They can assign bindings to the virtual “register” binding space, t\# for SRVs, u\# for UAVs, b\# for CBVs, s\# for samplers, or rely on the compiler to pick assignments (and query the resulting mappings using shader reflection afterwards).</span></span> <span data-ttu-id="4f290-216">根簽章會將描述中繼資料表、根描述元和根常數對應至此虛擬登錄空間。</span><span class="sxs-lookup"><span data-stu-id="4f290-216">The root signature maps descriptor tables, root descriptors, and root constants to this virtual register space.</span></span>

<span data-ttu-id="4f290-217">以下是 HLSL 著色器可能具有的一些宣告範例。</span><span class="sxs-lookup"><span data-stu-id="4f290-217">The following are some example declarations an HLSL shader might have.</span></span> <span data-ttu-id="4f290-218">請注意，沒有根簽章或描述中繼資料表的參考。</span><span class="sxs-lookup"><span data-stu-id="4f290-218">Note that there are no references to root signatures or descriptor tables.</span></span>

``` syntax
Texture2D foo[5] : register(t2);
Buffer bar : register(t7);
RWBuffer dataLog : register(u1);

Sampler samp : register(s0);

struct Data
{
    UINT index;
    float4 color;
};
ConstantBuffer<Data> myData : register(b0);

Texture2D terrain[] : register(t8); // Unbounded array
Texture2D misc[] : register(t0,space1); // Another unbounded array 
                                        // space1 avoids overlap with above t#

struct MoreData
{
    float4x4 xform;
};
ConstantBuffer<MoreData> myMoreData : register(b1);

struct Stuff
{
    float2 factor;
    UINT drawID;
};
ConstantBuffer<Stuff> myStuff[][3][8]  : register(b2, space3)
```

## <a name="related-topics"></a><span data-ttu-id="4f290-219">相關主題</span><span class="sxs-lookup"><span data-stu-id="4f290-219">Related topics</span></span>

* [<span data-ttu-id="4f290-220">使用 HLSL 5.1 的動態索引</span><span class="sxs-lookup"><span data-stu-id="4f290-220">Dynamic Indexing using HLSL 5.1</span></span>](dynamic-indexing-using-hlsl-5-1.md)
* [<span data-ttu-id="4f290-221">效果-編譯器工具</span><span class="sxs-lookup"><span data-stu-id="4f290-221">Effect-Compiler Tool</span></span>](../direct3dtools/fxc.md)
* [<span data-ttu-id="4f290-222">適用于 Direct3D 12 的 HLSL 著色器模型5.1 功能</span><span class="sxs-lookup"><span data-stu-id="4f290-222">HLSL Shader Model 5.1 Features for Direct3D 12</span></span>](../direct3dhlsl/hlsl-shader-model-5-1-features-for-direct3d-12.md)
* [<span data-ttu-id="4f290-223">依轉譯器排序的視圖</span><span class="sxs-lookup"><span data-stu-id="4f290-223">Rasterizer Ordered Views</span></span>](rasterizer-order-views.md)
* [<span data-ttu-id="4f290-224">資源系結</span><span class="sxs-lookup"><span data-stu-id="4f290-224">Resource Binding</span></span>](resource-binding.md)
* [<span data-ttu-id="4f290-225">根簽章</span><span class="sxs-lookup"><span data-stu-id="4f290-225">Root Signatures</span></span>](root-signatures.md)
* [<span data-ttu-id="4f290-226">著色器模型5。1</span><span class="sxs-lookup"><span data-stu-id="4f290-226">Shader Model 5.1</span></span>](../direct3dhlsl/shader-model-5-1.md)
* [<span data-ttu-id="4f290-227">著色器指定的樣板參考值</span><span class="sxs-lookup"><span data-stu-id="4f290-227">Shader Specified Stencil Reference Value</span></span>](shader-specified-stencil-reference-value.md)
* [<span data-ttu-id="4f290-228">在 HLSL 中指定根簽章</span><span class="sxs-lookup"><span data-stu-id="4f290-228">Specifying Root Signatures in HLSL</span></span>](specifying-root-signatures-in-hlsl.md)