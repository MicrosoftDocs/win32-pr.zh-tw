---
description: 將陣列 (x、y、z、1) 由指定的矩陣進行轉換。
ms.assetid: f64c55df-ea93-4c93-be89-eee650e6ecf0
title: 'D3DXVec3TransformArray 函式 (D3DX10Math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3TransformArray
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 9ae223d4e1b8c424230ba12719f25258dae18548
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104035398"
---
# <a name="d3dxvec3transformarray-function-d3dx10mathh"></a><span data-ttu-id="d4a66-103">D3DXVec3TransformArray 函式 (D3DX10Math) </span><span class="sxs-lookup"><span data-stu-id="d4a66-103">D3DXVec3TransformArray function (D3DX10Math.h)</span></span>

<span data-ttu-id="d4a66-104">將陣列 (x、y、z、1) 由指定的矩陣進行轉換。</span><span class="sxs-lookup"><span data-stu-id="d4a66-104">Transforms an array (x, y, z, 1) by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4a66-105">語法</span><span class="sxs-lookup"><span data-stu-id="d4a66-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec3TransformArray(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_          UINT        OutStride,
  _In_    const D3DXVECTOR3 *pV,
  _In_          UINT        VStride,
  _In_    const D3DXMATRIX  *pM,
  _In_          UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="d4a66-106">參數</span><span class="sxs-lookup"><span data-stu-id="d4a66-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4a66-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="d4a66-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d4a66-108">類型： **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="d4a66-108">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="d4a66-109">[**D3DXVECTOR4**](d3d10-d3dxvector4.md)陣列的指標，這是作業的結果。</span><span class="sxs-lookup"><span data-stu-id="d4a66-109">Pointer to the [**D3DXVECTOR4**](d3d10-d3dxvector4.md) array that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="d4a66-110">*OutStride* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d4a66-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4a66-111">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d4a66-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d4a66-112">輸出資料流程中向量之間的 Stride。</span><span class="sxs-lookup"><span data-stu-id="d4a66-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="d4a66-113">*pV* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d4a66-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4a66-114">Type： **Const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="d4a66-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="d4a66-115">來源 [**D3DXVECTOR3**](d3d10-d3dxvector3.md) 陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="d4a66-115">Pointer to the source [**D3DXVECTOR3**](d3d10-d3dxvector3.md) array.</span></span>

</dd> <dt>

<span data-ttu-id="d4a66-116">*VStride* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d4a66-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4a66-117">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d4a66-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d4a66-118">輸入資料流程中向量之間的 Stride。</span><span class="sxs-lookup"><span data-stu-id="d4a66-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="d4a66-119">*pM* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d4a66-119">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4a66-120">Type： **Const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="d4a66-120">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="d4a66-121">來源 [**D3DXMATRIX**](d3d10-d3dxmatrix.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="d4a66-121">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="d4a66-122">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d4a66-122">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4a66-123">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d4a66-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d4a66-124">陣列中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="d4a66-124">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4a66-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="d4a66-125">Return value</span></span>

<span data-ttu-id="d4a66-126">類型： **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="d4a66-126">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="d4a66-127">[**D3DXVECTOR4**](d3d10-d3dxvector4.md)轉換陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="d4a66-127">Pointer to a [**D3DXVECTOR4**](d3d10-d3dxvector4.md) transformed array.</span></span>

## <a name="remarks"></a><span data-ttu-id="d4a66-128">備註</span><span class="sxs-lookup"><span data-stu-id="d4a66-128">Remarks</span></span>

<span data-ttu-id="d4a66-129">此函式會將陣列 pV (x、y、z、1) 由矩陣 pM 來轉換。</span><span class="sxs-lookup"><span data-stu-id="d4a66-129">This function transforms the array pV (x, y, z, 1) by the matrix pM.</span></span>

<span data-ttu-id="d4a66-130">此函式的傳回值與不悅參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="d4a66-130">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="d4a66-131">如此一來，D3DXVec3TransformArray 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="d4a66-131">In this way, the D3DXVec3TransformArray function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4a66-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="d4a66-132">Requirements</span></span>



| <span data-ttu-id="d4a66-133">需求</span><span class="sxs-lookup"><span data-stu-id="d4a66-133">Requirement</span></span> | <span data-ttu-id="d4a66-134">值</span><span class="sxs-lookup"><span data-stu-id="d4a66-134">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d4a66-135">標頭</span><span class="sxs-lookup"><span data-stu-id="d4a66-135">Header</span></span><br/> | <dl> <span data-ttu-id="d4a66-136"><dt>D3DX10Math。h</dt></span><span class="sxs-lookup"><span data-stu-id="d4a66-136"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4a66-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d4a66-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4a66-138">數學函數</span><span class="sxs-lookup"><span data-stu-id="d4a66-138">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
