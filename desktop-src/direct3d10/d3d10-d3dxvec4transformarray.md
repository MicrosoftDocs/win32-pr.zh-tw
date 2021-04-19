---
description: 將陣列 (x、y、z、w) 由指定的矩陣進行轉換。
ms.assetid: afd5cccb-e22f-4726-a84e-9eac1c1c277f
title: 'D3DXVec4TransformArray 函式 (D3DX10Math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4TransformArray
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 5571fb19786e19a61c85741bcf6d4acb5231e977
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106981256"
---
# <a name="d3dxvec4transformarray-function-d3dx10mathh"></a><span data-ttu-id="1156f-103">D3DXVec4TransformArray 函式 (D3DX10Math) </span><span class="sxs-lookup"><span data-stu-id="1156f-103">D3DXVec4TransformArray function (D3DX10Math.h)</span></span>

<span data-ttu-id="1156f-104">將陣列 (x、y、z、w) 由指定的矩陣進行轉換。</span><span class="sxs-lookup"><span data-stu-id="1156f-104">Transforms an array (x, y, z, w) by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="1156f-105">語法</span><span class="sxs-lookup"><span data-stu-id="1156f-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4TransformArray(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_          UINT        OutStride,
  _In_    const D3DXVECTOR4 *pV,
  _In_          UINT        VStride,
  _In_    const D3DXMATRIX  *pM,
  _In_          UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="1156f-106">參數</span><span class="sxs-lookup"><span data-stu-id="1156f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1156f-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="1156f-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1156f-108">類型： **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="1156f-108">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="1156f-109">[**D3DXVECTOR4**](d3d10-d3dxvector4.md)陣列的指標，這是作業的結果。</span><span class="sxs-lookup"><span data-stu-id="1156f-109">Pointer to the [**D3DXVECTOR4**](d3d10-d3dxvector4.md) array that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="1156f-110">*OutStride* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1156f-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1156f-111">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1156f-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1156f-112">輸出資料流程中向量之間的 Stride。</span><span class="sxs-lookup"><span data-stu-id="1156f-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="1156f-113">*pV* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1156f-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1156f-114">Type： **Const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="1156f-114">Type: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="1156f-115">來源 D3DXVECTOR4 陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="1156f-115">Pointer to the source D3DXVECTOR4 array.</span></span>

</dd> <dt>

<span data-ttu-id="1156f-116">*VStride* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1156f-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1156f-117">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1156f-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1156f-118">輸入資料流程中向量之間的 Stride。</span><span class="sxs-lookup"><span data-stu-id="1156f-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="1156f-119">*pM* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1156f-119">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1156f-120">Type： **Const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="1156f-120">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="1156f-121">來源 [**D3DXMATRIX**](d3d10-d3dxmatrix.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="1156f-121">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="1156f-122">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1156f-122">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1156f-123">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1156f-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1156f-124">陣列中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="1156f-124">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1156f-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="1156f-125">Return value</span></span>

<span data-ttu-id="1156f-126">類型： **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="1156f-126">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="1156f-127">[**D3DXVECTOR4**](d3d10-d3dxvector4.md)結構的指標，此結構是已轉換的陣列。</span><span class="sxs-lookup"><span data-stu-id="1156f-127">Pointer to a [**D3DXVECTOR4**](d3d10-d3dxvector4.md) structure that is the transformed array.</span></span>

## <a name="remarks"></a><span data-ttu-id="1156f-128">備註</span><span class="sxs-lookup"><span data-stu-id="1156f-128">Remarks</span></span>

<span data-ttu-id="1156f-129">此函式會將陣列 pV (x、y、z、w) 由矩陣 pM 進行轉換。</span><span class="sxs-lookup"><span data-stu-id="1156f-129">This function transforms the array pV (x, y, z, w) by the matrix pM.</span></span>

<span data-ttu-id="1156f-130">此函式的傳回值與 *不悅* 參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="1156f-130">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="1156f-131">如此一來， **D3DXVec4TransformArray** 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="1156f-131">In this way, the **D3DXVec4TransformArray** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="1156f-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="1156f-132">Requirements</span></span>



| <span data-ttu-id="1156f-133">需求</span><span class="sxs-lookup"><span data-stu-id="1156f-133">Requirement</span></span> | <span data-ttu-id="1156f-134">值</span><span class="sxs-lookup"><span data-stu-id="1156f-134">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1156f-135">標頭</span><span class="sxs-lookup"><span data-stu-id="1156f-135">Header</span></span><br/> | <dl> <span data-ttu-id="1156f-136"><dt>D3DX10Math。h</dt></span><span class="sxs-lookup"><span data-stu-id="1156f-136"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1156f-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1156f-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1156f-138">數學函數</span><span class="sxs-lookup"><span data-stu-id="1156f-138">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
