---
description: 定義用於網格正切框架計算的設定。
ms.assetid: b525b4cc-9a2d-4569-bae8-7cc7f7832cbc
title: 'D3DXTANGENT 列舉 (D3dx9mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTANGENT
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 43e3c5ced0eee3366b85070ce89d19154d048ab4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106993877"
---
# <a name="d3dxtangent-enumeration"></a><span data-ttu-id="583ca-103">D3DXTANGENT 列舉</span><span class="sxs-lookup"><span data-stu-id="583ca-103">D3DXTANGENT enumeration</span></span>

<span data-ttu-id="583ca-104">定義用於網格正切框架計算的設定。</span><span class="sxs-lookup"><span data-stu-id="583ca-104">Defines settings used for mesh tangent frame computations.</span></span>

## <a name="syntax"></a><span data-ttu-id="583ca-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="583ca-105">Syntax</span></span>


```C++
typedef enum D3DXTANGENT { 
  D3DXTANGENT_WRAP_U                   = 0x01,
  D3DXTANGENT_WRAP_V                   = 0x02,
  D3DXTANGENT_WRAP_UV                  = 0x03,
  D3DXTANGENT_DONT_NORMALIZE_PARTIALS  = 0x04,
  D3DXTANGENT_DONT_ORTHOGONALIZE       = 0x08,
  D3DXTANGENT_ORTHOGONALIZE_FROM_V     = 0x010,
  D3DXTANGENT_ORTHOGONALIZE_FROM_U     = 0x020,
  D3DXTANGENT_WEIGHT_BY_AREA           = 0x040,
  D3DXTANGENT_WEIGHT_EQUAL             = 0x080,
  D3DXTANGENT_WIND_CW                  = 0x0100,
  D3DXTANGENT_CALCULATE_NORMALS        = 0x0200,
  D3DXTANGENT_GENERATE_IN_PLACE        = 0x0400
} D3DXTANGENT, *LPD3DXTANGENT;
```



## <a name="constants"></a><span data-ttu-id="583ca-106">常數</span><span class="sxs-lookup"><span data-stu-id="583ca-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="583ca-107"><span id="D3DXTANGENT_WRAP_U"></span><span id="d3dxtangent_wrap_u"></span>**D3DXTANGENT \_ WRAP \_ U**</span><span class="sxs-lookup"><span data-stu-id="583ca-107"><span id="D3DXTANGENT_WRAP_U"></span><span id="d3dxtangent_wrap_u"></span>**D3DXTANGENT\_WRAP\_U**</span></span>
</dt> <dd>

<span data-ttu-id="583ca-108">U 方向的材質座標值介於0和1之間。</span><span class="sxs-lookup"><span data-stu-id="583ca-108">Texture coordinate values in the u direction are between 0 and 1.</span></span> <span data-ttu-id="583ca-109">在此情況下，將會選擇材質座標集合，以將三角形的周邊最小化。</span><span class="sxs-lookup"><span data-stu-id="583ca-109">In this case a texture coordinate set will be chosen that minimizes the perimeter of the triangle.</span></span> <span data-ttu-id="583ca-110">請參閱 [ (Direct3D 9) 的材質包裝 ](texture-wrapping.md)。</span><span class="sxs-lookup"><span data-stu-id="583ca-110">See [Texture Wrapping (Direct3D 9)](texture-wrapping.md).</span></span>

</dd> <dt>

<span data-ttu-id="583ca-111"><span id="D3DXTANGENT_WRAP_V"></span><span id="d3dxtangent_wrap_v"></span>**D3DXTANGENT \_ WRAP \_ V**</span><span class="sxs-lookup"><span data-stu-id="583ca-111"><span id="D3DXTANGENT_WRAP_V"></span><span id="d3dxtangent_wrap_v"></span>**D3DXTANGENT\_WRAP\_V**</span></span>
</dt> <dd>

<span data-ttu-id="583ca-112">V 方向的材質座標值介於0和1之間。</span><span class="sxs-lookup"><span data-stu-id="583ca-112">Texture coordinate values in the v direction are between 0 and 1.</span></span> <span data-ttu-id="583ca-113">在此情況下，將會選擇材質座標集合，以將三角形的周邊最小化。</span><span class="sxs-lookup"><span data-stu-id="583ca-113">In this case a texture coordinate set will be chosen that minimizes the perimeter of the triangle.</span></span> <span data-ttu-id="583ca-114">請參閱 [ (Direct3D 9) 的材質包裝 ](texture-wrapping.md)。</span><span class="sxs-lookup"><span data-stu-id="583ca-114">See [Texture Wrapping (Direct3D 9)](texture-wrapping.md).</span></span>

