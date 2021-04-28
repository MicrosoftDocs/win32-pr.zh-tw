---
description: D3DXVec3TransformNormal 函式 (D3DX10Math) -由指定的矩陣轉換一般的3D 向量。
ms.assetid: 8068b80f-6222-4f23-8b1c-2ff5592fa898
title: 'D3DXVec3TransformNormal 函式 (D3DX10Math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3TransformNormal
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 0fc1456b89f3e11f2076a8e7b6b960d15e9c7083
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103056"
---
# <a name="d3dxvec3transformnormal-function-d3dx10mathh"></a><span data-ttu-id="c9006-103">D3DXVec3TransformNormal 函式 (D3DX10Math) </span><span class="sxs-lookup"><span data-stu-id="c9006-103">D3DXVec3TransformNormal function (D3DX10Math.h)</span></span>

<span data-ttu-id="c9006-104">依指定的矩陣轉換一般的3D 向量。</span><span class="sxs-lookup"><span data-stu-id="c9006-104">Transforms the 3D vector normal by the given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9006-105">語法</span><span class="sxs-lookup"><span data-stu-id="c9006-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3TransformNormal(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="c9006-106">參數</span><span class="sxs-lookup"><span data-stu-id="c9006-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9006-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="c9006-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c9006-108">類型： **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="c9006-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="c9006-109">作業結果之 [**D3DXVECTOR3**](d3d10-d3dxvector3.md) 的指標。</span><span class="sxs-lookup"><span data-stu-id="c9006-109">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="c9006-110">*pV* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c9006-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9006-111">Type： **Const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="c9006-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="c9006-112">來源 D3DXVECTOR3 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="c9006-112">Pointer to the source D3DXVECTOR3 structure.</span></span>

</dd> <dt>

<span data-ttu-id="c9006-113">*pM* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c9006-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9006-114">Type： **Const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="c9006-114">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="c9006-115">來源 [**D3DXMATRIX**](d3d10-d3dxmatrix.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="c9006-115">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9006-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="c9006-116">Return value</span></span>

<span data-ttu-id="c9006-117">類型： **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="c9006-117">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="c9006-118">D3DXVECTOR3 結構的指標，此結構是已轉換的向量。</span><span class="sxs-lookup"><span data-stu-id="c9006-118">Pointer to a D3DXVECTOR3 structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9006-119">備註</span><span class="sxs-lookup"><span data-stu-id="c9006-119">Remarks</span></span>

<span data-ttu-id="c9006-120">此函式會將向量 (pV->x，pV->y，pV >z，0) 由 pM 指向的矩陣。</span><span class="sxs-lookup"><span data-stu-id="c9006-120">This function transforms the vector (pV->x, pV->y, pV->z, 0) by the matrix pointed to by pM.</span></span>

<span data-ttu-id="c9006-121">如果您想要轉換一般，您傳遞給此函式的矩陣應該是您用來轉換點之矩陣反向的調換。</span><span class="sxs-lookup"><span data-stu-id="c9006-121">If you want to transform a normal, the matrix you pass to this function should be the transpose of the inverse of the matrix you would use to transform a point.</span></span>

<span data-ttu-id="c9006-122">此函式的傳回值與不悅參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="c9006-122">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="c9006-123">如此一來， **D3DXVec3TransformNormal** 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="c9006-123">In this way, the **D3DXVec3TransformNormal** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9006-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="c9006-124">Requirements</span></span>



| <span data-ttu-id="c9006-125">需求</span><span class="sxs-lookup"><span data-stu-id="c9006-125">Requirement</span></span> | <span data-ttu-id="c9006-126">值</span><span class="sxs-lookup"><span data-stu-id="c9006-126">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c9006-127">標頭</span><span class="sxs-lookup"><span data-stu-id="c9006-127">Header</span></span><br/> | <dl> <span data-ttu-id="c9006-128"><dt>D3DX10Math。h</dt></span><span class="sxs-lookup"><span data-stu-id="c9006-128"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9006-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c9006-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9006-130">數學函數</span><span class="sxs-lookup"><span data-stu-id="c9006-130">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
