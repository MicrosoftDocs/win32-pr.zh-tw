---
description: 從三個點結構的平面。
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
ms.openlocfilehash: c537915c56cdbbfb33228b0c5a5ea3f2acc2baff
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106981986"
---
# <a name="d3dxplanefrompoints-function-d3dx9mathh"></a><span data-ttu-id="bc0d0-103">D3DXPlaneFromPoints 函式 (D3dx9math) </span><span class="sxs-lookup"><span data-stu-id="bc0d0-103">D3DXPlaneFromPoints function (D3dx9math.h)</span></span>

<span data-ttu-id="bc0d0-104">從三個點結構的平面。</span><span class="sxs-lookup"><span data-stu-id="bc0d0-104">Constructs a plane from three points.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc0d0-105">語法</span><span class="sxs-lookup"><span data-stu-id="bc0d0-105">Syntax</span></span>


```C++
D3DXPLANE* D3DXPlaneFromPoints(
  _Inout_       D3DXPLANE   *pOut,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pV2,
  _In_    const D3DXVECTOR3 *pV3
);
```



## <a name="parameters"></a><span data-ttu-id="bc0d0-106">參數</span><span class="sxs-lookup"><span data-stu-id="bc0d0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc0d0-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="bc0d0-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="bc0d0-108">類型： **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="bc0d0-108">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="bc0d0-109">[**D3DXPLANE**](d3dxplane.md)結構的指標，此結構是作業的結果。</span><span class="sxs-lookup"><span data-stu-id="bc0d0-109">Pointer to the [**D3DXPLANE**](d3dxplane.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="bc0d0-110">*pV1* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bc0d0-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc0d0-111">Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="bc0d0-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="bc0d0-112">[**D3DXVECTOR3**](d3dxvector3.md)結構的指標，定義用來建立平面的其中一個點。</span><span class="sxs-lookup"><span data-stu-id="bc0d0-112">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, defining one of the points used to construct the plane.</span></span>

</dd> <dt>

<span data-ttu-id="bc0d0-113">*pV2* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bc0d0-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc0d0-114">Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="bc0d0-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="bc0d0-115">[**D3DXVECTOR3**](d3dxvector3.md)結構的指標，定義用來建立平面的其中一個點。</span><span class="sxs-lookup"><span data-stu-id="bc0d0-115">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, defining one of the points used to construct the plane.</span></span>

</dd> <dt>

<span data-ttu-id="bc0d0-116">*pV3* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bc0d0-116">*pV3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc0d0-117">Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="bc0d0-117">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="bc0d0-118">[**D3DXVECTOR3**](d3dxvector3.md)結構的指標，定義用來建立平面的其中一個點。</span><span class="sxs-lookup"><span data-stu-id="bc0d0-118">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, defining one of the points used to construct the plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc0d0-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="bc0d0-119">Return value</span></span>

<span data-ttu-id="bc0d0-120">類型： **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="bc0d0-120">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="bc0d0-121">從指定點所建立之 [**D3DXPLANE**](d3dxplane.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="bc0d0-121">Pointer to the [**D3DXPLANE**](d3dxplane.md) structure constructed from the given points.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc0d0-122">備註</span><span class="sxs-lookup"><span data-stu-id="bc0d0-122">Remarks</span></span>

<span data-ttu-id="bc0d0-123">此函式的傳回值與 *不悅* 參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="bc0d0-123">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="bc0d0-124">如此一來， **D3DXPlaneFromPoints** 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="bc0d0-124">In this way, the **D3DXPlaneFromPoints** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc0d0-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="bc0d0-125">Requirements</span></span>



| <span data-ttu-id="bc0d0-126">需求</span><span class="sxs-lookup"><span data-stu-id="bc0d0-126">Requirement</span></span> | <span data-ttu-id="bc0d0-127">值</span><span class="sxs-lookup"><span data-stu-id="bc0d0-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bc0d0-128">標頭</span><span class="sxs-lookup"><span data-stu-id="bc0d0-128">Header</span></span><br/>  | <dl> <span data-ttu-id="bc0d0-129"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="bc0d0-129"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="bc0d0-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="bc0d0-130">Library</span></span><br/> | <dl> <span data-ttu-id="bc0d0-131"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="bc0d0-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="bc0d0-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bc0d0-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc0d0-133">數學函數</span><span class="sxs-lookup"><span data-stu-id="bc0d0-133">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="bc0d0-134">**D3DXPlaneFromPointNormal**</span><span class="sxs-lookup"><span data-stu-id="bc0d0-134">**D3DXPlaneFromPointNormal**</span></span>](d3dxplanefrompointnormal.md)
</dt> </dl>

 

 




