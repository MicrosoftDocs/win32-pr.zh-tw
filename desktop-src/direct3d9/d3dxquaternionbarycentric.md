---
description: D3DXQuaternionBaryCentric 函式 (D3dx9math) -傳回 barycentric 座標中的四元數。
ms.assetid: 8fcd2e16-1bf1-4e18-afc9-17c92f2bbac5
title: 'D3DXQuaternionBaryCentric 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionBaryCentric
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2ce0cfc7b3a59dc2a3cae6fa240015e70a035695
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094106"
---
# <a name="d3dxquaternionbarycentric-function-d3dx9mathh"></a><span data-ttu-id="1f36e-103">D3DXQuaternionBaryCentric 函式 (D3dx9math) </span><span class="sxs-lookup"><span data-stu-id="1f36e-103">D3DXQuaternionBaryCentric function (D3dx9math.h)</span></span>

<span data-ttu-id="1f36e-104">傳回 barycentric 座標中的四元數。</span><span class="sxs-lookup"><span data-stu-id="1f36e-104">Returns a quaternion in barycentric coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f36e-105">語法</span><span class="sxs-lookup"><span data-stu-id="1f36e-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionBaryCentric(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ1,
  _In_    const D3DXQUATERNION *pQ2,
  _In_    const D3DXQUATERNION *pQ3,
  _In_          FLOAT          f,
  _In_          FLOAT          g
);
```



## <a name="parameters"></a><span data-ttu-id="1f36e-106">參數</span><span class="sxs-lookup"><span data-stu-id="1f36e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f36e-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="1f36e-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1f36e-108">類型： **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="1f36e-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="1f36e-109">[**D3DXQUATERNION**](d3dxquaternion.md)結構的指標，此結構是作業的結果。</span><span class="sxs-lookup"><span data-stu-id="1f36e-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="1f36e-110">*pQ1* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1f36e-110">*pQ1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f36e-111">Type： **Const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="1f36e-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="1f36e-112">來源 [**D3DXQUATERNION**](d3dxquaternion.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="1f36e-112">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="1f36e-113">*pQ2* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1f36e-113">*pQ2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f36e-114">Type： **Const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="1f36e-114">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="1f36e-115">來源 [**D3DXQUATERNION**](d3dxquaternion.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="1f36e-115">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="1f36e-116">*pQ3* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1f36e-116">*pQ3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f36e-117">Type： **Const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="1f36e-117">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="1f36e-118">來源 [**D3DXQUATERNION**](d3dxquaternion.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="1f36e-118">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="1f36e-119">*f* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1f36e-119">*f* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f36e-120">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1f36e-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1f36e-121">加權係數。</span><span class="sxs-lookup"><span data-stu-id="1f36e-121">Weighting factor.</span></span> <span data-ttu-id="1f36e-122">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="1f36e-122">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="1f36e-123">*g* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1f36e-123">*g* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f36e-124">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1f36e-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1f36e-125">加權係數。</span><span class="sxs-lookup"><span data-stu-id="1f36e-125">Weighting factor.</span></span> <span data-ttu-id="1f36e-126">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="1f36e-126">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f36e-127">傳回值</span><span class="sxs-lookup"><span data-stu-id="1f36e-127">Return value</span></span>

<span data-ttu-id="1f36e-128">類型： **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="1f36e-128">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="1f36e-129">Barycentric 座標中 [**D3DXQUATERNION**](d3dxquaternion.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="1f36e-129">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure in Barycentric coordinates.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f36e-130">備註</span><span class="sxs-lookup"><span data-stu-id="1f36e-130">Remarks</span></span>

<span data-ttu-id="1f36e-131">為了計算 barycentric 座標， **D3DXQuaternionBaryCentric** 函式會執行下列一連串的球面線性插補作業：</span><span class="sxs-lookup"><span data-stu-id="1f36e-131">To compute the barycentric coordinates, the **D3DXQuaternionBaryCentric** function implements the following series of spherical linear interpolation operations:</span></span>


```
Slerp(Slerp(Q1, Q2, f+g), Slerp(Q1, Q3, f+g), g/(f+g))
```



<span data-ttu-id="1f36e-132">此函式的傳回值與 *不悅* 參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="1f36e-132">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="1f36e-133">如此一來， **D3DXQuaternionBaryCentric** 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="1f36e-133">In this way, the **D3DXQuaternionBaryCentric** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="1f36e-134">針對尚未正規化的任何四元數輸入，請使用 [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) 。</span><span class="sxs-lookup"><span data-stu-id="1f36e-134">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

<span data-ttu-id="1f36e-135">Barycentric 座標會根據三角形的頂點定義三角形內的點。</span><span class="sxs-lookup"><span data-stu-id="1f36e-135">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="1f36e-136">如需 barycentric 座標的更深入說明，請參閱 [Mathworld 的 Barycentric 座標描述](https://mathworld.wolfram.com/BarycentricCoordinates.html)。</span><span class="sxs-lookup"><span data-stu-id="1f36e-136">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="1f36e-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="1f36e-137">Requirements</span></span>



| <span data-ttu-id="1f36e-138">需求</span><span class="sxs-lookup"><span data-stu-id="1f36e-138">Requirement</span></span> | <span data-ttu-id="1f36e-139">值</span><span class="sxs-lookup"><span data-stu-id="1f36e-139">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1f36e-140">標頭</span><span class="sxs-lookup"><span data-stu-id="1f36e-140">Header</span></span><br/>  | <dl> <span data-ttu-id="1f36e-141"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="1f36e-141"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="1f36e-142">程式庫</span><span class="sxs-lookup"><span data-stu-id="1f36e-142">Library</span></span><br/> | <dl> <span data-ttu-id="1f36e-143"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="1f36e-143"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1f36e-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1f36e-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f36e-145">數學函數</span><span class="sxs-lookup"><span data-stu-id="1f36e-145">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
