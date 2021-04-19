---
description: 從點和一般結構來建立平面。
ms.assetid: af396bbb-09b7-492f-a25f-9c950da7e605
title: 'D3DXPlaneFromPointNormal 函式 (D3dx9math) '
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8eeb8ea3a1725e0bf615be888d8e862c97730a2c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106981807"
---
# <a name="d3dxplanefrompointnormal-function-d3dx9mathh"></a><span data-ttu-id="fbd10-103">D3DXPlaneFromPointNormal 函式 (D3dx9math) </span><span class="sxs-lookup"><span data-stu-id="fbd10-103">D3DXPlaneFromPointNormal function (D3dx9math.h)</span></span>

<span data-ttu-id="fbd10-104">從點和一般結構來建立平面。</span><span class="sxs-lookup"><span data-stu-id="fbd10-104">Constructs a plane from a point and a normal.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbd10-105">語法</span><span class="sxs-lookup"><span data-stu-id="fbd10-105">Syntax</span></span>


```C++
D3DXPLANE* D3DXPlaneFromPointNormal(
  _Inout_       D3DXPLANE   *pOut,
  _In_    const D3DXVECTOR3 *pPoint,
  _In_    const D3DXVECTOR3 *pNormal
);
```



## <a name="parameters"></a><span data-ttu-id="fbd10-106">參數</span><span class="sxs-lookup"><span data-stu-id="fbd10-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fbd10-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="fbd10-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="fbd10-108">類型： **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="fbd10-108">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="fbd10-109">[**D3DXPLANE**](d3dxplane.md)結構的指標，此結構是作業的結果。</span><span class="sxs-lookup"><span data-stu-id="fbd10-109">Pointer to the [**D3DXPLANE**](d3dxplane.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="fbd10-110">*pPoint* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fbd10-110">*pPoint* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fbd10-111">Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="fbd10-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="fbd10-112">[**D3DXVECTOR3**](d3dxvector3.md)結構的指標，定義用來建立平面的點。</span><span class="sxs-lookup"><span data-stu-id="fbd10-112">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, defining the point used to construct the plane.</span></span>

</dd> <dt>

<span data-ttu-id="fbd10-113">*pNormal* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fbd10-113">*pNormal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fbd10-114">Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="fbd10-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="fbd10-115">[**D3DXVECTOR3**](d3dxvector3.md)結構的指標，定義用來建立平面的一般。</span><span class="sxs-lookup"><span data-stu-id="fbd10-115">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, defining the normal used to construct the plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fbd10-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="fbd10-116">Return value</span></span>

<span data-ttu-id="fbd10-117">類型： **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="fbd10-117">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="fbd10-118">從點和標準所建立的 [**D3DXPLANE**](d3dxplane.md) 結構指標。</span><span class="sxs-lookup"><span data-stu-id="fbd10-118">Pointer to the [**D3DXPLANE**](d3dxplane.md) structure constructed from the point and the normal.</span></span>

## <a name="remarks"></a><span data-ttu-id="fbd10-119">備註</span><span class="sxs-lookup"><span data-stu-id="fbd10-119">Remarks</span></span>

<span data-ttu-id="fbd10-120">此函式的傳回值與 *不悅* 參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="fbd10-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="fbd10-121">如此一來， **D3DXPlaneFromPointNormal** 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="fbd10-121">In this way, the **D3DXPlaneFromPointNormal** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="fbd10-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="fbd10-122">Requirements</span></span>



| <span data-ttu-id="fbd10-123">需求</span><span class="sxs-lookup"><span data-stu-id="fbd10-123">Requirement</span></span> | <span data-ttu-id="fbd10-124">值</span><span class="sxs-lookup"><span data-stu-id="fbd10-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fbd10-125">標頭</span><span class="sxs-lookup"><span data-stu-id="fbd10-125">Header</span></span><br/>  | <dl> <span data-ttu-id="fbd10-126"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="fbd10-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="fbd10-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="fbd10-127">Library</span></span><br/> | <dl> <span data-ttu-id="fbd10-128"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="fbd10-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fbd10-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fbd10-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbd10-130">數學函數</span><span class="sxs-lookup"><span data-stu-id="fbd10-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="fbd10-131">**D3DXPlaneFromPoints**</span><span class="sxs-lookup"><span data-stu-id="fbd10-131">**D3DXPlaneFromPoints**</span></span>](d3dxplanefrompoints.md)
</dt> </dl>

 

 




