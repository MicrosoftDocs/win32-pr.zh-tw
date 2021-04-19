---
description: 投射陣列 (x、y、z、0) 從螢幕空間到物件空間。
ms.assetid: 02db5b32-7fa3-4cde-bd63-0d8b3dfc31e7
title: 'D3DXVec3UnprojectArray 函式 (D3DX10Math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3UnprojectArray
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: c7293339145253f817e8ed8b6812906b49792193
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106988175"
---
# <a name="d3dxvec3unprojectarray-function-d3dx10mathh"></a><span data-ttu-id="ad60b-103">D3DXVec3UnprojectArray 函式 (D3DX10Math) </span><span class="sxs-lookup"><span data-stu-id="ad60b-103">D3DXVec3UnprojectArray function (D3DX10Math.h)</span></span>

<span data-ttu-id="ad60b-104">投射陣列 (x、y、z、0) 從螢幕空間到物件空間。</span><span class="sxs-lookup"><span data-stu-id="ad60b-104">Projects an array (x, y, z, 0) from screen space into object space.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad60b-105">語法</span><span class="sxs-lookup"><span data-stu-id="ad60b-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3UnprojectArray(
  _Inout_       D3DXVECTOR3    *pOut,
  _In_          UINT           OutStride,
  _In_    const D3DXVECTOR3    *pV,
  _In_          UINT           VStride,
  _In_    const D3D10_VIEWPORT *pViewport,
  _In_    const D3DXMATRIX     *pProjection,
  _In_    const D3DXMATRIX     *pView,
  _In_    const D3DXMATRIX     *pWorld,
  _In_          UINT           n
);
```



## <a name="parameters"></a><span data-ttu-id="ad60b-106">參數</span><span class="sxs-lookup"><span data-stu-id="ad60b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad60b-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="ad60b-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ad60b-108">類型： **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="ad60b-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="ad60b-109">作業結果之 [**D3DXVECTOR3**](d3d10-d3dxvector3.md) 的指標。</span><span class="sxs-lookup"><span data-stu-id="ad60b-109">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="ad60b-110">*OutStride* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ad60b-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad60b-111">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ad60b-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ad60b-112">輸出資料流程中向量之間的 Stride。</span><span class="sxs-lookup"><span data-stu-id="ad60b-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="ad60b-113">*pV* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ad60b-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad60b-114">Type： **Const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="ad60b-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="ad60b-115">來源 D3DXVECTOR3 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="ad60b-115">Pointer to the source D3DXVECTOR3 structure.</span></span>

</dd> <dt>

<span data-ttu-id="ad60b-116">*VStride* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ad60b-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad60b-117">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ad60b-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ad60b-118">輸入資料流程中向量之間的 Stride。</span><span class="sxs-lookup"><span data-stu-id="ad60b-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="ad60b-119">*pViewport* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ad60b-119">*pViewport* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad60b-120">Type： **Const [**D3D10 \_ 視口**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport) \***</span><span class="sxs-lookup"><span data-stu-id="ad60b-120">Type: **const [**D3D10\_VIEWPORT**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport)\***</span></span>

<span data-ttu-id="ad60b-121">[**D3D10 \_ 區**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport)的指標，表示區。</span><span class="sxs-lookup"><span data-stu-id="ad60b-121">Pointer to a [**D3D10\_VIEWPORT**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport), representing the viewport.</span></span>

</dd> <dt>

<span data-ttu-id="ad60b-122">*pProjection* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ad60b-122">*pProjection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad60b-123">Type： **Const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="ad60b-123">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="ad60b-124">[**D3DXMATRIX**](d3d10-d3dxmatrix.md)結構的指標，表示投射矩陣。</span><span class="sxs-lookup"><span data-stu-id="ad60b-124">Pointer to a [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure, representing the projection matrix.</span></span>

</dd> <dt>

<span data-ttu-id="ad60b-125">*pView* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ad60b-125">*pView* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad60b-126">Type： **Const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="ad60b-126">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="ad60b-127">D3DXMATRIX 結構的指標，代表視圖矩陣。</span><span class="sxs-lookup"><span data-stu-id="ad60b-127">Pointer to a D3DXMATRIX structure, representing the view matrix.</span></span>

</dd> <dt>

<span data-ttu-id="ad60b-128">*pWorld* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ad60b-128">*pWorld* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad60b-129">Type： **Const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="ad60b-129">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="ad60b-130">D3DXMATRIX 結構的指標，代表世界矩陣。</span><span class="sxs-lookup"><span data-stu-id="ad60b-130">Pointer to a D3DXMATRIX structure, representing the world matrix.</span></span>

</dd> <dt>

<span data-ttu-id="ad60b-131">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ad60b-131">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad60b-132">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ad60b-132">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ad60b-133">陣列中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="ad60b-133">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad60b-134">傳回值</span><span class="sxs-lookup"><span data-stu-id="ad60b-134">Return value</span></span>

<span data-ttu-id="ad60b-135">類型： **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="ad60b-135">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="ad60b-136">D3DXVECTOR3 結構的指標，此結構是從螢幕空間投射到物件空間的陣列。</span><span class="sxs-lookup"><span data-stu-id="ad60b-136">Pointer to a D3DXVECTOR3 structure that is the array projected from screen space to object space.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad60b-137">備註</span><span class="sxs-lookup"><span data-stu-id="ad60b-137">Remarks</span></span>

<span data-ttu-id="ad60b-138">此函式的傳回值與不悅參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="ad60b-138">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="ad60b-139">如此一來， [**D3DXVec3Unproject**](d3d10-d3dxvec3unproject.md) 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="ad60b-139">In this way, the [**D3DXVec3Unproject**](d3d10-d3dxvec3unproject.md) function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad60b-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="ad60b-140">Requirements</span></span>



| <span data-ttu-id="ad60b-141">需求</span><span class="sxs-lookup"><span data-stu-id="ad60b-141">Requirement</span></span> | <span data-ttu-id="ad60b-142">值</span><span class="sxs-lookup"><span data-stu-id="ad60b-142">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ad60b-143">標頭</span><span class="sxs-lookup"><span data-stu-id="ad60b-143">Header</span></span><br/> | <dl> <span data-ttu-id="ad60b-144"><dt>D3DX10Math。h</dt></span><span class="sxs-lookup"><span data-stu-id="ad60b-144"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad60b-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ad60b-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad60b-146">數學函數</span><span class="sxs-lookup"><span data-stu-id="ad60b-146">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
