---
description: D3DXVec2TransformNormalArray 函式 (D3DX10Math) -轉換陣列 (x、y、0、0) 指定的矩陣。
ms.assetid: a53f998a-f2a5-4e4b-bc1c-c1f46284d78b
title: 'D3DXVec2TransformNormalArray 函式 (D3DX10Math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2TransformNormalArray
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: b4e18fc2bb8c62bb86947b9eab35daae9d0242ba
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108276"
---
# <a name="d3dxvec2transformnormalarray-function-d3dx10mathh"></a><span data-ttu-id="f3e90-103">D3DXVec2TransformNormalArray 函式 (D3DX10Math) </span><span class="sxs-lookup"><span data-stu-id="f3e90-103">D3DXVec2TransformNormalArray function (D3DX10Math.h)</span></span>

<span data-ttu-id="f3e90-104">將陣列 (x、y、0、0) 由指定的矩陣進行轉換。</span><span class="sxs-lookup"><span data-stu-id="f3e90-104">Transforms an array (x, y, 0, 0) by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3e90-105">語法</span><span class="sxs-lookup"><span data-stu-id="f3e90-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2TransformNormalArray(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_          UINT        OutStride,
  _In_    const D3DXVECTOR2 *pV,
  _In_          UINT        VStride,
  _In_    const D3DXMATRIX  *pM,
  _In_          UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="f3e90-106">參數</span><span class="sxs-lookup"><span data-stu-id="f3e90-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3e90-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="f3e90-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f3e90-108">類型： **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="f3e90-108">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="f3e90-109">作業結果之 [**D3DXVECTOR2**](d3d10-d3dxvector2.md) 的指標。</span><span class="sxs-lookup"><span data-stu-id="f3e90-109">Pointer to the [**D3DXVECTOR2**](d3d10-d3dxvector2.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="f3e90-110">*OutStride* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f3e90-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3e90-111">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f3e90-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f3e90-112">輸出資料流程中向量之間的 Stride。</span><span class="sxs-lookup"><span data-stu-id="f3e90-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="f3e90-113">*pV* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f3e90-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3e90-114">Type： **Const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="f3e90-114">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="f3e90-115">來源 D3DXVECTOR2 陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="f3e90-115">Pointer to the source D3DXVECTOR2 array.</span></span>

</dd> <dt>

<span data-ttu-id="f3e90-116">*VStride* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f3e90-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3e90-117">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f3e90-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f3e90-118">輸入資料流程中向量之間的 Stride。</span><span class="sxs-lookup"><span data-stu-id="f3e90-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="f3e90-119">*pM* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f3e90-119">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3e90-120">Type： **Const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="f3e90-120">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="f3e90-121">來源 [**D3DXMATRIX**](d3d10-d3dxmatrix.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="f3e90-121">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="f3e90-122">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f3e90-122">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3e90-123">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f3e90-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f3e90-124">陣列中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="f3e90-124">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3e90-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="f3e90-125">Return value</span></span>

<span data-ttu-id="f3e90-126">類型： **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="f3e90-126">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="f3e90-127">D3DXVECTOR2 結構的指標，此結構是已轉換的陣列。</span><span class="sxs-lookup"><span data-stu-id="f3e90-127">Pointer to a D3DXVECTOR2 structure that is the transformed array.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3e90-128">備註</span><span class="sxs-lookup"><span data-stu-id="f3e90-128">Remarks</span></span>

<span data-ttu-id="f3e90-129">此函式會將向量 (pV->x，pV->y，0，0) 由 pM 指向的矩陣。</span><span class="sxs-lookup"><span data-stu-id="f3e90-129">This function transforms the vector (pV->x, pV->y, 0, 0) by the matrix pointed to by pM.</span></span>

<span data-ttu-id="f3e90-130">如果您想要轉換一般，您傳遞給此函式的矩陣應該是您用來轉換點之矩陣反向的調換。</span><span class="sxs-lookup"><span data-stu-id="f3e90-130">If you want to transform a normal, the matrix you pass to this function should be the transpose of the inverse of the matrix you would use to transform a point.</span></span>

<span data-ttu-id="f3e90-131">此函式的傳回值與不悅參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="f3e90-131">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="f3e90-132">如此一來， **D3DXVec2TransformNormalArray** 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="f3e90-132">In this way, the **D3DXVec2TransformNormalArray** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3e90-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="f3e90-133">Requirements</span></span>



| <span data-ttu-id="f3e90-134">需求</span><span class="sxs-lookup"><span data-stu-id="f3e90-134">Requirement</span></span> | <span data-ttu-id="f3e90-135">值</span><span class="sxs-lookup"><span data-stu-id="f3e90-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f3e90-136">標頭</span><span class="sxs-lookup"><span data-stu-id="f3e90-136">Header</span></span><br/>  | <dl> <span data-ttu-id="f3e90-137"><dt>D3DX10Math。h</dt></span><span class="sxs-lookup"><span data-stu-id="f3e90-137"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="f3e90-138">程式庫</span><span class="sxs-lookup"><span data-stu-id="f3e90-138">Library</span></span><br/> | <dl> <span data-ttu-id="f3e90-139"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="f3e90-139"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f3e90-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f3e90-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3e90-141">數學函數</span><span class="sxs-lookup"><span data-stu-id="f3e90-141">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
