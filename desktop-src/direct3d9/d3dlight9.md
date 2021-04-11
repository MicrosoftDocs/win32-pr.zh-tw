---
description: 定義一組光源屬性。
ms.assetid: 25ce9d72-949c-41fc-8e3b-146d6a2de0dc
title: 'D3DLIGHT9 結構 (D3D9Types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DLIGHT9
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 90e72fbb2bf4f1d74a74dc177346387b36eb25e0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196313"
---
# <a name="d3dlight9-structure"></a><span data-ttu-id="70a0d-103">D3DLIGHT9 結構</span><span class="sxs-lookup"><span data-stu-id="70a0d-103">D3DLIGHT9 structure</span></span>

<span data-ttu-id="70a0d-104">定義一組光源屬性。</span><span class="sxs-lookup"><span data-stu-id="70a0d-104">Defines a set of lighting properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="70a0d-105">語法</span><span class="sxs-lookup"><span data-stu-id="70a0d-105">Syntax</span></span>


```C++
typedef struct D3DLIGHT9 {
  D3DLIGHTTYPE  Type;
  D3DCOLORVALUE Diffuse;
  D3DCOLORVALUE Specular;
  D3DCOLORVALUE Ambient;
  D3DVECTOR     Position;
  D3DVECTOR     Direction;
  float         Range;
  float         Falloff;
  float         Attenuation0;
  float         Attenuation1;
  float         Attenuation2;
  float         Theta;
  float         Phi;
} D3DLIGHT9, *LPD3DLIGHT;
```



## <a name="members"></a><span data-ttu-id="70a0d-106">成員</span><span class="sxs-lookup"><span data-stu-id="70a0d-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="70a0d-107">**型別**</span><span class="sxs-lookup"><span data-stu-id="70a0d-107">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="70a0d-108">類型： **[ **D3DLIGHTTYPE**](./d3dlighttype.md)**</span><span class="sxs-lookup"><span data-stu-id="70a0d-108">Type: **[**D3DLIGHTTYPE**](./d3dlighttype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="70a0d-109">燈光來源的類型。</span><span class="sxs-lookup"><span data-stu-id="70a0d-109">Type of the light source.</span></span> <span data-ttu-id="70a0d-110">這個值是 [**D3DLIGHTTYPE**](./d3dlighttype.md) 列舉型別的其中一個成員。</span><span class="sxs-lookup"><span data-stu-id="70a0d-110">This value is one of the members of the [**D3DLIGHTTYPE**](./d3dlighttype.md) enumerated type.</span></span>

</dd> <dt>

<span data-ttu-id="70a0d-111">**擴散**</span><span class="sxs-lookup"><span data-stu-id="70a0d-111">**Diffuse**</span></span>
</dt> <dd>

<span data-ttu-id="70a0d-112">類型： **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**</span><span class="sxs-lookup"><span data-stu-id="70a0d-112">Type: **[**D3DCOLORVALUE**](d3dcolorvalue.md)**</span></span>

</dd> <dd>

