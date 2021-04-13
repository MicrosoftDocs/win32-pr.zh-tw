---
description: 依指定的矩陣轉換2D 向量。
ms.assetid: 4b57eb7f-fae9-48ac-a806-510da75d25a6
title: 'D3DXVec2Transform 函式 (D3DX10Math) '
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 513623e0004d8ede1fc2d142b2c7f8a7c226d5e4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104386465"
---
# <a name="d3dxvec2transform-function-d3dx10mathh"></a><span data-ttu-id="c8732-103">D3DXVec2Transform 函式 (D3DX10Math) </span><span class="sxs-lookup"><span data-stu-id="c8732-103">D3DXVec2Transform function (D3DX10Math.h)</span></span>

<span data-ttu-id="c8732-104">依指定的矩陣轉換2D 向量。</span><span class="sxs-lookup"><span data-stu-id="c8732-104">Transforms a 2D vector by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8732-105">語法</span><span class="sxs-lookup"><span data-stu-id="c8732-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec2Transform(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR2 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="c8732-106">參數</span><span class="sxs-lookup"><span data-stu-id="c8732-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8732-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="c8732-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c8732-108">類型： **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="c8732-108">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="c8732-109">[**D3DXVECTOR4**](d3d10-d3dxvector4.md)結構的指標，此結構是作業的結果。</span><span class="sxs-lookup"><span data-stu-id="c8732-109">Pointer to the [**D3DXVECTOR4**](d3d10-d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="c8732-110">*pV* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c8732-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8732-111">Type： **Const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="c8732-111">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="c8732-112">來源 [**D3DXVECTOR2**](d3d10-d3dxvector2.md)的指標。</span><span class="sxs-lookup"><span data-stu-id="c8732-112">Pointer to the source [**D3DXVECTOR2**](d3d10-d3dxvector2.md).</span></span>

</dd> <dt>

<span data-ttu-id="c8732-113">*pM* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c8732-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8732-114">Type： **Const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="c8732-114">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="c8732-115">來源 [**D3DXMATRIX**](d3d10-d3dxmatrix.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="c8732-115">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8732-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="c8732-116">Return value</span></span>

<span data-ttu-id="c8732-117">類型： **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="c8732-117">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="c8732-118">D3DXVECTOR4 結構的指標，此結構是已轉換的向量。</span><span class="sxs-lookup"><span data-stu-id="c8732-118">Pointer to a D3DXVECTOR4 structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8732-119">備註</span><span class="sxs-lookup"><span data-stu-id="c8732-119">Remarks</span></span>

<span data-ttu-id="c8732-120">此函式會將向量 pV (x、y、0、1) 由矩陣 pM 進行轉換。</span><span class="sxs-lookup"><span data-stu-id="c8732-120">This function transforms the vector pV (x, y, 0, 1) by the matrix pM.</span></span>

<span data-ttu-id="c8732-121">此函式的傳回值與不悅參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="c8732-121">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="c8732-122">如此一來，D3DXVec2Transform 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="c8732-122">In this way, the D3DXVec2Transform function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8732-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="c8732-123">Requirements</span></span>



| <span data-ttu-id="c8732-124">需求</span><span class="sxs-lookup"><span data-stu-id="c8732-124">Requirement</span></span> | <span data-ttu-id="c8732-125">值</span><span class="sxs-lookup"><span data-stu-id="c8732-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c8732-126">標頭</span><span class="sxs-lookup"><span data-stu-id="c8732-126">Header</span></span><br/>  | <dl> <span data-ttu-id="c8732-127"><dt>D3DX10Math。h</dt></span><span class="sxs-lookup"><span data-stu-id="c8732-127"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="c8732-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="c8732-128">Library</span></span><br/> | <dl> <span data-ttu-id="c8732-129"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="c8732-129"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c8732-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c8732-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8732-131">數學函數</span><span class="sxs-lookup"><span data-stu-id="c8732-131">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
