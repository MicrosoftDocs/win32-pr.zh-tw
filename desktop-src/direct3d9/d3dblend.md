---
description: 定義支援的 blend 模式。
ms.assetid: 60ff384c-15a0-4c6f-9e2c-59fdea76b7a1
title: 'D3DBLEND 列舉 (D3D9Types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DBLEND
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 55edb432913720f58860d4f5cb87d8da9b9a8681
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343383"
---
# <a name="d3dblend-enumeration"></a><span data-ttu-id="33212-103">D3DBLEND 列舉</span><span class="sxs-lookup"><span data-stu-id="33212-103">D3DBLEND enumeration</span></span>

<span data-ttu-id="33212-104">定義支援的 blend 模式。</span><span class="sxs-lookup"><span data-stu-id="33212-104">Defines the supported blend mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="33212-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="33212-105">Syntax</span></span>


```C++
typedef enum D3DBLEND { 
  D3DBLEND_ZERO             = 1,
  D3DBLEND_ONE              = 2,
  D3DBLEND_SRCCOLOR         = 3,
  D3DBLEND_INVSRCCOLOR      = 4,
  D3DBLEND_SRCALPHA         = 5,
  D3DBLEND_INVSRCALPHA      = 6,
  D3DBLEND_DESTALPHA        = 7,
  D3DBLEND_INVDESTALPHA     = 8,
  D3DBLEND_DESTCOLOR        = 9,
  D3DBLEND_INVDESTCOLOR     = 10,
  D3DBLEND_SRCALPHASAT      = 11,
  D3DBLEND_BOTHSRCALPHA     = 12,
  D3DBLEND_BOTHINVSRCALPHA  = 13,
  D3DBLEND_BLENDFACTOR      = 14,
  D3DBLEND_INVBLENDFACTOR   = 15,
  D3DBLEND_SRCCOLOR2        = 16,
  D3DBLEND_INVSRCCOLOR2     = 17,
  D3DBLEND_FORCE_DWORD      = 0x7fffffff
} D3DBLEND, *LPD3DBLEND;
```



## <a name="constants"></a><span data-ttu-id="33212-106">常數</span><span class="sxs-lookup"><span data-stu-id="33212-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="33212-107"><span id="D3DBLEND_ZERO"></span><span id="d3dblend_zero"></span>**D3DBLEND \_ 零**</span><span class="sxs-lookup"><span data-stu-id="33212-107"><span id="D3DBLEND_ZERO"></span><span id="d3dblend_zero"></span>**D3DBLEND\_ZERO**</span></span>
</dt> <dd>

<span data-ttu-id="33212-108">Blend 因數是 (0、0、0、0) 。</span><span class="sxs-lookup"><span data-stu-id="33212-108">Blend factor is (0, 0, 0, 0).</span></span>

</dd> <dt>

<span data-ttu-id="33212-109"><span id="D3DBLEND_ONE"></span><span id="d3dblend_one"></span>**D3DBLEND \_ 一**</span><span class="sxs-lookup"><span data-stu-id="33212-109"><span id="D3DBLEND_ONE"></span><span id="d3dblend_one"></span>**D3DBLEND\_ONE**</span></span>
</dt> <dd>

<span data-ttu-id="33212-110">Blend 因數是 (1，1，1，1) 。</span><span class="sxs-lookup"><span data-stu-id="33212-110">Blend factor is (1, 1, 1, 1).</span></span>

</dd> <dt>

<span data-ttu-id="33212-111"><span id="D3DBLEND_SRCCOLOR"></span><span id="d3dblend_srccolor"></span>**D3DBLEND \_ SRCCOLOR**</span><span class="sxs-lookup"><span data-stu-id="33212-111"><span id="D3DBLEND_SRCCOLOR"></span><span id="d3dblend_srccolor"></span>**D3DBLEND\_SRCCOLOR**</span></span>
</dt> <dd>

<span data-ttu-id="33212-112">Blend 因數是 (Rs、Gs、Bs) 。</span><span class="sxs-lookup"><span data-stu-id="33212-112">Blend factor is (Rₛ, Gₛ, Bₛ, Aₛ).</span></span>

