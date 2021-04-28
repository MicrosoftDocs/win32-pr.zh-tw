---
description: D3DXPlaneFromPoints 函式 (D3dx9math) -從三個點來結構出一個平面。
ms.assetid: 13d5ce6b-0046-441b-b826-f34f4fe16979
title: 'D3DXPlaneFromPoints 函式 (D3dx9math) '
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0d945dff9c124f4c66cea4f9d61c490c6eaf7a66
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094156"
---
# <a name="d3dxplanefrompoints-function-d3dx9mathh"></a><span data-ttu-id="c8995-103">D3DXPlaneFromPoints 函式 (D3dx9math) </span><span class="sxs-lookup"><span data-stu-id="c8995-103">D3DXPlaneFromPoints function (D3dx9math.h)</span></span>

<span data-ttu-id="c8995-104">從三個點結構的平面。</span><span class="sxs-lookup"><span data-stu-id="c8995-104">Constructs a plane from three points.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8995-105">語法</span><span class="sxs-lookup"><span data-stu-id="c8995-105">Syntax</span></span>


```C++
D3DXPLANE* D3DXPlaneFromPoints(
  _Inout_       D3DXPLANE   *pOut,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pV2,
  _In_    const D3DXVECTOR3 *pV3
);
```



## <a name="parameters"></a><span data-ttu-id="c8995-106">參數</span><span class="sxs-lookup"><span data-stu-id="c8995-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8995-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="c8995-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c8995-108">類型： **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="c8995-108">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="c8995-109">[**D3DXPLANE**](d3dxplane.md)結構的指標，此結構是作業的結果。</span><span class="sxs-lookup"><span data-stu-id="c8995-109">Pointer to the [**D3DXPLANE**](d3dxplane.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="c8995-110">*pV1* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c8995-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8995-111">Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="c8995-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="c8995-112">[**D3DXVECTOR3**](d3dxvector3.md)結構的指標，定義用來建立平面的其中一個點。</span><span class="sxs-lookup"><span data-stu-id="c8995-112">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, defining one of the points used to construct the plane.</span></span>

</dd> <dt>

<span data-ttu-id="c8995-113">*pV2* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c8995-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8995-114">Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="c8995-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="c8995-115">[**D3DXVECTOR3**](d3dxvector3.md)結構的指標，定義用來建立平面的其中一個點。</span><span class="sxs-lookup"><span data-stu-id="c8995-115">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, defining one of the points used to construct the plane.</span></span>

</dd> <dt>

<span data-ttu-id="c8995-116">*pV3* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c8995-116">*pV3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8995-117">Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="c8995-117">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="c8995-118">[**D3DXVECTOR3**](d3dxvector3.md)結構的指標，定義用來建立平面的其中一個點。</span><span class="sxs-lookup"><span data-stu-id="c8995-118">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, defining one of the points used to construct the plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8995-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="c8995-119">Return value</span></span>

<span data-ttu-id="c8995-120">類型： **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="c8995-120">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="c8995-121">從指定點所建立之 [**D3DXPLANE**](d3dxplane.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="c8995-121">Pointer to the [**D3DXPLANE**](d3dxplane.md) structure constructed from the given points.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8995-122">備註</span><span class="sxs-lookup"><span data-stu-id="c8995-122">Remarks</span></span>

<span data-ttu-id="c8995-123">此函式的傳回值與 *不悅* 參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="c8995-123">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="c8995-124">如此一來， **D3DXPlaneFromPoints** 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="c8995-124">In this way, the **D3DXPlaneFromPoints** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8995-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="c8995-125">Requirements</span></span>



| <span data-ttu-id="c8995-126">需求</span><span class="sxs-lookup"><span data-stu-id="c8995-126">Requirement</span></span> | <span data-ttu-id="c8995-127">值</span><span class="sxs-lookup"><span data-stu-id="c8995-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c8995-128">標頭</span><span class="sxs-lookup"><span data-stu-id="c8995-128">Header</span></span><br/>  | <dl> <span data-ttu-id="c8995-129"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="c8995-129"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="c8995-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="c8995-130">Library</span></span><br/> | <dl> <span data-ttu-id="c8995-131"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="c8995-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c8995-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c8995-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8995-133">數學函數</span><span class="sxs-lookup"><span data-stu-id="c8995-133">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="c8995-134">**D3DXPlaneFromPointNormal**</span><span class="sxs-lookup"><span data-stu-id="c8995-134">**D3DXPlaneFromPointNormal**</span></span>](d3dxplanefrompointnormal.md)
</dt> </dl>

 

 




