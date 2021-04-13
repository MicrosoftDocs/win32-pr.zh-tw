---
description: 定義每一階段的材質混合作業。
ms.assetid: 7bfdcb15-c3c3-4e7e-b924-6ecfa350e2f3
title: 'D3DTEXTUREOP 列舉 (D3D9Types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTEXTUREOP
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: d35e2d4b65cd41a49d8ed8edb3252295ca3baef3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322783"
---
# <a name="d3dtextureop-enumeration"></a><span data-ttu-id="01ce3-103">D3DTEXTUREOP 列舉</span><span class="sxs-lookup"><span data-stu-id="01ce3-103">D3DTEXTUREOP enumeration</span></span>

<span data-ttu-id="01ce3-104">定義每一階段的材質混合作業。</span><span class="sxs-lookup"><span data-stu-id="01ce3-104">Defines per-stage texture-blending operations.</span></span>

## <a name="syntax"></a><span data-ttu-id="01ce3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="01ce3-105">Syntax</span></span>


```C++
typedef enum D3DTEXTUREOP { 
  D3DTOP_DISABLE                    = 1,
  D3DTOP_SELECTARG1                 = 2,
  D3DTOP_SELECTARG2                 = 3,
  D3DTOP_MODULATE                   = 4,
  D3DTOP_MODULATE2X                 = 5,
  D3DTOP_MODULATE4X                 = 6,
  D3DTOP_ADD                        = 7,
  D3DTOP_ADDSIGNED                  = 8,
  D3DTOP_ADDSIGNED2X                = 9,
  D3DTOP_SUBTRACT                   = 10,
  D3DTOP_ADDSMOOTH                  = 11,
  D3DTOP_BLENDDIFFUSEALPHA          = 12,
  D3DTOP_BLENDTEXTUREALPHA          = 13,
  D3DTOP_BLENDFACTORALPHA           = 14,
  D3DTOP_BLENDTEXTUREALPHAPM        = 15,
  D3DTOP_BLENDCURRENTALPHA          = 16,
  D3DTOP_PREMODULATE                = 17,
  D3DTOP_MODULATEALPHA_ADDCOLOR     = 18,
  D3DTOP_MODULATECOLOR_ADDALPHA     = 19,
  D3DTOP_MODULATEINVALPHA_ADDCOLOR  = 20,
  D3DTOP_MODULATEINVCOLOR_ADDALPHA  = 21,
  D3DTOP_BUMPENVMAP                 = 22,
  D3DTOP_BUMPENVMAPLUMINANCE        = 23,
  D3DTOP_DOTPRODUCT3                = 24,
  D3DTOP_MULTIPLYADD                = 25,
  D3DTOP_LERP                       = 26,
  D3DTOP_FORCE_DWORD                = 0x7fffffff
} D3DTEXTUREOP, *LPD3DTEXTUREOP;
```



## <a name="constants"></a><span data-ttu-id="01ce3-106">常數</span><span class="sxs-lookup"><span data-stu-id="01ce3-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="01ce3-107"><span id="D3DTOP_DISABLE"></span><span id="d3dtop_disable"></span>**D3DTOP \_ DISABLE**</span><span class="sxs-lookup"><span data-stu-id="01ce3-107"><span id="D3DTOP_DISABLE"></span><span id="d3dtop_disable"></span>**D3DTOP\_DISABLE**</span></span>
</dt> <dd>

<span data-ttu-id="01ce3-108">停用此材質階段的輸出，以及索引較高的所有階段。</span><span class="sxs-lookup"><span data-stu-id="01ce3-108">Disables output from this texture stage and all stages with a higher index.</span></span> <span data-ttu-id="01ce3-109">若要停用材質對應，請將此設定為第一個材質階段的色彩運算 (階段 0) 。</span><span class="sxs-lookup"><span data-stu-id="01ce3-109">To disable texture mapping, set this as the color operation for the first texture stage (stage 0).</span></span> <span data-ttu-id="01ce3-110">啟用色彩作業時，無法停用 Alpha 作業。</span><span class="sxs-lookup"><span data-stu-id="01ce3-110">Alpha operations cannot be disabled when color operations are enabled.</span></span> <span data-ttu-id="01ce3-111">當色彩混合啟用時，將 Alpha 作業設定為 D3DTOP \_ 停用會導致未定義的行為。</span><span class="sxs-lookup"><span data-stu-id="01ce3-111">Setting the alpha operation to D3DTOP\_DISABLE when color blending is enabled causes undefined behavior.</span></span>

</dd> <dt>