</dd> <dt>

<span data-ttu-id="33212-113"><span id="D3DBLEND_INVSRCCOLOR"></span><span id="d3dblend_invsrccolor"></span>**D3DBLEND \_ INVSRCCOLOR**</span><span class="sxs-lookup"><span data-stu-id="33212-113"><span id="D3DBLEND_INVSRCCOLOR"></span><span id="d3dblend_invsrccolor"></span>**D3DBLEND\_INVSRCCOLOR**</span></span>
</dt> <dd>

<span data-ttu-id="33212-114">Blend 因數是 (1-Rs、1-Gs、1 Bs、1) 。</span><span class="sxs-lookup"><span data-stu-id="33212-114">Blend factor is (1 - Rₛ, 1 - Gₛ, 1 - Bₛ, 1 - Aₛ).</span></span>

</dd> <dt>

<span data-ttu-id="33212-115"><span id="D3DBLEND_SRCALPHA"></span><span id="d3dblend_srcalpha"></span>**D3DBLEND \_ SRCALPHA**</span><span class="sxs-lookup"><span data-stu-id="33212-115"><span id="D3DBLEND_SRCALPHA"></span><span id="d3dblend_srcalpha"></span>**D3DBLEND\_SRCALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="33212-116">Blend 因數會 (As，as 和) 。</span><span class="sxs-lookup"><span data-stu-id="33212-116">Blend factor is (Aₛ, Aₛ, Aₛ, Aₛ).</span></span>

</dd> <dt>

<span data-ttu-id="33212-117"><span id="D3DBLEND_INVSRCALPHA"></span><span id="d3dblend_invsrcalpha"></span>**D3DBLEND \_ INVSRCALPHA**</span><span class="sxs-lookup"><span data-stu-id="33212-117"><span id="D3DBLEND_INVSRCALPHA"></span><span id="d3dblend_invsrcalpha"></span>**D3DBLEND\_INVSRCALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="33212-118">Blend 因數是 ( 1-as，1-as，1-as，1) 。</span><span class="sxs-lookup"><span data-stu-id="33212-118">Blend factor is ( 1 - Aₛ, 1 - Aₛ, 1 - Aₛ, 1 - Aₛ).</span></span>

</dd> <dt>

<span data-ttu-id="33212-119"><span id="D3DBLEND_DESTALPHA"></span><span id="d3dblend_destalpha"></span>**D3DBLEND \_ DESTALPHA**</span><span class="sxs-lookup"><span data-stu-id="33212-119"><span id="D3DBLEND_DESTALPHA"></span><span id="d3dblend_destalpha"></span>**D3DBLEND\_DESTALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="33212-120">Blend 因數是<sub> (a d a d</sub> <sub>a d</sub> <sub>a d</sub> <sub>) 。</sub></span><span class="sxs-lookup"><span data-stu-id="33212-120">Blend factor is (A<sub>d</sub> A<sub>d</sub> A<sub>d</sub> A<sub>d</sub>).</span></span>

</dd> <dt>

<span data-ttu-id="33212-121"><span id="D3DBLEND_INVDESTALPHA"></span><span id="d3dblend_invdestalpha"></span>**D3DBLEND \_ INVDESTALPHA**</span><span class="sxs-lookup"><span data-stu-id="33212-121"><span id="D3DBLEND_INVDESTALPHA"></span><span id="d3dblend_invdestalpha"></span>**D3DBLEND\_INVDESTALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="33212-122">Blend 因數是 (1-A<sub>d</sub> 1<sub>-a d 1-</sub> a<sub>d</sub> 1-a<sub>d</sub>) 。</span><span class="sxs-lookup"><span data-stu-id="33212-122">Blend factor is (1 - A<sub>d</sub> 1 - A<sub>d</sub> 1 - A<sub>d</sub> 1 - A<sub>d</sub>).</span></span>

</dd> <dt>

