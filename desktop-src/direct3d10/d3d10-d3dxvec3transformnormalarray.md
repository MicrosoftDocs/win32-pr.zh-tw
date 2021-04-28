---
description: D3DXVec3TransformNormalArray 函式 (D3DX10Math) -轉換陣列 (x、y、z、0) 指定的矩陣。
ms.assetid: 7f0a41ce-bd3a-4e35-9a5d-8178a4e7bd44
title: 'D3DXVec3TransformNormalArray 函式 (D3DX10Math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3TransformNormalArray
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: d391717056d1cd8a6957a6647612ed8b1ca65e41
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103046"
---
# <a name="d3dxvec3transformnormalarray-function-d3dx10mathh"></a><span data-ttu-id="aeb19-103">D3DXVec3TransformNormalArray 函式 (D3DX10Math) </span><span class="sxs-lookup"><span data-stu-id="aeb19-103">D3DXVec3TransformNormalArray function (D3DX10Math.h)</span></span>

<span data-ttu-id="aeb19-104">將陣列 (x、y、z、0) 由指定的矩陣進行轉換。</span><span class="sxs-lookup"><span data-stu-id="aeb19-104">Transforms an array (x, y, z, 0) by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="aeb19-105">語法</span><span class="sxs-lookup"><span data-stu-id="aeb19-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3TransformNormalArray(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_          UINT        OutStride,
  _In_    const D3DXVECTOR3 *pV,
  _In_          UINT        VStride,
  _In_    const D3DXMATRIX  *pM,
  _In_          UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="aeb19-106">參數</span><span class="sxs-lookup"><span data-stu-id="aeb19-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aeb19-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="aeb19-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="aeb19-108">類型： **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="aeb19-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="aeb19-109">[**D3DXVECTOR3**](d3d10-d3dxvector3.md)陣列的指標，這是作業的結果。</span><span class="sxs-lookup"><span data-stu-id="aeb19-109">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) array that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="aeb19-110">*OutStride* \[在\]</span><span class="sxs-lookup"><span data-stu-id="aeb19-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aeb19-111">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="aeb19-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="aeb19-112">輸出資料流程中向量之間的 Stride。</span><span class="sxs-lookup"><span data-stu-id="aeb19-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="aeb19-113">*pV* \[在\]</span><span class="sxs-lookup"><span data-stu-id="aeb19-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aeb19-114">Type： **Const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="aeb19-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="aeb19-115">來源 D3DXVECTOR3 陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="aeb19-115">Pointer to the source D3DXVECTOR3 array.</span></span>

</dd> <dt>

<span data-ttu-id="aeb19-116">*VStride* \[在\]</span><span class="sxs-lookup"><span data-stu-id="aeb19-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aeb19-117">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="aeb19-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="aeb19-118">輸入資料流程中向量之間的 Stride。</span><span class="sxs-lookup"><span data-stu-id="aeb19-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="aeb19-119">*pM* \[在\]</span><span class="sxs-lookup"><span data-stu-id="aeb19-119">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aeb19-120">Type： **Const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="aeb19-120">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="aeb19-121">來源 [**D3DXMATRIX**](d3d10-d3dxmatrix.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="aeb19-121">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="aeb19-122">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aeb19-122">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aeb19-123">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="aeb19-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="aeb19-124">陣列中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="aeb19-124">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aeb19-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="aeb19-125">Return value</span></span>

<span data-ttu-id="aeb19-126">類型： **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="aeb19-126">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="aeb19-127">D3DXVECTOR3 陣列的指標，該陣列為已轉換的陣列。</span><span class="sxs-lookup"><span data-stu-id="aeb19-127">Pointer to a D3DXVECTOR3 array that is the transformed array.</span></span>

## <a name="remarks"></a><span data-ttu-id="aeb19-128">備註</span><span class="sxs-lookup"><span data-stu-id="aeb19-128">Remarks</span></span>

<span data-ttu-id="aeb19-129">此函式會將向量 (pV->x，pV->y，pV >z，0) 由 pM 指向的矩陣。</span><span class="sxs-lookup"><span data-stu-id="aeb19-129">This function transforms the vector (pV->x, pV->y, pV->z, 0) by the matrix pointed to by pM.</span></span>

<span data-ttu-id="aeb19-130">如果您想要轉換一般，您傳遞給此函式的矩陣應該是您用來轉換點之矩陣反向的調換。</span><span class="sxs-lookup"><span data-stu-id="aeb19-130">If you want to transform a normal, the matrix you pass to this function should be the transpose of the inverse of the matrix you would use to transform a point.</span></span>

<span data-ttu-id="aeb19-131">此函式的傳回值與不悅參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="aeb19-131">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="aeb19-132">如此一來， **D3DXVec3TransformNormalArray** 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="aeb19-132">In this way, the **D3DXVec3TransformNormalArray** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="aeb19-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="aeb19-133">Requirements</span></span>



| <span data-ttu-id="aeb19-134">需求</span><span class="sxs-lookup"><span data-stu-id="aeb19-134">Requirement</span></span> | <span data-ttu-id="aeb19-135">值</span><span class="sxs-lookup"><span data-stu-id="aeb19-135">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aeb19-136">標頭</span><span class="sxs-lookup"><span data-stu-id="aeb19-136">Header</span></span><br/> | <dl> <span data-ttu-id="aeb19-137"><dt>D3DX10Math。h</dt></span><span class="sxs-lookup"><span data-stu-id="aeb19-137"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aeb19-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="aeb19-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aeb19-139">數學函數</span><span class="sxs-lookup"><span data-stu-id="aeb19-139">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
