---
description: D3DXVec2TransformNormal 函式 (D3dx9math) -依指定的矩陣轉換2D 向量標準。
ms.assetid: aa9adf6d-5aae-4acf-bbd9-f5c14d90470e
title: 'D3DXVec2TransformNormal 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2TransformNormal
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c8ed31300027fcb2e827988809cce1c50dbf77de
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097906"
---
# <a name="d3dxvec2transformnormal-function-d3dx9mathh"></a><span data-ttu-id="60b64-103">D3DXVec2TransformNormal 函式 (D3dx9math) </span><span class="sxs-lookup"><span data-stu-id="60b64-103">D3DXVec2TransformNormal function (D3dx9math.h)</span></span>

<span data-ttu-id="60b64-104">依指定的矩陣轉換2D 向量標準。</span><span class="sxs-lookup"><span data-stu-id="60b64-104">Transforms the 2D vector normal by the given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="60b64-105">語法</span><span class="sxs-lookup"><span data-stu-id="60b64-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2TransformNormal(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="60b64-106">參數</span><span class="sxs-lookup"><span data-stu-id="60b64-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60b64-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="60b64-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="60b64-108">類型： **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="60b64-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="60b64-109">[**D3DXVECTOR2**](d3dxvector2.md)結構的指標，此結構是作業的結果。</span><span class="sxs-lookup"><span data-stu-id="60b64-109">Pointer to the [**D3DXVECTOR2**](d3dxvector2.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="60b64-110">*pV* \[在\]</span><span class="sxs-lookup"><span data-stu-id="60b64-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60b64-111">Type： **Const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="60b64-111">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="60b64-112">來源 [**D3DXVECTOR2**](d3dxvector2.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="60b64-112">Pointer to the source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="60b64-113">*pM* \[在\]</span><span class="sxs-lookup"><span data-stu-id="60b64-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60b64-114">Type： **Const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="60b64-114">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="60b64-115">來源 [**D3DXMATRIX**](d3dxmatrix.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="60b64-115">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60b64-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="60b64-116">Return value</span></span>

<span data-ttu-id="60b64-117">類型： **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="60b64-117">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="60b64-118">[**D3DXVECTOR2**](d3dxvector2.md)結構的指標，此結構是已轉換的向量。</span><span class="sxs-lookup"><span data-stu-id="60b64-118">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="60b64-119">備註</span><span class="sxs-lookup"><span data-stu-id="60b64-119">Remarks</span></span>

<span data-ttu-id="60b64-120">此函式會將向量 (*pv-*>x， *pv-*>y，0，0) 由 *pM* 指向的矩陣。</span><span class="sxs-lookup"><span data-stu-id="60b64-120">This function transforms the vector (*pV-*>x, *pV-*>y, 0, 0) by the matrix pointed to by *pM*.</span></span>

<span data-ttu-id="60b64-121">如果您想要轉換一般，您傳遞給此函式的矩陣應該是您用來轉換點之矩陣反向的調換。</span><span class="sxs-lookup"><span data-stu-id="60b64-121">If you want to transform a normal, the matrix you pass to this function should be the transpose of the inverse of the matrix you would use to transform a point.</span></span>

<span data-ttu-id="60b64-122">此函式的傳回值與 *不悅* 參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="60b64-122">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="60b64-123">如此一來， **D3DXVec2TransformNormal** 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="60b64-123">In this way, the **D3DXVec2TransformNormal** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="60b64-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="60b64-124">Requirements</span></span>



| <span data-ttu-id="60b64-125">需求</span><span class="sxs-lookup"><span data-stu-id="60b64-125">Requirement</span></span> | <span data-ttu-id="60b64-126">值</span><span class="sxs-lookup"><span data-stu-id="60b64-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="60b64-127">標頭</span><span class="sxs-lookup"><span data-stu-id="60b64-127">Header</span></span><br/>  | <dl> <span data-ttu-id="60b64-128"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="60b64-128"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="60b64-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="60b64-129">Library</span></span><br/> | <dl> <span data-ttu-id="60b64-130"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="60b64-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="60b64-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="60b64-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60b64-132">數學函數</span><span class="sxs-lookup"><span data-stu-id="60b64-132">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="60b64-133">**D3DXVec2Transform**</span><span class="sxs-lookup"><span data-stu-id="60b64-133">**D3DXVec2Transform**</span></span>](d3dxvec2transform.md)
</dt> <dt>

[<span data-ttu-id="60b64-134">**D3DXVec2TransformCoord**</span><span class="sxs-lookup"><span data-stu-id="60b64-134">**D3DXVec2TransformCoord**</span></span>](d3dxvec2transformcoord.md)
</dt> </dl>

 

 




