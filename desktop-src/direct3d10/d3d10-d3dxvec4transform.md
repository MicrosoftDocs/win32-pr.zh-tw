---
description: 依指定的矩陣轉換4D 向量。
ms.assetid: ccbf33bc-1f94-4cf8-b048-220d54516e00
title: 'D3DXVec4Transform 函式 (D3DX10Math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Transform
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 56fc6b3041d799cda3e98d459b2523d4b171df10
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103853979"
---
# <a name="d3dxvec4transform-function-d3dx10mathh"></a><span data-ttu-id="7a49f-103">D3DXVec4Transform 函式 (D3DX10Math) </span><span class="sxs-lookup"><span data-stu-id="7a49f-103">D3DXVec4Transform function (D3DX10Math.h)</span></span>

<span data-ttu-id="7a49f-104">依指定的矩陣轉換4D 向量。</span><span class="sxs-lookup"><span data-stu-id="7a49f-104">Transforms a 4D vector by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a49f-105">語法</span><span class="sxs-lookup"><span data-stu-id="7a49f-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4Transform(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="7a49f-106">參數</span><span class="sxs-lookup"><span data-stu-id="7a49f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a49f-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="7a49f-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7a49f-108">類型： **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="7a49f-108">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="7a49f-109">作業結果之 [**D3DXVECTOR4**](d3d10-d3dxvector4.md) 的指標。</span><span class="sxs-lookup"><span data-stu-id="7a49f-109">Pointer to the [**D3DXVECTOR4**](d3d10-d3dxvector4.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="7a49f-110">*pV* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7a49f-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a49f-111">Type： **Const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="7a49f-111">Type: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="7a49f-112">來源 D3DXVECTOR4 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="7a49f-112">Pointer to the source D3DXVECTOR4 structure.</span></span>

</dd> <dt>

<span data-ttu-id="7a49f-113">*pM* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7a49f-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a49f-114">Type： **Const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="7a49f-114">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="7a49f-115">來源 [**D3DXMATRIX**](d3d10-d3dxmatrix.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="7a49f-115">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a49f-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="7a49f-116">Return value</span></span>

<span data-ttu-id="7a49f-117">類型： **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="7a49f-117">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="7a49f-118">D3DXVECTOR4 結構的指標，此結構是轉換的4D 向量。</span><span class="sxs-lookup"><span data-stu-id="7a49f-118">Pointer to a D3DXVECTOR4 structure that is the transformed 4D vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a49f-119">備註</span><span class="sxs-lookup"><span data-stu-id="7a49f-119">Remarks</span></span>

<span data-ttu-id="7a49f-120">此函式的傳回值與不悅參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="7a49f-120">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="7a49f-121">如此一來，D3DXVec4Transform 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="7a49f-121">In this way, the D3DXVec4Transform function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a49f-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="7a49f-122">Requirements</span></span>



| <span data-ttu-id="7a49f-123">需求</span><span class="sxs-lookup"><span data-stu-id="7a49f-123">Requirement</span></span> | <span data-ttu-id="7a49f-124">值</span><span class="sxs-lookup"><span data-stu-id="7a49f-124">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7a49f-125">標頭</span><span class="sxs-lookup"><span data-stu-id="7a49f-125">Header</span></span><br/> | <dl> <span data-ttu-id="7a49f-126"><dt>D3DX10Math。h</dt></span><span class="sxs-lookup"><span data-stu-id="7a49f-126"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a49f-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7a49f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a49f-128">數學函數</span><span class="sxs-lookup"><span data-stu-id="7a49f-128">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
