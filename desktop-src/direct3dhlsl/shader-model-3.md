---
title: '著色器模型 3 (HLSL 參考) '
description: 頂點著色器和圖元著色器會從舊版著色器中大幅簡化。
ms.assetid: 01ac85cb-b309-4169-acc2-320a929b65cb
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2d87c791694e91de135052b4172e3bd5f55577d7
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/09/2021
ms.locfileid: "111827097"
---
# <a name="shader-model-3-hlsl-reference"></a><span data-ttu-id="4b111-103">著色器模型 3 (HLSL 參考) </span><span class="sxs-lookup"><span data-stu-id="4b111-103">Shader model 3 (HLSL reference)</span></span>

<span data-ttu-id="4b111-104">頂點著色器和圖元著色器會從舊版著色器中大幅簡化。</span><span class="sxs-lookup"><span data-stu-id="4b111-104">Vertex shaders and pixel shaders are simplified considerably from earlier shader versions.</span></span> <span data-ttu-id="4b111-105">如果您在硬體中執行著色器，您可能不會使用 vs \_ 3 \_ 0 或 ps \_ 3 \_ 0 搭配任何其他著色器版本，也不能使用任何著色器類型搭配固定函式管線。</span><span class="sxs-lookup"><span data-stu-id="4b111-105">If you are implementing shaders in hardware, you may not use vs\_3\_0 or ps\_3\_0 with any other shader versions, and you may not use either shader type with the fixed function pipeline.</span></span> <span data-ttu-id="4b111-106">這些變更可讓您簡化驅動程式和執行時間。</span><span class="sxs-lookup"><span data-stu-id="4b111-106">These changes make it possible to simplify drivers and the runtime.</span></span> <span data-ttu-id="4b111-107">唯一的例外是，僅限軟體的 vs \_ 3 \_ 0 著色器可搭配任何圖元著色器版本使用。</span><span class="sxs-lookup"><span data-stu-id="4b111-107">The only exception is that software-only vs\_3\_0 shaders may be used with any pixel shader version.</span></span> <span data-ttu-id="4b111-108">此外，如果您使用僅限軟體的 vs \_ 3 \_ 0 著色器與先前的圖元著色器版本，頂點著色器只能使用與彈性頂點格式相容的輸出語義 (FVF) 代碼。</span><span class="sxs-lookup"><span data-stu-id="4b111-108">In addition, if you are using a software-only vs\_3\_0 shader with a previous pixel shader version, the vertex shader can only use output semantics that are compatible with flexible vertex format (FVF) codes.</span></span>

<span data-ttu-id="4b111-109">在頂點著色器輸出上使用的語義必須在圖元著色器輸入上使用。</span><span class="sxs-lookup"><span data-stu-id="4b111-109">The semantics used on vertex shader outputs must be used on pixel shader inputs.</span></span> <span data-ttu-id="4b111-110">此語義可用來將頂點著色器輸出對應至圖元著色器輸入，類似于頂點宣告對應至頂點著色器輸入暫存器和先前著色器模型的方式。</span><span class="sxs-lookup"><span data-stu-id="4b111-110">The semantics are used to map the vertex shader outputs to the pixel shader inputs, similar to the way the vertex declaration is mapped to the vertex shader input registers and previous shader models.</span></span> <span data-ttu-id="4b111-111">請參閱 vs 3.0 和 ps 3.0 著色器的 Match 語義。</span><span class="sxs-lookup"><span data-stu-id="4b111-111">See Match Semantics on vs 3.0 and ps 3.0 Shaders.</span></span>

<span data-ttu-id="4b111-112">已新增其他換行模式轉譯狀態，以涵蓋此新配置中額外紋理座標的可能性。</span><span class="sxs-lookup"><span data-stu-id="4b111-112">Additional wrap mode render states have been added to cover the possibility of additional texture coordinates in this new scheme.</span></span> <span data-ttu-id="4b111-113">具有 D3DDECLUSAGE TEXCOORD 的屬性 \_ 和從0到15的使用方式索引，會在設定對應 [**的 \_ D3DRS \* 換行**](/windows/desktop/direct3d9/d3drenderstatetype)時，以 wrap 模式插補。</span><span class="sxs-lookup"><span data-stu-id="4b111-113">Attributes with D3DDECLUSAGE\_TEXCOORD and usage index from 0 to 15 are interpolated in wrap mode when the corresponding [**D3DRS\_WRAP\***](/windows/desktop/direct3d9/d3drenderstatetype) is set.</span></span>

