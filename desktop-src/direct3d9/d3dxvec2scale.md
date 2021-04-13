---
description: 調整2D 向量。
ms.assetid: 1887bc48-3766-42d7-840b-1e29d78db4ce
title: 'D3DXVec2Scale 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2Scale
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 941e85763b15724e3c810c0416b5b142c9d95913
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322816"
---
# <a name="d3dxvec2scale-function"></a><span data-ttu-id="9a7b2-103">D3DXVec2Scale 函式</span><span class="sxs-lookup"><span data-stu-id="9a7b2-103">D3DXVec2Scale function</span></span>

<span data-ttu-id="9a7b2-104">調整2D 向量。</span><span class="sxs-lookup"><span data-stu-id="9a7b2-104">Scales a 2D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a7b2-105">語法</span><span class="sxs-lookup"><span data-stu-id="9a7b2-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2Scale(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV,
  _In_          FLOAT       s
);
```



## <a name="parameters"></a><span data-ttu-id="9a7b2-106">參數</span><span class="sxs-lookup"><span data-stu-id="9a7b2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a7b2-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="9a7b2-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="9a7b2-108">類型： **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="9a7b2-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="9a7b2-109">[**D3DXVECTOR2**](d3dxvector2.md)結構的指標，此結構是作業的結果。</span><span class="sxs-lookup"><span data-stu-id="9a7b2-109">Pointer to the [**D3DXVECTOR2**](d3dxvector2.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="9a7b2-110">*pV* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9a7b2-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a7b2-111">Type： **Const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="9a7b2-111">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="9a7b2-112">來源 [**D3DXVECTOR2**](d3dxvector2.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="9a7b2-112">Pointer to the source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="9a7b2-113"> \[ 中的 s\]</span><span class="sxs-lookup"><span data-stu-id="9a7b2-113">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a7b2-114">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9a7b2-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9a7b2-115">調整值。</span><span class="sxs-lookup"><span data-stu-id="9a7b2-115">Scaling value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a7b2-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="9a7b2-116">Return value</span></span>

<span data-ttu-id="9a7b2-117">類型： **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="9a7b2-117">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="9a7b2-118">[**D3DXVECTOR2**](d3dxvector2.md)結構的指標，此結構是縮放向量。</span><span class="sxs-lookup"><span data-stu-id="9a7b2-118">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure that is the scaled vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a7b2-119">備註</span><span class="sxs-lookup"><span data-stu-id="9a7b2-119">Remarks</span></span>

<span data-ttu-id="9a7b2-120">此函式的傳回值與 *不悅* 參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="9a7b2-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="9a7b2-121">如此一來， **D3DXVec2Scale** 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="9a7b2-121">In this way, the **D3DXVec2Scale** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a7b2-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="9a7b2-122">Requirements</span></span>



| <span data-ttu-id="9a7b2-123">需求</span><span class="sxs-lookup"><span data-stu-id="9a7b2-123">Requirement</span></span> | <span data-ttu-id="9a7b2-124">值</span><span class="sxs-lookup"><span data-stu-id="9a7b2-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9a7b2-125">標頭</span><span class="sxs-lookup"><span data-stu-id="9a7b2-125">Header</span></span><br/>  | <dl> <span data-ttu-id="9a7b2-126"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="9a7b2-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="9a7b2-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="9a7b2-127">Library</span></span><br/> | <dl> <span data-ttu-id="9a7b2-128"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="9a7b2-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9a7b2-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9a7b2-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a7b2-130">數學函數</span><span class="sxs-lookup"><span data-stu-id="9a7b2-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="9a7b2-131">**D3DXVec2Add**</span><span class="sxs-lookup"><span data-stu-id="9a7b2-131">**D3DXVec2Add**</span></span>](d3dxvec2add.md)
</dt> <dt>

[<span data-ttu-id="9a7b2-132">**D3DXVec2Subtract**</span><span class="sxs-lookup"><span data-stu-id="9a7b2-132">**D3DXVec2Subtract**</span></span>](d3dxvec2subtract.md)
</dt> </dl>

 

 