<span data-ttu-id="33212-123"><span id="D3DBLEND_DESTCOLOR"></span><span id="d3dblend_destcolor"></span>**D3DBLEND \_ DESTCOLOR**</span><span class="sxs-lookup"><span data-stu-id="33212-123"><span id="D3DBLEND_DESTCOLOR"></span><span id="d3dblend_destcolor"></span>**D3DBLEND\_DESTCOLOR**</span></span>
</dt> <dd>

<span data-ttu-id="33212-124">Blend 因數是 (R<sub>d</sub>、G<sub>d</sub>、B<sub>d</sub>、<sub>d</sub>) 。</span><span class="sxs-lookup"><span data-stu-id="33212-124">Blend factor is (R<sub>d</sub>, G<sub>d</sub>, B<sub>d</sub>, A<sub>d</sub>).</span></span>

</dd> <dt>

<span data-ttu-id="33212-125"><span id="D3DBLEND_INVDESTCOLOR"></span><span id="d3dblend_invdestcolor"></span>**D3DBLEND \_ INVDESTCOLOR**</span><span class="sxs-lookup"><span data-stu-id="33212-125"><span id="D3DBLEND_INVDESTCOLOR"></span><span id="d3dblend_invdestcolor"></span>**D3DBLEND\_INVDESTCOLOR**</span></span>
</dt> <dd>

<span data-ttu-id="33212-126">Blend 因數是 (1-R<sub>d</sub>、1-G<sub>d</sub>、1-B<sub>d</sub>、1-A<sub>d</sub>) 。</span><span class="sxs-lookup"><span data-stu-id="33212-126">Blend factor is (1 - R<sub>d</sub>, 1 - G<sub>d</sub>, 1 - B<sub>d</sub>, 1 - A<sub>d</sub>).</span></span>

</dd> <dt>

<span data-ttu-id="33212-127"><span id="D3DBLEND_SRCALPHASAT"></span><span id="d3dblend_srcalphasat"></span>**D3DBLEND \_ SRCALPHASAT**</span><span class="sxs-lookup"><span data-stu-id="33212-127"><span id="D3DBLEND_SRCALPHASAT"></span><span id="d3dblend_srcalphasat"></span>**D3DBLEND\_SRCALPHASAT**</span></span>
</dt> <dd>

<span data-ttu-id="33212-128">Blend 因數是 (f、f、f、1) ;其中 f = min (為，1-A<sub>d</sub>) 。</span><span class="sxs-lookup"><span data-stu-id="33212-128">Blend factor is (f, f, f, 1); where f = min(Aₛ, 1 - A<sub>d</sub>).</span></span>

</dd> <dt>

<span data-ttu-id="33212-129"><span id="D3DBLEND_BOTHSRCALPHA"></span><span id="d3dblend_bothsrcalpha"></span>**D3DBLEND \_ BOTHSRCALPHA**</span><span class="sxs-lookup"><span data-stu-id="33212-129"><span id="D3DBLEND_BOTHSRCALPHA"></span><span id="d3dblend_bothsrcalpha"></span>**D3DBLEND\_BOTHSRCALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="33212-130">已 **淘汰**。</span><span class="sxs-lookup"><span data-stu-id="33212-130">**Obsolete**.</span></span> <span data-ttu-id="33212-131">從 DirectX 6 開始，您可以藉由將來源和目的地 blend 因數設定為 \_ \_ 在個別呼叫中 D3DBLEND SRCALPHA 和 D3DBLEND INVSRCALPHA 來達到相同的效果。</span><span class="sxs-lookup"><span data-stu-id="33212-131">Starting with DirectX 6, you can achieve the same effect by setting the source and destination blend factors to D3DBLEND\_SRCALPHA and D3DBLEND\_INVSRCALPHA in separate calls.</span></span>

</dd> <dt>