</dd> <dt>

<span data-ttu-id="583ca-115"><span id="D3DXTANGENT_WRAP_UV"></span><span id="d3dxtangent_wrap_uv"></span>**D3DXTANGENT \_ WRAP \_ UV**</span><span class="sxs-lookup"><span data-stu-id="583ca-115"><span id="D3DXTANGENT_WRAP_UV"></span><span id="d3dxtangent_wrap_uv"></span>**D3DXTANGENT\_WRAP\_UV**</span></span>
</dt> <dd>

<span data-ttu-id="583ca-116">您和 v 方向的材質座標值都介於0和1之間。</span><span class="sxs-lookup"><span data-stu-id="583ca-116">Texture coordinate values in both u and v directions are between 0 and 1.</span></span> <span data-ttu-id="583ca-117">在此情況下，將會選擇材質座標集合，以將三角形的周邊最小化。</span><span class="sxs-lookup"><span data-stu-id="583ca-117">In this case a texture coordinate set will be chosen that minimizes the perimeter of the triangle.</span></span> <span data-ttu-id="583ca-118">請參閱 [ (Direct3D 9) 的材質包裝 ](texture-wrapping.md)。</span><span class="sxs-lookup"><span data-stu-id="583ca-118">See [Texture Wrapping (Direct3D 9)](texture-wrapping.md).</span></span>

</dd> <dt>

<span data-ttu-id="583ca-119"><span id="D3DXTANGENT_DONT_NORMALIZE_PARTIALS"></span><span id="d3dxtangent_dont_normalize_partials"></span>**D3DXTANGENT 不會 \_ \_ 標準化 \_ 部分**</span><span class="sxs-lookup"><span data-stu-id="583ca-119"><span id="D3DXTANGENT_DONT_NORMALIZE_PARTIALS"></span><span id="d3dxtangent_dont_normalize_partials"></span>**D3DXTANGENT\_DONT\_NORMALIZE\_PARTIALS**</span></span>
</dt> <dd>

<span data-ttu-id="583ca-120">請勿標準化材質座標的部分衍生。</span><span class="sxs-lookup"><span data-stu-id="583ca-120">Do not normalize partial derivatives with respect to texture coordinates.</span></span> <span data-ttu-id="583ca-121">如果未正規化，部分衍生的小數位數會與3D 模型的尺規成正比，除以 (u，v) 空間中的三角形小數位數。</span><span class="sxs-lookup"><span data-stu-id="583ca-121">If not normalized, the scale of the partial derivatives is proportional to the scale of the 3D model divided by the scale of the triangle in (u, v) space.</span></span> <span data-ttu-id="583ca-122">這個調整規模值會提供量值，以指定的方向伸展材品質。</span><span class="sxs-lookup"><span data-stu-id="583ca-122">This scale value provides a measure of how much the texture is stretched in a given direction.</span></span> <span data-ttu-id="583ca-123">產生的向量長度是部分衍生的長度的加權總和。</span><span class="sxs-lookup"><span data-stu-id="583ca-123">The resulting vector length is a weighted sum of the lengths of the partial derivatives.</span></span>

</dd> <dt>

<span data-ttu-id="583ca-124"><span id="D3DXTANGENT_DONT_ORTHOGONALIZE"></span><span id="d3dxtangent_dont_orthogonalize"></span>**D3DXTANGENT \_ 不 \_ ORTHOGONALIZE**</span><span class="sxs-lookup"><span data-stu-id="583ca-124"><span id="D3DXTANGENT_DONT_ORTHOGONALIZE"></span><span id="d3dxtangent_dont_orthogonalize"></span>**D3DXTANGENT\_DONT\_ORTHOGONALIZE**</span></span>
</dt> <dd>

<span data-ttu-id="583ca-125">請勿將材質座標轉換成正笛卡兒座標。</span><span class="sxs-lookup"><span data-stu-id="583ca-125">Do not transform texture coordinates to orthogonal Cartesian coordinates.</span></span> <span data-ttu-id="583ca-126">與您的 D3DXTANGENT \_ ORTHOGONALIZE 彼此互斥 \_ \_ ，並 \_ \_ 從 V D3DXTANGENT ORTHOGONALIZE \_ 。</span><span class="sxs-lookup"><span data-stu-id="583ca-126">Mutually exclusive with D3DXTANGENT\_ORTHOGONALIZE\_FROM\_U and D3DXTANGENT\_ORTHOGONALIZE\_FROM\_V.</span></span>

