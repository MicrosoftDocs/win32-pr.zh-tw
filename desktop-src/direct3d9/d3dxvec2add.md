---
description: 加入兩個2D 向量。
ms.assetid: 82b2fdf6-1b1f-4768-8c0b-ac8faa77d7ed
title: 'D3DXVec2Add 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2Add
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5087177448b01763bd94acb9b50c27c6cdf38815
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946078"
---
# <a name="d3dxvec2add-function"></a><span data-ttu-id="7b47b-103">D3DXVec2Add 函式</span><span class="sxs-lookup"><span data-stu-id="7b47b-103">D3DXVec2Add function</span></span>

<span data-ttu-id="7b47b-104">加入兩個2D 向量。</span><span class="sxs-lookup"><span data-stu-id="7b47b-104">Adds two 2D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b47b-105">語法</span><span class="sxs-lookup"><span data-stu-id="7b47b-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2Add(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV1,
  _In_    const D3DXVECTOR2 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="7b47b-106">參數</span><span class="sxs-lookup"><span data-stu-id="7b47b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b47b-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="7b47b-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7b47b-108">類型： **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="7b47b-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="7b47b-109">[**D3DXVECTOR2**](d3dxvector2.md)結構的指標，此結構是作業的結果。</span><span class="sxs-lookup"><span data-stu-id="7b47b-109">Pointer to the [**D3DXVECTOR2**](d3dxvector2.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="7b47b-110">*pV1* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7b47b-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b47b-111">Type： **Const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="7b47b-111">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="7b47b-112">來源 [**D3DXVECTOR2**](d3dxvector2.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="7b47b-112">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="7b47b-113">*pV2* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7b47b-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b47b-114">Type： **Const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="7b47b-114">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="7b47b-115">來源 [**D3DXVECTOR2**](d3dxvector2.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="7b47b-115">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b47b-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="7b47b-116">Return value</span></span>

<span data-ttu-id="7b47b-117">類型： **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="7b47b-117">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="7b47b-118">[**D3DXVECTOR2**](d3dxvector2.md)結構的指標，這是兩個向量的總和。</span><span class="sxs-lookup"><span data-stu-id="7b47b-118">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure that is the sum of the two vectors.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b47b-119">備註</span><span class="sxs-lookup"><span data-stu-id="7b47b-119">Remarks</span></span>

<span data-ttu-id="7b47b-120">此函式的傳回值與 *不悅* 參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="7b47b-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="7b47b-121">如此一來， **D3DXVec2Add** 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="7b47b-121">In this way, the **D3DXVec2Add** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b47b-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="7b47b-122">Requirements</span></span>



| <span data-ttu-id="7b47b-123">需求</span><span class="sxs-lookup"><span data-stu-id="7b47b-123">Requirement</span></span> | <span data-ttu-id="7b47b-124">值</span><span class="sxs-lookup"><span data-stu-id="7b47b-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7b47b-125">標頭</span><span class="sxs-lookup"><span data-stu-id="7b47b-125">Header</span></span><br/>  | <dl> <span data-ttu-id="7b47b-126"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="7b47b-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="7b47b-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="7b47b-127">Library</span></span><br/> | <dl> <span data-ttu-id="7b47b-128"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="7b47b-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7b47b-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7b47b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b47b-130">數學函數</span><span class="sxs-lookup"><span data-stu-id="7b47b-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="7b47b-131">**D3DXVec2Subtract**</span><span class="sxs-lookup"><span data-stu-id="7b47b-131">**D3DXVec2Subtract**</span></span>](d3dxvec2subtract.md)
</dt> <dt>

[<span data-ttu-id="7b47b-132">**D3DXVec2Scale**</span><span class="sxs-lookup"><span data-stu-id="7b47b-132">**D3DXVec2Scale**</span></span>](d3dxvec2scale.md)
</dt> </dl>

 

 