<span data-ttu-id="01ce3-112"><span id="D3DTOP_SELECTARG1"></span><span id="d3dtop_selectarg1"></span>**D3DTOP \_ SELECTARG1**</span><span class="sxs-lookup"><span data-stu-id="01ce3-112"><span id="D3DTOP_SELECTARG1"></span><span id="d3dtop_selectarg1"></span>**D3DTOP\_SELECTARG1**</span></span>
</dt> <dd>

<span data-ttu-id="01ce3-113">使用這個紋理階段的第一個色彩或 Alpha 引數（未修改）作為輸出。</span><span class="sxs-lookup"><span data-stu-id="01ce3-113">Use this texture stage's first color or alpha argument, unmodified, as the output.</span></span> <span data-ttu-id="01ce3-114">當搭配使用 D3DTSS COLOROP 材質階段狀態時，此作業會影響 color 引數 \_ ，而當搭配 D3DTSS ALPHAOP 使用時，則會影響 Alpha 引數 \_ 。</span><span class="sxs-lookup"><span data-stu-id="01ce3-114">This operation affects the color argument when used with the D3DTSS\_COLOROP texture-stage state, and the alpha argument when used with D3DTSS\_ALPHAOP.</span></span>

![此引數的方程式 (s (rgba) = arg1) ](images/topfrm1.png)

</dd> <dt>

<span data-ttu-id="01ce3-116"><span id="D3DTOP_SELECTARG2"></span><span id="d3dtop_selectarg2"></span>**D3DTOP \_ SELECTARG2**</span><span class="sxs-lookup"><span data-stu-id="01ce3-116"><span id="D3DTOP_SELECTARG2"></span><span id="d3dtop_selectarg2"></span>**D3DTOP\_SELECTARG2**</span></span>
</dt> <dd>

<span data-ttu-id="01ce3-117">使用這個紋理階段的第二個色彩或 Alpha 引數（未修改）作為輸出。</span><span class="sxs-lookup"><span data-stu-id="01ce3-117">Use this texture stage's second color or alpha argument, unmodified, as the output.</span></span> <span data-ttu-id="01ce3-118">當搭配使用 D3DTSS COLOROP 材質階段狀態時，此作業會影響 color 引數 \_ ，而當搭配 D3DTSS ALPHAOP 使用時，則會影響 Alpha 引數 \_ 。</span><span class="sxs-lookup"><span data-stu-id="01ce3-118">This operation affects the color argument when used with the D3DTSS\_COLOROP texture stage state, and the alpha argument when used with D3DTSS\_ALPHAOP.</span></span>

![此引數的方程式 (s (rgba) = arg2) ](images/topfrm2.png)

</dd> <dt>

<span data-ttu-id="01ce3-120"><span id="D3DTOP_MODULATE"></span><span id="d3dtop_modulate"></span>**D3DTOP \_ lambert**</span><span class="sxs-lookup"><span data-stu-id="01ce3-120"><span id="D3DTOP_MODULATE"></span><span id="d3dtop_modulate"></span>**D3DTOP\_MODULATE**</span></span>
</dt> <dd>

<span data-ttu-id="01ce3-121">將引數的元件相乘。</span><span class="sxs-lookup"><span data-stu-id="01ce3-121">Multiply the components of the arguments.</span></span>

![lambert 作業的方程式 (s (rgba) = arg1 x arg 2) ](images/topfrm3.png)

</dd> <dt>

<span data-ttu-id="01ce3-123"><span id="D3DTOP_MODULATE2X"></span><span id="d3dtop_modulate2x"></span>**D3DTOP \_ MODULATE2X**</span><span class="sxs-lookup"><span data-stu-id="01ce3-123"><span id="D3DTOP_MODULATE2X"></span><span id="d3dtop_modulate2x"></span>**D3DTOP\_MODULATE2X**</span></span>
</dt> <dd>

<span data-ttu-id="01ce3-124">將引數的元件相乘，並將產品移至左邊的1位 (有效地將它們乘以 2) 以進行 brightening。</span><span class="sxs-lookup"><span data-stu-id="01ce3-124">Multiply the components of the arguments, and shift the products to the left 1 bit (effectively multiplying them by 2) for brightening.</span></span>

![modulate2x 作業的方程式 (s (rgba) = (arg1 x arg 2) 然後左移 1) ](images/topfrm4.png)

</dd> <dt>

<span data-ttu-id="01ce3-126"><span id="D3DTOP_MODULATE4X"></span><span id="d3dtop_modulate4x"></span>**D3DTOP \_ MODULATE4X**</span><span class="sxs-lookup"><span data-stu-id="01ce3-126"><span id="D3DTOP_MODULATE4X"></span><span id="d3dtop_modulate4x"></span>**D3DTOP\_MODULATE4X**</span></span>
</dt> <dd>

