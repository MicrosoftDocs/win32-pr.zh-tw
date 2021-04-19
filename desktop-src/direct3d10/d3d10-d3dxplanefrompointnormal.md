---
description: 從點和一般結構來建立平面。
ms.assetid: 93c644d2-ab8c-47a1-9a3b-8b9c6a13178b
title: 'D3DXPlaneFromPointNormal 函式 (D3DX10Math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneFromPointNormal
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 9900a9f6838e253bd195374d00f90ee31fae07a7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106986539"
---
# <a name="d3dxplanefrompointnormal-function-d3dx10mathh"></a><span data-ttu-id="defb8-103">D3DXPlaneFromPointNormal 函式 (D3DX10Math) </span><span class="sxs-lookup"><span data-stu-id="defb8-103">D3DXPlaneFromPointNormal function (D3DX10Math.h)</span></span>

<span data-ttu-id="defb8-104">從點和一般結構來建立平面。</span><span class="sxs-lookup"><span data-stu-id="defb8-104">Constructs a plane from a point and a normal.</span></span>

## <a name="syntax"></a><span data-ttu-id="defb8-105">語法</span><span class="sxs-lookup"><span data-stu-id="defb8-105">Syntax</span></span>


```C++
D3DXPLANE* D3DXPlaneFromPointNormal(
  _Inout_       D3DXPLANE   *pOut,
  _In_    const D3DXVECTOR3 *pPoint,
  _In_    const D3DXVECTOR3 *pNormal
);
```



## <a name="parameters"></a><span data-ttu-id="defb8-106">參數</span><span class="sxs-lookup"><span data-stu-id="defb8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="defb8-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="defb8-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="defb8-108">類型： **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="defb8-108">Type: **[**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="defb8-109">作業結果之 [**D3DXPLANE**](d3d10-d3dxplane.md) 的指標。</span><span class="sxs-lookup"><span data-stu-id="defb8-109">Pointer to the [**D3DXPLANE**](d3d10-d3dxplane.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="defb8-110">*pPoint* \[在\]</span><span class="sxs-lookup"><span data-stu-id="defb8-110">*pPoint* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="defb8-111">Type： **Const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="defb8-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="defb8-112">[**D3DXVECTOR3**](d3d10-d3dxvector3.md)的指標，定義用來建立平面的點。</span><span class="sxs-lookup"><span data-stu-id="defb8-112">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md), defining the point used to construct the plane.</span></span>

</dd> <dt>

<span data-ttu-id="defb8-113">*pNormal* \[在\]</span><span class="sxs-lookup"><span data-stu-id="defb8-113">*pNormal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="defb8-114">Type： **Const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="defb8-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="defb8-115">D3DXVECTOR3 結構的指標，定義用來建立平面的一般。</span><span class="sxs-lookup"><span data-stu-id="defb8-115">Pointer to a D3DXVECTOR3 structure, defining the normal used to construct the plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="defb8-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="defb8-116">Return value</span></span>

<span data-ttu-id="defb8-117">類型： **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="defb8-117">Type: **[**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="defb8-118">從點和標準所建立的 D3DXPLANE 結構指標。</span><span class="sxs-lookup"><span data-stu-id="defb8-118">Pointer to the D3DXPLANE structure constructed from the point and the normal.</span></span>

## <a name="remarks"></a><span data-ttu-id="defb8-119">備註</span><span class="sxs-lookup"><span data-stu-id="defb8-119">Remarks</span></span>

<span data-ttu-id="defb8-120">此函式的傳回值與不悅參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="defb8-120">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="defb8-121">如此一來，D3DXPlaneFromPointNormal 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="defb8-121">In this way, the D3DXPlaneFromPointNormal function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="defb8-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="defb8-122">Requirements</span></span>



| <span data-ttu-id="defb8-123">需求</span><span class="sxs-lookup"><span data-stu-id="defb8-123">Requirement</span></span> | <span data-ttu-id="defb8-124">值</span><span class="sxs-lookup"><span data-stu-id="defb8-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="defb8-125">標頭</span><span class="sxs-lookup"><span data-stu-id="defb8-125">Header</span></span><br/>  | <dl> <span data-ttu-id="defb8-126"><dt>D3DX10Math。h</dt></span><span class="sxs-lookup"><span data-stu-id="defb8-126"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="defb8-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="defb8-127">Library</span></span><br/> | <dl> <span data-ttu-id="defb8-128"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="defb8-128"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="defb8-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="defb8-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="defb8-130">數學函數</span><span class="sxs-lookup"><span data-stu-id="defb8-130">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
