---
description: 指定材質屬性。
ms.assetid: 943e6f6d-8091-462f-8c44-e0c27686934a
title: 'D3DMATERIAL9 結構 (D3D9Types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DMATERIAL9
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: b9c3ad93fe2cb80fe758e2e66da37cce9d4267ad
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104386473"
---
# <a name="d3dmaterial9-structure"></a><span data-ttu-id="93f5a-103">D3DMATERIAL9 結構</span><span class="sxs-lookup"><span data-stu-id="93f5a-103">D3DMATERIAL9 structure</span></span>

<span data-ttu-id="93f5a-104">指定材質屬性。</span><span class="sxs-lookup"><span data-stu-id="93f5a-104">Specifies material properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="93f5a-105">語法</span><span class="sxs-lookup"><span data-stu-id="93f5a-105">Syntax</span></span>


```C++
typedef struct D3DMATERIAL9 {
  D3DCOLORVALUE Diffuse;
  D3DCOLORVALUE Ambient;
  D3DCOLORVALUE Specular;
  D3DCOLORVALUE Emissive;
  float         Power;
} D3DMATERIAL9, *LPD3DMATERIAL9;
```



## <a name="members"></a><span data-ttu-id="93f5a-106">成員</span><span class="sxs-lookup"><span data-stu-id="93f5a-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="93f5a-107">**擴散**</span><span class="sxs-lookup"><span data-stu-id="93f5a-107">**Diffuse**</span></span>
</dt> <dd>

<span data-ttu-id="93f5a-108">類型： **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**</span><span class="sxs-lookup"><span data-stu-id="93f5a-108">Type: **[**D3DCOLORVALUE**](d3dcolorvalue.md)**</span></span>

</dd> <dd>

<span data-ttu-id="93f5a-109">值，指定材質的擴散色彩。</span><span class="sxs-lookup"><span data-stu-id="93f5a-109">Value specifying the diffuse color of the material.</span></span> <span data-ttu-id="93f5a-110">請參閱 [**D3DCOLORVALUE**](d3dcolorvalue.md)。</span><span class="sxs-lookup"><span data-stu-id="93f5a-110">See [**D3DCOLORVALUE**](d3dcolorvalue.md).</span></span>

</dd> <dt>

<span data-ttu-id="93f5a-111">**環境**</span><span class="sxs-lookup"><span data-stu-id="93f5a-111">**Ambient**</span></span>
</dt> <dd>

<span data-ttu-id="93f5a-112">類型： **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**</span><span class="sxs-lookup"><span data-stu-id="93f5a-112">Type: **[**D3DCOLORVALUE**](d3dcolorvalue.md)**</span></span>

</dd> <dd>

<span data-ttu-id="93f5a-113">值，指定材質的環境色彩。</span><span class="sxs-lookup"><span data-stu-id="93f5a-113">Value specifying the ambient color of the material.</span></span> <span data-ttu-id="93f5a-114">請參閱 [**D3DCOLORVALUE**](d3dcolorvalue.md)。</span><span class="sxs-lookup"><span data-stu-id="93f5a-114">See [**D3DCOLORVALUE**](d3dcolorvalue.md).</span></span>

</dd> <dt>

<span data-ttu-id="93f5a-115">**反射**</span><span class="sxs-lookup"><span data-stu-id="93f5a-115">**Specular**</span></span>
</dt> <dd>

<span data-ttu-id="93f5a-116">類型： **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**</span><span class="sxs-lookup"><span data-stu-id="93f5a-116">Type: **[**D3DCOLORVALUE**](d3dcolorvalue.md)**</span></span>

</dd> <dd>

<span data-ttu-id="93f5a-117">值，指定材質的反射色彩。</span><span class="sxs-lookup"><span data-stu-id="93f5a-117">Value specifying the specular color of the material.</span></span> <span data-ttu-id="93f5a-118">請參閱 [**D3DCOLORVALUE**](d3dcolorvalue.md)。</span><span class="sxs-lookup"><span data-stu-id="93f5a-118">See [**D3DCOLORVALUE**](d3dcolorvalue.md).</span></span>

