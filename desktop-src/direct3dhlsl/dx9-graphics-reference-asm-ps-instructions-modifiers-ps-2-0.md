---
title: Ps_2_0 和更新版本的修飾詞
description: 指令修飾詞會在將指令寫入目的地登錄之前，先影響指令的結果。
ms.assetid: eb2a8a1f-51bc-4516-b679-a8fb25b0dda0
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7141576b80b7a05a3e61ee9a98fa36958b1d5530
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840868"
---
# <a name="modifiers-for-ps_2_0-and-above"></a><span data-ttu-id="c5bcc-103">Ps \_ 2 \_ 0 和更新版本的修飾詞</span><span class="sxs-lookup"><span data-stu-id="c5bcc-103">Modifiers for ps\_2\_0 and Above</span></span>

<span data-ttu-id="c5bcc-104">指令修飾詞會在將指令寫入目的地登錄之前，先影響指令的結果。</span><span class="sxs-lookup"><span data-stu-id="c5bcc-104">Instruction modifiers affect the result of the instruction before it is written into the destination register.</span></span>

<span data-ttu-id="c5bcc-105">本章節包含圖元著色器第2版和更新版本所執行之指令修飾詞的參考資訊 \_ 。</span><span class="sxs-lookup"><span data-stu-id="c5bcc-105">This section contains reference information for the instruction modifiers implemented by pixel shader version 2\_0 and above.</span></span>



