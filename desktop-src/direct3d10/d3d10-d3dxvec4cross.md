---
description: 判斷四個維度中的交叉乘積。
ms.assetid: 4f728fbd-cf5a-4d2e-ba4f-487616d83f6d
title: 'D3DXVec4Cross 函式 (D3DX10Math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Cross
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 8e3e2a612740a207ea4dc44243ce24ebbab7fc08
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106988610"
---
# <a name="d3dxvec4cross-function-d3dx10mathh"></a><span data-ttu-id="b9a53-103">D3DXVec4Cross 函式 (D3DX10Math) </span><span class="sxs-lookup"><span data-stu-id="b9a53-103">D3DXVec4Cross function (D3DX10Math.h)</span></span>

<span data-ttu-id="b9a53-104">判斷四個維度中的交叉乘積。</span><span class="sxs-lookup"><span data-stu-id="b9a53-104">Determines the cross-product in four dimensions.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9a53-105">語法</span><span class="sxs-lookup"><span data-stu-id="b9a53-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4Cross(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV1,
  _In_    const D3DXVECTOR4 *pV2,
  _In_    const D3DXVECTOR4 *pV3
);
```



## <a name="parameters"></a><span data-ttu-id="b9a53-106">參數</span><span class="sxs-lookup"><span data-stu-id="b9a53-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9a53-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="b9a53-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b9a53-108">類型： **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="b9a53-108">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="b9a53-109">作業結果之 [**D3DXVECTOR4**](d3d10-d3dxvector4.md) 的指標。</span><span class="sxs-lookup"><span data-stu-id="b9a53-109">Pointer to the [**D3DXVECTOR4**](d3d10-d3dxvector4.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="b9a53-110">*pV1* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b9a53-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9a53-111">Type： **Const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="b9a53-111">Type: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="b9a53-112">來源 D3DXVECTOR4 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="b9a53-112">Pointer to a source D3DXVECTOR4 structure.</span></span>

</dd> <dt>

<span data-ttu-id="b9a53-113">*pV2* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b9a53-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9a53-114">Type： **Const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="b9a53-114">Type: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="b9a53-115">來源 D3DXVECTOR4 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="b9a53-115">Pointer to a source D3DXVECTOR4 structure.</span></span>

</dd> <dt>

<span data-ttu-id="b9a53-116">*pV3* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b9a53-116">*pV3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9a53-117">Type： **Const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="b9a53-117">Type: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="b9a53-118">來源 D3DXVECTOR4 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="b9a53-118">Pointer to a source D3DXVECTOR4 structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9a53-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="b9a53-119">Return value</span></span>

<span data-ttu-id="b9a53-120">類型： **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="b9a53-120">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="b9a53-121">D3DXVECTOR4 結構的指標，該結構為交叉乘積。</span><span class="sxs-lookup"><span data-stu-id="b9a53-121">Pointer to a D3DXVECTOR4 structure that is the cross product.</span></span>

## <a name="remarks"></a><span data-ttu-id="b9a53-122">備註</span><span class="sxs-lookup"><span data-stu-id="b9a53-122">Remarks</span></span>

<span data-ttu-id="b9a53-123">此函式的傳回值與不悅參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="b9a53-123">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="b9a53-124">如此一來，D3DXVec4Cross 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="b9a53-124">In this way, the D3DXVec4Cross function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9a53-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="b9a53-125">Requirements</span></span>



| <span data-ttu-id="b9a53-126">需求</span><span class="sxs-lookup"><span data-stu-id="b9a53-126">Requirement</span></span> | <span data-ttu-id="b9a53-127">值</span><span class="sxs-lookup"><span data-stu-id="b9a53-127">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b9a53-128">標頭</span><span class="sxs-lookup"><span data-stu-id="b9a53-128">Header</span></span><br/> | <dl> <span data-ttu-id="b9a53-129"><dt>D3DX10Math。h</dt></span><span class="sxs-lookup"><span data-stu-id="b9a53-129"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9a53-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b9a53-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9a53-131">數學函數</span><span class="sxs-lookup"><span data-stu-id="b9a53-131">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