</dd> <dt>

<span data-ttu-id="93f5a-119">**放射**</span><span class="sxs-lookup"><span data-stu-id="93f5a-119">**Emissive**</span></span>
</dt> <dd>

<span data-ttu-id="93f5a-120">類型： **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**</span><span class="sxs-lookup"><span data-stu-id="93f5a-120">Type: **[**D3DCOLORVALUE**](d3dcolorvalue.md)**</span></span>

</dd> <dd>

<span data-ttu-id="93f5a-121">值，指定材質的放射色彩。</span><span class="sxs-lookup"><span data-stu-id="93f5a-121">Value specifying the emissive color of the material.</span></span> <span data-ttu-id="93f5a-122">請參閱 [**D3DCOLORVALUE**](d3dcolorvalue.md)。</span><span class="sxs-lookup"><span data-stu-id="93f5a-122">See [**D3DCOLORVALUE**](d3dcolorvalue.md).</span></span>

</dd> <dt>

<span data-ttu-id="93f5a-123">**電源**</span><span class="sxs-lookup"><span data-stu-id="93f5a-123">**Power**</span></span>
</dt> <dd>

<span data-ttu-id="93f5a-124">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="93f5a-124">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="93f5a-125">指定反射醒目顯示清晰度的浮點值。</span><span class="sxs-lookup"><span data-stu-id="93f5a-125">Floating-point value specifying the sharpness of specular highlights.</span></span> <span data-ttu-id="93f5a-126">值愈高，反白顯示的愈銳利。</span><span class="sxs-lookup"><span data-stu-id="93f5a-126">The higher the value, the sharper the highlight.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="93f5a-127">備註</span><span class="sxs-lookup"><span data-stu-id="93f5a-127">Remarks</span></span>

<span data-ttu-id="93f5a-128">若要關閉高光，請 \_ 使用 [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)將 D3DRS SPECULARENABLE 設定為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="93f5a-128">To turn off specular highlights, set D3DRS\_SPECULARENABLE to **FALSE**, using [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md).</span></span> <span data-ttu-id="93f5a-129">這是最快的選項，因為系統不會計算任何高光。</span><span class="sxs-lookup"><span data-stu-id="93f5a-129">This is the fastest option because no specular highlights will be calculated.</span></span>

<span data-ttu-id="93f5a-130">如需使用燈光引擎計算反射光源的詳細資訊，請參閱 [ (Direct3D 9) 的反射光源 ](specular-lighting.md)。</span><span class="sxs-lookup"><span data-stu-id="93f5a-130">For more information about using the lighting engine to calculate specular lighting, see [Specular Lighting (Direct3D 9)](specular-lighting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="93f5a-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="93f5a-131">Requirements</span></span>



| <span data-ttu-id="93f5a-132">需求</span><span class="sxs-lookup"><span data-stu-id="93f5a-132">Requirement</span></span> | <span data-ttu-id="93f5a-133">值</span><span class="sxs-lookup"><span data-stu-id="93f5a-133">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="93f5a-134">標頭</span><span class="sxs-lookup"><span data-stu-id="93f5a-134">Header</span></span><br/> | <dl> <span data-ttu-id="93f5a-135"><dt>D3D9Types。h</dt></span><span class="sxs-lookup"><span data-stu-id="93f5a-135"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93f5a-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="93f5a-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93f5a-137">Direct3D 結構</span><span class="sxs-lookup"><span data-stu-id="93f5a-137">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="93f5a-138">**IDirect3DDevice9::GetMaterial**</span><span class="sxs-lookup"><span data-stu-id="93f5a-138">**IDirect3DDevice9::GetMaterial**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getmaterial)
</dt> <dt>

[<span data-ttu-id="93f5a-139">**IDirect3DDevice9::SetMaterial**</span><span class="sxs-lookup"><span data-stu-id="93f5a-139">**IDirect3DDevice9::SetMaterial**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial)
</dt> </dl>

 

 