| <span data-ttu-id="c5bcc-106">Name</span><span class="sxs-lookup"><span data-stu-id="c5bcc-106">Name</span></span>                                     | <span data-ttu-id="c5bcc-107">語法</span><span class="sxs-lookup"><span data-stu-id="c5bcc-107">Syntax</span></span>     | <span data-ttu-id="c5bcc-108">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c5bcc-108">2\_0</span></span> | <span data-ttu-id="c5bcc-109">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="c5bcc-109">2\_x</span></span> | <span data-ttu-id="c5bcc-110">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="c5bcc-110">2\_sw</span></span> | <span data-ttu-id="c5bcc-111">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c5bcc-111">3\_0</span></span> | <span data-ttu-id="c5bcc-112">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="c5bcc-112">3\_sw</span></span> |
|------------------------------------------|------------|------|------|-------|------|-------|
| [<span data-ttu-id="c5bcc-113">質心</span><span class="sxs-lookup"><span data-stu-id="c5bcc-113">Centroid</span></span>](#centroid)                    | <span data-ttu-id="c5bcc-114">\_質心</span><span class="sxs-lookup"><span data-stu-id="c5bcc-114">\_centroid</span></span> | <span data-ttu-id="c5bcc-115">x</span><span class="sxs-lookup"><span data-stu-id="c5bcc-115">x</span></span>    | <span data-ttu-id="c5bcc-116">x</span><span class="sxs-lookup"><span data-stu-id="c5bcc-116">x</span></span>    | <span data-ttu-id="c5bcc-117">x</span><span class="sxs-lookup"><span data-stu-id="c5bcc-117">x</span></span>     | <span data-ttu-id="c5bcc-118">x</span><span class="sxs-lookup"><span data-stu-id="c5bcc-118">x</span></span>    | <span data-ttu-id="c5bcc-119">x</span><span class="sxs-lookup"><span data-stu-id="c5bcc-119">x</span></span>     |
| [<span data-ttu-id="c5bcc-120">部分有效 \_ 位數</span><span class="sxs-lookup"><span data-stu-id="c5bcc-120">Partial\_Precision</span></span>](#partial-precision) | <span data-ttu-id="c5bcc-121">\_Pp</span><span class="sxs-lookup"><span data-stu-id="c5bcc-121">\_pp</span></span>       | <span data-ttu-id="c5bcc-122">x</span><span class="sxs-lookup"><span data-stu-id="c5bcc-122">x</span></span>    | <span data-ttu-id="c5bcc-123">x</span><span class="sxs-lookup"><span data-stu-id="c5bcc-123">x</span></span>    | <span data-ttu-id="c5bcc-124">x</span><span class="sxs-lookup"><span data-stu-id="c5bcc-124">x</span></span>     | <span data-ttu-id="c5bcc-125">x</span><span class="sxs-lookup"><span data-stu-id="c5bcc-125">x</span></span>    | <span data-ttu-id="c5bcc-126">x</span><span class="sxs-lookup"><span data-stu-id="c5bcc-126">x</span></span>     |
| [<span data-ttu-id="c5bcc-127">飽和</span><span class="sxs-lookup"><span data-stu-id="c5bcc-127">Saturate</span></span>](#saturate)                    | <span data-ttu-id="c5bcc-128">\_坐</span><span class="sxs-lookup"><span data-stu-id="c5bcc-128">\_sat</span></span>      | <span data-ttu-id="c5bcc-129">x</span><span class="sxs-lookup"><span data-stu-id="c5bcc-129">x</span></span>    | <span data-ttu-id="c5bcc-130">x</span><span class="sxs-lookup"><span data-stu-id="c5bcc-130">x</span></span>    | <span data-ttu-id="c5bcc-131">x</span><span class="sxs-lookup"><span data-stu-id="c5bcc-131">x</span></span>     | <span data-ttu-id="c5bcc-132">x</span><span class="sxs-lookup"><span data-stu-id="c5bcc-132">x</span></span>    | <span data-ttu-id="c5bcc-133">x</span><span class="sxs-lookup"><span data-stu-id="c5bcc-133">x</span></span>     |



 

## <a name="centroid"></a><span data-ttu-id="c5bcc-134">質心</span><span class="sxs-lookup"><span data-stu-id="c5bcc-134">Centroid</span></span>

<span data-ttu-id="c5bcc-135">距心修飾詞是選擇性的修飾詞，可在基本範圍未涵蓋多取樣圖元中心時，個屬性內插補點。</span><span class="sxs-lookup"><span data-stu-id="c5bcc-135">The centroid modifier is an optional modifier that clamps attribute interpolation within the range of the primitive when a multisample pixel center is not covered by the primitive.</span></span> <span data-ttu-id="c5bcc-136">這可以在 [距心取樣](https://msdn.microsoft.com/library/ee415231(VS.85).aspx)中看到。</span><span class="sxs-lookup"><span data-stu-id="c5bcc-136">This can be seen in [Centroid Sampling](https://msdn.microsoft.com/library/ee415231(VS.85).aspx).</span></span>

<span data-ttu-id="c5bcc-137">您可以將距心修飾詞套用至元件指令，如下所示：</span><span class="sxs-lookup"><span data-stu-id="c5bcc-137">You can apply the centroid modifier to an assembly instruction as shown here:</span></span>


```
dcl_texcoord0_centroid v0
```



<span data-ttu-id="c5bcc-138">您也可以將距心修飾詞套用至語義，如下所示：</span><span class="sxs-lookup"><span data-stu-id="c5bcc-138">You can also apply the centroid modifier to a semantic as shown here:</span></span>


```
float4 TexturePointCentroidPS( float4 TexCoord : TEXCOORD0_centroid ) : COLOR0
{
    return tex2D( PointSampler, TexCoord );
}
```



<span data-ttu-id="c5bcc-139">此外，以色彩語義宣告的任何 [輸入色彩](dx9-graphics-reference-asm-ps-registers-input-color.md) 暫存器 (v \#) 都會自動套用距心。</span><span class="sxs-lookup"><span data-stu-id="c5bcc-139">In addition, any [Input Color Register](dx9-graphics-reference-asm-ps-registers-input-color.md) (v\#) declared with a color semantic will automatically have centroid applied.</span></span> <span data-ttu-id="c5bcc-140">從距心取樣的屬性計算而來的漸層不保證正確。</span><span class="sxs-lookup"><span data-stu-id="c5bcc-140">Gradients computed from attributes that are centroid sampled are not guaranteed to be accurate.</span></span>

## <a name="partial-precision"></a><span data-ttu-id="c5bcc-141">部分有效位數</span><span class="sxs-lookup"><span data-stu-id="c5bcc-141">Partial Precision</span></span>

<span data-ttu-id="c5bcc-142">部分精確度指令修飾詞 (\_ pp) 指出部分有效位數是可接受的，但前提是基礎實作為支援的區域。</span><span class="sxs-lookup"><span data-stu-id="c5bcc-142">The partial precision instruction modifier (\_pp) indicates areas where partial precision is acceptable, provided that the underlying implementation supports it.</span></span> <span data-ttu-id="c5bcc-143">您一律可以自由地忽略修飾詞，並以完整的精確度執行受影響的作業。</span><span class="sxs-lookup"><span data-stu-id="c5bcc-143">Implementations are always free to ignore the modifier and perform the affected operations in full precision.</span></span>

<span data-ttu-id="c5bcc-144">\_Pp 修飾詞可以出現在兩個內容中：</span><span class="sxs-lookup"><span data-stu-id="c5bcc-144">The \_pp modifier can occur in two contexts:</span></span>

-   <span data-ttu-id="c5bcc-145">在紋理座標宣告上，以部分精確度形式啟用將材質座標傳遞給圖元著色器。</span><span class="sxs-lookup"><span data-stu-id="c5bcc-145">On a texture coordinate declaration to enable passing texture coordinates to the pixel shader in partial-precision form.</span></span> <span data-ttu-id="c5bcc-146">例如，這可讓您使用材質座標將色彩資料轉送至圖元著色器，但在某些實作為中，部分精確度可能會比完整有效位數更快。</span><span class="sxs-lookup"><span data-stu-id="c5bcc-146">This allows, for example, the use of texture coordinates to relay color data to the pixel shader, which may be faster with partial precision than with full precision in some implementations.</span></span> <span data-ttu-id="c5bcc-147">如果沒有這個修飾詞，材質座標必須以完整的精確度傳遞。</span><span class="sxs-lookup"><span data-stu-id="c5bcc-147">In the absence of this modifier, texture coordinates must be passed in full precision.</span></span>
-   <span data-ttu-id="c5bcc-148">包含材質載入指示的任何指示。</span><span class="sxs-lookup"><span data-stu-id="c5bcc-148">On any instruction including texture load instructions.</span></span> <span data-ttu-id="c5bcc-149">這表示可以執行實作為部分有效位數的指令，並儲存部分精確度結果。</span><span class="sxs-lookup"><span data-stu-id="c5bcc-149">This indicates that the implementation is allowed to execute the instruction with partial precision and store a partial precision result.</span></span> <span data-ttu-id="c5bcc-150">如果沒有明確的修飾詞，就必須以完整的精確度來執行指令， (無論輸入的精確度) 為何。</span><span class="sxs-lookup"><span data-stu-id="c5bcc-150">In the absence of an explicit modifier, the instruction must be performed at full precision (regardless of the input precision).</span></span>

<span data-ttu-id="c5bcc-151">範例：</span><span class="sxs-lookup"><span data-stu-id="c5bcc-151">Examples:</span></span>


```
dcl_texcoord0_pp t1
cmp_pp r0, r1, r2, r3
```



## <a name="saturate"></a><span data-ttu-id="c5bcc-152">飽和度</span><span class="sxs-lookup"><span data-stu-id="c5bcc-152">Saturate</span></span>

<span data-ttu-id="c5bcc-153">飽和的指令修飾詞 (\_ sat) 在寫入至目的地暫存器之前，會將指示結果) 到範圍 \[ 0、1，以 (或個 \] 。</span><span class="sxs-lookup"><span data-stu-id="c5bcc-153">The saturate instruction modifier (\_sat) saturates (or clamps) the instruction result to the range \[0, 1\] before writing to the destination register.</span></span>

<span data-ttu-id="c5bcc-154">\_Sat 指令修飾詞可以搭配[frc-ps](frc---ps.md)、 [sincos](sincos---ps.md)和任何 tex 指令以外的任何指令使用 \* 。</span><span class="sxs-lookup"><span data-stu-id="c5bcc-154">The \_sat instruction modifier can be used with any instruction except [frc - ps](frc---ps.md), [sincos - ps](sincos---ps.md), and any tex\* instructions.</span></span>

<span data-ttu-id="c5bcc-155">若是 ps \_ 2 \_ 0、ps \_ 2 \_ x 和 ps \_ 2 \_ sw，則 \_ 不能使用 sat 指令修飾詞搭配寫入任何輸出暫存器 ([輸出色彩](dx9-graphics-reference-asm-ps-registers-output-color.md) 暫存器或 [輸出深度](dx9-graphics-reference-asm-ps-registers-output-depth.md) 暫存器) 的指示。</span><span class="sxs-lookup"><span data-stu-id="c5bcc-155">For ps\_2\_0, ps\_2\_x, and ps\_2\_sw, the \_sat instruction modifier cannot be used with instructions writing to any output registers ([Output Color Register](dx9-graphics-reference-asm-ps-registers-output-color.md) or [Output Depth Register](dx9-graphics-reference-asm-ps-registers-output-depth.md)).</span></span> <span data-ttu-id="c5bcc-156">這種限制不適用於 ps \_ 3 \_ 0 和更新版本。</span><span class="sxs-lookup"><span data-stu-id="c5bcc-156">This restriction does not apply to ps\_3\_0 and above.</span></span>

<span data-ttu-id="c5bcc-157">範例：</span><span class="sxs-lookup"><span data-stu-id="c5bcc-157">Example:</span></span>


```
dp3_sat r0, v0, c1
```



## <a name="related-topics"></a><span data-ttu-id="c5bcc-158">相關主題</span><span class="sxs-lookup"><span data-stu-id="c5bcc-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c5bcc-159">圖元著色器指示</span><span class="sxs-lookup"><span data-stu-id="c5bcc-159">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




