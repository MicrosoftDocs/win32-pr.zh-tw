---
title: Common-Shader 核心
description: Common-Shader 核心
ms.assetid: f3cf2969-83a4-461f-8177-d336536194ba
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e27ebe7d908c473890ac5b851eac3e0bc840c859
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839607"
---
# <a name="common-shader-core"></a><span data-ttu-id="624bd-103">Common-Shader 核心</span><span class="sxs-lookup"><span data-stu-id="624bd-103">Common-Shader Core</span></span>

<span data-ttu-id="624bd-104">在著色器模型4中，所有著色器階段都會使用通用著色器核心來執行相同的基本功能。</span><span class="sxs-lookup"><span data-stu-id="624bd-104">In Shader Model 4, all shader stages implement the same base functionality using a common-shader core.</span></span> <span data-ttu-id="624bd-105">此外，三個著色器階段 (頂點、幾何和圖元) 提供每個階段專屬的功能，例如從幾何著色器階段產生新的基本專案，或捨棄圖元著色器階段中特定圖元的能力。</span><span class="sxs-lookup"><span data-stu-id="624bd-105">In addition, each of the three shader stages (vertex, geometry, and pixel) offer functionality unique to each stage, such as the ability to generate new primitives from the geometry shader stage or to discard a specific pixel in the pixel shader stage.</span></span> <span data-ttu-id="624bd-106">下圖顯示資料如何流經著色器階段，以及通用著色器核心與著色器記憶體資源之間的關聯性。</span><span class="sxs-lookup"><span data-stu-id="624bd-106">The following diagram shows how data flows through a shader stage, and the relationship of the common-shader core with shader memory resources.</span></span>

![著色器階段中的資料流程圖](images/d3d10-shader-unit.png)

-   <span data-ttu-id="624bd-108">**輸入資料**：頂點著色器會從輸入組合語言階段收到其輸入;幾何和圖元著色器會接收來自上一個著色器階段的輸入。</span><span class="sxs-lookup"><span data-stu-id="624bd-108">**Input Data**: A vertex shader receives its inputs from the input assembler stage; geometry and pixel shaders receive their inputs from the previous shader stage.</span></span> <span data-ttu-id="624bd-109">額外的輸入包括 [系統值的語法](dx-graphics-hlsl-semantics.md)，可供管線中的第一個單位取用。</span><span class="sxs-lookup"><span data-stu-id="624bd-109">Additional inputs include [system-value semantics](dx-graphics-hlsl-semantics.md), which are consumable by the first unit in the pipeline to which they are applicable.</span></span>
-   <span data-ttu-id="624bd-110">**輸出資料**：著色器會產生輸出結果，以傳遞至管線中的後續階段。</span><span class="sxs-lookup"><span data-stu-id="624bd-110">**Output Data**: Shaders generate output results to be passed onto the subsequent stage in the pipeline.</span></span> <span data-ttu-id="624bd-111">針對幾何著色器，單一調用的資料輸出數量可能會不同。</span><span class="sxs-lookup"><span data-stu-id="624bd-111">For a geometry shader, the amount of data output from a single invocation can vary.</span></span> <span data-ttu-id="624bd-112">某些輸出會由常見的著色器核心 (（例如頂點位置和轉譯目標陣列索引) ）來解讀，而其他輸出則是設計成由應用程式來解讀。</span><span class="sxs-lookup"><span data-stu-id="624bd-112">Some outputs are interpreted by the common-shader core (such as vertex position and render-target-array index), others are designed to be interpreted by an application.</span></span>
-   <span data-ttu-id="624bd-113">**著色器程式碼**：著色器可以從記憶體讀取、執行向量浮點數、整數算數運算或流程式控制製作業。</span><span class="sxs-lookup"><span data-stu-id="624bd-113">**Shader Code**: Shaders can read from memory, perform vector floating point and integer arithmetic operations, or flow control operations.</span></span> <span data-ttu-id="624bd-114">在著色器中可執行檔語句數目沒有任何限制。</span><span class="sxs-lookup"><span data-stu-id="624bd-114">There is no limit to the number of statements that can be implemented in a shader.</span></span>
-   <span data-ttu-id="624bd-115">**取樣** 器：取樣器定義如何取樣和篩選紋理。</span><span class="sxs-lookup"><span data-stu-id="624bd-115">**Samplers**: Samplers define how to sample and filter textures.</span></span> <span data-ttu-id="624bd-116">最多可同時將16個取樣器系結至著色器。</span><span class="sxs-lookup"><span data-stu-id="624bd-116">As many as 16 samplers can be bound to a shader simultaneously.</span></span>
-   <span data-ttu-id="624bd-117">**材質**：紋理可以使用取樣器進行篩選，或使用 [load](dx-graphics-hlsl-to-load.md) 內建函數直接以每個材質為基礎來讀取。</span><span class="sxs-lookup"><span data-stu-id="624bd-117">**Textures**: Textures can be filtered using samplers or read on a per-texel basis directly with the [load](dx-graphics-hlsl-to-load.md) intrinsic function.</span></span>
-   <span data-ttu-id="624bd-118">**緩衝區**：緩衝區永遠不會經過篩選，但是可以使用 [load](dx-graphics-hlsl-to-load.md) 內建函數，以每個元素為基礎來讀取緩衝區。</span><span class="sxs-lookup"><span data-stu-id="624bd-118">**Buffers**: Buffers are never filtered, but can be read from memory on a per-element basis directly with the [load](dx-graphics-hlsl-to-load.md) intrinsic function.</span></span> <span data-ttu-id="624bd-119">多達128的材質和緩衝區資源 (結合的) 可同時系結至著色器。</span><span class="sxs-lookup"><span data-stu-id="624bd-119">As many as 128 texture and buffer resources (combined) can be bound to a shader simultaneously.</span></span>
-   <span data-ttu-id="624bd-120">**常數緩衝區**：常數緩衝區已針對著色器常數變數進行優化。</span><span class="sxs-lookup"><span data-stu-id="624bd-120">**Constant Buffers**: Constant buffers are optimized for shader constant-variables.</span></span> <span data-ttu-id="624bd-121">最多可以同時將16個常數緩衝區系結至著色器階段。</span><span class="sxs-lookup"><span data-stu-id="624bd-121">As many as 16 constant buffers can be bound to a shader stage simultaneously.</span></span> <span data-ttu-id="624bd-122">其設計目的是要從 CPU 進行較頻繁的更新;因此，它們具有額外的大小、配置和存取限制。</span><span class="sxs-lookup"><span data-stu-id="624bd-122">They are designed for more frequent update from the CPU; therefore, they have additional size, layout, and access restrictions.</span></span>



