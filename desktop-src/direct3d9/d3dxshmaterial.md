---
description: 球形調和 (SH) 預先計算 radiance transfer (PRT) 材質特性。
ms.assetid: 2be49f96-ac61-46aa-8d56-d8eee8dca9ed
title: 'D3DXSHMATERIAL 結構 (D3dx9mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHMATERIAL
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 0600cc0c1ebe086f0d6679182125350b1ee8ca98
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106975670"
---
# <a name="d3dxshmaterial-structure"></a><span data-ttu-id="77ea5-103">D3DXSHMATERIAL 結構</span><span class="sxs-lookup"><span data-stu-id="77ea5-103">D3DXSHMATERIAL structure</span></span>

<span data-ttu-id="77ea5-104">球形調和 (SH) 預先計算 radiance transfer (PRT) 材質特性。</span><span class="sxs-lookup"><span data-stu-id="77ea5-104">Spherical harmonic (SH) precomputed radiance transfer (PRT) material characteristics.</span></span>

## <a name="syntax"></a><span data-ttu-id="77ea5-105">語法</span><span class="sxs-lookup"><span data-stu-id="77ea5-105">Syntax</span></span>


```C++
typedef struct D3DXSHMATERIAL {
  D3DCOLORVALUE Diffuse;
  BOOL          bMirror;
  BOOL          bSubSurf;
  FLOAT         RelativeIndexOfRefraction;
  D3DCOLORVALUE Absorption;
  D3DCOLORVALUE ReducedScattering;
} D3DXSHMATERIAL, *LPD3DXSHMATERIAL;
```



## <a name="members"></a><span data-ttu-id="77ea5-106">成員</span><span class="sxs-lookup"><span data-stu-id="77ea5-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="77ea5-107">**擴散**</span><span class="sxs-lookup"><span data-stu-id="77ea5-107">**Diffuse**</span></span>
</dt> <dd>

<span data-ttu-id="77ea5-108">類型： **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**</span><span class="sxs-lookup"><span data-stu-id="77ea5-108">Type: **[**D3DCOLORVALUE**](d3dcolorvalue.md)**</span></span>

</dd> <dd>

<span data-ttu-id="77ea5-109">介面的擴散 >albedo。</span><span class="sxs-lookup"><span data-stu-id="77ea5-109">Diffuse albedo of the surface.</span></span> <span data-ttu-id="77ea5-110">如果物件是鏡像，則會忽略此值。</span><span class="sxs-lookup"><span data-stu-id="77ea5-110">This value is ignored if the object is a mirror.</span></span>

</dd> <dt>

<span data-ttu-id="77ea5-111">**bMirror**</span><span class="sxs-lookup"><span data-stu-id="77ea5-111">**bMirror**</span></span>
</dt> <dd>

<span data-ttu-id="77ea5-112">類型： **[ **BOOL**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="77ea5-112">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="77ea5-113">必須設定為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="77ea5-113">Must be set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="77ea5-114">**bSubSurf**</span><span class="sxs-lookup"><span data-stu-id="77ea5-114">**bSubSurf**</span></span>
</dt> <dd>

<span data-ttu-id="77ea5-115">類型： **[ **BOOL**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="77ea5-115">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="77ea5-116">設定為 **TRUE** 以啟用地下散佈;任何地下散佈的物件都不能是鏡像。</span><span class="sxs-lookup"><span data-stu-id="77ea5-116">Set to **TRUE** to enable subsurface scattering; any object that does subsurface scattering cannot be a mirror.</span></span>

</dd> <dt>

<span data-ttu-id="77ea5-117">**RelativeIndexOfRefraction**</span><span class="sxs-lookup"><span data-stu-id="77ea5-117">**RelativeIndexOfRefraction**</span></span>
</dt> <dd>

<span data-ttu-id="77ea5-118">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="77ea5-118">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="77ea5-119">折射的相對索引是折射的兩個絕對索引之間的比率。</span><span class="sxs-lookup"><span data-stu-id="77ea5-119">Relative index of refraction is the ratio between two absolute indexes of refraction.</span></span> <span data-ttu-id="77ea5-120">折射的索引是發生角度的正弦與折射角度正弦的比率。</span><span class="sxs-lookup"><span data-stu-id="77ea5-120">An index of refraction is the ratio of the sine of the angle of incidence to the sine of the angle of refraction.</span></span>

</dd> <dt>

<span data-ttu-id="77ea5-121">**吸收**</span><span class="sxs-lookup"><span data-stu-id="77ea5-121">**Absorption**</span></span>
</dt> <dd>

<span data-ttu-id="77ea5-122">類型： **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**</span><span class="sxs-lookup"><span data-stu-id="77ea5-122">Type: **[**D3DCOLORVALUE**](d3dcolorvalue.md)**</span></span>

</dd> <dd>

<span data-ttu-id="77ea5-123">吸收係數是磁片區轉譯方程式的參數，可用來將參與媒體中的輕量傳播模型。</span><span class="sxs-lookup"><span data-stu-id="77ea5-123">The absorption coefficient is a parameter to the volume rendering equation used to model light propagation in a participating medium.</span></span>

</dd> <dt>

<span data-ttu-id="77ea5-124">**ReducedScattering**</span><span class="sxs-lookup"><span data-stu-id="77ea5-124">**ReducedScattering**</span></span>
</dt> <dd>

<span data-ttu-id="77ea5-125">類型： **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**</span><span class="sxs-lookup"><span data-stu-id="77ea5-125">Type: **[**D3DCOLORVALUE**](d3dcolorvalue.md)**</span></span>

</dd> <dd>

<span data-ttu-id="77ea5-126">減少的散佈係數是磁片區轉譯方程式的參數，可用來在參與的媒體中建立燈光傳播的模型。</span><span class="sxs-lookup"><span data-stu-id="77ea5-126">The reduced scattering coefficient is a parameter to the volume rendering equation used to model light propagation in a participating medium.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="77ea5-127">備註</span><span class="sxs-lookup"><span data-stu-id="77ea5-127">Remarks</span></span>

<span data-ttu-id="77ea5-128">非光譜場景會使用材質中的紅色色板，而非亮度值。</span><span class="sxs-lookup"><span data-stu-id="77ea5-128">Non-spectral scenes use the red channel from the materials instead of the luminance value.</span></span>

<span data-ttu-id="77ea5-129">如需 PRT 的詳細資訊，請參閱：</span><span class="sxs-lookup"><span data-stu-id="77ea5-129">For more information about PRT see:</span></span>

-   <span data-ttu-id="77ea5-130">Jensen，Henrik Wann，et al.exe. Siggraph 訴訟：地下 Light Transport 的實際模型，2001。</span><span class="sxs-lookup"><span data-stu-id="77ea5-130">Jensen, Henrik Wann, et al. Siggraph Proceedings: A Practical Model for Subsurface Light Transport, 2001.</span></span>

## <a name="requirements"></a><span data-ttu-id="77ea5-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="77ea5-131">Requirements</span></span>



| <span data-ttu-id="77ea5-132">需求</span><span class="sxs-lookup"><span data-stu-id="77ea5-132">Requirement</span></span> | <span data-ttu-id="77ea5-133">值</span><span class="sxs-lookup"><span data-stu-id="77ea5-133">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="77ea5-134">標頭</span><span class="sxs-lookup"><span data-stu-id="77ea5-134">Header</span></span><br/> | <dl> <span data-ttu-id="77ea5-135"><dt>D3dx9mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="77ea5-135"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77ea5-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="77ea5-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77ea5-137">D3DX 結構</span><span class="sxs-lookup"><span data-stu-id="77ea5-137">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