</dd> <dt>

<span data-ttu-id="583ca-127"><span id="D3DXTANGENT_ORTHOGONALIZE_FROM_V"></span><span id="d3dxtangent_orthogonalize_from_v"></span>**\_ \_ 從 V D3DXTANGENT \_ ORTHOGONALIZE**</span><span class="sxs-lookup"><span data-stu-id="583ca-127"><span id="D3DXTANGENT_ORTHOGONALIZE_FROM_V"></span><span id="d3dxtangent_orthogonalize_from_v"></span>**D3DXTANGENT\_ORTHOGONALIZE\_FROM\_V**</span></span>
</dt> <dd>

<span data-ttu-id="583ca-128">針對每個頂點個別計算紋理座標 v 的部分衍生，然後根據您的部分衍生，以與 v 和一般向量相關的局部衍生乘積來計算部分衍生。</span><span class="sxs-lookup"><span data-stu-id="583ca-128">Compute the partial derivative with respect to texture coordinate v independently for each vertex, and then compute the partial derivative with respect to u as the cross product of the partial derivative with respect to v and the normal vector.</span></span> <span data-ttu-id="583ca-129">與 D3DXTANGENT 互斥，不是 \_ \_ 來自 U 的 ORTHOGONALIZE 和 D3DXTANGENT \_ ORTHOGONALIZE \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="583ca-129">Mutually exclusive with D3DXTANGENT\_DONT\_ORTHOGONALIZE and D3DXTANGENT\_ORTHOGONALIZE\_FROM\_U.</span></span>

</dd> <dt>

<span data-ttu-id="583ca-130"><span id="D3DXTANGENT_ORTHOGONALIZE_FROM_U"></span><span id="d3dxtangent_orthogonalize_from_u"></span>**\_ \_ 從 U D3DXTANGENT \_ ORTHOGONALIZE**</span><span class="sxs-lookup"><span data-stu-id="583ca-130"><span id="D3DXTANGENT_ORTHOGONALIZE_FROM_U"></span><span id="d3dxtangent_orthogonalize_from_u"></span>**D3DXTANGENT\_ORTHOGONALIZE\_FROM\_U**</span></span>
</dt> <dd>

<span data-ttu-id="583ca-131">針對每個頂點個別計算材質座標 u 的部分衍生，然後計算以 v 作為標準向量交叉乘積的部分衍生，以及與您相關的部分衍生。</span><span class="sxs-lookup"><span data-stu-id="583ca-131">Compute the partial derivative with respect to texture coordinate u independently for each vertex, and then compute the partial derivative with respect to v as the cross product of the normal vector and the partial derivative with respect to u.</span></span> <span data-ttu-id="583ca-132">與 D3DXTANGENT 互斥，不是 \_ \_ 來自 V 的 ORTHOGONALIZE 和 D3DXTANGENT \_ ORTHOGONALIZE \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="583ca-132">Mutually exclusive with D3DXTANGENT\_DONT\_ORTHOGONALIZE and D3DXTANGENT\_ORTHOGONALIZE\_FROM\_V.</span></span>

</dd> <dt>

<span data-ttu-id="583ca-133"><span id="D3DXTANGENT_WEIGHT_BY_AREA"></span><span id="d3dxtangent_weight_by_area"></span>**\_ \_ 依區域的 D3DXTANGENT 權數 \_**</span><span class="sxs-lookup"><span data-stu-id="583ca-133"><span id="D3DXTANGENT_WEIGHT_BY_AREA"></span><span id="d3dxtangent_weight_by_area"></span>**D3DXTANGENT\_WEIGHT\_BY\_AREA**</span></span>
</dt> <dd>

<span data-ttu-id="583ca-134">根據附加至該頂點的三角形區域，加權計算的每個頂點一般或部分衍生向量的方向。</span><span class="sxs-lookup"><span data-stu-id="583ca-134">Weight the direction of the computed per-vertex normal or partial derivative vector according to the areas of triangles attached to that vertex.</span></span> <span data-ttu-id="583ca-135">與 D3DXTANGENT \_ 權數相等互斥 \_ 。</span><span class="sxs-lookup"><span data-stu-id="583ca-135">Mutually exclusive with D3DXTANGENT\_WEIGHT\_EQUAL.</span></span>

</dd> <dt>

<span data-ttu-id="583ca-136"><span id="D3DXTANGENT_WEIGHT_EQUAL"></span><span id="d3dxtangent_weight_equal"></span>**D3DXTANGENT \_ 權數 \_ 等於**</span><span class="sxs-lookup"><span data-stu-id="583ca-136"><span id="D3DXTANGENT_WEIGHT_EQUAL"></span><span id="d3dxtangent_weight_equal"></span>**D3DXTANGENT\_WEIGHT\_EQUAL**</span></span>
</dt> <dd>