|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="624bd-123">Direct3D 9 與 Direct3D 10 之間的差異：</span><span class="sxs-lookup"><span data-stu-id="624bd-123">Differences between Direct3D 9 and Direct3D 10:</span></span><br/> <span data-ttu-id="624bd-124">在 Direct3D 9 中，每個著色器單位都有一個小型常數暫存器檔案，用來儲存所有常數著色器變數。</span><span class="sxs-lookup"><span data-stu-id="624bd-124">In Direct3D 9, each shader unit had a single, small constant register file to store all constant shader variables.</span></span> <span data-ttu-id="624bd-125">使用這個有限的常數空間來容納所有著色器，需要經常回收 CPU 的常數。</span><span class="sxs-lookup"><span data-stu-id="624bd-125">Accommodating all shaders with this limited constant space required frequent recycling of constants by the CPU.</span></span><br/> <span data-ttu-id="624bd-126">在 Direct3D 10 中，常數會儲存在記憶體中不可變的緩衝區，並如同其他任何資源一樣進行管理。</span><span class="sxs-lookup"><span data-stu-id="624bd-126">In Direct3D 10, constants are stored in immutable buffers in memory and are managed like any other resource.</span></span> <span data-ttu-id="624bd-127">應用程式可以建立的常數緩衝區數目沒有任何限制。</span><span class="sxs-lookup"><span data-stu-id="624bd-127">There is no limit to the number of constant buffers an application can create.</span></span> <span data-ttu-id="624bd-128">藉由更新和使用頻率將常陣列織成緩衝區，更新常數以容納所有著色器所需的頻寬量將可大幅減少。</span><span class="sxs-lookup"><span data-stu-id="624bd-128">By organizing constants into buffers by frequency of update and usage, the amount of bandwidth required to update constants to accommodate all shaders can be significantly reduced.</span></span><br/> |



 

