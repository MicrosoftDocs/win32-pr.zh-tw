---
title: 語法變數
description: 使用下列語法規則來宣告 HLSL 變數。
ms.assetid: 684c42d1-2dd4-42e1-9cff-580edb5c6bcd
keywords:
- '外部、變數語法 (DirectX HLSL) '
- 'nointerpolation， (DirectX HLSL 的變數語法) '
- " (DirectX HLSL) 的共用、變數語法"
- 'groupshared， (DirectX HLSL 的變數語法) '
- '靜態、變數語法 (DirectX HLSL) '
- " (DirectX HLSL) 的統一、變數語法"
- 'volatile、變數語法 (DirectX HLSL) '
- " (DirectX HLSL) 的精確、變數語法"
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 446444e09b0b6aff3e0ba8ca8b12cfbf6dc94128
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826066"
---
# <a name="variable-syntax"></a><span data-ttu-id="f0226-111">語法變數</span><span class="sxs-lookup"><span data-stu-id="f0226-111">Variable Syntax</span></span>

<span data-ttu-id="f0226-112">使用下列語法規則來宣告 HLSL 變數。</span><span class="sxs-lookup"><span data-stu-id="f0226-112">Use the following syntax rules to declare HLSL variables.</span></span>

<span data-ttu-id="f0226-113">\[*儲存體 \_類別* \] \[ *類型 \_ 修飾* 詞 \] *類型名稱* \[ *索引* \] \[ *：語義* \] \[ *： Packoffset* \] \[ *： Register* \] ;   \[  \] 批註 \[*= 初始 \_值*                    \]</span><span class="sxs-lookup"><span data-stu-id="f0226-113">\[*Storage\_Class*\] \[*Type\_Modifier*\] *Type Name*\[*Index*\]     \[*: Semantic*\]     \[*: Packoffset*\]     \[*: Register*\];    \[*Annotations*\]     \[*= Initial\_Value*\]</span></span>



 

## <a name="parameters"></a><span data-ttu-id="f0226-114">參數</span><span class="sxs-lookup"><span data-stu-id="f0226-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0226-115"><span id="Storage_Class_"></span><span id="storage_class_"></span><span id="STORAGE_CLASS_"></span>*儲存 \_ 類別*</span><span class="sxs-lookup"><span data-stu-id="f0226-115"><span id="Storage_Class_"></span><span id="storage_class_"></span><span id="STORAGE_CLASS_"></span>*Storage\_Class*</span></span> 
</dt> <dd>

<span data-ttu-id="f0226-116">選擇性的儲存類別修飾詞，可提供關於變數範圍和存留期的編譯器提示;您可以依任何順序指定修飾詞。</span><span class="sxs-lookup"><span data-stu-id="f0226-116">Optional storage-class modifiers that give the compiler hints about variable scope and lifetime; the modifiers can be specified in any order.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f0226-117">值</span><span class="sxs-lookup"><span data-stu-id="f0226-117">Value</span></span></th>
<th><span data-ttu-id="f0226-118">描述</span><span class="sxs-lookup"><span data-stu-id="f0226-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f0226-119"><strong>extern</strong></span><span class="sxs-lookup"><span data-stu-id="f0226-119"><strong>extern</strong></span></span></td>
<td><span data-ttu-id="f0226-120">將全域變數標示為著色器的外部輸入;這是所有全域變數的預設標記。</span><span class="sxs-lookup"><span data-stu-id="f0226-120">Mark a global variable as an external input to the shader; this is the default marking for all global variables.</span></span> <span data-ttu-id="f0226-121">無法與 <strong>static</strong>合併。</span><span class="sxs-lookup"><span data-stu-id="f0226-121">Cannot be combined with <strong>static</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f0226-122"><strong>nointerpolation</strong></span><span class="sxs-lookup"><span data-stu-id="f0226-122"><strong>nointerpolation</strong></span></span></td>
<td><span data-ttu-id="f0226-123">在將端點著色器傳遞給圖元著色器之前，請勿先插補其輸出。</span><span class="sxs-lookup"><span data-stu-id="f0226-123">Do not interpolate the outputs of a vertex shader before passing them to a pixel shader.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f0226-124"><strong>精確</strong></span><span class="sxs-lookup"><span data-stu-id="f0226-124"><strong>precise</strong></span></span></td>
<td><span data-ttu-id="f0226-125">套用至變數的 <strong>精確</strong> 關鍵字會限制任何用來產生以下列方式指派給該變數之值的計算：</span><span class="sxs-lookup"><span data-stu-id="f0226-125">The <strong>precise</strong> keyword when applied to a variable will restrict any calculations used to produce the value assigned to that variable in the following ways:</span></span>

