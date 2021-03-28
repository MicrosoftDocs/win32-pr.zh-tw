---
title: sincos-ps
description: 計算正弦和余弦值（以弧度為單位）。 |sincos-ps
ms.assetid: 639237ea-1b7a-4959-9093-78f134c11863
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1e7ccdca91af206862384ae14cf25a85d0817814
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104991994"
---
# <a name="sincos---ps"></a><span data-ttu-id="64ba4-104">sincos-ps</span><span class="sxs-lookup"><span data-stu-id="64ba4-104">sincos - ps</span></span>

<span data-ttu-id="64ba4-105">計算正弦和余弦值（以弧度為單位）。</span><span class="sxs-lookup"><span data-stu-id="64ba4-105">Computes sine and cosine, in radians.</span></span>

## <a name="syntax"></a><span data-ttu-id="64ba4-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="64ba4-106">Syntax</span></span>

### <a name="ps_2_0-and-ps_2_x"></a><span data-ttu-id="64ba4-107">ps \_ 2 \_ 0 和 ps \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="64ba4-107">ps\_2\_0 and ps\_2\_x</span></span>



| <span data-ttu-id="64ba4-108">sincos dst。版</span><span class="sxs-lookup"><span data-stu-id="64ba4-108">sincos dst.{x\</span></span>|<span data-ttu-id="64ba4-109">x</span><span class="sxs-lookup"><span data-stu-id="64ba4-109">y\</span></span>|<span data-ttu-id="64ba4-110">xy}、src0。版</span><span class="sxs-lookup"><span data-stu-id="64ba4-110">xy}, src0.{x\</span></span>|<span data-ttu-id="64ba4-111">x</span><span class="sxs-lookup"><span data-stu-id="64ba4-111">y\</span></span>|<span data-ttu-id="64ba4-112">#a1</span><span class="sxs-lookup"><span data-stu-id="64ba4-112">z\</span></span>|<span data-ttu-id="64ba4-113">w}、src1、src2 收取</span><span class="sxs-lookup"><span data-stu-id="64ba4-113">w}, src1, src2</span></span> |
|------------------------------------------------------|



 

<span data-ttu-id="64ba4-114">其中：</span><span class="sxs-lookup"><span data-stu-id="64ba4-114">Where:</span></span>

-   <span data-ttu-id="64ba4-115">dst 是目的地註冊，而且必須是 (r) 的 [暫時性註冊](dx9-graphics-reference-asm-ps-registers-temporary.md) \# 。</span><span class="sxs-lookup"><span data-stu-id="64ba4-115">dst is the destination register and has to be a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#).</span></span> <span data-ttu-id="64ba4-116">目的地暫存器必須剛好有下列三個遮罩中的其中一個：. x. x. x. x. \| y \| 。</span><span class="sxs-lookup"><span data-stu-id="64ba4-116">The destination register must have exactly one of the following three masks: .x \| .y \| .xy.</span></span>
-   <span data-ttu-id="64ba4-117">src0 是提供輸入角度的來源暫存器，其必須在 \[ -pi、+ pi 內 \] 。</span><span class="sxs-lookup"><span data-stu-id="64ba4-117">src0 is a source register that provides the input angle, which must be within \[-pi, +pi\].</span></span> <span data-ttu-id="64ba4-118">{x \| y \| z \| w} 是必要的複製 swizzle。</span><span class="sxs-lookup"><span data-stu-id="64ba4-118">{x\|y\|z\|w} is the required replicate swizzle.</span></span>
-   <span data-ttu-id="64ba4-119">src1 和 src2 收取是來源暫存器，必須是兩個不同的 [常數 Float Register](dx9-graphics-reference-asm-ps-registers-constant-float.md)s (c \#) 。</span><span class="sxs-lookup"><span data-stu-id="64ba4-119">src1 and src2 are source registers and must be two different [Constant Float Register](dx9-graphics-reference-asm-ps-registers-constant-float.md)s (c\#).</span></span> <span data-ttu-id="64ba4-120">Src1 和 src2 收取的值必須分別是宏 [**D3DSINCOSCONST1**](/windows/desktop/direct3d9/d3dsincosconst1) 和 [**D3DSINCOSCONST2**](/windows/desktop/direct3d9/d3dsincosconst2) 的值。</span><span class="sxs-lookup"><span data-stu-id="64ba4-120">The values of src1 and src2 must be that of the macros [**D3DSINCOSCONST1**](/windows/desktop/direct3d9/d3dsincosconst1) and [**D3DSINCOSCONST2**](/windows/desktop/direct3d9/d3dsincosconst2) respectively.</span></span>

### <a name="ps_3_0"></a><span data-ttu-id="64ba4-121">ps \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="64ba4-121">ps\_3\_0</span></span>



| <span data-ttu-id="64ba4-122">sincos dst。版</span><span class="sxs-lookup"><span data-stu-id="64ba4-122">sincos dst.{x\</span></span>|<span data-ttu-id="64ba4-123">x</span><span class="sxs-lookup"><span data-stu-id="64ba4-123">y\</span></span>|<span data-ttu-id="64ba4-124">xy}、src0。版</span><span class="sxs-lookup"><span data-stu-id="64ba4-124">xy}, src0.{x\</span></span>|<span data-ttu-id="64ba4-125">x</span><span class="sxs-lookup"><span data-stu-id="64ba4-125">y\</span></span>|<span data-ttu-id="64ba4-126">#a1</span><span class="sxs-lookup"><span data-stu-id="64ba4-126">z\</span></span>|<span data-ttu-id="64ba4-127">w</span><span class="sxs-lookup"><span data-stu-id="64ba4-127">w}</span></span> |
|------------------------------------------|



 

<span data-ttu-id="64ba4-128">其中：</span><span class="sxs-lookup"><span data-stu-id="64ba4-128">Where:</span></span>

-   <span data-ttu-id="64ba4-129">dst 是目的地註冊，必須是 [暫時的註冊](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \#) 。</span><span class="sxs-lookup"><span data-stu-id="64ba4-129">dst is a destination register and has to be a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#).</span></span> <span data-ttu-id="64ba4-130">目的地暫存器必須剛好有下列三個遮罩中的其中一個：. x. x. x. x. \| y \| 。</span><span class="sxs-lookup"><span data-stu-id="64ba4-130">The destination register must have exactly one of the following three masks: .x \| .y \| .xy.</span></span>
-   <span data-ttu-id="64ba4-131">src0 是提供輸入角度的來源暫存器，其必須在 \[ -pi、+ pi 內 \] 。</span><span class="sxs-lookup"><span data-stu-id="64ba4-131">src0 is a source register that provides the input angle, which must be within \[-pi, +pi\].</span></span> <span data-ttu-id="64ba4-132">{x \| y \| z \| w} 是必要的複製 swizzle。</span><span class="sxs-lookup"><span data-stu-id="64ba4-132">{x\|y\|z\|w} is the required replicate swizzle.</span></span>

## <a name="remarks"></a><span data-ttu-id="64ba4-133">備註</span><span class="sxs-lookup"><span data-stu-id="64ba4-133">Remarks</span></span>



| <span data-ttu-id="64ba4-134">圖元著色器版本</span><span class="sxs-lookup"><span data-stu-id="64ba4-134">Pixel shader versions</span></span> | <span data-ttu-id="64ba4-135">1\_1</span><span class="sxs-lookup"><span data-stu-id="64ba4-135">1\_1</span></span> | <span data-ttu-id="64ba4-136">1\_2</span><span class="sxs-lookup"><span data-stu-id="64ba4-136">1\_2</span></span> | <span data-ttu-id="64ba4-137">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="64ba4-137">1\_3</span></span> | <span data-ttu-id="64ba4-138">1\_4</span><span class="sxs-lookup"><span data-stu-id="64ba4-138">1\_4</span></span> | <span data-ttu-id="64ba4-139">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="64ba4-139">2\_0</span></span> | <span data-ttu-id="64ba4-140">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="64ba4-140">2\_x</span></span> | <span data-ttu-id="64ba4-141">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="64ba4-141">2\_sw</span></span> | <span data-ttu-id="64ba4-142">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="64ba4-142">3\_0</span></span> | <span data-ttu-id="64ba4-143">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="64ba4-143">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="64ba4-144">sincos</span><span class="sxs-lookup"><span data-stu-id="64ba4-144">sincos</span></span>                |      |      |      |      | <span data-ttu-id="64ba4-145">x</span><span class="sxs-lookup"><span data-stu-id="64ba4-145">x</span></span>    | <span data-ttu-id="64ba4-146">x</span><span class="sxs-lookup"><span data-stu-id="64ba4-146">x</span></span>    | <span data-ttu-id="64ba4-147">x</span><span class="sxs-lookup"><span data-stu-id="64ba4-147">x</span></span>     | <span data-ttu-id="64ba4-148">x</span><span class="sxs-lookup"><span data-stu-id="64ba4-148">x</span></span>    | <span data-ttu-id="64ba4-149">x</span><span class="sxs-lookup"><span data-stu-id="64ba4-149">x</span></span>     |



 

### <a name="ps_2_0-and-ps_2_x"></a><span data-ttu-id="64ba4-150">ps \_ 2 \_ 0 和 ps \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="64ba4-150">ps\_2\_0 and ps\_2\_x</span></span>

<span data-ttu-id="64ba4-151">針對 ps \_ 2 \_ 0 和 ps \_ 2 \_ x，sincos 可以搭配 predication 使用，但 [對述](dx9-graphics-reference-asm-ps-registers-predicate.md) 詞登錄的 swizzle 有一項限制 (p0) ：只允許複寫 swizzle (. \| y. \| z \| . w) 。</span><span class="sxs-lookup"><span data-stu-id="64ba4-151">For ps\_2\_0 and ps\_2\_x, sincos can be used with predication, but with one restriction to the swizzle of the [Predicate Register](dx9-graphics-reference-asm-ps-registers-predicate.md) (p0): only replicate swizzle (.x \| .y \| .z \| .w) is allowed.</span></span>

<span data-ttu-id="64ba4-152">針對 ps \_ 2 \_ 0 和 ps \_ 2 \_ x，指令的運作方式如下 (V = src0 與複寫 swizzle) 的純量值：</span><span class="sxs-lookup"><span data-stu-id="64ba4-152">For ps\_2\_0 and ps\_2\_x, the instruction operates as follows (V = the scalar value from src0 with a replicate swizzle):</span></span>

-   <span data-ttu-id="64ba4-153">如果寫入遮罩是. x：</span><span class="sxs-lookup"><span data-stu-id="64ba4-153">If the write mask is .x:</span></span>
    ```
    dest.x = cos(V)
    dest.y is undefined when the instruction completes
    dest.z is undefined when the instruction completes
    dest.w is not touched by the instruction
    ```

    

-   <span data-ttu-id="64ba4-154">如果寫入遮罩為. y：</span><span class="sxs-lookup"><span data-stu-id="64ba4-154">If the write mask is .y:</span></span>
    ```
    dest.x is undefined when the instruction completes
    dest.y = sin(V)
    dest.z is undefined when the instruction completes
    dest.w is not touched by the instruction
    ```

    

-   <span data-ttu-id="64ba4-155">如果寫入遮罩是 xy：</span><span class="sxs-lookup"><span data-stu-id="64ba4-155">If the write mask is .xy:</span></span>
    ```
    dest.x = cos(V)
    dest.y = sin(V)
    dest.z is undefined when the instruction completes
    dest.w is not touched by the instruction
    ```

    

### <a name="ps_3_0"></a><span data-ttu-id="64ba4-156">ps \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="64ba4-156">ps\_3\_0</span></span>

<span data-ttu-id="64ba4-157">針對 ps \_ 3 \_ 0，sincos 可以搭配 predication 使用，而不受任何限制。</span><span class="sxs-lookup"><span data-stu-id="64ba4-157">For ps\_3\_0, sincos can be used with predication without any restriction.</span></span> <span data-ttu-id="64ba4-158">請參閱述詞 [註冊](dx9-graphics-reference-asm-ps-registers-predicate.md)。</span><span class="sxs-lookup"><span data-stu-id="64ba4-158">See [Predicate Register](dx9-graphics-reference-asm-ps-registers-predicate.md).</span></span>

<span data-ttu-id="64ba4-159">針對 ps \_ 3 \_ 0，指令的運作方式如下 (V = src0 與複寫 swizzle) 的純量值：</span><span class="sxs-lookup"><span data-stu-id="64ba4-159">For ps\_3\_0, the instruction operates as follows (V = the scalar value from src0 with a replicate swizzle):</span></span>

-   <span data-ttu-id="64ba4-160">如果寫入遮罩是. x：</span><span class="sxs-lookup"><span data-stu-id="64ba4-160">If the write mask is .x:</span></span>
    ```
    dest.x = cos(V)
    dest.y is not touched by the instruction
    dest.z is not touched by the instruction
    dest.w is not touched by the instruction
    ```

    

-   <span data-ttu-id="64ba4-161">如果寫入遮罩為. y：</span><span class="sxs-lookup"><span data-stu-id="64ba4-161">If the write mask is .y:</span></span>
    ```
    dest.x is not touched by the instruction
    dest.y = sin(V)
    dest.z is not touched by the instruction
    dest.w is not touched by the instruction
    ```

    

-   <span data-ttu-id="64ba4-162">如果寫入遮罩是 xy：</span><span class="sxs-lookup"><span data-stu-id="64ba4-162">If the write mask is .xy:</span></span>
    ```
    dest.x = cos(V)
    dest.y = sin(V)
    dest.z is not touched by the instruction
    dest.w is not touched by the instruction
    ```

    

<span data-ttu-id="64ba4-163">應用程式可以使用下列著色器的虛擬程式碼，將任意角度 (弧度) 至範圍 \[ -pi、+ pi \] ：</span><span class="sxs-lookup"><span data-stu-id="64ba4-163">The application can map an arbitrary angle (in radians) to the range \[-pi, +pi\] using the following shader pseudocode:</span></span>


```
def c0, pi, 0.5, 2*pi, 1/(2*pi)
mad r0.x, input_angle, c0.w, c0.y
frc r0.x, r0.x
mad r0.x, r0.x, c0.z, -c0.x
```



## <a name="related-topics"></a><span data-ttu-id="64ba4-164">相關主題</span><span class="sxs-lookup"><span data-stu-id="64ba4-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="64ba4-165">圖元著色器指示</span><span class="sxs-lookup"><span data-stu-id="64ba4-165">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 
