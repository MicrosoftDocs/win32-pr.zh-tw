---
description: 依指定的矩陣轉換2D 向量標準。
ms.assetid: fc238bb1-155f-4018-9c92-16352726920d
title: 'D3DXVec2TransformNormal 函式 (D3DX10Math) '
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: c4043a8f5a57f14be3e8506dc257690ef581835d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946114"
---
# <a name="d3dxvec2transformnormal-function-d3dx10mathh"></a><span data-ttu-id="a583a-103">D3DXVec2TransformNormal 函式 (D3DX10Math) </span><span class="sxs-lookup"><span data-stu-id="a583a-103">D3DXVec2TransformNormal function (D3DX10Math.h)</span></span>

<span data-ttu-id="a583a-104">依指定的矩陣轉換2D 向量標準。</span><span class="sxs-lookup"><span data-stu-id="a583a-104">Transforms the 2D vector normal by the given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="a583a-105">語法</span><span class="sxs-lookup"><span data-stu-id="a583a-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2TransformNormal(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="a583a-106">參數</span><span class="sxs-lookup"><span data-stu-id="a583a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a583a-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="a583a-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a583a-108">類型： **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="a583a-108">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="a583a-109">作業結果之 [**D3DXVECTOR2**](d3d10-d3dxvector2.md) 的指標。</span><span class="sxs-lookup"><span data-stu-id="a583a-109">Pointer to the [**D3DXVECTOR2**](d3d10-d3dxvector2.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="a583a-110">*pV* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a583a-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a583a-111">Type： **Const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="a583a-111">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="a583a-112">來源 D3DXVECTOR2 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="a583a-112">Pointer to the source D3DXVECTOR2 structure.</span></span>

</dd> <dt>

<span data-ttu-id="a583a-113">*pM* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a583a-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a583a-114">Type： **Const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="a583a-114">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="a583a-115">來源 [**D3DXMATRIX**](d3d10-d3dxmatrix.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="a583a-115">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a583a-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="a583a-116">Return value</span></span>

<span data-ttu-id="a583a-117">類型： **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="a583a-117">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="a583a-118">D3DXVECTOR2 結構的指標，此結構是已轉換的向量。</span><span class="sxs-lookup"><span data-stu-id="a583a-118">Pointer to a D3DXVECTOR2 structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="a583a-119">備註</span><span class="sxs-lookup"><span data-stu-id="a583a-119">Remarks</span></span>

<span data-ttu-id="a583a-120">此函式會將向量 (pV->x，pV->y，0，0) 由 pM 指向的矩陣。</span><span class="sxs-lookup"><span data-stu-id="a583a-120">This function transforms the vector (pV->x, pV->y, 0, 0) by the matrix pointed to by pM.</span></span>

<span data-ttu-id="a583a-121">如果您想要轉換一般，您傳遞給此函式的矩陣應該是您用來轉換點之矩陣反向的調換。</span><span class="sxs-lookup"><span data-stu-id="a583a-121">If you want to transform a normal, the matrix you pass to this function should be the transpose of the inverse of the matrix you would use to transform a point.</span></span>

<span data-ttu-id="a583a-122">此函式的傳回值與不悅參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="a583a-122">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="a583a-123">如此一來， **D3DXVec2TransformNormal** 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="a583a-123">In this way, the **D3DXVec2TransformNormal** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="a583a-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="a583a-124">Requirements</span></span>



| <span data-ttu-id="a583a-125">需求</span><span class="sxs-lookup"><span data-stu-id="a583a-125">Requirement</span></span> | <span data-ttu-id="a583a-126">值</span><span class="sxs-lookup"><span data-stu-id="a583a-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a583a-127">標頭</span><span class="sxs-lookup"><span data-stu-id="a583a-127">Header</span></span><br/>  | <dl> <span data-ttu-id="a583a-128"><dt>D3DX10Math。h</dt></span><span class="sxs-lookup"><span data-stu-id="a583a-128"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="a583a-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="a583a-129">Library</span></span><br/> | <dl> <span data-ttu-id="a583a-130"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="a583a-130"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a583a-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a583a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a583a-132">數學函數</span><span class="sxs-lookup"><span data-stu-id="a583a-132">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