## <a name="integer-and-bitwise-support"></a><span data-ttu-id="624bd-129">整數和位支援</span><span class="sxs-lookup"><span data-stu-id="624bd-129">Integer and Bitwise Support</span></span>

<span data-ttu-id="624bd-130">通用著色器核心提供一組完整的 IEEE 相容32位整數和位運算。</span><span class="sxs-lookup"><span data-stu-id="624bd-130">The common shader core provides a full set of IEEE-compliant 32-bit integer and bitwise operations.</span></span> <span data-ttu-id="624bd-131">這些作業可在圖形硬體範例中啟用新的演算法類別，包括壓縮和封裝技術、FFTs 和等位程式流程式控制制。</span><span class="sxs-lookup"><span data-stu-id="624bd-131">These operations enable a new class of algorithms in graphics hardware examples include compression and packing techniques, FFTs, and bitfield program-flow control.</span></span>

<span data-ttu-id="624bd-132">Direct3D 10 HLSL 中的 **int** 和 **uint** 資料類型會對應到硬體中的32位整數。</span><span class="sxs-lookup"><span data-stu-id="624bd-132">The **int** and **uint** data types in Direct3D 10 HLSL map to 32-bit integers in hardware.</span></span>



|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="624bd-133">Direct3D 9 與 Direct3D 10 之間的差異：</span><span class="sxs-lookup"><span data-stu-id="624bd-133">Differences between Direct3D 9 and Direct3D 10:</span></span><br/> <span data-ttu-id="624bd-134">在 HLSL 中標示為整數的 Direct3D 9 資料流程輸入已被解釋為浮點數。</span><span class="sxs-lookup"><span data-stu-id="624bd-134">In Direct3D 9 stream inputs marked as integer in HLSL were interpreted as floating-point.</span></span> <span data-ttu-id="624bd-135">在 Direct3D 10 中，標示為整數的資料流程輸入會轉譯為32位整數。</span><span class="sxs-lookup"><span data-stu-id="624bd-135">In Direct3D 10, stream inputs marked as integer are interpreted as a 32- bit integer.</span></span><br/> <span data-ttu-id="624bd-136">此外，布林值現在已設定所有位，或所有位未設定。</span><span class="sxs-lookup"><span data-stu-id="624bd-136">In addition, boolean values are now all bits set or all bits unset.</span></span> <span data-ttu-id="624bd-137">如果值不等於 0.0 f，則轉換成 **bool** 的資料會被解釋為 true (正數和負零都可以是 false) ，否則會傳回 false。</span><span class="sxs-lookup"><span data-stu-id="624bd-137">Data converted to **bool** will be interpreted as true if the value is not equal to 0.0f (both positive and negative zero are allowed to be false) and false otherwise.</span></span><br/> |



 

## <a name="bitwise-operators"></a><span data-ttu-id="624bd-138">位元運算子</span><span class="sxs-lookup"><span data-stu-id="624bd-138">Bitwise operators</span></span>

<span data-ttu-id="624bd-139">常見的著色器核心支援下列位運算子：</span><span class="sxs-lookup"><span data-stu-id="624bd-139">The common shader core supports the following bitwise operators:</span></span>



