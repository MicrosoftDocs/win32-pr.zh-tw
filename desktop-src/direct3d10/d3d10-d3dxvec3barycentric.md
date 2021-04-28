---
description: D3DXVec3BaryCentric 函式 (D3DX10Math) -使用指定的3D 向量，傳回 Barycentric 座標中的點。
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
ms.openlocfilehash: e350bde6d1b898088ccb9b68d10a9a346935bfd5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108246"
---
# <a name="d3dxvec3barycentric-function-d3dx10mathh"></a><span data-ttu-id="a1774-103">D3DXVec3BaryCentric 函式 (D3DX10Math) </span><span class="sxs-lookup"><span data-stu-id="a1774-103">D3DXVec3BaryCentric function (D3DX10Math.h)</span></span>

<span data-ttu-id="a1774-104">使用指定的3D 向量，傳回 Barycentric 座標中的點。</span><span class="sxs-lookup"><span data-stu-id="a1774-104">Returns a point in Barycentric coordinates, using the specified 3D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1774-105">語法</span><span class="sxs-lookup"><span data-stu-id="a1774-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="a1774-106">參數</span><span class="sxs-lookup"><span data-stu-id="a1774-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1774-107">*不悅* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a1774-107">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1774-108">類型： **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="a1774-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="a1774-109">作業結果之 [**D3DXVECTOR3**](d3d10-d3dxvector3.md) 的指標。</span><span class="sxs-lookup"><span data-stu-id="a1774-109">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="a1774-110">*pV1* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a1774-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1774-111">Type： **Const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="a1774-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="a1774-112">來源 D3DXVECTOR3 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="a1774-112">Pointer to a source D3DXVECTOR3 structure.</span></span>

</dd> <dt>

<span data-ttu-id="a1774-113">*pV2* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a1774-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1774-114">Type： **Const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="a1774-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="a1774-115">來源 D3DXVECTOR3 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="a1774-115">Pointer to a source D3DXVECTOR3 structure.</span></span>

</dd> <dt>

<span data-ttu-id="a1774-116">*pV3* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a1774-116">*pV3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1774-117">Type： **Const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="a1774-117">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="a1774-118">來源 D3DXVECTOR3 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="a1774-118">Pointer to a source D3DXVECTOR3 structure.</span></span>

</dd> <dt>

<span data-ttu-id="a1774-119">*f* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a1774-119">*f* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1774-120">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a1774-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a1774-121">加權係數。</span><span class="sxs-lookup"><span data-stu-id="a1774-121">Weighting factor.</span></span> <span data-ttu-id="a1774-122">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="a1774-122">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="a1774-123">*g* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a1774-123">*g* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1774-124">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a1774-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a1774-125">加權係數。</span><span class="sxs-lookup"><span data-stu-id="a1774-125">Weighting factor.</span></span> <span data-ttu-id="a1774-126">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="a1774-126">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1774-127">傳回值</span><span class="sxs-lookup"><span data-stu-id="a1774-127">Return value</span></span>

<span data-ttu-id="a1774-128">類型： **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="a1774-128">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="a1774-129">Barycentric 座標中 D3DXVECTOR3 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="a1774-129">Pointer to a D3DXVECTOR3 structure in Barycentric coordinates.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1774-130">備註</span><span class="sxs-lookup"><span data-stu-id="a1774-130">Remarks</span></span>

<span data-ttu-id="a1774-131">D3DXVec3BaryCentric 函式可讓您瞭解三角形中和周圍的點，而不受三角形實際位置的影響。</span><span class="sxs-lookup"><span data-stu-id="a1774-131">The D3DXVec3BaryCentric function provides a way to understand points in and around a triangle, independent of where the triangle is actually located.</span></span> <span data-ttu-id="a1774-132">此函式會使用下列方程式傳回結果點： V1 + f (V2-V1) + g (V3-V1) 。</span><span class="sxs-lookup"><span data-stu-id="a1774-132">This function returns the resulting point by using the following equation: V1 + f(V2-V1) + g(V3-V1).</span></span>