<span data-ttu-id="01ce3-127">將引數的元件相乘，並將產品移至左邊的2位 (有效地將它們乘以 4) 以進行 brightening。</span><span class="sxs-lookup"><span data-stu-id="01ce3-127">Multiply the components of the arguments, and shift the products to the left 2 bits (effectively multiplying them by 4) for brightening.</span></span>

![modulate4x 作業的方程式 (s (rgba) = (arg1 x arg 2) 然後左移 2) ](images/topfrm5.png)

</dd> <dt>

<span data-ttu-id="01ce3-129"><span id="D3DTOP_ADD"></span><span id="d3dtop_add"></span>**D3DTOP \_ 新增**</span><span class="sxs-lookup"><span data-stu-id="01ce3-129"><span id="D3DTOP_ADD"></span><span id="d3dtop_add"></span>**D3DTOP\_ADD**</span></span>
</dt> <dd>

<span data-ttu-id="01ce3-130">加入引數的元件。</span><span class="sxs-lookup"><span data-stu-id="01ce3-130">Add the components of the arguments.</span></span>

![新增作業的方程式 (s (rgba) = arg1 + arg 2) ](images/topfrm6.png)

</dd> <dt>

<span data-ttu-id="01ce3-132"><span id="D3DTOP_ADDSIGNED"></span><span id="d3dtop_addsigned"></span>**D3DTOP \_ ADDSIGNED**</span><span class="sxs-lookup"><span data-stu-id="01ce3-132"><span id="D3DTOP_ADDSIGNED"></span><span id="d3dtop_addsigned"></span>**D3DTOP\_ADDSIGNED**</span></span>
</dt> <dd>

<span data-ttu-id="01ce3-133">將引數的元件新增為-0.5 偏差，使值的有效範圍從-0.5 到0.5。</span><span class="sxs-lookup"><span data-stu-id="01ce3-133">Add the components of the arguments with a - 0.5 bias, making the effective range of values from - 0.5 through 0.5.</span></span>

![新增簽署作業 (s 的方程式 (rgba) = arg1 + arg 2 – 0.5) ](images/topfrm7.png)

</dd> <dt>

<span data-ttu-id="01ce3-135"><span id="D3DTOP_ADDSIGNED2X"></span><span id="d3dtop_addsigned2x"></span>**D3DTOP \_ ADDSIGNED2X**</span><span class="sxs-lookup"><span data-stu-id="01ce3-135"><span id="D3DTOP_ADDSIGNED2X"></span><span id="d3dtop_addsigned2x"></span>**D3DTOP\_ADDSIGNED2X**</span></span>
</dt> <dd>

<span data-ttu-id="01ce3-136">將引數的元件新增為-0.5 偏差，然後將產品轉移至左方的1位。</span><span class="sxs-lookup"><span data-stu-id="01ce3-136">Add the components of the arguments with a - 0.5 bias, and shift the products to the left 1 bit.</span></span>

![新增帶正負號之2x 作業 ( (s 的方程式 (rgba) = arg1 + arg 2-0.5) 然後左移 1) ](images/topfrm8.png)

</dd> <dt>

<span data-ttu-id="01ce3-138"><span id="D3DTOP_SUBTRACT"></span><span id="d3dtop_subtract"></span>**D3DTOP \_ 減**</span><span class="sxs-lookup"><span data-stu-id="01ce3-138"><span id="D3DTOP_SUBTRACT"></span><span id="d3dtop_subtract"></span>**D3DTOP\_SUBTRACT**</span></span>
</dt> <dd>

<span data-ttu-id="01ce3-139">從第一個引數的元件減去第二個引數的元件。</span><span class="sxs-lookup"><span data-stu-id="01ce3-139">Subtract the components of the second argument from those of the first argument.</span></span>

![減法運算的方程式 (s (rgba) = arg1-arg 2) ](images/topfrm9.png)

</dd> <dt>

<span data-ttu-id="01ce3-141"><span id="D3DTOP_ADDSMOOTH"></span><span id="d3dtop_addsmooth"></span>**D3DTOP \_ ADDSMOOTH**</span><span class="sxs-lookup"><span data-stu-id="01ce3-141"><span id="D3DTOP_ADDSMOOTH"></span><span id="d3dtop_addsmooth"></span>**D3DTOP\_ADDSMOOTH**</span></span>
</dt> <dd>

<span data-ttu-id="01ce3-142">新增第一個和第二個引數;然後將其產品從總和減去。</span><span class="sxs-lookup"><span data-stu-id="01ce3-142">Add the first and second arguments; then subtract their product from the sum.</span></span>

