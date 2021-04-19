---
description: 尋找平面和直線之間的交集。
ms.assetid: aea1c4e1-f8c0-46df-bb33-2b517396d69e
title: 'D3DXPlaneIntersectLine 函式 (D3DX10Math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneIntersectLine
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 00d25fcba9e5884cec10da96964ad0f5daa9ed14
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106992744"
---
# <a name="d3dxplaneintersectline-function-d3dx10mathh"></a><span data-ttu-id="571fc-103">D3DXPlaneIntersectLine 函式 (D3DX10Math) </span><span class="sxs-lookup"><span data-stu-id="571fc-103">D3DXPlaneIntersectLine function (D3DX10Math.h)</span></span>

<span data-ttu-id="571fc-104">尋找平面和直線之間的交集。</span><span class="sxs-lookup"><span data-stu-id="571fc-104">Finds the intersection between a plane and a line.</span></span>

## <a name="syntax"></a><span data-ttu-id="571fc-105">語法</span><span class="sxs-lookup"><span data-stu-id="571fc-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXPlaneIntersectLine(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXPLANE   *pP,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="571fc-106">參數</span><span class="sxs-lookup"><span data-stu-id="571fc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="571fc-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="571fc-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="571fc-108">類型： **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="571fc-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="571fc-109">[**D3DXVECTOR3**](d3d10-d3dxvector3.md)的指標，識別指定之平面和線條之間的交集。</span><span class="sxs-lookup"><span data-stu-id="571fc-109">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md), identifying the intersection between the specified plane and line.</span></span>

</dd> <dt>

<span data-ttu-id="571fc-110">*pP* \[在\]</span><span class="sxs-lookup"><span data-stu-id="571fc-110">*pP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="571fc-111">Type： **Const [**D3DXPLANE**](../direct3d9/d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="571fc-111">Type: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="571fc-112">來源 [**D3DXPLANE**](d3d10-d3dxplane.md)的指標。</span><span class="sxs-lookup"><span data-stu-id="571fc-112">Pointer to the source [**D3DXPLANE**](d3d10-d3dxplane.md).</span></span>

</dd> <dt>

<span data-ttu-id="571fc-113">*pV1* \[在\]</span><span class="sxs-lookup"><span data-stu-id="571fc-113">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="571fc-114">Type： **Const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="571fc-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="571fc-115">來源 D3DXVECTOR3 結構的指標，定義行起始點。</span><span class="sxs-lookup"><span data-stu-id="571fc-115">Pointer to a source D3DXVECTOR3 structure, defining a line starting point.</span></span>

</dd> <dt>

<span data-ttu-id="571fc-116">*pV2* \[在\]</span><span class="sxs-lookup"><span data-stu-id="571fc-116">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="571fc-117">Type： **Const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="571fc-117">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="571fc-118">來源 D3DXVECTOR3 結構的指標，定義線條結束點。</span><span class="sxs-lookup"><span data-stu-id="571fc-118">Pointer to a source D3DXVECTOR3 structure, defining a line ending point.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="571fc-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="571fc-119">Return value</span></span>

<span data-ttu-id="571fc-120">類型： **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="571fc-120">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="571fc-121">D3DXVECTOR3 結構的指標，此結構是指定之平面和線條之間的交集。</span><span class="sxs-lookup"><span data-stu-id="571fc-121">Pointer to a D3DXVECTOR3 structure that is the intersection between the specified plane and line.</span></span>

## <a name="remarks"></a><span data-ttu-id="571fc-122">備註</span><span class="sxs-lookup"><span data-stu-id="571fc-122">Remarks</span></span>

<span data-ttu-id="571fc-123">如果直線與平面平行，則會傳回 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="571fc-123">If the line is parallel to the plane, **NULL** is returned.</span></span>

<span data-ttu-id="571fc-124">此函式的傳回值與不悅參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="571fc-124">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="571fc-125">如此一來，D3DXPlaneIntersectLine 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="571fc-125">In this way, the D3DXPlaneIntersectLine function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="571fc-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="571fc-126">Requirements</span></span>



| <span data-ttu-id="571fc-127">需求</span><span class="sxs-lookup"><span data-stu-id="571fc-127">Requirement</span></span> | <span data-ttu-id="571fc-128">值</span><span class="sxs-lookup"><span data-stu-id="571fc-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="571fc-129">標頭</span><span class="sxs-lookup"><span data-stu-id="571fc-129">Header</span></span><br/>  | <dl> <span data-ttu-id="571fc-130"><dt>D3DX10Math。h</dt></span><span class="sxs-lookup"><span data-stu-id="571fc-130"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="571fc-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="571fc-131">Library</span></span><br/> | <dl> <span data-ttu-id="571fc-132"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="571fc-132"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="571fc-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="571fc-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="571fc-134">數學函數</span><span class="sxs-lookup"><span data-stu-id="571fc-134">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
