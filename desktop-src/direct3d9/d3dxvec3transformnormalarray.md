---
description: D3DXVec3TransformNormalArray 函式 (D3dx9math) -轉換陣列 (x、y、z、0) 指定的矩陣。
ms.assetid: c12fad52-d541-483f-a919-e6031aa4f761
title: 'D3DXVec3TransformNormalArray 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3TransformNormalArray
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 74da959002bfbd0c488e630f09c89e848708b1b1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097726"
---
# <a name="d3dxvec3transformnormalarray-function-d3dx9mathh"></a><span data-ttu-id="22264-103">D3DXVec3TransformNormalArray 函式 (D3dx9math) </span><span class="sxs-lookup"><span data-stu-id="22264-103">D3DXVec3TransformNormalArray function (D3dx9math.h)</span></span>

<span data-ttu-id="22264-104">將陣列 (x、y、z、0) 由指定的矩陣進行轉換。</span><span class="sxs-lookup"><span data-stu-id="22264-104">Transforms an array (x, y, z, 0) by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="22264-105">語法</span><span class="sxs-lookup"><span data-stu-id="22264-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="22264-106">參數</span><span class="sxs-lookup"><span data-stu-id="22264-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22264-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="22264-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="22264-108">類型： **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="22264-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="22264-109">[**D3DXVECTOR3**](d3dxvector3.md)陣列的指標，這是作業的結果。</span><span class="sxs-lookup"><span data-stu-id="22264-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) array that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="22264-110">*OutStride* \[在\]</span><span class="sxs-lookup"><span data-stu-id="22264-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22264-111">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="22264-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="22264-112">輸出資料流程中向量之間的 Stride。</span><span class="sxs-lookup"><span data-stu-id="22264-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="22264-113">*pV* \[在\]</span><span class="sxs-lookup"><span data-stu-id="22264-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22264-114">Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="22264-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="22264-115">來源 [**D3DXVECTOR3**](d3dxvector3.md) 陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="22264-115">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) array.</span></span>

</dd> <dt>

<span data-ttu-id="22264-116">*VStride* \[在\]</span><span class="sxs-lookup"><span data-stu-id="22264-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22264-117">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="22264-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="22264-118">輸入資料流程中向量之間的 Stride。</span><span class="sxs-lookup"><span data-stu-id="22264-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="22264-119">*pM* \[在\]</span><span class="sxs-lookup"><span data-stu-id="22264-119">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22264-120">Type： **Const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="22264-120">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="22264-121">來源 [**D3DXMATRIX**](d3dxmatrix.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="22264-121">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="22264-122">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="22264-122">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22264-123">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="22264-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="22264-124">陣列中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="22264-124">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22264-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="22264-125">Return value</span></span>

<span data-ttu-id="22264-126">類型： **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="22264-126">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="22264-127">[**D3DXVECTOR3**](d3dxvector3.md)陣列的指標，該陣列為已轉換的陣列。</span><span class="sxs-lookup"><span data-stu-id="22264-127">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) array that is the transformed array.</span></span>

## <a name="remarks"></a><span data-ttu-id="22264-128">備註</span><span class="sxs-lookup"><span data-stu-id="22264-128">Remarks</span></span>

<span data-ttu-id="22264-129">此函式會將向量 (*pv*->x， *pv*->y， *pv*>z，0) 由 *pM* 指向的矩陣。</span><span class="sxs-lookup"><span data-stu-id="22264-129">This function transforms the vector (*pV*->x, *pV*->y, *pV*->z, 0) by the matrix pointed to by *pM*.</span></span>

<span data-ttu-id="22264-130">如果您想要轉換一般，您傳遞給此函式的矩陣應該是您用來轉換點之矩陣反向的調換。</span><span class="sxs-lookup"><span data-stu-id="22264-130">If you want to transform a normal, the matrix you pass to this function should be the transpose of the inverse of the matrix you would use to transform a point.</span></span>

<span data-ttu-id="22264-131">此函式的傳回值與 *不悅* 參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="22264-131">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="22264-132">如此一來， **D3DXVec3TransformNormalArray** 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="22264-132">In this way, the **D3DXVec3TransformNormalArray** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="22264-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="22264-133">Requirements</span></span>



| <span data-ttu-id="22264-134">需求</span><span class="sxs-lookup"><span data-stu-id="22264-134">Requirement</span></span> | <span data-ttu-id="22264-135">值</span><span class="sxs-lookup"><span data-stu-id="22264-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="22264-136">標頭</span><span class="sxs-lookup"><span data-stu-id="22264-136">Header</span></span><br/>  | <dl> <span data-ttu-id="22264-137"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="22264-137"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="22264-138">程式庫</span><span class="sxs-lookup"><span data-stu-id="22264-138">Library</span></span><br/> | <dl> <span data-ttu-id="22264-139"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="22264-139"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="22264-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="22264-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22264-141">數學函數</span><span class="sxs-lookup"><span data-stu-id="22264-141">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