![加入平滑作業 (s 的方程式 (rgba) = arg1 + arg 2 x (1-arg1) ) ](images/topfrm10.png)

</dd> <dt>

<span data-ttu-id="01ce3-144"><span id="D3DTOP_BLENDDIFFUSEALPHA"></span><span id="d3dtop_blenddiffusealpha"></span>**D3DTOP \_ BLENDDIFFUSEALPHA**</span><span class="sxs-lookup"><span data-stu-id="01ce3-144"><span id="D3DTOP_BLENDDIFFUSEALPHA"></span><span id="d3dtop_blenddiffusealpha"></span>**D3DTOP\_BLENDDIFFUSEALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="01ce3-145">以線性方式混合此材質階段，使用每個頂點的插入 Alpha。</span><span class="sxs-lookup"><span data-stu-id="01ce3-145">Linearly blend this texture stage, using the interpolated alpha from each vertex.</span></span>

![blend 漫射 Alpha 運算的方程式 (s (rgba) = arg1 x Alpha + arg 2 x (1-Alpha) ) ](images/topfrm11.png)

</dd> <dt>

<span data-ttu-id="01ce3-147"><span id="D3DTOP_BLENDTEXTUREALPHA"></span><span id="d3dtop_blendtexturealpha"></span>**D3DTOP \_ BLENDTEXTUREALPHA**</span><span class="sxs-lookup"><span data-stu-id="01ce3-147"><span id="D3DTOP_BLENDTEXTUREALPHA"></span><span id="d3dtop_blendtexturealpha"></span>**D3DTOP\_BLENDTEXTUREALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="01ce3-148">使用這個階段材質的 Alpha，以線性方式混合此材質階段。</span><span class="sxs-lookup"><span data-stu-id="01ce3-148">Linearly blend this texture stage, using the alpha from this stage's texture.</span></span>

![blend 材質 Alpha 運算的方程式 (s (rgba) = arg1 x Alpha + arg 2 x (1-Alpha) ) ](images/topfrm11.png)

</dd> <dt>

<span data-ttu-id="01ce3-150"><span id="D3DTOP_BLENDFACTORALPHA"></span><span id="d3dtop_blendfactoralpha"></span>**D3DTOP \_ BLENDFACTORALPHA**</span><span class="sxs-lookup"><span data-stu-id="01ce3-150"><span id="D3DTOP_BLENDFACTORALPHA"></span><span id="d3dtop_blendfactoralpha"></span>**D3DTOP\_BLENDFACTORALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="01ce3-151">使用具有 D3DRS TEXTUREFACTOR 轉譯狀態的純量 Alpha 組，以線性方式混合此材質階段 \_ 。</span><span class="sxs-lookup"><span data-stu-id="01ce3-151">Linearly blend this texture stage, using a scalar alpha set with the D3DRS\_TEXTUREFACTOR render state.</span></span>

![blend 因數 Alpha 運算的方程式 (s (rgba) = arg1 x Alpha + arg 2 x (1-Alpha) ) ](images/topfrm11.png)

</dd> <dt>

<span data-ttu-id="01ce3-153"><span id="D3DTOP_BLENDTEXTUREALPHAPM"></span><span id="d3dtop_blendtexturealphapm"></span>**D3DTOP \_ BLENDTEXTUREALPHAPM**</span><span class="sxs-lookup"><span data-stu-id="01ce3-153"><span id="D3DTOP_BLENDTEXTUREALPHAPM"></span><span id="d3dtop_blendtexturealphapm"></span>**D3DTOP\_BLENDTEXTUREALPHAPM**</span></span>
</dt> <dd>

<span data-ttu-id="01ce3-154">以線性方式混合使用預乘 Alpha 的材質階段。</span><span class="sxs-lookup"><span data-stu-id="01ce3-154">Linearly blend a texture stage that uses a premultiplied alpha.</span></span>

![blend 材質 Alpha pm 運算的方程式 (s (rgba) = arg1 + arg 2 x (1-Alpha) ) ](images/topfrm12.png)

</dd> <dt>

<span data-ttu-id="01ce3-156"><span id="D3DTOP_BLENDCURRENTALPHA"></span><span id="d3dtop_blendcurrentalpha"></span>**D3DTOP \_ BLENDCURRENTALPHA**</span><span class="sxs-lookup"><span data-stu-id="01ce3-156"><span id="D3DTOP_BLENDCURRENTALPHA"></span><span id="d3dtop_blendcurrentalpha"></span>**D3DTOP\_BLENDCURRENTALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="01ce3-157">使用從上一個材質階段取得的 Alpha，以線性方式混合此材質階段。</span><span class="sxs-lookup"><span data-stu-id="01ce3-157">Linearly blend this texture stage, using the alpha taken from the previous texture stage.</span></span>