*   <span data-ttu-id="f0226-126">個別的作業會分開保存。</span><span class="sxs-lookup"><span data-stu-id="f0226-126">Separate operations are kept separate.</span></span> <span data-ttu-id="f0226-127">例如，mul 和 add 作業可能已融合到 mad 作業中， <strong>精確</strong> 地強制操作保持獨立。</span><span class="sxs-lookup"><span data-stu-id="f0226-127">For example, where a mul and add operation might have been fused into a mad operation, <strong>precise</strong> forces the operations to remain separate.</span></span> <span data-ttu-id="f0226-128">相反地，您必須明確地使用 mad 內建函式。</span><span class="sxs-lookup"><span data-stu-id="f0226-128">Instead, you must explicitly use the mad intrinsic function.</span></span>
*   <span data-ttu-id="f0226-129">維護作業的順序。</span><span class="sxs-lookup"><span data-stu-id="f0226-129">Order of operations are maintained.</span></span> <span data-ttu-id="f0226-130">其中的指令順序可能已隨機放置，以改善效能， <strong>精確</strong> 地確保編譯器會保留所寫入的順序。</span><span class="sxs-lookup"><span data-stu-id="f0226-130">Where the order of instructions might have been shuffled to improve performance, <strong>precise</strong> ensures that the compiler preserves the order as written.</span></span>
*   <span data-ttu-id="f0226-131">不受限於 IEEE unsafe 作業。</span><span class="sxs-lookup"><span data-stu-id="f0226-131">IEEE unsafe operations are restricted.</span></span> <span data-ttu-id="f0226-132">編譯器可能會使用的快速數學運算不會將其用於 NaN (而不是) ，而 INF (無限) 值的情況下，會 <strong>精確</strong> 地強制遵循與 NAN 和 inf 值有關的 IEEE 需求。</span><span class="sxs-lookup"><span data-stu-id="f0226-132">Where the compiler might have used fast math operations that don't account for NaN (not a number) and INF (infinite) values, <strong>precise</strong> forces IEEE requirements concerning NaN and INF values to be respected.</span></span> <span data-ttu-id="f0226-133">如果沒有 <strong>精確</strong>，則這些優化和數學運算不是 IEEE 安全的。</span><span class="sxs-lookup"><span data-stu-id="f0226-133">Without <strong>precise</strong>, these optimizations and mathematical operations are not IEEE safe.</span></span>
*   <span data-ttu-id="f0226-134"><strong>精確</strong>地限定變數並不會讓使用變數<strong>精確</strong>的作業。</span><span class="sxs-lookup"><span data-stu-id="f0226-134">Qualifying a variable <strong>precise</strong> doesn't make operations that use the variable <strong>precise</strong>.</span></span> <span data-ttu-id="f0226-135">由於 <strong>精確</strong> 地只會傳播至參與指派給 <strong>精確</strong>變數之值的作業，所以正確地 <strong>精確</strong> 地計算所需的計算可能會很困難，因此我們建議您在宣告著色器時 <strong>，直接將</strong> 著色器輸出標記為明確地，不論是在結構欄位上，或是在輸入函式的傳回型別上。</span><span class="sxs-lookup"><span data-stu-id="f0226-135">Since <strong>precise</strong> propagates only to operations that contribute to the values that are assigned to the <strong>precise</strong>-qualified variable, correctly making desired calculations <strong>precise</strong> can be tricky, so we recommended that you mark the shader outputs <strong>precise</strong> directly where you declare them, whether that's on a structure field, or on an output parameter, or the return type of the entry function.</span></span>

<span data-ttu-id="f0226-136">以這種方式控制優化的能力，會藉由停用可能會影響最終結果的優化（因為累積的精確度差異差異），來維持已修改之輸出變數的結果 invariance。</span><span class="sxs-lookup"><span data-stu-id="f0226-136">The ability to control optimizations in this way maintains result invariance for the modified output variable by disabling optimizations that might affect final results due to differences in accumulated precision differences.</span></span> <span data-ttu-id="f0226-137">當您想要讓鑲嵌式的著色器維持水緊密的 patch 接縫，或比對多個行程的深度值時，它會很有用。</span><span class="sxs-lookup"><span data-stu-id="f0226-137">It is useful when you want shaders for tessellation to maintain water-tight patch seams or match depth values over multiple passes.</span></span>

