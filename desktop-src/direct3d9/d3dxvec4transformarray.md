---
description: D3DXVec4TransformArray 函式 (D3dx9math) -轉換陣列 (x、y、0、1) 指定的矩陣。
ms.assetid: 11d69f65-2aef-46f4-b274-e173a11382a8
title: 'D3DXVec4TransformArray 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4TransformArray
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5f5435b7e88a5424db9457fac077495fcfd8828a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097626"
---
# <a name="d3dxvec4transformarray-function-d3dx9mathh"></a><span data-ttu-id="dabd1-103">D3DXVec4TransformArray 函式 (D3dx9math) </span><span class="sxs-lookup"><span data-stu-id="dabd1-103">D3DXVec4TransformArray function (D3dx9math.h)</span></span>

<span data-ttu-id="dabd1-104">將陣列 (x、y、0、1) 由指定的矩陣進行轉換。</span><span class="sxs-lookup"><span data-stu-id="dabd1-104">Transforms an array (x, y, 0, 1) by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="dabd1-105">語法</span><span class="sxs-lookup"><span data-stu-id="dabd1-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="dabd1-106">參數</span><span class="sxs-lookup"><span data-stu-id="dabd1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dabd1-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="dabd1-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="dabd1-108">類型： **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="dabd1-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="dabd1-109">[**D3DXVECTOR4**](d3dxvector4.md)陣列的指標，這是作業的結果。</span><span class="sxs-lookup"><span data-stu-id="dabd1-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) array that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="dabd1-110">*OutStride* \[在\]</span><span class="sxs-lookup"><span data-stu-id="dabd1-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dabd1-111">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dabd1-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dabd1-112">輸出資料流程中向量之間的 Stride。</span><span class="sxs-lookup"><span data-stu-id="dabd1-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="dabd1-113">*pV* \[在\]</span><span class="sxs-lookup"><span data-stu-id="dabd1-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dabd1-114">Type： **Const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="dabd1-114">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="dabd1-115">來源 [**D3DXVECTOR4**](d3dxvector4.md) 陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="dabd1-115">Pointer to the source [**D3DXVECTOR4**](d3dxvector4.md) array.</span></span>

</dd> <dt>

<span data-ttu-id="dabd1-116">*VStride* \[在\]</span><span class="sxs-lookup"><span data-stu-id="dabd1-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dabd1-117">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dabd1-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dabd1-118">輸入資料流程中向量之間的 Stride。</span><span class="sxs-lookup"><span data-stu-id="dabd1-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="dabd1-119">*pM* \[在\]</span><span class="sxs-lookup"><span data-stu-id="dabd1-119">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dabd1-120">Type： **Const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="dabd1-120">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="dabd1-121">來源 [**D3DXMATRIX**](d3dxmatrix.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="dabd1-121">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="dabd1-122">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dabd1-122">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dabd1-123">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dabd1-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dabd1-124">陣列中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="dabd1-124">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dabd1-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="dabd1-125">Return value</span></span>

<span data-ttu-id="dabd1-126">類型： **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="dabd1-126">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="dabd1-127">[**D3DXVECTOR4**](d3dxvector4.md)結構的指標，此結構是已轉換的陣列。</span><span class="sxs-lookup"><span data-stu-id="dabd1-127">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure that is the transformed array.</span></span>

## <a name="remarks"></a><span data-ttu-id="dabd1-128">備註</span><span class="sxs-lookup"><span data-stu-id="dabd1-128">Remarks</span></span>

<span data-ttu-id="dabd1-129">此函式會將陣列 *pV* (x、y、0、1) 由矩陣 *pM* 來轉換。</span><span class="sxs-lookup"><span data-stu-id="dabd1-129">This function transforms the array *pV* (x, y, 0, 1) by the matrix *pM*.</span></span>

<span data-ttu-id="dabd1-130">此函式的傳回值與 *不悅* 參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="dabd1-130">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="dabd1-131">如此一來， **D3DXVec4TransformArray** 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="dabd1-131">In this way, the **D3DXVec4TransformArray** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="dabd1-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="dabd1-132">Requirements</span></span>



| <span data-ttu-id="dabd1-133">需求</span><span class="sxs-lookup"><span data-stu-id="dabd1-133">Requirement</span></span> | <span data-ttu-id="dabd1-134">值</span><span class="sxs-lookup"><span data-stu-id="dabd1-134">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dabd1-135">標頭</span><span class="sxs-lookup"><span data-stu-id="dabd1-135">Header</span></span><br/>  | <dl> <span data-ttu-id="dabd1-136"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="dabd1-136"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="dabd1-137">程式庫</span><span class="sxs-lookup"><span data-stu-id="dabd1-137">Library</span></span><br/> | <dl> <span data-ttu-id="dabd1-138"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="dabd1-138"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="dabd1-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dabd1-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dabd1-140">數學函數</span><span class="sxs-lookup"><span data-stu-id="dabd1-140">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