-   [<span data-ttu-id="4b111-114">頂點著色器模型3功能</span><span class="sxs-lookup"><span data-stu-id="4b111-114">Vertex Shader Model 3 Features</span></span>](#vertex-shader-model-3-features)
-   [<span data-ttu-id="4b111-115">圖元著色器模型3功能</span><span class="sxs-lookup"><span data-stu-id="4b111-115">Pixel Shader Model 3 Features</span></span>](#pixel-shader-model-3-features)
-   [<span data-ttu-id="4b111-116">Vs \_ 3 \_ 0 和 ps \_ 3 \_ 0 著色器的 Match 語義</span><span class="sxs-lookup"><span data-stu-id="4b111-116">Match Semantics on vs\_3\_0 and ps\_3\_0 Shaders</span></span>](/windows)
-   [<span data-ttu-id="4b111-117">霧化、深度和網底模式變更</span><span class="sxs-lookup"><span data-stu-id="4b111-117">Fog, Depth, and Shading Mode Changes</span></span>](#fog-depth-and-shading-mode-changes)
-   [<span data-ttu-id="4b111-118">浮點數和整數轉換</span><span class="sxs-lookup"><span data-stu-id="4b111-118">Floating Point and Integer Conversions</span></span>](#floating-point-and-integer-conversions)
-   [<span data-ttu-id="4b111-119">指定完整或部分有效位數</span><span class="sxs-lookup"><span data-stu-id="4b111-119">Specifying Full or Partial Precision</span></span>](#specifying-full-or-partial-precision)
-   [<span data-ttu-id="4b111-120">軟體頂點和圖元著色器</span><span class="sxs-lookup"><span data-stu-id="4b111-120">Software Vertex and Pixel Shaders</span></span>](#software-vertex-and-pixel-shaders)

## <a name="vertex-shader-model-3-features"></a><span data-ttu-id="4b111-121">頂點著色器模型3功能</span><span class="sxs-lookup"><span data-stu-id="4b111-121">Vertex Shader Model 3 Features</span></span>

<span data-ttu-id="4b111-122">頂點著色器輸出暫存器類型已折迭為十二個暫存器 (請參閱 [輸出](dx9-graphics-reference-asm-vs-registers-output.md) 暫存器) 。</span><span class="sxs-lookup"><span data-stu-id="4b111-122">The vertex shader output register types have been collapsed into twelve registers (see [Output Registers](dx9-graphics-reference-asm-vs-registers-output.md)).</span></span> <span data-ttu-id="4b111-123">每個使用的暫存器都必須使用 [dcl](dcl-usage---ps.md) 指令和語義 (（例如，dcl \_ color0 o0. xyzw) ）來宣告。</span><span class="sxs-lookup"><span data-stu-id="4b111-123">Each register that is used needs to be declared using the [dcl](dcl-usage---ps.md) instruction and a semantic (for example, dcl\_color0 o0.xyzw).</span></span>

<span data-ttu-id="4b111-124">3 \_ 0 頂點著色器模型 (vs \_ 3 \_ 0) 使用更強大的暫存器 \_ \_ 索引、一組簡化的輸出暫存器、在頂點著色器中取樣材質的能力，以及控制著色器輸入初始化速度的能力，來擴充 vs 2 0 的功能。</span><span class="sxs-lookup"><span data-stu-id="4b111-124">The 3\_0 vertex shader model (vs\_3\_0) expands on the features of vs\_2\_0 with more powerful register indexing, a set of simplified output registers, the ability to sample a texture in a vertex shader, and the ability to control the rate at which shader inputs are initialized.</span></span>

### <a name="index-any-register"></a><span data-ttu-id="4b111-125">編制任何註冊的索引</span><span class="sxs-lookup"><span data-stu-id="4b111-125">Index Any Register</span></span>

<span data-ttu-id="4b111-126">您可以使用[迴圈計數器](dx9-graphics-reference-asm-vs-registers-loop-counter.md)暫存器來編制所有 ([輸入](dx9-graphics-reference-asm-vs-registers-input.md)登錄和[輸出](dx9-graphics-reference-asm-vs-registers-output.md)暫存器) 的暫存器 (只有常數暫存器可以在舊版中編制索引。 ) </span><span class="sxs-lookup"><span data-stu-id="4b111-126">All registers( [Input Register](dx9-graphics-reference-asm-vs-registers-input.md) and [Output Registers](dx9-graphics-reference-asm-vs-registers-output.md)) can be indexed using [Loop Counter Register](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (only constant registers could be indexed in earlier versions.)</span></span>

<span data-ttu-id="4b111-127">您必須先宣告輸入和輸出暫存器，再為它們編制索引。</span><span class="sxs-lookup"><span data-stu-id="4b111-127">You must declare input and output registers before indexing them.</span></span> <span data-ttu-id="4b111-128">不過，您不能為任何以位置或點大小語義宣告的輸出暫存器編制索引。</span><span class="sxs-lookup"><span data-stu-id="4b111-128">However, you may not index any output register that has been declared with a position or point size semantic.</span></span> <span data-ttu-id="4b111-129">事實上，如果使用索引編制，就必須分別在 o0 和 o1 登錄中宣告位置和 psize 的語法。</span><span class="sxs-lookup"><span data-stu-id="4b111-129">In fact, if indexing is used the position and psize semantics have to be declared in the o0 and o1 registers respectively.</span></span>

<span data-ttu-id="4b111-130">您只允許為連續的暫存器範圍編制索引;也就是說，您無法在尚未宣告的暫存器之間進行索引。</span><span class="sxs-lookup"><span data-stu-id="4b111-130">You are only allowed to index a continuous range of registers; that is, you cannot index across registers that have not been declared.</span></span> <span data-ttu-id="4b111-131">雖然這種限制可能很不方便，但卻允許進行硬體優化。</span><span class="sxs-lookup"><span data-stu-id="4b111-131">While this restriction may be inconvenient, it permits hardware optimization to take place.</span></span> <span data-ttu-id="4b111-132">嘗試在非連續的暫存器中編制索引，將會產生未定義的結果。</span><span class="sxs-lookup"><span data-stu-id="4b111-132">Attempting to index across non-contiguous registers will produce undefined results.</span></span> <span data-ttu-id="4b111-133">著色器驗證不會強制執行這種限制。</span><span class="sxs-lookup"><span data-stu-id="4b111-133">Shader validation does not enforce this restriction.</span></span>

### <a name="simplify-output-registers"></a><span data-ttu-id="4b111-134">簡化輸出暫存器</span><span class="sxs-lookup"><span data-stu-id="4b111-134">Simplify Output Registers</span></span>

<span data-ttu-id="4b111-135">所有不同類型的輸出暫存器已折迭為十二個輸出暫存器：1代表位置、2表示色彩、8表示材質，1表示霧化或點大小。</span><span class="sxs-lookup"><span data-stu-id="4b111-135">All the various types of output registers have been collapsed into twelve output registers: 1 for position, 2 for color, 8 for texture, and 1 for fog or point size.</span></span> <span data-ttu-id="4b111-136">這些暫存器將會插補任何針對圖元著色器所包含的資料。</span><span class="sxs-lookup"><span data-stu-id="4b111-136">These registers will interpolate any data they contain for the pixel shader.</span></span> <span data-ttu-id="4b111-137">輸出暫存器宣告是必要的，而且會將語義指派給每個註冊。</span><span class="sxs-lookup"><span data-stu-id="4b111-137">Output register declarations are required and semantics are assigned to each register.</span></span>

<span data-ttu-id="4b111-138">暫存器可以依照下列方式細分：</span><span class="sxs-lookup"><span data-stu-id="4b111-138">The registers can be broken down as follows:</span></span>

-   <span data-ttu-id="4b111-139">至少必須將一個暫存器宣告為四個元件的位置註冊。</span><span class="sxs-lookup"><span data-stu-id="4b111-139">At least one register must be declared as a four-component position register.</span></span> <span data-ttu-id="4b111-140">這是唯一必要的頂點著色器暫存器。</span><span class="sxs-lookup"><span data-stu-id="4b111-140">This is the only vertex shader register that is required.</span></span>
-   <span data-ttu-id="4b111-141">著色器所耗用的前十個暫存器最多可以使用四個元件 (xyzw) 最大值。</span><span class="sxs-lookup"><span data-stu-id="4b111-141">The first ten registers consumed by a shader may use up to four components (xyzw) maximum.</span></span>
-   <span data-ttu-id="4b111-142">最後一個 (或第十二個) 登錄只可包含純量 (例如) 的點大小。</span><span class="sxs-lookup"><span data-stu-id="4b111-142">The last (or twelfth) register may only contain a scalar (such as point size).</span></span>

<span data-ttu-id="4b111-143">如需暫存器的清單，請參閱暫存器 [-vs \_ 3 \_ 0](dx9-graphics-reference-asm-vs-registers-vs-3-0.md)。</span><span class="sxs-lookup"><span data-stu-id="4b111-143">For a listing of the registers, see [Registers - vs\_3\_0](dx9-graphics-reference-asm-vs-registers-vs-3-0.md).</span></span>

### <a name="texture-sample-in-a-vertex-shader"></a><span data-ttu-id="4b111-144">頂點著色器中的材質範例</span><span class="sxs-lookup"><span data-stu-id="4b111-144">Texture Sample in a Vertex Shader</span></span>

<span data-ttu-id="4b111-145">頂點著色器 3 \_ 0 支援使用 [texldl](texldl---vs.md)與頂點著色器中的材質查閱</span><span class="sxs-lookup"><span data-stu-id="4b111-145">Vertex shader 3\_0 supports texture lookup in the vertex shader using [texldl - vs](texldl---vs.md).</span></span>

## <a name="pixel-shader-model-3-features"></a><span data-ttu-id="4b111-146">圖元著色器模型3功能</span><span class="sxs-lookup"><span data-stu-id="4b111-146">Pixel Shader Model 3 Features</span></span>

<span data-ttu-id="4b111-147">圖元著色器色彩和材質暫存器已折迭為十個輸入暫存器 (查看輸入暫存器 [類型](dx9-graphics-reference-asm-ps-registers-ps-3-0.md)) 。</span><span class="sxs-lookup"><span data-stu-id="4b111-147">The pixel shader color and texture registers have been collapsed into ten input registers (see [Input Register Types](dx9-graphics-reference-asm-ps-registers-ps-3-0.md)).</span></span> <span data-ttu-id="4b111-148">臉部暫存器是浮點純量暫存器。</span><span class="sxs-lookup"><span data-stu-id="4b111-148">The Face Register is a floating point scalar register.</span></span> <span data-ttu-id="4b111-149">只有此註冊的正負號有效。</span><span class="sxs-lookup"><span data-stu-id="4b111-149">Only the sign of this register is valid.</span></span> <span data-ttu-id="4b111-150">如果正負號為負數，則基本型別會是背面的臉部。</span><span class="sxs-lookup"><span data-stu-id="4b111-150">If the sign is negative the primitive is a back face.</span></span> <span data-ttu-id="4b111-151">例如，您可以在圖元著色器內使用它來達成雙面光源。</span><span class="sxs-lookup"><span data-stu-id="4b111-151">This can be used inside a pixel shader to achieve two-sided lighting, for instance.</span></span> <span data-ttu-id="4b111-152">位置暫存器會參考目前的 (x，y) 圖元。</span><span class="sxs-lookup"><span data-stu-id="4b111-152">The Position Register references the current (x,y) pixels.</span></span>

<span data-ttu-id="4b111-153">您可以使用下列內容來設定著色器常數暫存器：</span><span class="sxs-lookup"><span data-stu-id="4b111-153">The shader constant registers can be set using:</span></span>

-   [<span data-ttu-id="4b111-154">**SetPixelShaderConstantB**</span><span class="sxs-lookup"><span data-stu-id="4b111-154">**SetPixelShaderConstantB**</span></span>](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb)
-   [<span data-ttu-id="4b111-155">**SetPixelShaderConstantI**</span><span class="sxs-lookup"><span data-stu-id="4b111-155">**SetPixelShaderConstantI**</span></span>](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstanti)
-   [<span data-ttu-id="4b111-156">**SetPixelShaderConstantF**</span><span class="sxs-lookup"><span data-stu-id="4b111-156">**SetPixelShaderConstantF**</span></span>](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf)

## <a name="match-semantics-on-vs_3_0-and-ps_3_0-shaders"></a><span data-ttu-id="4b111-157">Vs \_ 3 \_ 0 和 ps \_ 3 \_ 0 著色器的 Match 語義</span><span class="sxs-lookup"><span data-stu-id="4b111-157">Match Semantics on vs\_3\_0 and ps\_3\_0 Shaders</span></span>

<span data-ttu-id="4b111-158">Vs \_ 3 \_ 0 和 ps \_ 3 0 有一些語義用法的限制 \_ 。</span><span class="sxs-lookup"><span data-stu-id="4b111-158">There are some restrictions on semantic usage with vs\_3\_0 and ps\_3\_0.</span></span> <span data-ttu-id="4b111-159">一般情況下，使用符合著色器輸出所使用之語義的著色器輸入時，您必須特別小心。</span><span class="sxs-lookup"><span data-stu-id="4b111-159">In general, you need to be careful when using a semantic for a shader input that matches a semantic used on a shader output.</span></span>

<span data-ttu-id="4b111-160">比方說，這個圖元著色器會將多個名稱封裝成一個暫存器：</span><span class="sxs-lookup"><span data-stu-id="4b111-160">For instance, this pixel shader packs multiple names into one register:</span></span>


```
ps_3_0 
dcl_texcoord0 v0.x 
dcl_texcoord1 v0.yz // Valid to pack multiple names into one register 
dcl_texcoord2_centroid v1.w
...
```



<span data-ttu-id="4b111-161">每個註冊程式都有不同的語義。</span><span class="sxs-lookup"><span data-stu-id="4b111-161">Each register has a different semantic.</span></span> <span data-ttu-id="4b111-162">請注意，您也可以使用不同 (多個) 的語法來命名 v0. x 和 yz，因為使用寫入遮罩。</span><span class="sxs-lookup"><span data-stu-id="4b111-162">Notice that you can also name v0.x and v0.yz with different (multiple) semantics because of the use of the write mask.</span></span>

<span data-ttu-id="4b111-163">由於圖元著色器的比較，以下的 vs \_ 3 \_ 0 著色器無法與其配對：</span><span class="sxs-lookup"><span data-stu-id="4b111-163">Given the pixel shader, the following vs\_3\_0 shader cannot be paired with it:</span></span>


```
vs_3_0 
... 
dcl_texcoord0 o5.x 
dcl_texcoord1 o6.yzw 
...
```



<span data-ttu-id="4b111-164">這兩個著色器與 [**D3DDECLUSAGE \_ TEXCOORD0**](/windows/desktop/direct3d9/d3ddeclusage) 和 **D3DDECLUSAGE \_ TEXCOORD1** 語義的使用衝突。</span><span class="sxs-lookup"><span data-stu-id="4b111-164">These two shaders conflict with their use of the [**D3DDECLUSAGE\_TEXCOORD0**](/windows/desktop/direct3d9/d3ddeclusage) And **D3DDECLUSAGE\_TEXCOORD1** semantics.</span></span>

<span data-ttu-id="4b111-165">重寫類似的頂點著色器，以避免語義衝突：</span><span class="sxs-lookup"><span data-stu-id="4b111-165">Rewrite the vertex shader like this to avoid the semantic collision:</span></span>


```
vs_3_0 
... 
dcl_texcoord2 o3 
dcl_texcoord3 o9 
...
```



<span data-ttu-id="4b111-166">同樣地，在圖元著色器中不同輸入暫存器上所宣告的語義名稱 (v0，而圖元著色器中的 v1) 不能用在這個頂點著色器的單一輸出暫存器中。</span><span class="sxs-lookup"><span data-stu-id="4b111-166">Similarly, a semantic name declared on different input registers in the pixel shader (v0 and v1 in the pixel shader) cannot be used in a single output register in this vertex shader.</span></span> <span data-ttu-id="4b111-167">比方說，這個頂點著色器無法與圖元著色器配對，因為 D3DDECLUSAGE \_ TEXCOORD1 同時用於圖元著色器輸入暫存器 (v0、v1) 和頂點著色器輸出 register o3。</span><span class="sxs-lookup"><span data-stu-id="4b111-167">For instance, this vertex shader cannot be paired with the pixel shader because D3DDECLUSAGE\_TEXCOORD1 is used for both pixel shader input registers (v0, v1) and the vertex shader output register o3.</span></span>


```
vs_3_0 
... 
dcl_texcoord0 o3.x 
dcl_texcoord1 o3.yz 

dcl_texcoord2 o3.w // BAD! Would be valid if this were not o3 
dcl_texcoord3 o9 ... 
```



<span data-ttu-id="4b111-168">另一方面，此頂點著色器無法與圖元著色器配對，因為具有指定語義之參數的輸出遮罩不會提供圖元著色器所要求的資料：</span><span class="sxs-lookup"><span data-stu-id="4b111-168">On the other hand, this vertex shader cannot be paired with the pixel shader because the output mask for a parameter with a given semantic does not provide the data that is requested by the pixel shader:</span></span>


```
vs_3_0 
... 
dcl_texcoord0 o5.x 
dcl_texcoord1 o5.yzw 
dcl_texcoord2 o7.yz // BAD! Would be valid if w were included 
dcl_texcoord3 o9 
... 
```



<span data-ttu-id="4b111-169">此頂點著色器不會提供圖元著色器所要求的其中一個語義名稱的輸出，因此著色器配對無效：</span><span class="sxs-lookup"><span data-stu-id="4b111-169">This vertex shader does not provide an output with one of the semantic names requested by the pixel shader, so the shader pairing is invalid:</span></span>


```
vs_3_0 
... 
dcl_texcoord0 o5.x 
dcl_texcoord1 o5.yzw 
dcl_texcoord3 o9 
// The pixel shader wants texcoord2, with a w component, 
// but it isn't output by this vertex shader at all! 
... 
```



## <a name="fog-depth-and-shading-mode-changes"></a><span data-ttu-id="4b111-170">霧化、深度和網底模式變更</span><span class="sxs-lookup"><span data-stu-id="4b111-170">Fog, Depth, and Shading Mode Changes</span></span>

<span data-ttu-id="4b111-171">在 \_ 裁剪和三角形柵格化期間設定 D3DRS SHADEMODE 的平面陰影時，具有 D3DDECLUSAGE \_ 色彩的屬性會以平面陰影的方式插補。</span><span class="sxs-lookup"><span data-stu-id="4b111-171">When D3DRS\_SHADEMODE is set for flat shading during clipping and triangle rasterization, attributes with D3DDECLUSAGE\_COLOR are interpolated as flat shaded.</span></span> <span data-ttu-id="4b111-172">如果登錄的任何元件是以色彩語義宣告，但相同暫存器的其他元件是以不同的語義來宣告，則在該暫存器中的元件上，不會有色彩語義來定義一般陰影插補 (線性和一般的) 。</span><span class="sxs-lookup"><span data-stu-id="4b111-172">If any components of a register are declared with a color semantic but other components of the same register are given different semantics, flat shading interpolation (linear vs. flat) will be undefined on the components in that register without a color semantic.</span></span>

<span data-ttu-id="4b111-173">如果需要霧化轉譯，vs \_ 3 \_ 0 和 ps \_ 3 \_ 0 著色器必須執行霧化。</span><span class="sxs-lookup"><span data-stu-id="4b111-173">If fog rendering is desired, vs\_3\_0 and ps\_3\_0 shaders must implement fog.</span></span> <span data-ttu-id="4b111-174">不會在著色器以外完成任何霧化計算。</span><span class="sxs-lookup"><span data-stu-id="4b111-174">No fog calculations are done outside of the shaders.</span></span> <span data-ttu-id="4b111-175">Vs 3 0 中沒有任何霧化暫存器 \_ \_ ，以及額外的語義 D3DDECLUSAGE 會 \_ 針對每個頂點計算的霧化 blend 因數 (霧化) 和 D3DDECLUSAGE \_ 深度 (以將深度值傳遞給圖元著色器，以計算已加入的霧化 blend 因數) 。</span><span class="sxs-lookup"><span data-stu-id="4b111-175">There is no fog register in vs\_3\_0, and additional semantics D3DDECLUSAGE\_FOG (for fog blend factor computed per vertex) and D3DDECLUSAGE\_DEPTH (for passing in a depth value to the pixel shader to compute the fog blend factor) have been added.</span></span>

<span data-ttu-id="4b111-176">\_使用圖元著色器3.0 時，會忽略材質階段狀態 D3DTSS TEXCOORDINDEX。</span><span class="sxs-lookup"><span data-stu-id="4b111-176">Texture stage state D3DTSS\_TEXCOORDINDEX is ignored when using pixel shader 3.0.</span></span>

<span data-ttu-id="4b111-177">已新增下列值來容納這些變更：</span><span class="sxs-lookup"><span data-stu-id="4b111-177">The following values have been added to accommodate these changes:</span></span>


```
// Fog and Depth usages
D3DDECLUSAGE_FOG 
D3DDECLUSAGE_DEPTH 

// Additional wrap states for vs_3_0 attributes with D3DDECLUSAGE_TEXCOORD 
D3DRS_WRAP8 
D3DRS_WRAP9 
D3DRS_WRAP10 
D3DRS_WRAP11 
D3DRS_WRAP12 
D3DRS_WRAP13 
D3DRS_WRAP14 
D3DRS_WRAP15
```



## <a name="floating-point-and-integer-conversions"></a><span data-ttu-id="4b111-178">浮點數和整數轉換</span><span class="sxs-lookup"><span data-stu-id="4b111-178">Floating Point and Integer Conversions</span></span>

<span data-ttu-id="4b111-179">浮點數數學會以不同的精確度和範圍 (在管線的不同部分中的16位、24位和32位) 。</span><span class="sxs-lookup"><span data-stu-id="4b111-179">Floating point math happens at different precision and ranges (16-bit, 24-bit, and 32-bit) in different parts of the pipeline.</span></span> <span data-ttu-id="4b111-180">值大於進入管線之管線的動態範圍 (例如，將32位的 float 紋理對應取樣為 ps 2 0 中的24位浮點管線 \_ \_) 建立未定義的結果。</span><span class="sxs-lookup"><span data-stu-id="4b111-180">A value greater than the dynamic range of the pipeline that enters that pipeline (for example, a 32-bit float texture map is sampled into a 24-bit float pipeline in ps\_2\_0) creates an undefined result.</span></span> <span data-ttu-id="4b111-181">針對可預測的行為，您應該將這類值固定到動態範圍的最大值。</span><span class="sxs-lookup"><span data-stu-id="4b111-181">For predictable behavior, you should clamp such a value to the dynamic range maximum.</span></span>

<span data-ttu-id="4b111-182">從浮點值到整數的轉換會在數個位置發生，例如：</span><span class="sxs-lookup"><span data-stu-id="4b111-182">Conversion from a floating point value to an integer happens in several places such as:</span></span>

-   <span data-ttu-id="4b111-183">遇到 [mova vs](mova---vs.md) 指令時。</span><span class="sxs-lookup"><span data-stu-id="4b111-183">When encountering a [mova - vs](mova---vs.md) instruction.</span></span>
-   <span data-ttu-id="4b111-184">在紋理定址期間。</span><span class="sxs-lookup"><span data-stu-id="4b111-184">During texture addressing.</span></span>
-   <span data-ttu-id="4b111-185">當寫出至非浮點數轉譯目標時。</span><span class="sxs-lookup"><span data-stu-id="4b111-185">When writing out to a non-floating point render target.</span></span>

## <a name="specifying-full-or-partial-precision"></a><span data-ttu-id="4b111-186">指定完整或部分有效位數</span><span class="sxs-lookup"><span data-stu-id="4b111-186">Specifying Full or Partial Precision</span></span>

<span data-ttu-id="4b111-187">Ps \_ 3 \_ 0 和 ps \_ 2 x 兩者都 \_ 提供兩種精確度層級的支援：</span><span class="sxs-lookup"><span data-stu-id="4b111-187">Both ps\_3\_0 and ps\_2\_x provide support for two levels of precision:</span></span>



| <span data-ttu-id="4b111-188">ps \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4b111-188">ps\_3\_0</span></span> | <span data-ttu-id="4b111-189">ps \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4b111-189">ps\_2\_0</span></span> | <span data-ttu-id="4b111-190">精確度</span><span class="sxs-lookup"><span data-stu-id="4b111-190">Precision</span></span>         | <span data-ttu-id="4b111-191">值</span><span class="sxs-lookup"><span data-stu-id="4b111-191">Value</span></span>                |
|----------|----------|-------------------|----------------------|
| <span data-ttu-id="4b111-192">x</span><span class="sxs-lookup"><span data-stu-id="4b111-192">x</span></span>        |          | <span data-ttu-id="4b111-193">完整</span><span class="sxs-lookup"><span data-stu-id="4b111-193">Full</span></span>              | <span data-ttu-id="4b111-194">fp32 或更高版本</span><span class="sxs-lookup"><span data-stu-id="4b111-194">fp32 or higher</span></span>       |
| <span data-ttu-id="4b111-195">x</span><span class="sxs-lookup"><span data-stu-id="4b111-195">x</span></span>        |          | <span data-ttu-id="4b111-196">部分有效位數</span><span class="sxs-lookup"><span data-stu-id="4b111-196">Partial precision</span></span> | <span data-ttu-id="4b111-197">fp16 = s10e5</span><span class="sxs-lookup"><span data-stu-id="4b111-197">fp16=s10e5</span></span>           |
| <span data-ttu-id="4b111-198">x</span><span class="sxs-lookup"><span data-stu-id="4b111-198">x</span></span>        | <span data-ttu-id="4b111-199">x</span><span class="sxs-lookup"><span data-stu-id="4b111-199">x</span></span>        | <span data-ttu-id="4b111-200">完整</span><span class="sxs-lookup"><span data-stu-id="4b111-200">Full</span></span>              | <span data-ttu-id="4b111-201">fp24 = s16e7 或更高版本</span><span class="sxs-lookup"><span data-stu-id="4b111-201">fp24=s16e7 or higher</span></span> |
| <span data-ttu-id="4b111-202">x</span><span class="sxs-lookup"><span data-stu-id="4b111-202">x</span></span>        | <span data-ttu-id="4b111-203">x</span><span class="sxs-lookup"><span data-stu-id="4b111-203">x</span></span>        | <span data-ttu-id="4b111-204">部分有效位數</span><span class="sxs-lookup"><span data-stu-id="4b111-204">Partial precision</span></span> | <span data-ttu-id="4b111-205">fp16 = s10e5</span><span class="sxs-lookup"><span data-stu-id="4b111-205">fp16=s10e5</span></span>           |



 

<span data-ttu-id="4b111-206">ps \_ 3 \_ 0 支援的精確度比 ps \_ 2 \_ 0 更高。</span><span class="sxs-lookup"><span data-stu-id="4b111-206">ps\_3\_0 supports more precision than ps\_2\_0 does.</span></span> <span data-ttu-id="4b111-207">依預設，所有作業都會以完整的精確度層級進行。</span><span class="sxs-lookup"><span data-stu-id="4b111-207">By default, all operations occur at the full precision level.</span></span>

<span data-ttu-id="4b111-208">部分精確度 (請參閱 [圖元著色器](dx9-graphics-reference-asm-ps-registers-modifiers.md) 暫存器的) 要求，方法是將 \_ pp 修飾詞新增至著色器程式碼 (前提是基礎實作為支援) 。</span><span class="sxs-lookup"><span data-stu-id="4b111-208">Partial precision (see [Pixel Shader Register Modifiers](dx9-graphics-reference-asm-ps-registers-modifiers.md)) is requested by adding the \_pp modifier to shader code (provided that the underlying implementation supports it).</span></span> <span data-ttu-id="4b111-209">您一律可以自由地忽略修飾詞，並以完整的精確度執行受影響的作業。</span><span class="sxs-lookup"><span data-stu-id="4b111-209">Implementations are always free to ignore the modifier and perform the affected operations in full precision.</span></span>

<span data-ttu-id="4b111-210">\_Pp 修飾詞可以出現在兩個內容中：</span><span class="sxs-lookup"><span data-stu-id="4b111-210">The \_pp modifier can occur in two contexts:</span></span>

-   <span data-ttu-id="4b111-211">在紋理座標宣告上，將部分有效位數材質座標傳遞給圖元著色器。</span><span class="sxs-lookup"><span data-stu-id="4b111-211">On a texture coordinate declaration to pass partial-precision texture coordinates to the pixel shader.</span></span> <span data-ttu-id="4b111-212">當材質將轉送色彩資料座標為圖元著色器時，可使用這種方式，在某些實執行中，部分精確度可能會比完整有效位數更快。</span><span class="sxs-lookup"><span data-stu-id="4b111-212">This could be used when texture coordinates relay color data to the pixel shader, which may be faster with partial precision than with full precision in some implementations.</span></span>
-   <span data-ttu-id="4b111-213">在要求使用部分有效位數的任何指示上，包括材質載入指示。</span><span class="sxs-lookup"><span data-stu-id="4b111-213">On any instruction to request the use of partial precision, including texture load instructions.</span></span> <span data-ttu-id="4b111-214">這表示可以執行實作為部分有效位數的指令，並儲存部分精確度結果。</span><span class="sxs-lookup"><span data-stu-id="4b111-214">This indicates that the implementation is allowed to execute the instruction with partial precision and store a partial-precision result.</span></span> <span data-ttu-id="4b111-215">如果沒有明確的修飾詞，就必須以完整的精確度來執行指令， (無論輸入運算元) 的精確度為何。</span><span class="sxs-lookup"><span data-stu-id="4b111-215">In the absence of an explicit modifier, the instruction must be performed at full precision (regardless of the precision of the input operands).</span></span>

<span data-ttu-id="4b111-216">應用程式可能會刻意選擇以效能的精確度來取捨。</span><span class="sxs-lookup"><span data-stu-id="4b111-216">An application might deliberately choose to trade off precision for performance.</span></span> <span data-ttu-id="4b111-217">有幾種著色器輸入資料是部分精確度處理的自然候選：</span><span class="sxs-lookup"><span data-stu-id="4b111-217">There are several kinds of shader input data which are natural candidates for partial precision processing:</span></span>

-   <span data-ttu-id="4b111-218">色彩反覆運算器以部分精確度值妥善表示。</span><span class="sxs-lookup"><span data-stu-id="4b111-218">Color iterators are well represented by partial-precision values.</span></span>
-   <span data-ttu-id="4b111-219">大部分格式的材質值都可以精確地以部分有效位數值表示， (從32位取樣的值、浮點數格式材質) 的明顯例外狀況。</span><span class="sxs-lookup"><span data-stu-id="4b111-219">Texture values from most formats can be accurately represented by partial-precision values (values sampled from 32-bit, floating-point format textures are an obvious exception).</span></span>
-   <span data-ttu-id="4b111-220">常數可以依適當的著色器，以局部精確度標記法表示。</span><span class="sxs-lookup"><span data-stu-id="4b111-220">Constants may be represented by partial-precision representation as appropriate to the shader.</span></span>

<span data-ttu-id="4b111-221">在所有這些情況下，開發人員都可以選擇指定部分精確度來處理資料，並知道不會遺失任何輸入資料精確度。</span><span class="sxs-lookup"><span data-stu-id="4b111-221">In all these cases the developer may choose to specify partial precision to process the data, knowing that no input data precision is lost.</span></span> <span data-ttu-id="4b111-222">在某些情況下，如果輸入和最終輸出值沒有超過部分有效位數，則著色器可能需要以完整的精確度執行計算的內部步驟。</span><span class="sxs-lookup"><span data-stu-id="4b111-222">In some cases, a shader may require that the internal steps of a calculation be performed at full precision even when input and final output values do not have more than partial precision.</span></span>

## <a name="software-vertex-and-pixel-shaders"></a><span data-ttu-id="4b111-223">軟體頂點和圖元著色器</span><span class="sxs-lookup"><span data-stu-id="4b111-223">Software Vertex and Pixel Shaders</span></span>

<span data-ttu-id="4b111-224">軟體實 (針對頂點著色器的執行時間和參考，以及第2版著色器) 的圖元著色器參考，且 \_ 會放寬某些驗證。</span><span class="sxs-lookup"><span data-stu-id="4b111-224">Software implementations (run-time and reference for vertex shaders and reference for pixel shaders) of version 2\_0 shaders and above have some validation relaxed.</span></span> <span data-ttu-id="4b111-225">這適用于偵錯工具和原型設計用途。</span><span class="sxs-lookup"><span data-stu-id="4b111-225">This is useful for debugging and prototyping purposes.</span></span> <span data-ttu-id="4b111-226">應用程式會向執行時間/組合器指出，它需要使用組合器中的 sw 旗標放寬某些驗證 \_ (例如 vs \_ 2 \_ sw) 。</span><span class="sxs-lookup"><span data-stu-id="4b111-226">The application indicates to the runtime/assembler that it needs some of the validation relaxed using the \_sw flag in the assembler (for example, vs\_2\_sw).</span></span> <span data-ttu-id="4b111-227">軟體著色器不會與硬體搭配運作。</span><span class="sxs-lookup"><span data-stu-id="4b111-227">A software shader will not work with hardware.</span></span>

<span data-ttu-id="4b111-228">vs \_ 2 \_ sw 是 vs 2 x 上限的放寬 \_ \_ ; 同樣地，ps \_ 2 \_ sw 是 ps 2 x 最大上限的放寬 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="4b111-228">vs\_2\_sw is a relaxation to the maximum caps of vs\_2\_x; similarly, ps\_2\_sw is a relaxation to the maximum caps of ps\_2\_x.</span></span> <span data-ttu-id="4b111-229">具體而言，下列驗證是寬鬆的：</span><span class="sxs-lookup"><span data-stu-id="4b111-229">Specifically, the following validations are relaxed:</span></span>



| <span data-ttu-id="4b111-230">著色器模型</span><span class="sxs-lookup"><span data-stu-id="4b111-230">Shader model</span></span>                                           |  <span data-ttu-id="4b111-231">資源</span><span class="sxs-lookup"><span data-stu-id="4b111-231">Resource</span></span>                                    |  <span data-ttu-id="4b111-232">限制</span><span class="sxs-lookup"><span data-stu-id="4b111-232">Limit</span></span>                                                                                                                                  |
|--------------------------------------------|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b111-233">vs \_ 2 \_ sw、vs \_ 3 \_ sw、ps \_ 2 \_ sw、ps \_ 3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="4b111-233">vs\_2\_sw, vs\_3\_sw, ps\_2\_sw, ps\_3\_sw</span></span> | <span data-ttu-id="4b111-234">指令計數</span><span class="sxs-lookup"><span data-stu-id="4b111-234">Instruction Counts</span></span>                   | <span data-ttu-id="4b111-235">無限制</span><span class="sxs-lookup"><span data-stu-id="4b111-235">Unlimited</span></span>                                                                                                                         |
| <span data-ttu-id="4b111-236">vs \_ 2 \_ sw、vs \_ 3 \_ sw、ps \_ 2 \_ sw、ps \_ 3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="4b111-236">vs\_2\_sw, vs\_3\_sw, ps\_2\_sw, ps\_3\_sw</span></span> | <span data-ttu-id="4b111-237">Float 常數暫存器</span><span class="sxs-lookup"><span data-stu-id="4b111-237">Float Constant Registers</span></span>             | <span data-ttu-id="4b111-238">8192</span><span class="sxs-lookup"><span data-stu-id="4b111-238">8192</span></span>                                                                                                                              |
| <span data-ttu-id="4b111-239">vs \_ 2 \_ sw、vs \_ 3 \_ sw、ps \_ 2 \_ sw、ps \_ 3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="4b111-239">vs\_2\_sw, vs\_3\_sw, ps\_2\_sw, ps\_3\_sw</span></span> | <span data-ttu-id="4b111-240">整數常數暫存器</span><span class="sxs-lookup"><span data-stu-id="4b111-240">Integer Constant Registers</span></span>           | <span data-ttu-id="4b111-241">2048</span><span class="sxs-lookup"><span data-stu-id="4b111-241">2048</span></span>                                                                                                                              |
| <span data-ttu-id="4b111-242">vs \_ 2 \_ sw、vs \_ 3 \_ sw、ps \_ 2 \_ sw、ps \_ 3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="4b111-242">vs\_2\_sw, vs\_3\_sw, ps\_2\_sw, ps\_3\_sw</span></span> | <span data-ttu-id="4b111-243">布林常數暫存器</span><span class="sxs-lookup"><span data-stu-id="4b111-243">Boolean Constant Registers</span></span>           | <span data-ttu-id="4b111-244">2048</span><span class="sxs-lookup"><span data-stu-id="4b111-244">2048</span></span>                                                                                                                              |
| <span data-ttu-id="4b111-245">ps \_ 2 \_ sw</span><span class="sxs-lookup"><span data-stu-id="4b111-245">ps\_2\_sw</span></span>                                  | <span data-ttu-id="4b111-246">相依-讀取深度</span><span class="sxs-lookup"><span data-stu-id="4b111-246">Dependent-read depth</span></span>                 | <span data-ttu-id="4b111-247">無限制</span><span class="sxs-lookup"><span data-stu-id="4b111-247">Unlimited</span></span>                                                                                                                         |
| <span data-ttu-id="4b111-248">vs \_ 2 \_ sw</span><span class="sxs-lookup"><span data-stu-id="4b111-248">vs\_2\_sw</span></span>                                  | <span data-ttu-id="4b111-249">流程式控制制指示與標籤</span><span class="sxs-lookup"><span data-stu-id="4b111-249">flow control instructions and labels</span></span> | <span data-ttu-id="4b111-250">無限制</span><span class="sxs-lookup"><span data-stu-id="4b111-250">Unlimited</span></span>                                                                                                                         |
| <span data-ttu-id="4b111-251">vs \_ 2 \_ sw、vs \_ 3 \_ sw、ps \_ 2 \_ sw、ps \_ 3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="4b111-251">vs\_2\_sw, vs\_3\_sw, ps\_2\_sw, ps\_3\_sw</span></span> | <span data-ttu-id="4b111-252">迴圈開始/步驟/計數</span><span class="sxs-lookup"><span data-stu-id="4b111-252">Loop start/step/counts</span></span>               | <span data-ttu-id="4b111-253">Rep 和迴圈指示的反復專案開始和反覆運算步驟大小為32位帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="4b111-253">Iteration start and iteration step size for rep and loop instructions are 32-bit signed integers.</span></span> <span data-ttu-id="4b111-254">Count 最多可達 \_ INT/64。</span><span class="sxs-lookup"><span data-stu-id="4b111-254">Count can be up to MAX\_INT/64.</span></span> |
| <span data-ttu-id="4b111-255">vs \_ 2 \_ sw、vs \_ 3 \_ sw、ps \_ 2 \_ sw、ps \_ 3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="4b111-255">vs\_2\_sw, vs\_3\_sw, ps\_2\_sw, ps\_3\_sw</span></span> | <span data-ttu-id="4b111-256">埠限制</span><span class="sxs-lookup"><span data-stu-id="4b111-256">Port limits</span></span>                          | <span data-ttu-id="4b111-257">所有註冊檔案的埠限制都是寬鬆的。</span><span class="sxs-lookup"><span data-stu-id="4b111-257">Port limits for all register files are relaxed.</span></span>                                                                                   |
| <span data-ttu-id="4b111-258">vs \_ 3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="4b111-258">vs\_3\_sw</span></span>                                  | <span data-ttu-id="4b111-259">Interpolators 數目</span><span class="sxs-lookup"><span data-stu-id="4b111-259">Number of interpolators</span></span>              | <span data-ttu-id="4b111-260">vs 3 sw 中的16個輸出暫存器 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="4b111-260">16 output registers in vs\_3\_sw.</span></span>                                                                                                 |
| <span data-ttu-id="4b111-261">ps \_ 3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="4b111-261">ps\_3\_sw</span></span>                                  | <span data-ttu-id="4b111-262">Interpolators 數目</span><span class="sxs-lookup"><span data-stu-id="4b111-262">Number of interpolators</span></span>              | <span data-ttu-id="4b111-263">14 (16-2) 適用于 ps 3 sw 的輸入暫存器 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="4b111-263">14(16-2) input registers for ps\_3\_sw.</span></span>                                                                                           |



 

## <a name="related-topics"></a><span data-ttu-id="4b111-264">相關主題</span><span class="sxs-lookup"><span data-stu-id="4b111-264">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4b111-265">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="4b111-265">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md)
</dt> </dl>

 

 
