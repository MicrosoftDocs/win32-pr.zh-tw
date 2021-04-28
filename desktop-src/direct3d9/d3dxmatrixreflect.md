---
description: D3DXMatrixReflect 函式 (D3dx9math) -建立一個可反映平面座標系統的矩陣。
ms.assetid: f6dc3834-42f2-4ad0-8098-8c5e25e10d58
title: 'D3DXMatrixReflect 函式 (D3dx9math) '
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e4118a5f0a1cd997d5fab5fecebae449d4c30b09
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118216"
---
# <a name="d3dxmatrixreflect-function-d3dx9mathh"></a><span data-ttu-id="2befb-103">D3DXMatrixReflect 函式 (D3dx9math) </span><span class="sxs-lookup"><span data-stu-id="2befb-103">D3DXMatrixReflect function (D3dx9math.h)</span></span>

<span data-ttu-id="2befb-104">建立可反映平面座標系統的矩陣。</span><span class="sxs-lookup"><span data-stu-id="2befb-104">Builds a matrix that reflects the coordinate system about a plane.</span></span>

## <a name="syntax"></a><span data-ttu-id="2befb-105">語法</span><span class="sxs-lookup"><span data-stu-id="2befb-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixReflect(
  _Inout_       D3DXMATRIX *pOut,
  _In_    const D3DXPLANE  *pPlane
);
```



## <a name="parameters"></a><span data-ttu-id="2befb-106">參數</span><span class="sxs-lookup"><span data-stu-id="2befb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2befb-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="2befb-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2befb-108">類型： **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="2befb-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="2befb-109">[**D3DXMATRIX**](d3dxmatrix.md)結構的指標，此結構是作業的結果。</span><span class="sxs-lookup"><span data-stu-id="2befb-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="2befb-110">*pPlane* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2befb-110">*pPlane* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2befb-111">Type： **Const [**D3DXPLANE**](d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="2befb-111">Type: **const [**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="2befb-112">來源 [**D3DXPLANE**](d3dxplane.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="2befb-112">Pointer to the source [**D3DXPLANE**](d3dxplane.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2befb-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="2befb-113">Return value</span></span>

<span data-ttu-id="2befb-114">類型： **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="2befb-114">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="2befb-115">[**D3DXMATRIX**](d3dxmatrix.md)結構的指標，此結構反映來源平面的座標系統。</span><span class="sxs-lookup"><span data-stu-id="2befb-115">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that reflects the coordinate system about the source plane.</span></span>

## <a name="remarks"></a><span data-ttu-id="2befb-116">備註</span><span class="sxs-lookup"><span data-stu-id="2befb-116">Remarks</span></span>

<span data-ttu-id="2befb-117">此函式會在建立反映的矩陣之前，將平面方程式標準化。</span><span class="sxs-lookup"><span data-stu-id="2befb-117">This function normalizes the plane equation before it creates the reflected matrix.</span></span>

<span data-ttu-id="2befb-118">此函式的傳回值與 *不悅* 參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="2befb-118">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="2befb-119">如此一來， **D3DXMatrixReflect** 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="2befb-119">In this way, the **D3DXMatrixReflect** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="2befb-120">此函數會使用下列公式來計算傳回的矩陣。</span><span class="sxs-lookup"><span data-stu-id="2befb-120">This function uses the following formula to compute the returned matrix.</span></span>


```
P = normalize(Plane);
    
-2 * P.a * P.a + 1  -2 * P.b * P.a      -2 * P.c * P.a        0
-2 * P.a * P.b      -2 * P.b * P.b + 1  -2 * P.c * P.b        0
-2 * P.a * P.c      -2 * P.b * P.c      -2 * P.c * P.c + 1    0
-2 * P.a * P.d      -2 * P.b * P.d      -2 * P.c * P.d        1
```



## <a name="requirements"></a><span data-ttu-id="2befb-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="2befb-121">Requirements</span></span>



| <span data-ttu-id="2befb-122">需求</span><span class="sxs-lookup"><span data-stu-id="2befb-122">Requirement</span></span> | <span data-ttu-id="2befb-123">值</span><span class="sxs-lookup"><span data-stu-id="2befb-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2befb-124">標頭</span><span class="sxs-lookup"><span data-stu-id="2befb-124">Header</span></span><br/>  | <dl> <span data-ttu-id="2befb-125"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="2befb-125"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="2befb-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="2befb-126">Library</span></span><br/> | <dl> <span data-ttu-id="2befb-127"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="2befb-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2befb-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2befb-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2befb-129">數學函數</span><span class="sxs-lookup"><span data-stu-id="2befb-129">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