| <span data-ttu-id="624bd-140">運算子</span><span class="sxs-lookup"><span data-stu-id="624bd-140">Operator</span></span>  | <span data-ttu-id="624bd-141">函式</span><span class="sxs-lookup"><span data-stu-id="624bd-141">Function</span></span>          |
|-----------|-------------------|
| ~         | <span data-ttu-id="624bd-142">邏輯 Not</span><span class="sxs-lookup"><span data-stu-id="624bd-142">Logical Not</span></span>       |
| <<  | <span data-ttu-id="624bd-143">左移</span><span class="sxs-lookup"><span data-stu-id="624bd-143">Left Shift</span></span>        |
| >>  | <span data-ttu-id="624bd-144">右移</span><span class="sxs-lookup"><span data-stu-id="624bd-144">Right Shift</span></span>       |
| &         | <span data-ttu-id="624bd-145">邏輯 And</span><span class="sxs-lookup"><span data-stu-id="624bd-145">Logical And</span></span>       |
| \|        | <span data-ttu-id="624bd-146">邏輯 Or</span><span class="sxs-lookup"><span data-stu-id="624bd-146">Logical Or</span></span>        |
| ^         | <span data-ttu-id="624bd-147">邏輯 Xor</span><span class="sxs-lookup"><span data-stu-id="624bd-147">Logical Xor</span></span>       |
| <<= | <span data-ttu-id="624bd-148">左移等於</span><span class="sxs-lookup"><span data-stu-id="624bd-148">Left shift Equal</span></span>  |
| >>= | <span data-ttu-id="624bd-149">右 Shift 等於</span><span class="sxs-lookup"><span data-stu-id="624bd-149">Right Shift Equal</span></span> |
| &=        | <span data-ttu-id="624bd-150">和相等</span><span class="sxs-lookup"><span data-stu-id="624bd-150">And Equal</span></span>         |
| \|=       | <span data-ttu-id="624bd-151">或等於</span><span class="sxs-lookup"><span data-stu-id="624bd-151">Or Equal</span></span>          |
| ^=        | <span data-ttu-id="624bd-152">Xor 等於</span><span class="sxs-lookup"><span data-stu-id="624bd-152">Xor Equal</span></span>         |



 

<span data-ttu-id="624bd-153">位運算子定義為只在 **int** 和 **uint** 資料類型上運作。</span><span class="sxs-lookup"><span data-stu-id="624bd-153">Bitwise operators are defined to operate only on **int** and **uint** data types.</span></span> <span data-ttu-id="624bd-154">嘗試在 **float** 或 **struct** 資料類型上使用位運算子將會產生錯誤。</span><span class="sxs-lookup"><span data-stu-id="624bd-154">Attempting to use bitwise operators on **float** or **struct** data types will result in an error.</span></span> <span data-ttu-id="624bd-155">位運算子跟其他運算子的優先順序，與 C 相同。</span><span class="sxs-lookup"><span data-stu-id="624bd-155">Bitwise operators follow the same precedence as C with regard to other operators.</span></span>

## <a name="binary-casts"></a><span data-ttu-id="624bd-156">二進位轉換</span><span class="sxs-lookup"><span data-stu-id="624bd-156">Binary Casts</span></span>

<span data-ttu-id="624bd-157">在整數和浮點類型之間進行轉換，將會在 C 截斷規則之後轉換數值。</span><span class="sxs-lookup"><span data-stu-id="624bd-157">Casting between an integer and a floating-point type will convert the numeric value following C truncation rules.</span></span> <span data-ttu-id="624bd-158">將值從 **float** 轉換成 **int**，再轉換回 **float** ，是因為目標資料類型的有效位數而產生的失真轉換。</span><span class="sxs-lookup"><span data-stu-id="624bd-158">Casting a value from a **float**, to an **int**, and back to a **float** is a lossy conversion dependent on the precision of the target data type.</span></span> <span data-ttu-id="624bd-159">以下是一些轉換功能： [**asfloat (DIRECTX HLSL)**](dx-graphics-hlsl-asfloat.md)、 [**ASINT (directx HLSL)**](dx-graphics-hlsl-asint.md)、 [**asuint (directx HLSL)**](dx-graphics-hlsl-asuint.md)。</span><span class="sxs-lookup"><span data-stu-id="624bd-159">Here are some of the conversion functions: [**asfloat (DirectX HLSL)**](dx-graphics-hlsl-asfloat.md), [**asint (DirectX HLSL)**](dx-graphics-hlsl-asint.md), [**asuint (DirectX HLSL)**](dx-graphics-hlsl-asuint.md).</span></span>

<span data-ttu-id="624bd-160">二進位轉換也可以使用 HLSL 內建函式來執行。</span><span class="sxs-lookup"><span data-stu-id="624bd-160">Binary casts can also be performed using HLSL intrinsic functions.</span></span> <span data-ttu-id="624bd-161">這些會導致編譯器將數位的位表示重新解譯到目標資料類型。</span><span class="sxs-lookup"><span data-stu-id="624bd-161">These cause the compiler to reinterpret the bit representation of a number into the target data type.</span></span>

## <a name="related-topics"></a><span data-ttu-id="624bd-162">相關主題</span><span class="sxs-lookup"><span data-stu-id="624bd-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="624bd-163">著色器模型4</span><span class="sxs-lookup"><span data-stu-id="624bd-163">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 





