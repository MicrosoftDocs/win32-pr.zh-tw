---
description: 傳回由兩個4D 向量的最小元件組成的4D 向量。
ms.assetid: ae3819a3-a5b6-47c2-b789-3e3f07db9f03
title: 'D3DXVec4Minimize 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Minimize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9ccd4806bfa368fafa481500d3bd28e0ff55b7d2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106992321"
---
# <a name="d3dxvec4minimize-function"></a><span data-ttu-id="550df-103">D3DXVec4Minimize 函式</span><span class="sxs-lookup"><span data-stu-id="550df-103">D3DXVec4Minimize function</span></span>

<span data-ttu-id="550df-104">傳回由兩個4D 向量的最小元件組成的4D 向量。</span><span class="sxs-lookup"><span data-stu-id="550df-104">Returns a 4D vector that is made up of the smallest components of two 4D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="550df-105">語法</span><span class="sxs-lookup"><span data-stu-id="550df-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4Minimize(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV1,
  _In_    const D3DXVECTOR4 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="550df-106">參數</span><span class="sxs-lookup"><span data-stu-id="550df-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="550df-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="550df-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="550df-108">類型： **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="550df-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="550df-109">[**D3DXVECTOR4**](d3dxvector4.md)結構的指標，此結構是作業的結果。</span><span class="sxs-lookup"><span data-stu-id="550df-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="550df-110">*pV1* \[在\]</span><span class="sxs-lookup"><span data-stu-id="550df-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="550df-111">Type： **Const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="550df-111">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="550df-112">來源 [**D3DXVECTOR4**](d3dxvector4.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="550df-112">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="550df-113">*pV2* \[在\]</span><span class="sxs-lookup"><span data-stu-id="550df-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="550df-114">Type： **Const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="550df-114">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="550df-115">來源 [**D3DXVECTOR4**](d3dxvector4.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="550df-115">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="550df-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="550df-116">Return value</span></span>

<span data-ttu-id="550df-117">類型： **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="550df-117">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="550df-118">[**D3DXVECTOR4**](d3dxvector4.md)結構的指標，此結構是由兩個向量的最小元件所組成。</span><span class="sxs-lookup"><span data-stu-id="550df-118">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure that is made up of the smallest components of the two vectors.</span></span>

## <a name="remarks"></a><span data-ttu-id="550df-119">備註</span><span class="sxs-lookup"><span data-stu-id="550df-119">Remarks</span></span>

<span data-ttu-id="550df-120">此函式的傳回值與 *不悅* 參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="550df-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="550df-121">如此一來， **D3DXVec4Minimize** 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="550df-121">In this way, the **D3DXVec4Minimize** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="550df-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="550df-122">Requirements</span></span>



| <span data-ttu-id="550df-123">需求</span><span class="sxs-lookup"><span data-stu-id="550df-123">Requirement</span></span> | <span data-ttu-id="550df-124">值</span><span class="sxs-lookup"><span data-stu-id="550df-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="550df-125">標頭</span><span class="sxs-lookup"><span data-stu-id="550df-125">Header</span></span><br/>  | <dl> <span data-ttu-id="550df-126"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="550df-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="550df-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="550df-127">Library</span></span><br/> | <dl> <span data-ttu-id="550df-128"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="550df-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="550df-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="550df-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="550df-130">數學函數</span><span class="sxs-lookup"><span data-stu-id="550df-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="550df-131">**D3DXVec4Maximize**</span><span class="sxs-lookup"><span data-stu-id="550df-131">**D3DXVec4Maximize**</span></span>](d3dxvec4maximize.md)
</dt> </dl>

 

 




