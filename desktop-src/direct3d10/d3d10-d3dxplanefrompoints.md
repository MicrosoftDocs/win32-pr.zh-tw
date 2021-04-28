---
description: D3DXPlaneFromPoints 函式 (D3DX10Math) -從三個點來結構出一個平面。
ms.assetid: 0e77af1b-cedf-482c-8398-10becb398a2c
title: 'D3DXPlaneFromPoints 函式 (D3DX10Math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneFromPoints
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: a3af01df7d1ce66029994226d040544b733a75df
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103316"
---
# <a name="d3dxplanefrompoints-function-d3dx10mathh"></a><span data-ttu-id="a1388-103">D3DXPlaneFromPoints 函式 (D3DX10Math) </span><span class="sxs-lookup"><span data-stu-id="a1388-103">D3DXPlaneFromPoints function (D3DX10Math.h)</span></span>

<span data-ttu-id="a1388-104">從三個點結構的平面。</span><span class="sxs-lookup"><span data-stu-id="a1388-104">Constructs a plane from three points.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1388-105">語法</span><span class="sxs-lookup"><span data-stu-id="a1388-105">Syntax</span></span>


```C++
D3DXPLANE* D3DXPlaneFromPoints(
  _Inout_       D3DXPLANE   *pOut,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pV2,
  _In_    const D3DXVECTOR3 *pV3
);
```



## <a name="parameters"></a><span data-ttu-id="a1388-106">參數</span><span class="sxs-lookup"><span data-stu-id="a1388-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1388-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="a1388-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a1388-108">類型： **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="a1388-108">Type: **[**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="a1388-109">作業結果之 [**D3DXPLANE**](d3d10-d3dxplane.md) 的指標。</span><span class="sxs-lookup"><span data-stu-id="a1388-109">Pointer to the [**D3DXPLANE**](d3d10-d3dxplane.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="a1388-110">*pV1* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a1388-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1388-111">Type： **Const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="a1388-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="a1388-112">[**D3DXVECTOR3**](d3d10-d3dxvector3.md)的指標，定義用來建立平面的其中一個點。</span><span class="sxs-lookup"><span data-stu-id="a1388-112">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md), defining one of the points used to construct the plane.</span></span>

</dd> <dt>

<span data-ttu-id="a1388-113">*pV2* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a1388-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1388-114">Type： **Const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="a1388-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="a1388-115">D3DXVECTOR3 結構的指標，定義用來建立平面的其中一個點。</span><span class="sxs-lookup"><span data-stu-id="a1388-115">Pointer to a D3DXVECTOR3 structure, defining one of the points used to construct the plane.</span></span>

</dd> <dt>

<span data-ttu-id="a1388-116">*pV3* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a1388-116">*pV3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1388-117">Type： **Const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="a1388-117">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="a1388-118">D3DXVECTOR3 結構的指標，定義用來建立平面的其中一個點。</span><span class="sxs-lookup"><span data-stu-id="a1388-118">Pointer to a D3DXVECTOR3 structure, defining one of the points used to construct the plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1388-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="a1388-119">Return value</span></span>

<span data-ttu-id="a1388-120">類型： **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="a1388-120">Type: **[**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="a1388-121">從指定點所建立之 D3DXPLANE 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="a1388-121">Pointer to the D3DXPLANE structure constructed from the given points.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1388-122">備註</span><span class="sxs-lookup"><span data-stu-id="a1388-122">Remarks</span></span>

<span data-ttu-id="a1388-123">此函式的傳回值與不悅參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="a1388-123">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="a1388-124">如此一來，D3DXPlaneFromPoints 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="a1388-124">In this way, the D3DXPlaneFromPoints function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1388-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="a1388-125">Requirements</span></span>



| <span data-ttu-id="a1388-126">需求</span><span class="sxs-lookup"><span data-stu-id="a1388-126">Requirement</span></span> | <span data-ttu-id="a1388-127">值</span><span class="sxs-lookup"><span data-stu-id="a1388-127">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a1388-128">標頭</span><span class="sxs-lookup"><span data-stu-id="a1388-128">Header</span></span><br/>  | <dl> <span data-ttu-id="a1388-129"><dt>D3DX10Math。h</dt></span><span class="sxs-lookup"><span data-stu-id="a1388-129"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="a1388-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="a1388-130">Library</span></span><br/> | <dl> <span data-ttu-id="a1388-131"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="a1388-131"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a1388-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a1388-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1388-133">數學函數</span><span class="sxs-lookup"><span data-stu-id="a1388-133">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
