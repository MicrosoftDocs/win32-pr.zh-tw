---
description: 將陣列 (x、y、0、0) 由指定的矩陣進行轉換。
ms.assetid: 9f5d8fdc-f3e1-41dc-be4e-9ffc6be1947f
title: 'D3DXVec2TransformNormalArray 函式 (D3dx9math) '
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0aece37f9bebb46bab8a0d2a1c27bf19e0c2b0bd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106995903"
---
# <a name="d3dxvec2transformnormalarray-function-d3dx9mathh"></a><span data-ttu-id="c8537-103">D3DXVec2TransformNormalArray 函式 (D3dx9math) </span><span class="sxs-lookup"><span data-stu-id="c8537-103">D3DXVec2TransformNormalArray function (D3dx9math.h)</span></span>

<span data-ttu-id="c8537-104">將陣列 (x、y、0、0) 由指定的矩陣進行轉換。</span><span class="sxs-lookup"><span data-stu-id="c8537-104">Transforms an array (x, y, 0, 0) by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8537-105">語法</span><span class="sxs-lookup"><span data-stu-id="c8537-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="c8537-106">參數</span><span class="sxs-lookup"><span data-stu-id="c8537-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8537-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="c8537-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c8537-108">類型： **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="c8537-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="c8537-109">[**D3DXVECTOR2**](d3dxvector2.md)結構的指標，此結構是作業的結果。</span><span class="sxs-lookup"><span data-stu-id="c8537-109">Pointer to the [**D3DXVECTOR2**](d3dxvector2.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="c8537-110">*OutStride* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c8537-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8537-111">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c8537-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c8537-112">輸出資料流程中向量之間的 Stride。</span><span class="sxs-lookup"><span data-stu-id="c8537-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="c8537-113">*pV* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c8537-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8537-114">Type： **Const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="c8537-114">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="c8537-115">來源 [**D3DXVECTOR2**](d3dxvector2.md) 陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="c8537-115">Pointer to the source [**D3DXVECTOR2**](d3dxvector2.md) array.</span></span>

</dd> <dt>

<span data-ttu-id="c8537-116">*VStride* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c8537-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8537-117">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c8537-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c8537-118">輸入資料流程中向量之間的 Stride。</span><span class="sxs-lookup"><span data-stu-id="c8537-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="c8537-119">*pM* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c8537-119">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8537-120">Type： **Const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="c8537-120">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="c8537-121">來源 [**D3DXMATRIX**](d3dxmatrix.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="c8537-121">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="c8537-122">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c8537-122">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8537-123">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c8537-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c8537-124">陣列中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="c8537-124">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8537-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="c8537-125">Return value</span></span>

<span data-ttu-id="c8537-126">類型： **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="c8537-126">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="c8537-127">[**D3DXVECTOR2**](d3dxvector2.md)結構的指標，此結構是已轉換的陣列。</span><span class="sxs-lookup"><span data-stu-id="c8537-127">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure that is the transformed array.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8537-128">備註</span><span class="sxs-lookup"><span data-stu-id="c8537-128">Remarks</span></span>

<span data-ttu-id="c8537-129">此函式會將向量 (*pv-*>x， *pv-*>y，0，0) 由 pM 指向的矩陣 *。*</span><span class="sxs-lookup"><span data-stu-id="c8537-129">This function transforms the vector (*pV-*>x, *pV-*>y, 0, 0) by the matrix pointed to by *pM.*</span></span>

<span data-ttu-id="c8537-130">如果您想要轉換一般，您傳遞給此函式的矩陣應該是您用來轉換點之矩陣反向的調換。</span><span class="sxs-lookup"><span data-stu-id="c8537-130">If you want to transform a normal, the matrix you pass to this function should be the transpose of the inverse of the matrix you would use to transform a point.</span></span>

<span data-ttu-id="c8537-131">此函式的傳回值與 *不悅* 參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="c8537-131">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="c8537-132">如此一來， **D3DXVec2TransformNormalArray** 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="c8537-132">In this way, the **D3DXVec2TransformNormalArray** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8537-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="c8537-133">Requirements</span></span>



| <span data-ttu-id="c8537-134">需求</span><span class="sxs-lookup"><span data-stu-id="c8537-134">Requirement</span></span> | <span data-ttu-id="c8537-135">值</span><span class="sxs-lookup"><span data-stu-id="c8537-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c8537-136">標頭</span><span class="sxs-lookup"><span data-stu-id="c8537-136">Header</span></span><br/>  | <dl> <span data-ttu-id="c8537-137"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="c8537-137"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="c8537-138">程式庫</span><span class="sxs-lookup"><span data-stu-id="c8537-138">Library</span></span><br/> | <dl> <span data-ttu-id="c8537-139"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="c8537-139"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c8537-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c8537-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8537-141">數學函數</span><span class="sxs-lookup"><span data-stu-id="c8537-141">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
