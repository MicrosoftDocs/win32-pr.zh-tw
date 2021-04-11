---
description: 將陣列 (x、y、0、1) 由指定的矩陣進行轉換。
ms.assetid: 66c8909c-6c20-4b32-9546-fcf2d0e824fa
title: 'D3DXVec2TransformArray 函式 (D3DX10Math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2TransformArray
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: c5aef5ecaa720e8c859d37f03ce88223187d16f0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103853999"
---
# <a name="d3dxvec2transformarray-function-d3dx10mathh"></a><span data-ttu-id="463cd-103">D3DXVec2TransformArray 函式 (D3DX10Math) </span><span class="sxs-lookup"><span data-stu-id="463cd-103">D3DXVec2TransformArray function (D3DX10Math.h)</span></span>

<span data-ttu-id="463cd-104">將陣列 (x、y、0、1) 由指定的矩陣進行轉換。</span><span class="sxs-lookup"><span data-stu-id="463cd-104">Transforms an array (x, y, 0, 1) by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="463cd-105">語法</span><span class="sxs-lookup"><span data-stu-id="463cd-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec2TransformArray(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_          UINT        OutStride,
  _In_    const D3DXVECTOR2 *pV,
  _In_          UINT        VStride,
  _In_    const D3DXMATRIX  *pM,
  _In_          UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="463cd-106">參數</span><span class="sxs-lookup"><span data-stu-id="463cd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="463cd-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="463cd-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="463cd-108">類型： **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="463cd-108">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="463cd-109">[**D3DXVECTOR4**](d3d10-d3dxvector4.md)結構的指標，此結構是作業的結果。</span><span class="sxs-lookup"><span data-stu-id="463cd-109">Pointer to the [**D3DXVECTOR4**](d3d10-d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="463cd-110">*OutStride* \[在\]</span><span class="sxs-lookup"><span data-stu-id="463cd-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="463cd-111">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="463cd-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="463cd-112">輸出資料流程中向量之間的 Stride。</span><span class="sxs-lookup"><span data-stu-id="463cd-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="463cd-113">*pV* \[在\]</span><span class="sxs-lookup"><span data-stu-id="463cd-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="463cd-114">Type： **Const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="463cd-114">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="463cd-115">來源 [**D3DXVECTOR2**](d3d10-d3dxvector2.md)的指標。</span><span class="sxs-lookup"><span data-stu-id="463cd-115">Pointer to the source [**D3DXVECTOR2**](d3d10-d3dxvector2.md).</span></span>

</dd> <dt>

<span data-ttu-id="463cd-116">*VStride* \[在\]</span><span class="sxs-lookup"><span data-stu-id="463cd-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="463cd-117">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="463cd-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="463cd-118">輸入資料流程中向量之間的 Stride。</span><span class="sxs-lookup"><span data-stu-id="463cd-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="463cd-119">*pM* \[在\]</span><span class="sxs-lookup"><span data-stu-id="463cd-119">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="463cd-120">Type： **Const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="463cd-120">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="463cd-121">來源 [**D3DXMATRIX**](d3d10-d3dxmatrix.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="463cd-121">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="463cd-122">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="463cd-122">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="463cd-123">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="463cd-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="463cd-124">陣列中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="463cd-124">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="463cd-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="463cd-125">Return value</span></span>

<span data-ttu-id="463cd-126">類型： **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="463cd-126">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="463cd-127">D3DXVECTOR4 結構的指標，此結構是已轉換的陣列。</span><span class="sxs-lookup"><span data-stu-id="463cd-127">Pointer to a D3DXVECTOR4 structure that is the transformed array.</span></span>

## <a name="remarks"></a><span data-ttu-id="463cd-128">備註</span><span class="sxs-lookup"><span data-stu-id="463cd-128">Remarks</span></span>

<span data-ttu-id="463cd-129">此函式會將陣列 pV (x、y、0、1) 由矩陣 pM 來轉換。</span><span class="sxs-lookup"><span data-stu-id="463cd-129">This function transforms the array pV (x, y, 0, 1) by the matrix pM.</span></span>

<span data-ttu-id="463cd-130">此函式的傳回值與不悅參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="463cd-130">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="463cd-131">如此一來， [**D3DXVec2Transform**](d3d10-d3dxvec2transform.md) 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="463cd-131">In this way, the [**D3DXVec2Transform**](d3d10-d3dxvec2transform.md) function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="463cd-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="463cd-132">Requirements</span></span>



| <span data-ttu-id="463cd-133">需求</span><span class="sxs-lookup"><span data-stu-id="463cd-133">Requirement</span></span> | <span data-ttu-id="463cd-134">值</span><span class="sxs-lookup"><span data-stu-id="463cd-134">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="463cd-135">標頭</span><span class="sxs-lookup"><span data-stu-id="463cd-135">Header</span></span><br/>  | <dl> <span data-ttu-id="463cd-136"><dt>D3DX10Math。h</dt></span><span class="sxs-lookup"><span data-stu-id="463cd-136"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="463cd-137">程式庫</span><span class="sxs-lookup"><span data-stu-id="463cd-137">Library</span></span><br/> | <dl> <span data-ttu-id="463cd-138"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="463cd-138"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="463cd-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="463cd-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="463cd-140">數學函數</span><span class="sxs-lookup"><span data-stu-id="463cd-140">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