![blend 目前 Alpha 運算的方程式 (s (rgba) = arg1 x Alpha + arg2 x (1-Alpha) ) ](images/topfrm11.png)

</dd> <dt>

<span data-ttu-id="01ce3-159"><span id="D3DTOP_PREMODULATE"></span><span id="d3dtop_premodulate"></span>**D3DTOP \_ PREMODULATE**</span><span class="sxs-lookup"><span data-stu-id="01ce3-159"><span id="D3DTOP_PREMODULATE"></span><span id="d3dtop_premodulate"></span>**D3DTOP\_PREMODULATE**</span></span>
</dt> <dd>

<span data-ttu-id="01ce3-160">\_階段 n 中設定了 D3DTOP PREMODULATE。</span><span class="sxs-lookup"><span data-stu-id="01ce3-160">D3DTOP\_PREMODULATE is set in stage n.</span></span> <span data-ttu-id="01ce3-161">階段 n 的輸出是 arg1。</span><span class="sxs-lookup"><span data-stu-id="01ce3-161">The output of stage n is arg1.</span></span> <span data-ttu-id="01ce3-162">此外，如果階段 n + 1 中有材質， \_ 階段 n + 1 中的任何 D3DTA 目前都會依階段 n + 1 中的材質預乘。</span><span class="sxs-lookup"><span data-stu-id="01ce3-162">Additionally, if there is a texture in stage n + 1, any D3DTA\_CURRENT in stage n + 1 is premultiplied by texture in stage n + 1.</span></span>

</dd> <dt>

<span data-ttu-id="01ce3-163"><span id="D3DTOP_MODULATEALPHA_ADDCOLOR"></span><span id="d3dtop_modulatealpha_addcolor"></span>**D3DTOP \_ MODULATEALPHA \_ ADDCOLOR**</span><span class="sxs-lookup"><span data-stu-id="01ce3-163"><span id="D3DTOP_MODULATEALPHA_ADDCOLOR"></span><span id="d3dtop_modulatealpha_addcolor"></span>**D3DTOP\_MODULATEALPHA\_ADDCOLOR**</span></span>
</dt> <dd>

<span data-ttu-id="01ce3-164">使用第一個引數的 Alpha lambert 第二個引數的色彩;然後將結果新增至引數1。</span><span class="sxs-lookup"><span data-stu-id="01ce3-164">Modulate the color of the second argument, using the alpha of the first argument; then add the result to argument one.</span></span> <span data-ttu-id="01ce3-165">只有色彩作業 (D3DTSS COLOROP) 才支援這項作業 \_ 。</span><span class="sxs-lookup"><span data-stu-id="01ce3-165">This operation is supported only for color operations (D3DTSS\_COLOROP).</span></span>

![add color lambert Alpha operation (s (rgba) = arg1 (rgb) + arg1 (rgb)  (x arg2) ) ](images/topfrm13.png)

</dd> <dt>

<span data-ttu-id="01ce3-167"><span id="D3DTOP_MODULATECOLOR_ADDALPHA"></span><span id="d3dtop_modulatecolor_addalpha"></span>**D3DTOP \_ MODULATECOLOR \_ ADDALPHA**</span><span class="sxs-lookup"><span data-stu-id="01ce3-167"><span id="D3DTOP_MODULATECOLOR_ADDALPHA"></span><span id="d3dtop_modulatecolor_addalpha"></span>**D3DTOP\_MODULATECOLOR\_ADDALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="01ce3-168">Lambert 引數;然後新增第一個引數的 Alpha。</span><span class="sxs-lookup"><span data-stu-id="01ce3-168">Modulate the arguments; then add the alpha of the first argument.</span></span> <span data-ttu-id="01ce3-169">只有色彩作業 (D3DTSS COLOROP) 才支援這項作業 \_ 。</span><span class="sxs-lookup"><span data-stu-id="01ce3-169">This operation is supported only for color operations (D3DTSS\_COLOROP).</span></span>

![新增 Alpha lambert 色彩作業的方程式 (s (rgba) = arg1 (rgb) x arg2 (rgb) + arg1 (a) ) ](images/topfrm14.png)

</dd> <dt>

