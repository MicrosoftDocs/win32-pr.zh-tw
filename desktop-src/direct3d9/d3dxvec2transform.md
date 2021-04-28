---
description: D3DXVec2Transform 函式 (D3dx9math) -依指定的矩陣轉換2D 向量。
ms.assetid: ccde9e34-2d99-4112-a8ed-3820d018b547
title: 'D3DXVec2Transform 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2Transform
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9b9b0f5ae0e3fda05cd8bdd92ee73b826f81b970
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097946"
---
# <a name="d3dxvec2transform-function-d3dx9mathh"></a><span data-ttu-id="d33ef-103">D3DXVec2Transform 函式 (D3dx9math) </span><span class="sxs-lookup"><span data-stu-id="d33ef-103">D3DXVec2Transform function (D3dx9math.h)</span></span>

<span data-ttu-id="d33ef-104">依指定的矩陣轉換2D 向量。</span><span class="sxs-lookup"><span data-stu-id="d33ef-104">Transforms a 2D vector by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="d33ef-105">語法</span><span class="sxs-lookup"><span data-stu-id="d33ef-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec2Transform(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR2 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="d33ef-106">參數</span><span class="sxs-lookup"><span data-stu-id="d33ef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d33ef-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="d33ef-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d33ef-108">類型： **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="d33ef-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="d33ef-109">[**D3DXVECTOR4**](d3dxvector4.md)結構的指標，此結構是作業的結果。</span><span class="sxs-lookup"><span data-stu-id="d33ef-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="d33ef-110">*pV* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d33ef-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d33ef-111">Type： **Const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="d33ef-111">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="d33ef-112">來源 [**D3DXVECTOR2**](d3dxvector2.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="d33ef-112">Pointer to the source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="d33ef-113">*pM* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d33ef-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d33ef-114">Type： **Const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="d33ef-114">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="d33ef-115">來源 [**D3DXMATRIX**](d3dxmatrix.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="d33ef-115">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d33ef-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="d33ef-116">Return value</span></span>

<span data-ttu-id="d33ef-117">類型： **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="d33ef-117">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="d33ef-118">[**D3DXVECTOR4**](d3dxvector4.md)結構的指標，此結構是已轉換的向量。</span><span class="sxs-lookup"><span data-stu-id="d33ef-118">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="d33ef-119">備註</span><span class="sxs-lookup"><span data-stu-id="d33ef-119">Remarks</span></span>

<span data-ttu-id="d33ef-120">此函式會將向量 *pV* (x、y、0、1) 由矩陣 *pM* 進行轉換。</span><span class="sxs-lookup"><span data-stu-id="d33ef-120">This function transforms the vector *pV* (x, y, 0, 1) by the matrix *pM*.</span></span>

<span data-ttu-id="d33ef-121">此函式的傳回值與 *不悅* 參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="d33ef-121">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="d33ef-122">如此一來， **D3DXVec2Transform** 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="d33ef-122">In this way, the **D3DXVec2Transform** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="d33ef-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="d33ef-123">Requirements</span></span>



| <span data-ttu-id="d33ef-124">需求</span><span class="sxs-lookup"><span data-stu-id="d33ef-124">Requirement</span></span> | <span data-ttu-id="d33ef-125">值</span><span class="sxs-lookup"><span data-stu-id="d33ef-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d33ef-126">標頭</span><span class="sxs-lookup"><span data-stu-id="d33ef-126">Header</span></span><br/>  | <dl> <span data-ttu-id="d33ef-127"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="d33ef-127"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="d33ef-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="d33ef-128">Library</span></span><br/> | <dl> <span data-ttu-id="d33ef-129"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d33ef-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d33ef-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d33ef-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d33ef-131">數學函數</span><span class="sxs-lookup"><span data-stu-id="d33ef-131">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="d33ef-132">**D3DXVec2TransformCoord**</span><span class="sxs-lookup"><span data-stu-id="d33ef-132">**D3DXVec2TransformCoord**</span></span>](d3dxvec2transformcoord.md)
</dt> <dt>

[<span data-ttu-id="d33ef-133">**D3DXVec2TransformNormal**</span><span class="sxs-lookup"><span data-stu-id="d33ef-133">**D3DXVec2TransformNormal**</span></span>](d3dxvec2transformnormal.md)
</dt> </dl>

 

 