<span data-ttu-id="33212-132"><span id="D3DBLEND_BOTHINVSRCALPHA"></span><span id="d3dblend_bothinvsrcalpha"></span>**D3DBLEND \_ BOTHINVSRCALPHA**</span><span class="sxs-lookup"><span data-stu-id="33212-132"><span id="D3DBLEND_BOTHINVSRCALPHA"></span><span id="d3dblend_bothinvsrcalpha"></span>**D3DBLEND\_BOTHINVSRCALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="33212-133">已 **淘汰**。</span><span class="sxs-lookup"><span data-stu-id="33212-133">**Obsolete**.</span></span> <span data-ttu-id="33212-134">來源 blend 因數是 (1-As，1-As，1-As，1) ，而目的地 blend 因數 (As，as，as) ;目的地 blend 選取專案會遭到覆寫。</span><span class="sxs-lookup"><span data-stu-id="33212-134">Source blend factor is (1 - Aₛ, 1 - Aₛ, 1 - Aₛ, 1 - Aₛ), and destination blend factor is (Aₛ, Aₛ, Aₛ, Aₛ); the destination blend selection is overridden.</span></span> <span data-ttu-id="33212-135">只有 D3DRS SRCBLEND 轉譯狀態才支援這個 blend 模式 \_ 。</span><span class="sxs-lookup"><span data-stu-id="33212-135">This blend mode is supported only for the D3DRS\_SRCBLEND render state.</span></span>

</dd> <dt>

<span data-ttu-id="33212-136"><span id="D3DBLEND_BLENDFACTOR"></span><span id="d3dblend_blendfactor"></span>**D3DBLEND \_ BLENDFACTOR**</span><span class="sxs-lookup"><span data-stu-id="33212-136"><span id="D3DBLEND_BLENDFACTOR"></span><span id="d3dblend_blendfactor"></span>**D3DBLEND\_BLENDFACTOR**</span></span>
</dt> <dd>

<span data-ttu-id="33212-137">框架緩衝區 blender 所使用的常數色彩混合係數。</span><span class="sxs-lookup"><span data-stu-id="33212-137">Constant color blending factor used by the frame-buffer blender.</span></span> <span data-ttu-id="33212-138">只有 \_ 在 [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)的 **SrcBlendCaps** 或 **DestBlendCaps** 成員中設定 D3DPBLENDCAPS BLENDFACTOR 時，才支援這個 blend 模式。</span><span class="sxs-lookup"><span data-stu-id="33212-138">This blend mode is supported only if D3DPBLENDCAPS\_BLENDFACTOR is set in the **SrcBlendCaps** or **DestBlendCaps** members of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="33212-139"><span id="D3DBLEND_INVBLENDFACTOR"></span><span id="d3dblend_invblendfactor"></span>**D3DBLEND \_ INVBLENDFACTOR**</span><span class="sxs-lookup"><span data-stu-id="33212-139"><span id="D3DBLEND_INVBLENDFACTOR"></span><span id="d3dblend_invblendfactor"></span>**D3DBLEND\_INVBLENDFACTOR**</span></span>
</dt> <dd>

<span data-ttu-id="33212-140">由框架緩衝區 blender 所使用的反向常數色彩混合係數。</span><span class="sxs-lookup"><span data-stu-id="33212-140">Inverted constant color-blending factor used by the frame-buffer blender.</span></span> <span data-ttu-id="33212-141">只有在 \_ [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)的 **SrcBlendCaps** 或 **DestBlendCaps** 成員中設定 D3DPBLENDCAPS BLENDFACTOR 位時，才支援這個 blend 模式。</span><span class="sxs-lookup"><span data-stu-id="33212-141">This blend mode is supported only if the D3DPBLENDCAPS\_BLENDFACTOR bit is set in the **SrcBlendCaps** or **DestBlendCaps** members of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="33212-142"><span id="D3DBLEND_SRCCOLOR2"></span><span id="d3dblend_srccolor2"></span>**D3DBLEND \_ SRCCOLOR2**</span><span class="sxs-lookup"><span data-stu-id="33212-142"><span id="D3DBLEND_SRCCOLOR2"></span><span id="d3dblend_srccolor2"></span>**D3DBLEND\_SRCCOLOR2**</span></span>
</dt> <dd>