<span data-ttu-id="01ce3-171"><span id="D3DTOP_MODULATEINVALPHA_ADDCOLOR"></span><span id="d3dtop_modulateinvalpha_addcolor"></span>**D3DTOP \_ MODULATEINVALPHA \_ ADDCOLOR**</span><span class="sxs-lookup"><span data-stu-id="01ce3-171"><span id="D3DTOP_MODULATEINVALPHA_ADDCOLOR"></span><span id="d3dtop_modulateinvalpha_addcolor"></span>**D3DTOP\_MODULATEINVALPHA\_ADDCOLOR**</span></span>
</dt> <dd>

<span data-ttu-id="01ce3-172">類似于 D3DTOP \_ MODULATEALPHA \_ ADDCOLOR，但使用第一個引數之 Alpha 的反向。</span><span class="sxs-lookup"><span data-stu-id="01ce3-172">Similar to D3DTOP\_MODULATEALPHA\_ADDCOLOR, but use the inverse of the alpha of the first argument.</span></span> <span data-ttu-id="01ce3-173">只有色彩作業 (D3DTSS COLOROP) 才支援這項作業 \_ 。</span><span class="sxs-lookup"><span data-stu-id="01ce3-173">This operation is supported only for color operations (D3DTSS\_COLOROP).</span></span>