<span data-ttu-id="a1774-133">平面 V1V2V3 中的任何點都可由 Barycentric 座標 (f，g) 表示。參數 f 控制要將多少 V2 加權至結果，而參數 g 控制在結果中加權多少 V3。</span><span class="sxs-lookup"><span data-stu-id="a1774-133">Any point in the plane V1V2V3 can be represented by the Barycentric coordinate (f,g).The parameter f controls how much V2 gets weighted into the result and the parameter g controls how much V3 gets weighted into the result.</span></span> <span data-ttu-id="a1774-134">最後，1-f-g 控制 V1 在結果中的加權量。</span><span class="sxs-lookup"><span data-stu-id="a1774-134">Lastly, 1-f-g controls how much V1 gets weighted into the result.</span></span>

<span data-ttu-id="a1774-135">請注意下列關聯性。</span><span class="sxs-lookup"><span data-stu-id="a1774-135">Note the following relations.</span></span>

-   <span data-ttu-id="a1774-136">如果 (f>= 0 &，& g>= 0 &，& 1-f-g>= 0) ，則點位於三角形 V1V2V3 內。</span><span class="sxs-lookup"><span data-stu-id="a1774-136">If (f>=0 &, & g>=0 &, & 1-f-g>=0), the point is inside the triangle V1V2V3.</span></span>
-   <span data-ttu-id="a1774-137">如果 (f = = 0 &，& g>= 0 &，& 1-f-g>= 0) ，則點位於行 V1V3 上。</span><span class="sxs-lookup"><span data-stu-id="a1774-137">If (f==0 &, & g>=0 &, & 1-f-g>=0), the point is on the line V1V3.</span></span>
-   <span data-ttu-id="a1774-138">如果 (f>= 0 &，& g = = 0 &，& 1-f-g>= 0) ，則點位於行 V1V2 上。</span><span class="sxs-lookup"><span data-stu-id="a1774-138">If (f>=0 &, & g==0 &, & 1-f-g>=0), the point is on the line V1V2.</span></span>
-   <span data-ttu-id="a1774-139">如果 (f>= 0 &，& g>= 0 &，& 1-f-g = = 0) ，則點位於行 V2V3 上。</span><span class="sxs-lookup"><span data-stu-id="a1774-139">If (f>=0 &, & g>=0 &, & 1-f-g==0), the point is on the line V2V3.</span></span>

<span data-ttu-id="a1774-140">Barycentric 座標是一種一般座標形式。</span><span class="sxs-lookup"><span data-stu-id="a1774-140">Barycentric coordinates are a form of general coordinates.</span></span> <span data-ttu-id="a1774-141">在此內容中，使用 Barycentric 座標代表座標系統中的變更。</span><span class="sxs-lookup"><span data-stu-id="a1774-141">In this context, using Barycentric coordinates represents a change in coordinate systems.</span></span> <span data-ttu-id="a1774-142">笛卡兒座標的 true 是 Barycentric 座標的 true。</span><span class="sxs-lookup"><span data-stu-id="a1774-142">What holds true for Cartesian coordinates holds true for Barycentric coordinates.</span></span>

<span data-ttu-id="a1774-143">此函式的傳回值與不悅參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="a1774-143">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="a1774-144">如此一來，D3DXVec3BaryCentric 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="a1774-144">In this way, the D3DXVec3BaryCentric function can be used as a parameter for another function.</span></span>

<span data-ttu-id="a1774-145">Barycentric 座標會根據三角形的頂點定義三角形內的點。</span><span class="sxs-lookup"><span data-stu-id="a1774-145">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="a1774-146">如需 barycentric 座標的更深入說明，請參閱 [Mathworld 的 Barycentric 座標描述](https://mathworld.wolfram.com/BarycentricCoordinates.html)。</span><span class="sxs-lookup"><span data-stu-id="a1774-146">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="a1774-147">規格需求</span><span class="sxs-lookup"><span data-stu-id="a1774-147">Requirements</span></span>



| <span data-ttu-id="a1774-148">需求</span><span class="sxs-lookup"><span data-stu-id="a1774-148">Requirement</span></span> | <span data-ttu-id="a1774-149">值</span><span class="sxs-lookup"><span data-stu-id="a1774-149">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a1774-150">標頭</span><span class="sxs-lookup"><span data-stu-id="a1774-150">Header</span></span><br/> | <dl> <span data-ttu-id="a1774-151"><dt>D3DX10Math。h</dt></span><span class="sxs-lookup"><span data-stu-id="a1774-151"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1774-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a1774-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1774-153">數學函數</span><span class="sxs-lookup"><span data-stu-id="a1774-153">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
