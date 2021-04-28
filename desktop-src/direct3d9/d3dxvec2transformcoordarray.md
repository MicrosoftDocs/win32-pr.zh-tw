---
description: D3DXVec2TransformCoordArray 函式 (D3dx9math) -轉換陣列 (x、y、0、1) 指定的矩陣，然後將結果投射回 w = 1。
ms.assetid: 23c88bed-344b-4b3a-bb92-e50cbe96daf9
title: 'D3DXVec2TransformCoordArray 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2TransformCoordArray
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 257cb77ba97396170f221cff1c512a73eb84179c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097936"
---
# <a name="d3dxvec2transformcoordarray-function-d3dx9mathh"></a><span data-ttu-id="d4ca2-103">D3DXVec2TransformCoordArray 函式 (D3dx9math) </span><span class="sxs-lookup"><span data-stu-id="d4ca2-103">D3DXVec2TransformCoordArray function (D3dx9math.h)</span></span>

<span data-ttu-id="d4ca2-104">將陣列 (x、y、0、1) 由指定的矩陣轉換，然後將結果投射回 w = 1。</span><span class="sxs-lookup"><span data-stu-id="d4ca2-104">Transforms an array (x, y, 0, 1) by a given matrix, and projects the result back into w = 1.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4ca2-105">語法</span><span class="sxs-lookup"><span data-stu-id="d4ca2-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2TransformCoordArray(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_          UINT        OutStride,
  _In_    const D3DXVECTOR2 *pV,
  _In_          UINT        VStride,
  _In_    const D3DXMATRIX  *pM,
  _In_          UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="d4ca2-106">參數</span><span class="sxs-lookup"><span data-stu-id="d4ca2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4ca2-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="d4ca2-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d4ca2-108">類型： **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="d4ca2-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="d4ca2-109">[**D3DXVECTOR2**](d3dxvector2.md)結構的指標，此結構是作業的結果。</span><span class="sxs-lookup"><span data-stu-id="d4ca2-109">Pointer to the [**D3DXVECTOR2**](d3dxvector2.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="d4ca2-110">*OutStride* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d4ca2-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4ca2-111">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d4ca2-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d4ca2-112">輸出資料流程中向量之間的 Stride。</span><span class="sxs-lookup"><span data-stu-id="d4ca2-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="d4ca2-113">*pV* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d4ca2-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4ca2-114">Type： **Const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="d4ca2-114">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="d4ca2-115">來源 [**D3DXVECTOR2**](d3dxvector2.md) 陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="d4ca2-115">Pointer to the source [**D3DXVECTOR2**](d3dxvector2.md) array.</span></span>

</dd> <dt>

<span data-ttu-id="d4ca2-116">*VStride* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d4ca2-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4ca2-117">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d4ca2-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d4ca2-118">輸入資料流程中向量之間的 Stride。</span><span class="sxs-lookup"><span data-stu-id="d4ca2-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="d4ca2-119">*pM* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d4ca2-119">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4ca2-120">Type： **Const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="d4ca2-120">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="d4ca2-121">來源 [**D3DXMATRIX**](d3dxmatrix.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="d4ca2-121">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="d4ca2-122">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d4ca2-122">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4ca2-123">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d4ca2-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d4ca2-124">陣列中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="d4ca2-124">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4ca2-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="d4ca2-125">Return value</span></span>

<span data-ttu-id="d4ca2-126">類型： **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="d4ca2-126">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="d4ca2-127">[**D3DXVECTOR4**](d3dxvector4.md)轉換陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="d4ca2-127">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) transformed array.</span></span>

## <a name="remarks"></a><span data-ttu-id="d4ca2-128">備註</span><span class="sxs-lookup"><span data-stu-id="d4ca2-128">Remarks</span></span>

<span data-ttu-id="d4ca2-129">此函式會將陣列 *pV* (x、y、0、1) 由矩陣 *pM* 轉換，然後將結果投射回 w = 1。</span><span class="sxs-lookup"><span data-stu-id="d4ca2-129">This function transforms the array *pV* (x, y, 0, 1) by the matrix *pM*, projecting the result back into w = 1.</span></span>

<span data-ttu-id="d4ca2-130">此函式的傳回值與 *不悅* 參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="d4ca2-130">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="d4ca2-131">如此一來， **D3DXVec2TransformCoordArray** 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="d4ca2-131">In this way, the **D3DXVec2TransformCoordArray** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4ca2-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="d4ca2-132">Requirements</span></span>



| <span data-ttu-id="d4ca2-133">需求</span><span class="sxs-lookup"><span data-stu-id="d4ca2-133">Requirement</span></span> | <span data-ttu-id="d4ca2-134">值</span><span class="sxs-lookup"><span data-stu-id="d4ca2-134">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d4ca2-135">標頭</span><span class="sxs-lookup"><span data-stu-id="d4ca2-135">Header</span></span><br/>  | <dl> <span data-ttu-id="d4ca2-136"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="d4ca2-136"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="d4ca2-137">程式庫</span><span class="sxs-lookup"><span data-stu-id="d4ca2-137">Library</span></span><br/> | <dl> <span data-ttu-id="d4ca2-138"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d4ca2-138"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d4ca2-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d4ca2-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4ca2-140">數學函數</span><span class="sxs-lookup"><span data-stu-id="d4ca2-140">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