![新增色彩 lambert 反向 Alpha 運算 (s (rgba) = (1-arg1 (x arg2) ) rgb (+ arg1) rgb (](images/topfrm15.png)

</dd> <dt>

<span data-ttu-id="01ce3-175"><span id="D3DTOP_MODULATEINVCOLOR_ADDALPHA"></span><span id="d3dtop_modulateinvcolor_addalpha"></span>**D3DTOP \_ MODULATEINVCOLOR \_ ADDALPHA**</span><span class="sxs-lookup"><span data-stu-id="01ce3-175"><span id="D3DTOP_MODULATEINVCOLOR_ADDALPHA"></span><span id="d3dtop_modulateinvcolor_addalpha"></span>**D3DTOP\_MODULATEINVCOLOR\_ADDALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="01ce3-176">類似于 D3DTOP \_ MODULATECOLOR \_ ADDALPHA，但使用第一個引數的色彩反轉。</span><span class="sxs-lookup"><span data-stu-id="01ce3-176">Similar to D3DTOP\_MODULATECOLOR\_ADDALPHA, but use the inverse of the color of the first argument.</span></span> <span data-ttu-id="01ce3-177">只有色彩作業 (D3DTSS COLOROP) 才支援這項作業 \_ 。</span><span class="sxs-lookup"><span data-stu-id="01ce3-177">This operation is supported only for color operations (D3DTSS\_COLOROP).</span></span>

![新增 Alpha lambert 反向色彩作業 (s (rgba) = (1-arg1 (rgb) ) x arg2 (rgb) + arg1 (a) ) ](images/topfrm16.png)

</dd> <dt>

<span data-ttu-id="01ce3-179"><span id="D3DTOP_BUMPENVMAP"></span><span id="d3dtop_bumpenvmap"></span>**D3DTOP \_ BUMPENVMAP**</span><span class="sxs-lookup"><span data-stu-id="01ce3-179"><span id="D3DTOP_BUMPENVMAP"></span><span id="d3dtop_bumpenvmap"></span>**D3DTOP\_BUMPENVMAP**</span></span>
</dt> <dd>

<span data-ttu-id="01ce3-180">使用下一個材質階段中的環境對應（沒有亮度），執行每圖元的凹凸對應。</span><span class="sxs-lookup"><span data-stu-id="01ce3-180">Perform per-pixel bump mapping, using the environment map in the next texture stage, without luminance.</span></span> <span data-ttu-id="01ce3-181">只有色彩作業 (D3DTSS COLOROP) 才支援這項作業 \_ 。</span><span class="sxs-lookup"><span data-stu-id="01ce3-181">This operation is supported only for color operations (D3DTSS\_COLOROP).</span></span>

</dd> <dt>

<span data-ttu-id="01ce3-182"><span id="D3DTOP_BUMPENVMAPLUMINANCE"></span><span id="d3dtop_bumpenvmapluminance"></span>**D3DTOP \_ BUMPENVMAPLUMINANCE**</span><span class="sxs-lookup"><span data-stu-id="01ce3-182"><span id="D3DTOP_BUMPENVMAPLUMINANCE"></span><span id="d3dtop_bumpenvmapluminance"></span>**D3DTOP\_BUMPENVMAPLUMINANCE**</span></span>
</dt> <dd>

<span data-ttu-id="01ce3-183">使用下一個材質階段中的環境對應，以亮度執行每個圖元的凹凸對應。</span><span class="sxs-lookup"><span data-stu-id="01ce3-183">Perform per-pixel bump mapping, using the environment map in the next texture stage, with luminance.</span></span> <span data-ttu-id="01ce3-184">只有色彩作業 (D3DTSS COLOROP) 才支援這項作業 \_ 。</span><span class="sxs-lookup"><span data-stu-id="01ce3-184">This operation is supported only for color operations (D3DTSS\_COLOROP).</span></span>

</dd> <dt>

<span data-ttu-id="01ce3-185"><span id="D3DTOP_DOTPRODUCT3"></span><span id="d3dtop_dotproduct3"></span>**D3DTOP \_ DOTPRODUCT3**</span><span class="sxs-lookup"><span data-stu-id="01ce3-185"><span id="D3DTOP_DOTPRODUCT3"></span><span id="d3dtop_dotproduct3"></span>**D3DTOP\_DOTPRODUCT3**</span></span>
</dt> <dd>

<span data-ttu-id="01ce3-186">將每個引數的元件 lambert 為帶正負號的元件，並新增其產品;然後，將總和複製到所有色彩通道，包括 Alpha。</span><span class="sxs-lookup"><span data-stu-id="01ce3-186">Modulate the components of each argument as signed components, add their products; then replicate the sum to all color channels, including alpha.</span></span> <span data-ttu-id="01ce3-187">這項操作支援色彩和 Alpha 運算。</span><span class="sxs-lookup"><span data-stu-id="01ce3-187">This operation is supported for color and alpha operations.</span></span>

![點乘積3作業的方程式 (s (rgba) = arg1 (r) x arg2 (r) + arg1 (g) x arg2 (g) + arg1 (b) x arg2 (b) ) ](images/topfrm17.png)

<span data-ttu-id="01ce3-189">在 DirectX 6 和 DirectX 7 中，多紋理作業會在用來模擬已簽署資料的一半 (y = x-0.5) 之前將上述輸入往下移動，並將純量結果自動壓制到正值，並複寫到所有三個輸出通道。</span><span class="sxs-lookup"><span data-stu-id="01ce3-189">In DirectX 6 and DirectX 7, multitexture operations the above inputs are all shifted down by half (y = x - 0.5) before use to simulate signed data, and the scalar result is automatically clamped to positive values and replicated to all three output channels.</span></span> <span data-ttu-id="01ce3-190">另外也請注意，做為色彩作業，這不會更新只是更新 RGB 元件的 Alpha。</span><span class="sxs-lookup"><span data-stu-id="01ce3-190">Also, note that as a color operation this does not updated the alpha it just updates the RGB components.</span></span>

<span data-ttu-id="01ce3-191">不過，在 DirectX 8.1 著色器中，您可以指定將輸出路由傳送至 rgb 或元件，或是 (預設) 。</span><span class="sxs-lookup"><span data-stu-id="01ce3-191">However, in DirectX 8.1 shaders you can specify that the output be routed to the .rgb or the .a components or both (the default).</span></span> <span data-ttu-id="01ce3-192">您也可以在 Alpha 通道上指定個別的純量運算。</span><span class="sxs-lookup"><span data-stu-id="01ce3-192">You can also specify a separate scalar operation on the alpha channel.</span></span>

</dd> <dt>

<span data-ttu-id="01ce3-193"><span id="D3DTOP_MULTIPLYADD"></span><span id="d3dtop_multiplyadd"></span>**D3DTOP \_ MULTIPLYADD**</span><span class="sxs-lookup"><span data-stu-id="01ce3-193"><span id="D3DTOP_MULTIPLYADD"></span><span id="d3dtop_multiplyadd"></span>**D3DTOP\_MULTIPLYADD**</span></span>
</dt> <dd>

<span data-ttu-id="01ce3-194">執行乘法累積運算。</span><span class="sxs-lookup"><span data-stu-id="01ce3-194">Performs a multiply-accumulate operation.</span></span> <span data-ttu-id="01ce3-195">它會接受最後兩個引數，將它們相乘，並將其新增至其餘的輸入/來源引數，並將其放入結果中。</span><span class="sxs-lookup"><span data-stu-id="01ce3-195">It takes the last two arguments, multiplies them together, and adds them to the remaining input/source argument, and places that into the result.</span></span>

<span data-ttu-id="01ce3-196">S<sub>RGBA</sub> = Arg1 + Arg2 \* Arg3</span><span class="sxs-lookup"><span data-stu-id="01ce3-196">S<sub>RGBA</sub> = Arg1 + Arg2 \* Arg3</span></span>

</dd> <dt>

<span data-ttu-id="01ce3-197"><span id="D3DTOP_LERP"></span><span id="d3dtop_lerp"></span>**D3DTOP \_ LERP**</span><span class="sxs-lookup"><span data-stu-id="01ce3-197"><span id="D3DTOP_LERP"></span><span id="d3dtop_lerp"></span>**D3DTOP\_LERP**</span></span>
</dt> <dd>

<span data-ttu-id="01ce3-198">以線性方式在第二個和第三個來源引數之間，以第一個來源引數指定的比例進行插補</span><span class="sxs-lookup"><span data-stu-id="01ce3-198">Linearly interpolates between the second and third source arguments by a proportion specified in the first source argument.</span></span>

<span data-ttu-id="01ce3-199">S<sub>RGBA</sub> = (arg1) \* Arg2 + (1-arg1) \* Arg3。</span><span class="sxs-lookup"><span data-stu-id="01ce3-199">S<sub>RGBA</sub> = (Arg1) \* Arg2 + (1- Arg1) \* Arg3.</span></span>

</dd> <dt>

<span data-ttu-id="01ce3-200"><span id="D3DTOP_FORCE_DWORD"></span><span id="d3dtop_force_dword"></span>**D3DTOP \_ 強制 \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="01ce3-200"><span id="D3DTOP_FORCE_DWORD"></span><span id="d3dtop_force_dword"></span>**D3DTOP\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="01ce3-201">強制此列舉的大小編譯為32位。</span><span class="sxs-lookup"><span data-stu-id="01ce3-201">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="01ce3-202">如果沒有這個值，某些編譯器會允許此列舉編譯成32位以外的大小。</span><span class="sxs-lookup"><span data-stu-id="01ce3-202">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="01ce3-203">不使用這個值。</span><span class="sxs-lookup"><span data-stu-id="01ce3-203">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="01ce3-204">備註</span><span class="sxs-lookup"><span data-stu-id="01ce3-204">Remarks</span></span>

<span data-ttu-id="01ce3-205">使用 D3DTSS \_ COLOROP 或 D3DTSS \_ ALPHAOP 值與 [**IDirect3DDevice9：： SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) 方法來設定色彩或 Alpha 運算時，會使用此類型的成員。</span><span class="sxs-lookup"><span data-stu-id="01ce3-205">The members of this type are used when setting color or alpha operations by using the D3DTSS\_COLOROP or D3DTSS\_ALPHAOP values with the [**IDirect3DDevice9::SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) method.</span></span>

<span data-ttu-id="01ce3-206">在上述公式中，S<sub>rgba</sub> 是紋理作業所產生的 rgba 色彩，而 Arg1、Arg2 和 Arg3 則代表材質引數的完整 RGBA 色彩。</span><span class="sxs-lookup"><span data-stu-id="01ce3-206">In the above formulas, S<sub>RGBA</sub> is the RGBA color produced by a texture operation, and Arg1, Arg2, and Arg3 represent the complete RGBA color of the texture arguments.</span></span> <span data-ttu-id="01ce3-207">引數的個別元件會以注標顯示。</span><span class="sxs-lookup"><span data-stu-id="01ce3-207">Individual components of an argument are shown with subscripts.</span></span> <span data-ttu-id="01ce3-208">例如，引數1的 Alpha 元件會顯示為 Arg1<sub>A</sub>。</span><span class="sxs-lookup"><span data-stu-id="01ce3-208">For example, the alpha component for argument 1 would be shown as Arg1<sub>A</sub>.</span></span>

## <a name="requirements"></a><span data-ttu-id="01ce3-209">規格需求</span><span class="sxs-lookup"><span data-stu-id="01ce3-209">Requirements</span></span>



| <span data-ttu-id="01ce3-210">需求</span><span class="sxs-lookup"><span data-stu-id="01ce3-210">Requirement</span></span> | <span data-ttu-id="01ce3-211">值</span><span class="sxs-lookup"><span data-stu-id="01ce3-211">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="01ce3-212">標頭</span><span class="sxs-lookup"><span data-stu-id="01ce3-212">Header</span></span><br/> | <dl> <span data-ttu-id="01ce3-213"><dt>D3D9Types。h</dt></span><span class="sxs-lookup"><span data-stu-id="01ce3-213"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01ce3-214">另請參閱</span><span class="sxs-lookup"><span data-stu-id="01ce3-214">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01ce3-215">Direct3D 列舉</span><span class="sxs-lookup"><span data-stu-id="01ce3-215">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="01ce3-216">**D3DTEXTURESTAGESTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="01ce3-216">**D3DTEXTURESTAGESTATETYPE**</span></span>](./d3dtexturestagestatetype.md)
</dt> </dl>

 

 
