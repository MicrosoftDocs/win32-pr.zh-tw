---
description: D3DXVec3ProjectArray 函式 (D3dx9math) -投射陣列 (x、y、z、0) 從物件空間到螢幕空間。
ms.assetid: cf022741-0bae-4c22-872f-bd94c3721aff
title: 'D3DXVec3ProjectArray 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3ProjectArray
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 10f0e19ad5bdbff59d7386223c88ed867e8d0d88
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097806"
---
# <a name="d3dxvec3projectarray-function-d3dx9mathh"></a><span data-ttu-id="6ce74-103">D3DXVec3ProjectArray 函式 (D3dx9math) </span><span class="sxs-lookup"><span data-stu-id="6ce74-103">D3DXVec3ProjectArray function (D3dx9math.h)</span></span>

<span data-ttu-id="6ce74-104">投射陣列 (x、y、z、0) 從物件空間到螢幕空間。</span><span class="sxs-lookup"><span data-stu-id="6ce74-104">Projects an array (x, y, z, 0) from object space into screen space.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ce74-105">語法</span><span class="sxs-lookup"><span data-stu-id="6ce74-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3ProjectArray(
  _Inout_       D3DXVECTOR3  *pOut,
  _In_          UINT         OutStride,
  _In_    const D3DXVECTOR3  *pV,
  _In_          UINT         VStride,
  _In_    const D3DVIEWPORT9 *pViewport,
  _In_    const D3DXMATRIX   *pProjection,
  _In_    const D3DXMATRIX   *pView,
  _In_    const D3DXMATRIX   *pWorld,
  _In_          UINT         n
);
```



## <a name="parameters"></a><span data-ttu-id="6ce74-106">參數</span><span class="sxs-lookup"><span data-stu-id="6ce74-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ce74-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="6ce74-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6ce74-108">類型： **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="6ce74-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="6ce74-109">[**D3DXVECTOR3**](d3dxvector3.md)結構的指標，此結構是作業的結果。</span><span class="sxs-lookup"><span data-stu-id="6ce74-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="6ce74-110">*OutStride* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6ce74-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ce74-111">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6ce74-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6ce74-112">輸出資料流程中向量之間的 Stride。</span><span class="sxs-lookup"><span data-stu-id="6ce74-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="6ce74-113">*pV* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6ce74-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ce74-114">Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="6ce74-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="6ce74-115">來源 [**D3DXVECTOR3**](d3dxvector3.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="6ce74-115">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="6ce74-116">*VStride* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6ce74-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ce74-117">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6ce74-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6ce74-118">輸入資料流程中向量之間的 Stride。</span><span class="sxs-lookup"><span data-stu-id="6ce74-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="6ce74-119">*pViewport* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6ce74-119">*pViewport* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ce74-120">Type： **Const [**D3DVIEWPORT9**](d3dviewport9.md) \***</span><span class="sxs-lookup"><span data-stu-id="6ce74-120">Type: **const [**D3DVIEWPORT9**](d3dviewport9.md)\***</span></span>

<span data-ttu-id="6ce74-121">[**D3DVIEWPORT9**](d3dviewport9.md)結構的指標，表示區。</span><span class="sxs-lookup"><span data-stu-id="6ce74-121">Pointer to a [**D3DVIEWPORT9**](d3dviewport9.md) structure, representing the viewport.</span></span>

</dd> <dt>

<span data-ttu-id="6ce74-122">*pProjection* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6ce74-122">*pProjection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ce74-123">Type： **Const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="6ce74-123">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="6ce74-124">[**D3DXMATRIX**](d3dxmatrix.md)結構的指標，表示投射矩陣。</span><span class="sxs-lookup"><span data-stu-id="6ce74-124">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure, representing the projection matrix.</span></span>

</dd> <dt>

<span data-ttu-id="6ce74-125">*pView* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6ce74-125">*pView* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ce74-126">Type： **Const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="6ce74-126">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="6ce74-127">[**D3DXMATRIX**](d3dxmatrix.md)結構的指標，代表視圖矩陣。</span><span class="sxs-lookup"><span data-stu-id="6ce74-127">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure, representing the view matrix.</span></span>

</dd> <dt>

<span data-ttu-id="6ce74-128">*pWorld* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6ce74-128">*pWorld* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ce74-129">Type： **Const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="6ce74-129">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="6ce74-130">[**D3DXMATRIX**](d3dxmatrix.md)結構的指標，代表世界矩陣。</span><span class="sxs-lookup"><span data-stu-id="6ce74-130">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure, representing the world matrix.</span></span>

</dd> <dt>

<span data-ttu-id="6ce74-131">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6ce74-131">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ce74-132">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6ce74-132">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6ce74-133">陣列中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="6ce74-133">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ce74-134">傳回值</span><span class="sxs-lookup"><span data-stu-id="6ce74-134">Return value</span></span>

<span data-ttu-id="6ce74-135">類型： **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="6ce74-135">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="6ce74-136">[**D3DXVECTOR3**](d3dxvector3.md)結構的指標，此結構是從物件空間投射到螢幕空間的陣列。</span><span class="sxs-lookup"><span data-stu-id="6ce74-136">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the array projected from object space to screen space.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ce74-137">備註</span><span class="sxs-lookup"><span data-stu-id="6ce74-137">Remarks</span></span>

<span data-ttu-id="6ce74-138">此函式的傳回值與 *不悅* 參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="6ce74-138">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="6ce74-139">如此一來， **D3DXVec3ProjectArray** 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="6ce74-139">In this way, the **D3DXVec3ProjectArray** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ce74-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="6ce74-140">Requirements</span></span>



| <span data-ttu-id="6ce74-141">需求</span><span class="sxs-lookup"><span data-stu-id="6ce74-141">Requirement</span></span> | <span data-ttu-id="6ce74-142">值</span><span class="sxs-lookup"><span data-stu-id="6ce74-142">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ce74-143">標頭</span><span class="sxs-lookup"><span data-stu-id="6ce74-143">Header</span></span><br/>  | <dl> <span data-ttu-id="6ce74-144"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="6ce74-144"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="6ce74-145">程式庫</span><span class="sxs-lookup"><span data-stu-id="6ce74-145">Library</span></span><br/> | <dl> <span data-ttu-id="6ce74-146"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="6ce74-146"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6ce74-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6ce74-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ce74-148">數學函數</span><span class="sxs-lookup"><span data-stu-id="6ce74-148">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="6ce74-149">**D3DXVec3Unproject**</span><span class="sxs-lookup"><span data-stu-id="6ce74-149">**D3DXVec3Unproject**</span></span>](d3dxvec3unproject.md)
</dt> </dl>

 

 
