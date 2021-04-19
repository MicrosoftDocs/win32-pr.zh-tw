---
description: 依指定的矩陣轉換2D 向量，將結果投射回 w = 1。
ms.assetid: bb24204f-0c8e-4dc5-bcae-12e3033d1a39
title: 'D3DXVec2TransformCoord 函式 (D3DX10Math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2TransformCoord
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 0d7e93c2b3a78160f2f1f1ad3342575b4369a057
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106992130"
---
# <a name="d3dxvec2transformcoord-function-d3dx10mathh"></a><span data-ttu-id="268e4-103">D3DXVec2TransformCoord 函式 (D3DX10Math) </span><span class="sxs-lookup"><span data-stu-id="268e4-103">D3DXVec2TransformCoord function (D3DX10Math.h)</span></span>

<span data-ttu-id="268e4-104">依指定的矩陣轉換2D 向量，將結果投射回 w = 1。</span><span class="sxs-lookup"><span data-stu-id="268e4-104">Transforms a 2D vector by a given matrix, projecting the result back into w = 1.</span></span>

## <a name="syntax"></a><span data-ttu-id="268e4-105">語法</span><span class="sxs-lookup"><span data-stu-id="268e4-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2TransformCoord(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="268e4-106">參數</span><span class="sxs-lookup"><span data-stu-id="268e4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="268e4-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="268e4-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="268e4-108">類型： **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="268e4-108">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="268e4-109">作業結果之 [**D3DXVECTOR2**](d3d10-d3dxvector2.md) 的指標。</span><span class="sxs-lookup"><span data-stu-id="268e4-109">Pointer to the [**D3DXVECTOR2**](d3d10-d3dxvector2.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="268e4-110">*pV* \[在\]</span><span class="sxs-lookup"><span data-stu-id="268e4-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="268e4-111">Type： **Const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="268e4-111">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="268e4-112">來源 D3DXVECTOR2 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="268e4-112">Pointer to the source D3DXVECTOR2 structure.</span></span>

</dd> <dt>

<span data-ttu-id="268e4-113">*pM* \[在\]</span><span class="sxs-lookup"><span data-stu-id="268e4-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="268e4-114">Type： **Const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="268e4-114">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="268e4-115">來源 [**D3DXMATRIX**](d3d10-d3dxmatrix.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="268e4-115">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="268e4-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="268e4-116">Return value</span></span>

<span data-ttu-id="268e4-117">類型： **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="268e4-117">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="268e4-118">D3DXVECTOR2 結構的指標，此結構是已轉換的向量。</span><span class="sxs-lookup"><span data-stu-id="268e4-118">Pointer to a D3DXVECTOR2 structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="268e4-119">備註</span><span class="sxs-lookup"><span data-stu-id="268e4-119">Remarks</span></span>

<span data-ttu-id="268e4-120">此函式會將向量、pV (x、y、0、1) ，由矩陣 pM 轉換，然後將結果投射回 w = 1。</span><span class="sxs-lookup"><span data-stu-id="268e4-120">This function transforms the vector, pV (x, y, 0, 1), by the matrix, pM, projecting the result back into w=1.</span></span>

<span data-ttu-id="268e4-121">此函式的傳回值與不悅參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="268e4-121">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="268e4-122">如此一來，D3DXVec2TransformCoord 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="268e4-122">In this way, the D3DXVec2TransformCoord function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="268e4-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="268e4-123">Requirements</span></span>



| <span data-ttu-id="268e4-124">需求</span><span class="sxs-lookup"><span data-stu-id="268e4-124">Requirement</span></span> | <span data-ttu-id="268e4-125">值</span><span class="sxs-lookup"><span data-stu-id="268e4-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="268e4-126">標頭</span><span class="sxs-lookup"><span data-stu-id="268e4-126">Header</span></span><br/>  | <dl> <span data-ttu-id="268e4-127"><dt>D3DX10Math。h</dt></span><span class="sxs-lookup"><span data-stu-id="268e4-127"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="268e4-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="268e4-128">Library</span></span><br/> | <dl> <span data-ttu-id="268e4-129"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="268e4-129"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="268e4-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="268e4-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="268e4-131">數學函數</span><span class="sxs-lookup"><span data-stu-id="268e4-131">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
