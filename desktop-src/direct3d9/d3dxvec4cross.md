---
description: 判斷四個維度中的交叉乘積。
ms.assetid: 10b965c9-7ed7-450c-86a0-114f068c888f
title: 'D3DXVec4Cross 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Cross
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 91e6e5662bff503ba96d96f135f98e60cf15c8fe
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196296"
---
# <a name="d3dxvec4cross-function-d3dx9mathh"></a><span data-ttu-id="4d008-103">D3DXVec4Cross 函式 (D3dx9math) </span><span class="sxs-lookup"><span data-stu-id="4d008-103">D3DXVec4Cross function (D3dx9math.h)</span></span>

<span data-ttu-id="4d008-104">判斷四個維度中的交叉乘積。</span><span class="sxs-lookup"><span data-stu-id="4d008-104">Determines the cross-product in four dimensions.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d008-105">語法</span><span class="sxs-lookup"><span data-stu-id="4d008-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4Cross(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV1,
  _In_    const D3DXVECTOR4 *pV2,
  _In_    const D3DXVECTOR4 *pV3
);
```



## <a name="parameters"></a><span data-ttu-id="4d008-106">參數</span><span class="sxs-lookup"><span data-stu-id="4d008-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d008-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="4d008-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4d008-108">類型： **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="4d008-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="4d008-109">[**D3DXVECTOR4**](d3dxvector4.md)結構的指標，此結構是作業的結果。</span><span class="sxs-lookup"><span data-stu-id="4d008-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="4d008-110">*pV1* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4d008-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d008-111">Type： **Const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="4d008-111">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="4d008-112">來源 [**D3DXVECTOR4**](d3dxvector4.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="4d008-112">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="4d008-113">*pV2* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4d008-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d008-114">Type： **Const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="4d008-114">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="4d008-115">來源 [**D3DXVECTOR4**](d3dxvector4.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="4d008-115">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="4d008-116">*pV3* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4d008-116">*pV3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d008-117">Type： **Const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="4d008-117">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="4d008-118">來源 [**D3DXVECTOR4**](d3dxvector4.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="4d008-118">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d008-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="4d008-119">Return value</span></span>

<span data-ttu-id="4d008-120">類型： **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="4d008-120">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="4d008-121">[**D3DXVECTOR4**](d3dxvector4.md)結構的指標，該結構為交叉乘積。</span><span class="sxs-lookup"><span data-stu-id="4d008-121">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure that is the cross product.</span></span>

## <a name="remarks"></a><span data-ttu-id="4d008-122">備註</span><span class="sxs-lookup"><span data-stu-id="4d008-122">Remarks</span></span>

<span data-ttu-id="4d008-123">此函式的傳回值與 *不悅* 參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="4d008-123">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="4d008-124">如此一來， **D3DXVec4Cross** 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="4d008-124">In this way, the **D3DXVec4Cross** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d008-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="4d008-125">Requirements</span></span>



| <span data-ttu-id="4d008-126">需求</span><span class="sxs-lookup"><span data-stu-id="4d008-126">Requirement</span></span> | <span data-ttu-id="4d008-127">值</span><span class="sxs-lookup"><span data-stu-id="4d008-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4d008-128">標頭</span><span class="sxs-lookup"><span data-stu-id="4d008-128">Header</span></span><br/>  | <dl> <span data-ttu-id="4d008-129"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="4d008-129"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="4d008-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="4d008-130">Library</span></span><br/> | <dl> <span data-ttu-id="4d008-131"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="4d008-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4d008-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4d008-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d008-133">數學函數</span><span class="sxs-lookup"><span data-stu-id="4d008-133">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="4d008-134">**D3DXVec4Dot**</span><span class="sxs-lookup"><span data-stu-id="4d008-134">**D3DXVec4Dot**</span></span>](d3dxvec4dot.md)
</dt> </dl>

 

 




