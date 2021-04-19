---
description: 使用指定的3D 向量，傳回 Barycentric 座標中的點。
ms.assetid: 572e151d-8044-480e-92b2-3f973d92d03e
title: 'D3DXVec3BaryCentric 函式 (D3DX10Math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3BaryCentric
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 3c14d01acc71a13cabb810d5b26d0afaf7f67f7c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106989198"
---
# <a name="d3dxvec3barycentric-function-d3dx10mathh"></a><span data-ttu-id="9fc30-103">D3DXVec3BaryCentric 函式 (D3DX10Math) </span><span class="sxs-lookup"><span data-stu-id="9fc30-103">D3DXVec3BaryCentric function (D3DX10Math.h)</span></span>

<span data-ttu-id="9fc30-104">使用指定的3D 向量，傳回 Barycentric 座標中的點。</span><span class="sxs-lookup"><span data-stu-id="9fc30-104">Returns a point in Barycentric coordinates, using the specified 3D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fc30-105">語法</span><span class="sxs-lookup"><span data-stu-id="9fc30-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3BaryCentric(
  _In_       D3DXVECTOR3 *pOut,
  _In_ const D3DXVECTOR3 *pV1,
  _In_ const D3DXVECTOR3 *pV2,
  _In_ const D3DXVECTOR3 *pV3,
  _In_       FLOAT       f,
  _In_       FLOAT       g
);
```



## <a name="parameters"></a><span data-ttu-id="9fc30-106">參數</span><span class="sxs-lookup"><span data-stu-id="9fc30-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9fc30-107">*不悅* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9fc30-107">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fc30-108">類型： **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="9fc30-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="9fc30-109">作業結果之 [**D3DXVECTOR3**](d3d10-d3dxvector3.md) 的指標。</span><span class="sxs-lookup"><span data-stu-id="9fc30-109">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="9fc30-110">*pV1* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9fc30-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fc30-111">Type： **Const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="9fc30-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="9fc30-112">來源 D3DXVECTOR3 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="9fc30-112">Pointer to a source D3DXVECTOR3 structure.</span></span>

</dd> <dt>

<span data-ttu-id="9fc30-113">*pV2* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9fc30-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fc30-114">Type： **Const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="9fc30-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="9fc30-115">來源 D3DXVECTOR3 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="9fc30-115">Pointer to a source D3DXVECTOR3 structure.</span></span>

</dd> <dt>

<span data-ttu-id="9fc30-116">*pV3* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9fc30-116">*pV3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fc30-117">Type： **Const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="9fc30-117">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="9fc30-118">來源 D3DXVECTOR3 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="9fc30-118">Pointer to a source D3DXVECTOR3 structure.</span></span>

</dd> <dt>

<span data-ttu-id="9fc30-119">*f* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9fc30-119">*f* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fc30-120">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9fc30-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9fc30-121">加權係數。</span><span class="sxs-lookup"><span data-stu-id="9fc30-121">Weighting factor.</span></span> <span data-ttu-id="9fc30-122">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="9fc30-122">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="9fc30-123">*g* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9fc30-123">*g* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fc30-124">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9fc30-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9fc30-125">加權係數。</span><span class="sxs-lookup"><span data-stu-id="9fc30-125">Weighting factor.</span></span> <span data-ttu-id="9fc30-126">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="9fc30-126">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9fc30-127">傳回值</span><span class="sxs-lookup"><span data-stu-id="9fc30-127">Return value</span></span>

<span data-ttu-id="9fc30-128">類型： **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="9fc30-128">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="9fc30-129">Barycentric 座標中 D3DXVECTOR3 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="9fc30-129">Pointer to a D3DXVECTOR3 structure in Barycentric coordinates.</span></span>

## <a name="remarks"></a><span data-ttu-id="9fc30-130">備註</span><span class="sxs-lookup"><span data-stu-id="9fc30-130">Remarks</span></span>

<span data-ttu-id="9fc30-131">D3DXVec3BaryCentric 函式可讓您瞭解三角形中和周圍的點，而不受三角形實際位置的影響。</span><span class="sxs-lookup"><span data-stu-id="9fc30-131">The D3DXVec3BaryCentric function provides a way to understand points in and around a triangle, independent of where the triangle is actually located.</span></span> <span data-ttu-id="9fc30-132">此函式會使用下列方程式傳回結果點： V1 + f (V2-V1) + g (V3-V1) 。</span><span class="sxs-lookup"><span data-stu-id="9fc30-132">This function returns the resulting point by using the following equation: V1 + f(V2-V1) + g(V3-V1).</span></span>

<span data-ttu-id="9fc30-133">平面 V1V2V3 中的任何點都可由 Barycentric 座標 (f，g) 表示。參數 f 控制要將多少 V2 加權至結果，而參數 g 控制在結果中加權多少 V3。</span><span class="sxs-lookup"><span data-stu-id="9fc30-133">Any point in the plane V1V2V3 can be represented by the Barycentric coordinate (f,g).The parameter f controls how much V2 gets weighted into the result and the parameter g controls how much V3 gets weighted into the result.</span></span> <span data-ttu-id="9fc30-134">最後，1-f-g 控制 V1 在結果中的加權量。</span><span class="sxs-lookup"><span data-stu-id="9fc30-134">Lastly, 1-f-g controls how much V1 gets weighted into the result.</span></span>

<span data-ttu-id="9fc30-135">請注意下列關聯性。</span><span class="sxs-lookup"><span data-stu-id="9fc30-135">Note the following relations.</span></span>

-   <span data-ttu-id="9fc30-136">如果 (f>= 0 &，& g>= 0 &，& 1-f-g>= 0) ，則點位於三角形 V1V2V3 內。</span><span class="sxs-lookup"><span data-stu-id="9fc30-136">If (f>=0 &, & g>=0 &, & 1-f-g>=0), the point is inside the triangle V1V2V3.</span></span>
-   <span data-ttu-id="9fc30-137">如果 (f = = 0 &，& g>= 0 &，& 1-f-g>= 0) ，則點位於行 V1V3 上。</span><span class="sxs-lookup"><span data-stu-id="9fc30-137">If (f==0 &, & g>=0 &, & 1-f-g>=0), the point is on the line V1V3.</span></span>
-   <span data-ttu-id="9fc30-138">如果 (f>= 0 &，& g = = 0 &，& 1-f-g>= 0) ，則點位於行 V1V2 上。</span><span class="sxs-lookup"><span data-stu-id="9fc30-138">If (f>=0 &, & g==0 &, & 1-f-g>=0), the point is on the line V1V2.</span></span>
-   <span data-ttu-id="9fc30-139">如果 (f>= 0 &，& g>= 0 &，& 1-f-g = = 0) ，則點位於行 V2V3 上。</span><span class="sxs-lookup"><span data-stu-id="9fc30-139">If (f>=0 &, & g>=0 &, & 1-f-g==0), the point is on the line V2V3.</span></span>

<span data-ttu-id="9fc30-140">Barycentric 座標是一種一般座標形式。</span><span class="sxs-lookup"><span data-stu-id="9fc30-140">Barycentric coordinates are a form of general coordinates.</span></span> <span data-ttu-id="9fc30-141">在此內容中，使用 Barycentric 座標代表座標系統中的變更。</span><span class="sxs-lookup"><span data-stu-id="9fc30-141">In this context, using Barycentric coordinates represents a change in coordinate systems.</span></span> <span data-ttu-id="9fc30-142">笛卡兒座標的 true 是 Barycentric 座標的 true。</span><span class="sxs-lookup"><span data-stu-id="9fc30-142">What holds true for Cartesian coordinates holds true for Barycentric coordinates.</span></span>

<span data-ttu-id="9fc30-143">此函式的傳回值與不悅參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="9fc30-143">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="9fc30-144">如此一來，D3DXVec3BaryCentric 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="9fc30-144">In this way, the D3DXVec3BaryCentric function can be used as a parameter for another function.</span></span>

<span data-ttu-id="9fc30-145">Barycentric 座標會根據三角形的頂點定義三角形內的點。</span><span class="sxs-lookup"><span data-stu-id="9fc30-145">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="9fc30-146">如需 barycentric 座標的更深入說明，請參閱 [Mathworld 的 Barycentric 座標描述](https://mathworld.wolfram.com/BarycentricCoordinates.html)。</span><span class="sxs-lookup"><span data-stu-id="9fc30-146">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="9fc30-147">規格需求</span><span class="sxs-lookup"><span data-stu-id="9fc30-147">Requirements</span></span>



| <span data-ttu-id="9fc30-148">需求</span><span class="sxs-lookup"><span data-stu-id="9fc30-148">Requirement</span></span> | <span data-ttu-id="9fc30-149">值</span><span class="sxs-lookup"><span data-stu-id="9fc30-149">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9fc30-150">標頭</span><span class="sxs-lookup"><span data-stu-id="9fc30-150">Header</span></span><br/> | <dl> <span data-ttu-id="9fc30-151"><dt>D3DX10Math。h</dt></span><span class="sxs-lookup"><span data-stu-id="9fc30-151"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9fc30-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9fc30-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fc30-153">數學函數</span><span class="sxs-lookup"><span data-stu-id="9fc30-153">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