<span data-ttu-id="70a0d-113">光線發出的擴散色彩。</span><span class="sxs-lookup"><span data-stu-id="70a0d-113">Diffuse color emitted by the light.</span></span> <span data-ttu-id="70a0d-114">此成員是 [**D3DCOLORVALUE**](d3dcolorvalue.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="70a0d-114">This member is a [**D3DCOLORVALUE**](d3dcolorvalue.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="70a0d-115">**反射**</span><span class="sxs-lookup"><span data-stu-id="70a0d-115">**Specular**</span></span>
</dt> <dd>

<span data-ttu-id="70a0d-116">類型： **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**</span><span class="sxs-lookup"><span data-stu-id="70a0d-116">Type: **[**D3DCOLORVALUE**](d3dcolorvalue.md)**</span></span>

</dd> <dd>

<span data-ttu-id="70a0d-117">光線發出的反射色彩。</span><span class="sxs-lookup"><span data-stu-id="70a0d-117">Specular color emitted by the light.</span></span> <span data-ttu-id="70a0d-118">此成員是 [**D3DCOLORVALUE**](d3dcolorvalue.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="70a0d-118">This member is a [**D3DCOLORVALUE**](d3dcolorvalue.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="70a0d-119">**環境**</span><span class="sxs-lookup"><span data-stu-id="70a0d-119">**Ambient**</span></span>
</dt> <dd>

<span data-ttu-id="70a0d-120">類型： **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**</span><span class="sxs-lookup"><span data-stu-id="70a0d-120">Type: **[**D3DCOLORVALUE**](d3dcolorvalue.md)**</span></span>

</dd> <dd>

<span data-ttu-id="70a0d-121">光線發出的環境色彩。</span><span class="sxs-lookup"><span data-stu-id="70a0d-121">Ambient color emitted by the light.</span></span> <span data-ttu-id="70a0d-122">此成員是 [**D3DCOLORVALUE**](d3dcolorvalue.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="70a0d-122">This member is a [**D3DCOLORVALUE**](d3dcolorvalue.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="70a0d-123">**位置**</span><span class="sxs-lookup"><span data-stu-id="70a0d-123">**Position**</span></span>
</dt> <dd>

<span data-ttu-id="70a0d-124">類型： **[ **D3DVECTOR**](d3dvector.md)**</span><span class="sxs-lookup"><span data-stu-id="70a0d-124">Type: **[**D3DVECTOR**](d3dvector.md)**</span></span>

</dd> <dd>

<span data-ttu-id="70a0d-125">光線在世界空間中的位置，由 [**D3DVECTOR**](d3dvector.md) 結構指定。</span><span class="sxs-lookup"><span data-stu-id="70a0d-125">Position of the light in world space, specified by a [**D3DVECTOR**](d3dvector.md) structure.</span></span> <span data-ttu-id="70a0d-126">這個成員沒有方向性光源的意義，而且在這種情況下會被忽略。</span><span class="sxs-lookup"><span data-stu-id="70a0d-126">This member has no meaning for directional lights and is ignored in that case.</span></span>

</dd> <dt>

<span data-ttu-id="70a0d-127">[方向]</span><span class="sxs-lookup"><span data-stu-id="70a0d-127">**Direction**</span></span>
</dt> <dd>

<span data-ttu-id="70a0d-128">類型： **[ **D3DVECTOR**](d3dvector.md)**</span><span class="sxs-lookup"><span data-stu-id="70a0d-128">Type: **[**D3DVECTOR**](d3dvector.md)**</span></span>

</dd> <dd>

<span data-ttu-id="70a0d-129">光線指向世界空間的方向，由 [**D3DVECTOR**](d3dvector.md) 結構指定。</span><span class="sxs-lookup"><span data-stu-id="70a0d-129">Direction that the light is pointing in world space, specified by a [**D3DVECTOR**](d3dvector.md) structure.</span></span> <span data-ttu-id="70a0d-130">這個成員只有方向和聚光燈的意義。</span><span class="sxs-lookup"><span data-stu-id="70a0d-130">This member has meaning only for directional and spotlights.</span></span> <span data-ttu-id="70a0d-131">此向量不需要正規化，但長度應為非零長度。</span><span class="sxs-lookup"><span data-stu-id="70a0d-131">This vector need not be normalized, but it should have a nonzero length.</span></span>

</dd> <dt>

<span data-ttu-id="70a0d-132">**範圍**</span><span class="sxs-lookup"><span data-stu-id="70a0d-132">**Range**</span></span>
</dt> <dd>

<span data-ttu-id="70a0d-133">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="70a0d-133">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="70a0d-134">光沒有任何作用的距離。</span><span class="sxs-lookup"><span data-stu-id="70a0d-134">Distance beyond which the light has no effect.</span></span> <span data-ttu-id="70a0d-135">這個成員允許的最大值是 FLT MAX 的平方根 \_ 。</span><span class="sxs-lookup"><span data-stu-id="70a0d-135">The maximum allowable value for this member is the square root of FLT\_MAX.</span></span> <span data-ttu-id="70a0d-136">此成員不會影響方向性光源。</span><span class="sxs-lookup"><span data-stu-id="70a0d-136">This member does not affect directional lights.</span></span>

</dd> <dt>

<span data-ttu-id="70a0d-137">**衰減**</span><span class="sxs-lookup"><span data-stu-id="70a0d-137">**Falloff**</span></span>
</dt> <dd>

<span data-ttu-id="70a0d-138">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="70a0d-138">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="70a0d-139">專注的內部錐形之間的照明減少 (Theta) 和外部錐形的外緣 (Phi) 指定的角度。</span><span class="sxs-lookup"><span data-stu-id="70a0d-139">Decrease in illumination between a spotlight's inner cone (the angle specified by Theta) and the outer edge of the outer cone (the angle specified by Phi).</span></span>

<span data-ttu-id="70a0d-140">對光源的衰減效果很微妙。</span><span class="sxs-lookup"><span data-stu-id="70a0d-140">The effect of falloff on the lighting is subtle.</span></span> <span data-ttu-id="70a0d-141">此外，藉由塑造衰減曲線，會造成較小的效能負面影響。</span><span class="sxs-lookup"><span data-stu-id="70a0d-141">Furthermore, a small performance penalty is incurred by shaping the falloff curve.</span></span> <span data-ttu-id="70a0d-142">基於這些理由，大部分的開發人員都會將此值設定為1.0。</span><span class="sxs-lookup"><span data-stu-id="70a0d-142">For these reasons, most developers set this value to 1.0.</span></span>

</dd> <dt>

<span data-ttu-id="70a0d-143">**Attenuation0**</span><span class="sxs-lookup"><span data-stu-id="70a0d-143">**Attenuation0**</span></span>
</dt> <dd>

<span data-ttu-id="70a0d-144">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="70a0d-144">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="70a0d-145">指定光線濃度如何隨著距離變更的值。</span><span class="sxs-lookup"><span data-stu-id="70a0d-145">Value specifying how the light intensity changes over distance.</span></span> <span data-ttu-id="70a0d-146">方向光線會忽略衰減值。</span><span class="sxs-lookup"><span data-stu-id="70a0d-146">Attenuation values are ignored for directional lights.</span></span> <span data-ttu-id="70a0d-147">此成員代表衰減常數。</span><span class="sxs-lookup"><span data-stu-id="70a0d-147">This member represents an attenuation constant.</span></span> <span data-ttu-id="70a0d-148">如需衰減的詳細資訊，請參閱 [ (Direct3D 9) 的淺色屬性 ](light-properties.md)。</span><span class="sxs-lookup"><span data-stu-id="70a0d-148">For information about attenuation, see [Light Properties (Direct3D 9)](light-properties.md).</span></span> <span data-ttu-id="70a0d-149">此成員的有效值範圍從0.0 到無限大。</span><span class="sxs-lookup"><span data-stu-id="70a0d-149">Valid values for this member range from 0.0 to infinity.</span></span> <span data-ttu-id="70a0d-150">若為非方向光源，則所有三個衰減值都不應同時設定為0.0。</span><span class="sxs-lookup"><span data-stu-id="70a0d-150">For non-directional lights, all three attenuation values should not be set to 0.0 at the same time.</span></span>

</dd> <dt>

<span data-ttu-id="70a0d-151">**Attenuation1**</span><span class="sxs-lookup"><span data-stu-id="70a0d-151">**Attenuation1**</span></span>
</dt> <dd>

<span data-ttu-id="70a0d-152">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="70a0d-152">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="70a0d-153">指定光線濃度如何隨著距離變更的值。</span><span class="sxs-lookup"><span data-stu-id="70a0d-153">Value specifying how the light intensity changes over distance.</span></span> <span data-ttu-id="70a0d-154">方向光線會忽略衰減值。</span><span class="sxs-lookup"><span data-stu-id="70a0d-154">Attenuation values are ignored for directional lights.</span></span> <span data-ttu-id="70a0d-155">此成員代表衰減常數。</span><span class="sxs-lookup"><span data-stu-id="70a0d-155">This member represents an attenuation constant.</span></span> <span data-ttu-id="70a0d-156">如需衰減的詳細資訊，請參閱 [ (Direct3D 9) 的淺色屬性 ](light-properties.md)。</span><span class="sxs-lookup"><span data-stu-id="70a0d-156">For information about attenuation, see [Light Properties (Direct3D 9)](light-properties.md).</span></span> <span data-ttu-id="70a0d-157">此成員的有效值範圍從0.0 到無限大。</span><span class="sxs-lookup"><span data-stu-id="70a0d-157">Valid values for this member range from 0.0 to infinity.</span></span> <span data-ttu-id="70a0d-158">若為非方向光源，則所有三個衰減值都不應同時設定為0.0。</span><span class="sxs-lookup"><span data-stu-id="70a0d-158">For non-directional lights, all three attenuation values should not be set to 0.0 at the same time.</span></span>

</dd> <dt>

<span data-ttu-id="70a0d-159">**Attenuation2**</span><span class="sxs-lookup"><span data-stu-id="70a0d-159">**Attenuation2**</span></span>
</dt> <dd>

<span data-ttu-id="70a0d-160">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="70a0d-160">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="70a0d-161">指定光線濃度如何隨著距離變更的值。</span><span class="sxs-lookup"><span data-stu-id="70a0d-161">Value specifying how the light intensity changes over distance.</span></span> <span data-ttu-id="70a0d-162">方向光線會忽略衰減值。</span><span class="sxs-lookup"><span data-stu-id="70a0d-162">Attenuation values are ignored for directional lights.</span></span> <span data-ttu-id="70a0d-163">此成員代表衰減常數。</span><span class="sxs-lookup"><span data-stu-id="70a0d-163">This member represents an attenuation constant.</span></span> <span data-ttu-id="70a0d-164">如需衰減的詳細資訊，請參閱 [ (Direct3D 9) 的淺色屬性 ](light-properties.md)。</span><span class="sxs-lookup"><span data-stu-id="70a0d-164">For information about attenuation, see [Light Properties (Direct3D 9)](light-properties.md).</span></span> <span data-ttu-id="70a0d-165">此成員的有效值範圍從0.0 到無限大。</span><span class="sxs-lookup"><span data-stu-id="70a0d-165">Valid values for this member range from 0.0 to infinity.</span></span> <span data-ttu-id="70a0d-166">若為非方向光源，則所有三個衰減值都不應同時設定為0.0。</span><span class="sxs-lookup"><span data-stu-id="70a0d-166">For non-directional lights, all three attenuation values should not be set to 0.0 at the same time.</span></span>

</dd> <dt>

<span data-ttu-id="70a0d-167">**Θ**</span><span class="sxs-lookup"><span data-stu-id="70a0d-167">**Theta**</span></span>
</dt> <dd>

<span data-ttu-id="70a0d-168">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="70a0d-168">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="70a0d-169">焦點的內部錐形角度（以弧度為單位），也就是完全發亮的聚焦錐形。</span><span class="sxs-lookup"><span data-stu-id="70a0d-169">Angle, in radians, of a spotlight's inner cone - that is, the fully illuminated spotlight cone.</span></span> <span data-ttu-id="70a0d-170">這個值必須介於0到 Phi 指定的值之間。</span><span class="sxs-lookup"><span data-stu-id="70a0d-170">This value must be in the range from 0 through the value specified by Phi.</span></span>

</dd> <dt>

<span data-ttu-id="70a0d-171">**披**</span><span class="sxs-lookup"><span data-stu-id="70a0d-171">**Phi**</span></span>
</dt> <dd>

<span data-ttu-id="70a0d-172">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="70a0d-172">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="70a0d-173">角度，以弧度為單位，定義焦點外部錐形的外緣。</span><span class="sxs-lookup"><span data-stu-id="70a0d-173">Angle, in radians, defining the outer edge of the spotlight's outer cone.</span></span> <span data-ttu-id="70a0d-174">焦點以外的點不會發亮。</span><span class="sxs-lookup"><span data-stu-id="70a0d-174">Points outside this cone are not lit by the spotlight.</span></span> <span data-ttu-id="70a0d-175">這個值必須介於0和 pi 之間。</span><span class="sxs-lookup"><span data-stu-id="70a0d-175">This value must be between 0 and pi.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="70a0d-176">規格需求</span><span class="sxs-lookup"><span data-stu-id="70a0d-176">Requirements</span></span>



| <span data-ttu-id="70a0d-177">需求</span><span class="sxs-lookup"><span data-stu-id="70a0d-177">Requirement</span></span> | <span data-ttu-id="70a0d-178">值</span><span class="sxs-lookup"><span data-stu-id="70a0d-178">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="70a0d-179">標頭</span><span class="sxs-lookup"><span data-stu-id="70a0d-179">Header</span></span><br/> | <dl> <span data-ttu-id="70a0d-180"><dt>D3D9Types。h</dt></span><span class="sxs-lookup"><span data-stu-id="70a0d-180"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70a0d-181">另請參閱</span><span class="sxs-lookup"><span data-stu-id="70a0d-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70a0d-182">Direct3D 結構</span><span class="sxs-lookup"><span data-stu-id="70a0d-182">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="70a0d-183">**GetLight**</span><span class="sxs-lookup"><span data-stu-id="70a0d-183">**GetLight**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getlight)
</dt> <dt>

[<span data-ttu-id="70a0d-184">**SetLight**</span><span class="sxs-lookup"><span data-stu-id="70a0d-184">**SetLight**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setlight)
</dt> </dl>

 

 