<span data-ttu-id="33212-143">Blend 因數是 (PSOutColor \[ 1 \] <sub>r</sub>、PSOutColor \[ 1 \] <sub>g</sub>、PSOutColor \[ 1 \] <sub>b</sub>，而不是使用) 。</span><span class="sxs-lookup"><span data-stu-id="33212-143">Blend factor is (PSOutColor\[1\]<sub>r</sub>, PSOutColor\[1\]<sub>g</sub>, PSOutColor\[1\]<sub>b</sub>, not used).</span></span> <span data-ttu-id="33212-144">請參閱轉譯 [目標混色](#render-target-blending)。</span><span class="sxs-lookup"><span data-stu-id="33212-144">See [Render Target Blending](#render-target-blending).</span></span>

<span data-ttu-id="33212-145">Direct3D 9 與 Direct3D 9Ex 之間的差異：</span><span class="sxs-lookup"><span data-stu-id="33212-145">Differences between Direct3D 9 and Direct3D 9Ex:</span></span>

- <span data-ttu-id="33212-146">此旗標僅適用于 Direct3D 9Ex。</span><span class="sxs-lookup"><span data-stu-id="33212-146">This flag is available in Direct3D 9Ex only.</span></span>



 

</dd> <dt>

<span data-ttu-id="33212-147"><span id="D3DBLEND_INVSRCCOLOR2"></span><span id="d3dblend_invsrccolor2"></span>**D3DBLEND \_ INVSRCCOLOR2**</span><span class="sxs-lookup"><span data-stu-id="33212-147"><span id="D3DBLEND_INVSRCCOLOR2"></span><span id="d3dblend_invsrccolor2"></span>**D3DBLEND\_INVSRCCOLOR2**</span></span>
</dt> <dd>

<span data-ttu-id="33212-148">Blend 因數是 (1-PSOutColor \[ 1 \] <sub>r</sub>、1-PSOutColor \[ 1 \] <sub>g</sub>、1-PSOutColor \[ 1 \] <sub>b</sub>，未使用) ) 。</span><span class="sxs-lookup"><span data-stu-id="33212-148">Blend factor is (1 - PSOutColor\[1\]<sub>r</sub>, 1 - PSOutColor\[1\]<sub>g</sub>, 1 - PSOutColor\[1\]<sub>b</sub>, not used)).</span></span> <span data-ttu-id="33212-149">請參閱轉譯 [目標混色](#render-target-blending)。</span><span class="sxs-lookup"><span data-stu-id="33212-149">See [Render Target Blending](#render-target-blending).</span></span>


<span data-ttu-id="33212-150">Direct3D 9 與 Direct3D 9Ex 之間的差異：</span><span class="sxs-lookup"><span data-stu-id="33212-150">Differences between Direct3D 9 and Direct3D 9Ex:</span></span>

- <span data-ttu-id="33212-151">此旗標僅適用于 Direct3D 9Ex。</span><span class="sxs-lookup"><span data-stu-id="33212-151">This flag is available in Direct3D 9Ex only.</span></span>



 

</dd> <dt>

<span data-ttu-id="33212-152"><span id="D3DBLEND_FORCE_DWORD"></span><span id="d3dblend_force_dword"></span>**D3DBLEND \_ 強制 \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="33212-152"><span id="D3DBLEND_FORCE_DWORD"></span><span id="d3dblend_force_dword"></span>**D3DBLEND\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="33212-153">強制此列舉的大小編譯為32位。</span><span class="sxs-lookup"><span data-stu-id="33212-153">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="33212-154">如果沒有這個值，某些編譯器會允許此列舉編譯成32位以外的大小。</span><span class="sxs-lookup"><span data-stu-id="33212-154">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="33212-155">不使用這個值。</span><span class="sxs-lookup"><span data-stu-id="33212-155">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="33212-156">備註</span><span class="sxs-lookup"><span data-stu-id="33212-156">Remarks</span></span>

<span data-ttu-id="33212-157">在上述成員描述中，來源和目的地的 RGBA 值會以 s 和 d 注標表示。</span><span class="sxs-lookup"><span data-stu-id="33212-157">In the preceding member descriptions, the RGBA values of the source and destination are indicated by the s and d subscripts.</span></span>

<span data-ttu-id="33212-158">下列轉譯狀態會使用這個列舉類型中的值：</span><span class="sxs-lookup"><span data-stu-id="33212-158">The values in this enumerated type are used by the following render states:</span></span>

-   <span data-ttu-id="33212-159">D3DRS \_ DESTBLEND</span><span class="sxs-lookup"><span data-stu-id="33212-159">D3DRS\_DESTBLEND</span></span>
-   <span data-ttu-id="33212-160">D3DRS \_ SRCBLEND</span><span class="sxs-lookup"><span data-stu-id="33212-160">D3DRS\_SRCBLEND</span></span>
-   <span data-ttu-id="33212-161">D3DRS \_ DESTBLENDALPHA</span><span class="sxs-lookup"><span data-stu-id="33212-161">D3DRS\_DESTBLENDALPHA</span></span>
-   <span data-ttu-id="33212-162">D3DRS \_ SRCBLENDALPHA</span><span class="sxs-lookup"><span data-stu-id="33212-162">D3DRS\_SRCBLENDALPHA</span></span>

<span data-ttu-id="33212-163">請參閱 [ **D3DRENDERSTATETYPE**](./d3drenderstatetype.md)</span><span class="sxs-lookup"><span data-stu-id="33212-163">See [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)</span></span>

### <a name="render-target-blending"></a><span data-ttu-id="33212-164">轉譯目標混色</span><span class="sxs-lookup"><span data-stu-id="33212-164">Render Target Blending</span></span>

<span data-ttu-id="33212-165">Direct3D 9Ex 改進了文字轉譯功能。</span><span class="sxs-lookup"><span data-stu-id="33212-165">Direct3D 9Ex has improved text rendering capabilities.</span></span> <span data-ttu-id="33212-166">轉譯純文字類型通常需要兩次傳遞。</span><span class="sxs-lookup"><span data-stu-id="33212-166">Rendering clear-type fonts would normally require two passes.</span></span> <span data-ttu-id="33212-167">為了消除第二次傳遞，可以使用圖元著色器輸出兩種色彩，我們可以呼叫 PSOutColor \[ 0 \] 和 PSOutColor \[ 1 \] 。</span><span class="sxs-lookup"><span data-stu-id="33212-167">To eliminate the second pass, a pixel shader can be used to output two colors, which we can call PSOutColor\[0\] and PSOutColor\[1\].</span></span> <span data-ttu-id="33212-168">第一個色彩會包含標準的3個色彩元件 (RGB) 。</span><span class="sxs-lookup"><span data-stu-id="33212-168">The first color would contain the standard 3 color components (RGB).</span></span> <span data-ttu-id="33212-169">第二個色彩會包含3個 Alpha 元件 (第一個色彩) 的每個元件各一個元件。</span><span class="sxs-lookup"><span data-stu-id="33212-169">The second color would contain 3 alpha components (one for each component of the first color).</span></span>

<span data-ttu-id="33212-170">這些新的混合模式僅用於第一個呈現目標上的文字轉譯。</span><span class="sxs-lookup"><span data-stu-id="33212-170">These new blending modes are only used for text rendering on the first render target.</span></span>

## <a name="requirements"></a><span data-ttu-id="33212-171">規格需求</span><span class="sxs-lookup"><span data-stu-id="33212-171">Requirements</span></span>



| <span data-ttu-id="33212-172">需求</span><span class="sxs-lookup"><span data-stu-id="33212-172">Requirement</span></span> | <span data-ttu-id="33212-173">值</span><span class="sxs-lookup"><span data-stu-id="33212-173">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="33212-174">標頭</span><span class="sxs-lookup"><span data-stu-id="33212-174">Header</span></span><br/> | <dl> <span data-ttu-id="33212-175"><dt>D3D9Types。h</dt></span><span class="sxs-lookup"><span data-stu-id="33212-175"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33212-176">另請參閱</span><span class="sxs-lookup"><span data-stu-id="33212-176">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33212-177">Direct3D 列舉</span><span class="sxs-lookup"><span data-stu-id="33212-177">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 
