---
description: D3DXMatrixReflect 函式 (D3DX10Math) -建立一個可反映平面座標系統的矩陣。
ms.assetid: bd2c5905-780e-4fac-a848-d7dbcfc390c6
title: 'D3DXMatrixReflect 函式 (D3DX10Math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixReflect
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: f96224c881dcd5db2cc1c356003ab96e8a626900
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103406"
---
# <a name="d3dxmatrixreflect-function-d3dx10mathh"></a><span data-ttu-id="9486b-103">D3DXMatrixReflect 函式 (D3DX10Math) </span><span class="sxs-lookup"><span data-stu-id="9486b-103">D3DXMatrixReflect function (D3DX10Math.h)</span></span>

<span data-ttu-id="9486b-104">建立可反映平面座標系統的矩陣。</span><span class="sxs-lookup"><span data-stu-id="9486b-104">Builds a matrix that reflects the coordinate system about a plane.</span></span>

## <a name="syntax"></a><span data-ttu-id="9486b-105">語法</span><span class="sxs-lookup"><span data-stu-id="9486b-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixReflect(
  _Inout_       D3DXMATRIX *pOut,
  _In_    const D3DXPLANE  *pPlane
);
```



## <a name="parameters"></a><span data-ttu-id="9486b-106">參數</span><span class="sxs-lookup"><span data-stu-id="9486b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9486b-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="9486b-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="9486b-108">類型： **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="9486b-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="9486b-109">[**D3DXMATRIX**](d3d10-d3dxmatrix.md)結構的指標，此結構是作業的結果。</span><span class="sxs-lookup"><span data-stu-id="9486b-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="9486b-110">*pPlane* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9486b-110">*pPlane* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9486b-111">Type： **Const [**D3DXPLANE**](../direct3d9/d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="9486b-111">Type: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="9486b-112">來源 [**D3DXPLANE**](d3d10-d3dxplane.md)的指標。</span><span class="sxs-lookup"><span data-stu-id="9486b-112">Pointer to the source [**D3DXPLANE**](d3d10-d3dxplane.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9486b-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="9486b-113">Return value</span></span>

<span data-ttu-id="9486b-114">類型： **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="9486b-114">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="9486b-115">D3DXMATRIX 結構的指標，此結構反映來源平面的座標系統。</span><span class="sxs-lookup"><span data-stu-id="9486b-115">Pointer to a D3DXMATRIX structure that reflects the coordinate system about the source plane.</span></span>

## <a name="remarks"></a><span data-ttu-id="9486b-116">備註</span><span class="sxs-lookup"><span data-stu-id="9486b-116">Remarks</span></span>

<span data-ttu-id="9486b-117">此函式會在建立反映的矩陣之前，將平面方程式標準化。</span><span class="sxs-lookup"><span data-stu-id="9486b-117">This function normalizes the plane equation before it creates the reflected matrix.</span></span>

<span data-ttu-id="9486b-118">此函式的傳回值與不悅參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="9486b-118">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="9486b-119">如此一來，D3DXMatrixReflect 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="9486b-119">In this way, the D3DXMatrixReflect function can be used as a parameter for another function.</span></span>

<span data-ttu-id="9486b-120">此函數會使用下列公式來計算傳回的矩陣。</span><span class="sxs-lookup"><span data-stu-id="9486b-120">This function uses the following formula to compute the returned matrix.</span></span>


```
P = normalize(Plane);
    
-2 * P.a * P.a + 1  -2 * P.b * P.a      -2 * P.c * P.a        0
-2 * P.a * P.b      -2 * P.b * P.b + 1  -2 * P.c * P.b        0
-2 * P.a * P.c      -2 * P.b * P.c      -2 * P.c * P.c + 1    0
-2 * P.a * P.d      -2 * P.b * P.d      -2 * P.c * P.d        1
```



## <a name="requirements"></a><span data-ttu-id="9486b-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="9486b-121">Requirements</span></span>



| <span data-ttu-id="9486b-122">需求</span><span class="sxs-lookup"><span data-stu-id="9486b-122">Requirement</span></span> | <span data-ttu-id="9486b-123">值</span><span class="sxs-lookup"><span data-stu-id="9486b-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9486b-124">標頭</span><span class="sxs-lookup"><span data-stu-id="9486b-124">Header</span></span><br/>  | <dl> <span data-ttu-id="9486b-125"><dt>D3DX10Math。h</dt></span><span class="sxs-lookup"><span data-stu-id="9486b-125"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="9486b-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="9486b-126">Library</span></span><br/> | <dl> <span data-ttu-id="9486b-127"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="9486b-127"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9486b-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9486b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9486b-129">數學函數</span><span class="sxs-lookup"><span data-stu-id="9486b-129">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