<span data-ttu-id="f0226-138">[範例程式碼](https://github.com/microsoft/DirectXShaderCompiler/blob/master/tools/clang/test/HLSLFileCheck/hlsl/types/modifiers/precise/precise4.hlsl)：</span><span class="sxs-lookup"><span data-stu-id="f0226-138">[Sample code](https://github.com/microsoft/DirectXShaderCompiler/blob/master/tools/clang/test/HLSLFileCheck/hlsl/types/modifiers/precise/precise4.hlsl):</span></span> 
```HLSL
matrix g_mWorldViewProjection;
void main(in float3 InPos : Position, out precise float4 OutPos : SV_Position)
{
  // operation is precise because it contributes to the precise parameter OutPos
  OutPos = mul( float4( InPos, 1.0 ), g_mWorldViewProjection );
}
```
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="f0226-139"><strong>共用</strong></span><span class="sxs-lookup"><span data-stu-id="f0226-139"><strong>shared</strong></span></span></td>
<td><span data-ttu-id="f0226-140">標示變數以在效果之間共用;這是編譯器的提示。</span><span class="sxs-lookup"><span data-stu-id="f0226-140">Mark a variable for sharing between effects; this is a hint to the compiler.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f0226-141"><strong>groupshared</strong></span><span class="sxs-lookup"><span data-stu-id="f0226-141"><strong>groupshared</strong></span></span></td>
<td><span data-ttu-id="f0226-142">標記執行緒群組的變數-計算著色器的共用記憶體。</span><span class="sxs-lookup"><span data-stu-id="f0226-142">Mark a variable for thread-group-shared memory for compute shaders.</span></span> <span data-ttu-id="f0226-143">在 D3D10 中，所有具有 groupshared 儲存類別之變數的總大小上限為16kb，D3D11 中的大小上限為32kb。</span><span class="sxs-lookup"><span data-stu-id="f0226-143">In D3D10 the maximum total size of all variables with the groupshared storage class is 16kb, in D3D11 the maximum size is 32kb.</span></span> <span data-ttu-id="f0226-144">請參閱範例。</span><span class="sxs-lookup"><span data-stu-id="f0226-144">See examples.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f0226-145"><strong>static</strong></span><span class="sxs-lookup"><span data-stu-id="f0226-145"><strong>static</strong></span></span></td>
<td><span data-ttu-id="f0226-146">標記本機變數，使其初始化一次，並在函式呼叫之間保存。</span><span class="sxs-lookup"><span data-stu-id="f0226-146">Mark a local variable so that it is initialized one time and persists between function calls.</span></span> <span data-ttu-id="f0226-147">如果宣告不包含初始化運算式，則值會設定為零。</span><span class="sxs-lookup"><span data-stu-id="f0226-147">If the declaration does not include an initializer, the value is set to zero.</span></span> <span data-ttu-id="f0226-148">應用程式看不到標記為 <strong>static</strong> 的全域變數。</span><span class="sxs-lookup"><span data-stu-id="f0226-148">A global variable marked <strong>static</strong> is not visible to an application.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f0226-149"><strong>uniform</strong></span><span class="sxs-lookup"><span data-stu-id="f0226-149"><strong>uniform</strong></span></span></td>
<td><span data-ttu-id="f0226-150">在著色器 (（例如，頂點著色器中的材質色彩）中，標記其資料為常數的變數) ;全域變數預設會被視為 <strong>統一</strong> 。</span><span class="sxs-lookup"><span data-stu-id="f0226-150">Mark a variable whose data is constant throughout the execution of a shader (such as a material color in a vertex shader); global variables are considered <strong>uniform</strong> by default.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f0226-151"><strong>volatile</strong></span><span class="sxs-lookup"><span data-stu-id="f0226-151"><strong>volatile</strong></span></span></td>
<td><span data-ttu-id="f0226-152">標記經常變更的變數;這是編譯器的提示。</span><span class="sxs-lookup"><span data-stu-id="f0226-152">Mark a variable that changes frequently; this is a hint to the compiler.</span></span> <span data-ttu-id="f0226-153">這個儲存類別修飾詞只適用于本機變數。</span><span class="sxs-lookup"><span data-stu-id="f0226-153">This storage class modifier only applies to a local variable.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="f0226-154">HLSL 編譯器目前會忽略這個儲存類別修飾詞。</span><span class="sxs-lookup"><span data-stu-id="f0226-154">The HLSL compiler currently ignores this storage class modifier.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="f0226-155"><span id="Type_Modifier"></span><span id="type_modifier"></span><span id="TYPE_MODIFIER"></span>*類型 \_ 修飾詞*</span><span class="sxs-lookup"><span data-stu-id="f0226-155"><span id="Type_Modifier"></span><span id="type_modifier"></span><span id="TYPE_MODIFIER"></span>*Type\_Modifier*</span></span>
</dt> <dd>

<span data-ttu-id="f0226-156">選擇性的變數類型修飾詞。</span><span class="sxs-lookup"><span data-stu-id="f0226-156">Optional variable-type modifier.</span></span>



| <span data-ttu-id="f0226-157">值</span><span class="sxs-lookup"><span data-stu-id="f0226-157">Value</span></span>             | <span data-ttu-id="f0226-158">描述</span><span class="sxs-lookup"><span data-stu-id="f0226-158">Description</span></span>                                                                                                                                                                                                                                  |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0226-159">**const**</span><span class="sxs-lookup"><span data-stu-id="f0226-159">**const**</span></span>         | <span data-ttu-id="f0226-160">標記無法由著色器變更的變數，因此必須在變數宣告中初始化。</span><span class="sxs-lookup"><span data-stu-id="f0226-160">Mark a variable that cannot be changed by a shader, therefore, it must be initialized in the variable declaration.</span></span> <span data-ttu-id="f0226-161">全域變數預設會被視為 **const** (藉由提供編譯器) 的/Gec 旗標來抑制此行為。</span><span class="sxs-lookup"><span data-stu-id="f0226-161">Global variables are considered **const** by default (suppress this behavior by supplying the /Gec flag to the compiler).</span></span> |
| <span data-ttu-id="f0226-162">**資料列 \_ 主要**</span><span class="sxs-lookup"><span data-stu-id="f0226-162">**row\_major**</span></span>    | <span data-ttu-id="f0226-163">標記將四個元件儲存在單一資料列中的變數，讓它們可以儲存在單一常數暫存器中。</span><span class="sxs-lookup"><span data-stu-id="f0226-163">Mark a variable that stores four components in a single row so they can be stored in a single constant register.</span></span>                                                                                                                             |
| <span data-ttu-id="f0226-164">**資料行 \_ 主要**</span><span class="sxs-lookup"><span data-stu-id="f0226-164">**column\_major**</span></span> | <span data-ttu-id="f0226-165">標記將4個元件儲存在單一資料行中的變數，以優化矩陣數學。</span><span class="sxs-lookup"><span data-stu-id="f0226-165">Mark a variable that stores 4 components in a single column to optimize matrix math.</span></span>                                                                                                                                                         |



 

> [!Note]  
> <span data-ttu-id="f0226-166">如果您未指定類型修飾詞值，編譯器會使用 [資料 **行 \_ 主要** ] 作為預設值。</span><span class="sxs-lookup"><span data-stu-id="f0226-166">If you do not specify a type-modifier value, the compiler uses **column\_major** as the default value.</span></span>

 

</dd> <dt>

<span data-ttu-id="f0226-167"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>*類型*</span><span class="sxs-lookup"><span data-stu-id="f0226-167"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>*Type*</span></span>
</dt> <dd>

<span data-ttu-id="f0226-168">資料類型中所列的任何 HLSL 類型 [ (DIRECTX HLSL) ](dx-graphics-hlsl-data-types.md)。</span><span class="sxs-lookup"><span data-stu-id="f0226-168">Any HLSL type listed in [Data Types (DirectX HLSL)](dx-graphics-hlsl-data-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="f0226-169"><span id="Name_Index_"></span><span id="name_index_"></span><span id="NAME_INDEX_"></span>*名稱* \[*索引*\]</span><span class="sxs-lookup"><span data-stu-id="f0226-169"><span id="Name_Index_"></span><span id="name_index_"></span><span id="NAME_INDEX_"></span>*Name*\[*Index*\]</span></span>
</dt> <dd>

<span data-ttu-id="f0226-170">可唯一識別著色器變數的 ASCII 字串。</span><span class="sxs-lookup"><span data-stu-id="f0226-170">ASCII string that uniquely identifies a shader variable.</span></span> <span data-ttu-id="f0226-171">若要定義選擇性陣列，請使用 **index** 作為陣列大小，也就是正整數 = 1。</span><span class="sxs-lookup"><span data-stu-id="f0226-171">To define an optional array, use **index** for the array size, which is a positive integer = 1.</span></span>

</dd> <dt>

<span data-ttu-id="f0226-172"><span id="Semantic"></span><span id="semantic"></span><span id="SEMANTIC"></span>*語義*</span><span class="sxs-lookup"><span data-stu-id="f0226-172"><span id="Semantic"></span><span id="semantic"></span><span id="SEMANTIC"></span>*Semantic*</span></span>
</dt> <dd>

<span data-ttu-id="f0226-173">選擇性的參數使用方式資訊，由編譯器用來連結著色器的輸入和輸出。</span><span class="sxs-lookup"><span data-stu-id="f0226-173">Optional parameter-usage information, used by the compiler to link shader inputs and outputs.</span></span> <span data-ttu-id="f0226-174">頂點和圖元著色器有數個預先定義的 [語義](dx-graphics-hlsl-semantics.md) 。</span><span class="sxs-lookup"><span data-stu-id="f0226-174">There are several predefined [semantics](dx-graphics-hlsl-semantics.md) for vertex and pixel shaders.</span></span> <span data-ttu-id="f0226-175">編譯器會忽略語義，除非宣告于全域變數上，或是傳遞至著色器的參數。</span><span class="sxs-lookup"><span data-stu-id="f0226-175">The compiler ignores semantics unless they are declared on a global variable, or a parameter passed into a shader.</span></span>

</dd> <dt>

<span data-ttu-id="f0226-176"><span id="Packoffset"></span><span id="packoffset"></span><span id="PACKOFFSET"></span>*Packoffset*</span><span class="sxs-lookup"><span data-stu-id="f0226-176"><span id="Packoffset"></span><span id="packoffset"></span><span id="PACKOFFSET"></span>*Packoffset*</span></span>
</dt> <dd>

<span data-ttu-id="f0226-177">手動封裝著色器常數的選擇性關鍵字。</span><span class="sxs-lookup"><span data-stu-id="f0226-177">Optional keyword for manually packing shader constants.</span></span> <span data-ttu-id="f0226-178">請參閱 [packoffset (DIRECTX HLSL) ](dx-graphics-hlsl-variable-packoffset.md)。</span><span class="sxs-lookup"><span data-stu-id="f0226-178">See [packoffset (DirectX HLSL)](dx-graphics-hlsl-variable-packoffset.md).</span></span>

</dd> <dt>

<span data-ttu-id="f0226-179"><span id="Register"></span><span id="register"></span><span id="REGISTER"></span>*註冊*</span><span class="sxs-lookup"><span data-stu-id="f0226-179"><span id="Register"></span><span id="register"></span><span id="REGISTER"></span>*Register*</span></span>
</dt> <dd>

<span data-ttu-id="f0226-180">選擇性的關鍵字，可將著色器變數手動指派給特定的註冊。</span><span class="sxs-lookup"><span data-stu-id="f0226-180">Optional keyword for manually assigning a shader variable to a particular register.</span></span> <span data-ttu-id="f0226-181">請參閱 [註冊 (DIRECTX HLSL) ](dx-graphics-hlsl-variable-register.md)。</span><span class="sxs-lookup"><span data-stu-id="f0226-181">See [register (DirectX HLSL)](dx-graphics-hlsl-variable-register.md).</span></span>

</dd> <dt>

<span data-ttu-id="f0226-182"><span id="Annotation_s_"></span><span id="annotation_s_"></span><span id="ANNOTATION_S_"></span>*注釋 (s)*</span><span class="sxs-lookup"><span data-stu-id="f0226-182"><span id="Annotation_s_"></span><span id="annotation_s_"></span><span id="ANNOTATION_S_"></span>*Annotation(s)*</span></span>
</dt> <dd>

<span data-ttu-id="f0226-183">附加至全域變數的選擇性中繼資料（以字串形式）。</span><span class="sxs-lookup"><span data-stu-id="f0226-183">Optional metadata, in the form of a string, attached to a global variable.</span></span> <span data-ttu-id="f0226-184">批註會由效果架構使用，並由 HLSL 忽略;若要查看更詳細的語法，請參閱 [批註語法](/windows/desktop/direct3d10/d3d10-effect-annotation-syntax)。</span><span class="sxs-lookup"><span data-stu-id="f0226-184">An annotation is used by the effect framework and ignored by HLSL; to see more detailed syntax, see [annotation syntax](/windows/desktop/direct3d10/d3d10-effect-annotation-syntax).</span></span>

</dd> <dt>

<span data-ttu-id="f0226-185"><span id="Initial_Value"></span><span id="initial_value"></span><span id="INITIAL_VALUE"></span>*初始值 \_*</span><span class="sxs-lookup"><span data-stu-id="f0226-185"><span id="Initial_Value"></span><span id="initial_value"></span><span id="INITIAL_VALUE"></span>*Initial\_Value*</span></span>
</dt> <dd>

<span data-ttu-id="f0226-186">選擇性初始值 (s) ;值的數目應符合 *型* 別中的元件數目。</span><span class="sxs-lookup"><span data-stu-id="f0226-186">Optional initial value(s); the number of values should match the number of components in *Type*.</span></span> <span data-ttu-id="f0226-187">每個標記為 **extern** 的全域變數都必須使用常值來初始化;標記為 **static** 的每個變數都必須使用常數進行初始化。</span><span class="sxs-lookup"><span data-stu-id="f0226-187">Each global variable marked **extern** must be initialized with a literal value; each variable marked **static** must be initialized with a constant.</span></span>

<span data-ttu-id="f0226-188">未標記為 **static** 或 **extern** 的全域變數不會編譯成著色器。</span><span class="sxs-lookup"><span data-stu-id="f0226-188">Global variables that are not marked **static** or **extern** are not compiled into the shader.</span></span> <span data-ttu-id="f0226-189">編譯器不會自動設定全域變數的預設值，也無法在優化中使用它們。</span><span class="sxs-lookup"><span data-stu-id="f0226-189">The compiler does not automatically set default values for global variables and cannot use them in optimizations.</span></span> <span data-ttu-id="f0226-190">若要初始化這種類型的全域變數，請使用反映來取得其值，然後將值複製到常數緩衝區。</span><span class="sxs-lookup"><span data-stu-id="f0226-190">To initialize this type of global variable, use reflection to get its value and then copy the value to a constant buffer.</span></span> <span data-ttu-id="f0226-191">例如，您可以使用 [**ID3D11ShaderReflection：： GetVariableByName**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getvariablebyname)方法來取得變數、使用 [**ID3D11ShaderReflectionVariable：： GetDesc**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflectionvariable-getdesc)方法取得著色器變數的描述，以及從 [**D3D11 \_ 著色器 \_ 變數 \_ DESC**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_shader_variable_desc)結構的 **DefaultValue** 成員取得初始值。</span><span class="sxs-lookup"><span data-stu-id="f0226-191">For example, you can use the [**ID3D11ShaderReflection::GetVariableByName**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getvariablebyname) method to get the variable, use the [**ID3D11ShaderReflectionVariable::GetDesc**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflectionvariable-getdesc) method to get the shader-variable description, and get the initial value from the **DefaultValue** member of the [**D3D11\_SHADER\_VARIABLE\_DESC**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_shader_variable_desc) structure.</span></span> <span data-ttu-id="f0226-192">若要將值複製到常數緩衝區，您必須確定已使用 CPU 寫入存取建立緩衝區 ([**D3D11 \_ cpu \_ 存取 \_ 寫入**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_cpu_access_flag)) 。</span><span class="sxs-lookup"><span data-stu-id="f0226-192">To copy the value to the constant buffer, you must ensure that the buffer was created with CPU write access ([**D3D11\_CPU\_ACCESS\_WRITE**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_cpu_access_flag)).</span></span> <span data-ttu-id="f0226-193">如需如何建立常數緩衝區的詳細資訊，請參閱 [如何：建立常數緩衝區](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-constant-how-to)。</span><span class="sxs-lookup"><span data-stu-id="f0226-193">For more information about how to create a constant buffer, see [How to: Create a Constant Buffer](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-constant-how-to).</span></span>

<span data-ttu-id="f0226-194">您也可以使用 [效果架構](../direct3d11/d3d11-graphics-programming-guide-effects.md) 來自動處理反映和設定初始值。</span><span class="sxs-lookup"><span data-stu-id="f0226-194">You can also use the [effects framework](../direct3d11/d3d11-graphics-programming-guide-effects.md) to automatically process the reflecting and setting the initial value.</span></span> <span data-ttu-id="f0226-195">例如，您可以使用 [**ID3DX11EffectPass：： Apply**](/windows/desktop/direct3d11/id3dx11effectpass-apply) 方法。</span><span class="sxs-lookup"><span data-stu-id="f0226-195">For example, you can use the [**ID3DX11EffectPass::Apply**](/windows/desktop/direct3d11/id3dx11effectpass-apply) method.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="f0226-196">範例</span><span class="sxs-lookup"><span data-stu-id="f0226-196">Examples</span></span>

<span data-ttu-id="f0226-197">以下是一些著色器變數宣告的範例。</span><span class="sxs-lookup"><span data-stu-id="f0226-197">Here are several examples of shader-variable declarations.</span></span>


```
float fVar;
```




```
float4 color;
float fVar = 3.1f;

int iVar[3];

int iVar[3] = {1,2,3};

uniform float4 position : SV_POSITION; 
const float4 lightDirection = {0,0,1};
      
```



### <a name="group-shared"></a><span data-ttu-id="f0226-198">群組共用</span><span class="sxs-lookup"><span data-stu-id="f0226-198">Group Shared</span></span>

<span data-ttu-id="f0226-199">HLSL 可讓計算著色器的執行緒透過共用記憶體交換值。</span><span class="sxs-lookup"><span data-stu-id="f0226-199">HLSL enables threads of a compute shader to exchange values via shared memory.</span></span> <span data-ttu-id="f0226-200">HLSL 提供關卡基本類型（例如 [**GroupMemoryBarrierWithGroupSync**](groupmemorybarrierwithgroupsync.md)），依此類推以確保在著色器中讀取和寫入共用記憶體的正確順序，並避免資料競爭。</span><span class="sxs-lookup"><span data-stu-id="f0226-200">HLSL provides barrier primitives such as [**GroupMemoryBarrierWithGroupSync**](groupmemorybarrierwithgroupsync.md), and so on to ensure the correct ordering of reads and writes to shared memory in the shader and to avoid data races.</span></span>

> [!Note]  
> <span data-ttu-id="f0226-201">硬體會以群組 (warps 或 wave) 的方式來執行執行緒，而在只同步屬於相同群組的執行緒是正確的情況下，有時可能會省略關卡同步處理來提高效能。</span><span class="sxs-lookup"><span data-stu-id="f0226-201">Hardware executes threads in groups (warps or wave-fronts), and barrier synchronization can sometimes be omitted to increase performance when only synchronizing threads that belong to the same group is correct.</span></span> <span data-ttu-id="f0226-202">但基於下列原因，我們強烈建議您省略：</span><span class="sxs-lookup"><span data-stu-id="f0226-202">But we highly discourage this omission for these reasons:</span></span>
>
> -   <span data-ttu-id="f0226-203">這項省略會導致無法移植的程式碼，這可能無法在某些硬體上運作，也不適用於通常以較小的群組執行執行緒的軟體 rasterizers。</span><span class="sxs-lookup"><span data-stu-id="f0226-203">This omission results in non-portable code, which might not work on some hardware and doesn't work on software rasterizers that typically execute threads in smaller groups.</span></span>
> -   <span data-ttu-id="f0226-204">相較于使用所有線程屏障，您可能會使用此省略來達成的效能改進。</span><span class="sxs-lookup"><span data-stu-id="f0226-204">The performance improvements that you might achieve with this omission will be minor compared to using all-thread barrier.</span></span>

 

<span data-ttu-id="f0226-205">在 Direct3D 10 中，寫入至 **groupshared** 時，不會同步處理執行緒，這表示每個執行緒會限制為數組中的單一位置以進行寫入。</span><span class="sxs-lookup"><span data-stu-id="f0226-205">In Direct3D 10 there is no synchronization of threads when writing to **groupshared**, so this means that each thread is limited to a single location in an array for writing.</span></span> <span data-ttu-id="f0226-206">寫入時，請使用 [SV \_ GroupIndex](dx-graphics-hlsl-semantics.md) 系統值來編制此陣列的索引，以確保兩個執行緒都不會發生衝突。</span><span class="sxs-lookup"><span data-stu-id="f0226-206">Use the [SV\_GroupIndex](dx-graphics-hlsl-semantics.md) system value to index into this array when writing to ensure that no two threads can collide.</span></span> <span data-ttu-id="f0226-207">就讀取而言，所有線程都可以存取整個陣列以進行讀取。</span><span class="sxs-lookup"><span data-stu-id="f0226-207">In terms of reading, all threads have access to the entire array for reading.</span></span>


```
struct GSData
{
    float4 Color;
    float Factor;
}

groupshared GSData data[5*5*1];

[numthreads(5,5,1)]
void main( uint index : SV_GroupIndex )
{
    data[index].Color = (float4)0;
    data[index].Factor = 2.0f;
    GroupMemoryBarrierWithGroupSync();
    ...
}
```



### <a name="packing"></a><span data-ttu-id="f0226-208">包裝</span><span class="sxs-lookup"><span data-stu-id="f0226-208">Packing</span></span>

<span data-ttu-id="f0226-209">封裝大小夠大的向量和純量子元件，以防止 boundarys 的註冊。</span><span class="sxs-lookup"><span data-stu-id="f0226-209">Pack subcomponents of vectors and scalars whose size is large enough to prevent crossing register boundarys.</span></span> <span data-ttu-id="f0226-210">例如，這些都是有效的：</span><span class="sxs-lookup"><span data-stu-id="f0226-210">For example, these are all valid:</span></span>


```
cbuffer MyBuffer
{
    float4 Element1 : packoffset(c0);
    float1 Element2 : packoffset(c1);
    float1 Element3 : packoffset(c1.y);
}
        
```



<span data-ttu-id="f0226-211">無法混合封裝類型。</span><span class="sxs-lookup"><span data-stu-id="f0226-211">Cannot mix packing types.</span></span>

<span data-ttu-id="f0226-212">就像 register 關鍵字一樣，packoffset 可以是特定的目標。</span><span class="sxs-lookup"><span data-stu-id="f0226-212">Like the register keyword, a packoffset can be target specific.</span></span> <span data-ttu-id="f0226-213">子元件封裝僅適用于 packoffset 關鍵字，而非 register 關鍵字。</span><span class="sxs-lookup"><span data-stu-id="f0226-213">Subcomponent packing is only available with the packoffset keyword, not the register keyword.</span></span> <span data-ttu-id="f0226-214">在 cbuffer 宣告中，Direct3D 10 目標會忽略 register 關鍵字，因為它會被假設為跨平臺相容性。</span><span class="sxs-lookup"><span data-stu-id="f0226-214">Inside a cbuffer declaration, the register keyword is ignored for Direct3D 10 targets as it is assumed to be for cross-platform compatibility.</span></span>

<span data-ttu-id="f0226-215">封裝的元素可能會重迭，而編譯器將不會發出任何錯誤或警告。</span><span class="sxs-lookup"><span data-stu-id="f0226-215">Packed elements may overlap and the compiler will give no error or warning.</span></span> <span data-ttu-id="f0226-216">在此範例中，Element2 和 Element3 會與 Element1. x 和 Element1 重迭。</span><span class="sxs-lookup"><span data-stu-id="f0226-216">In this example, Element2 and Element3 will overlap with Element1.x and Element1.y.</span></span>


```
cbuffer MyBuffer
{
    float4 Element1 : packoffset(c0);
    float1 Element2 : packoffset(c0);
    float1 Element3 : packoffset(c0.y);
}
        
```



<span data-ttu-id="f0226-217">使用 packoffset 的範例是： [HLSLWithoutFX10 範例](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx)。</span><span class="sxs-lookup"><span data-stu-id="f0226-217">A sample that uses packoffset is: [HLSLWithoutFX10 Sample](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f0226-218">相關主題</span><span class="sxs-lookup"><span data-stu-id="f0226-218">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f0226-219"> (DirectX HLSL) 的變數 </span><span class="sxs-lookup"><span data-stu-id="f0226-219">Variables (DirectX HLSL)</span></span>](dx-graphics-hlsl-variables.md)
</dt> </dl>

 