<span data-ttu-id="583ca-137">計算輸入網格每個三角形的單位長度一般向量。</span><span class="sxs-lookup"><span data-stu-id="583ca-137">Compute a unit-length normal vector for each triangle of the input mesh.</span></span> <span data-ttu-id="583ca-138">依區域以 D3DXTANGENT \_ 權數互相排斥 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="583ca-138">Mutually exclusive with D3DXTANGENT\_WEIGHT\_BY\_AREA.</span></span>

</dd> <dt>

<span data-ttu-id="583ca-139"><span id="D3DXTANGENT_WIND_CW"></span><span id="d3dxtangent_wind_cw"></span>**D3DXTANGENT \_ 風 \_ CW**</span><span class="sxs-lookup"><span data-stu-id="583ca-139"><span id="D3DXTANGENT_WIND_CW"></span><span id="d3dxtangent_wind_cw"></span>**D3DXTANGENT\_WIND\_CW**</span></span>
</dt> <dd>

<span data-ttu-id="583ca-140">頂點會依每個三角形的順向方向排序。</span><span class="sxs-lookup"><span data-stu-id="583ca-140">Vertices are ordered in a clockwise direction around each triangle.</span></span> <span data-ttu-id="583ca-141">因此，計算出的一般向量方向，會從使用逆時針頂點順序計算的方向反轉180度。</span><span class="sxs-lookup"><span data-stu-id="583ca-141">The computed normal vector direction is therefore inverted 180 degrees from the direction computed using counterclockwise vertex ordering.</span></span>

</dd> <dt>

<span data-ttu-id="583ca-142"><span id="D3DXTANGENT_CALCULATE_NORMALS"></span><span id="d3dxtangent_calculate_normals"></span>**D3DXTANGENT \_ 計算 \_ 法線**</span><span class="sxs-lookup"><span data-stu-id="583ca-142"><span id="D3DXTANGENT_CALCULATE_NORMALS"></span><span id="d3dxtangent_calculate_normals"></span>**D3DXTANGENT\_CALCULATE\_NORMALS**</span></span>
</dt> <dd>

<span data-ttu-id="583ca-143">針對輸入網格的每個三角形計算每個頂點的一般向量，並忽略輸入網格中已存在的任何一般向量。</span><span class="sxs-lookup"><span data-stu-id="583ca-143">Compute the per-vertex normal vector for each triangle of the input mesh, and ignore any normal vectors already in the input mesh.</span></span>

</dd> <dt>

<span data-ttu-id="583ca-144"><span id="D3DXTANGENT_GENERATE_IN_PLACE"></span><span id="d3dxtangent_generate_in_place"></span>**D3DXTANGENT \_ \_ 就地產生 \_**</span><span class="sxs-lookup"><span data-stu-id="583ca-144"><span id="D3DXTANGENT_GENERATE_IN_PLACE"></span><span id="d3dxtangent_generate_in_place"></span>**D3DXTANGENT\_GENERATE\_IN\_PLACE**</span></span>
</dt> <dd>

<span data-ttu-id="583ca-145">結果會儲存在原始的輸入網格中，而且不會使用輸出網格。</span><span class="sxs-lookup"><span data-stu-id="583ca-145">The results are stored in the original input mesh, and the output mesh is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="583ca-146">規格需求</span><span class="sxs-lookup"><span data-stu-id="583ca-146">Requirements</span></span>



| <span data-ttu-id="583ca-147">需求</span><span class="sxs-lookup"><span data-stu-id="583ca-147">Requirement</span></span> | <span data-ttu-id="583ca-148">值</span><span class="sxs-lookup"><span data-stu-id="583ca-148">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="583ca-149">標頭</span><span class="sxs-lookup"><span data-stu-id="583ca-149">Header</span></span><br/> | <dl> <span data-ttu-id="583ca-150"><dt>D3dx9mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="583ca-150"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="583ca-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="583ca-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="583ca-152">D3DX 列舉</span><span class="sxs-lookup"><span data-stu-id="583ca-152">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[<span data-ttu-id="583ca-153">**D3DXComputeTangentFrameEx**</span><span class="sxs-lookup"><span data-stu-id="583ca-153">**D3DXComputeTangentFrameEx**</span></span>](d3dxcomputetangentframeex.md)
</dt> </dl>

 

 




