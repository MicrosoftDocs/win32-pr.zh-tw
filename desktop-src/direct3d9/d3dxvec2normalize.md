---
description: 傳回2D 向量的正規化版本。
ms.assetid: 2796a5d1-cb1c-4093-87f2-a2ad43279d91
title: 'D3DXVec2Normalize 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2Normalize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ce3152c622c9083438d35c73b20e05ca2523efc2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104035345"
---
# <a name="d3dxvec2normalize-function-d3dx9mathh"></a><span data-ttu-id="6904c-103">D3DXVec2Normalize 函式 (D3dx9math) </span><span class="sxs-lookup"><span data-stu-id="6904c-103">D3DXVec2Normalize function (D3dx9math.h)</span></span>

<span data-ttu-id="6904c-104">傳回2D 向量的正規化版本。</span><span class="sxs-lookup"><span data-stu-id="6904c-104">Returns the normalized version of a 2D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="6904c-105">語法</span><span class="sxs-lookup"><span data-stu-id="6904c-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2Normalize(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV
);
```



## <a name="parameters"></a><span data-ttu-id="6904c-106">參數</span><span class="sxs-lookup"><span data-stu-id="6904c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6904c-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="6904c-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6904c-108">類型： **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="6904c-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="6904c-109">[**D3DXVECTOR2**](d3dxvector2.md)結構的指標，此結構是作業的結果。</span><span class="sxs-lookup"><span data-stu-id="6904c-109">Pointer to the [**D3DXVECTOR2**](d3dxvector2.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="6904c-110">*pV* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6904c-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6904c-111">Type： **Const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="6904c-111">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="6904c-112">來源 [**D3DXVECTOR2**](d3dxvector2.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="6904c-112">Pointer to the source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6904c-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="6904c-113">Return value</span></span>

<span data-ttu-id="6904c-114">類型： **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="6904c-114">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="6904c-115">[**D3DXVECTOR2**](d3dxvector2.md)結構的指標，此結構是向量的正規化版本。</span><span class="sxs-lookup"><span data-stu-id="6904c-115">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure that is the normalized version of the vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="6904c-116">備註</span><span class="sxs-lookup"><span data-stu-id="6904c-116">Remarks</span></span>

<span data-ttu-id="6904c-117">此函式的傳回值與 *不悅* 參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="6904c-117">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="6904c-118">如此一來， **D3DXVec2Normalize** 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="6904c-118">In this way, the **D3DXVec2Normalize** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="6904c-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="6904c-119">Requirements</span></span>



| <span data-ttu-id="6904c-120">需求</span><span class="sxs-lookup"><span data-stu-id="6904c-120">Requirement</span></span> | <span data-ttu-id="6904c-121">值</span><span class="sxs-lookup"><span data-stu-id="6904c-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6904c-122">標頭</span><span class="sxs-lookup"><span data-stu-id="6904c-122">Header</span></span><br/>  | <dl> <span data-ttu-id="6904c-123"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="6904c-123"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="6904c-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="6904c-124">Library</span></span><br/> | <dl> <span data-ttu-id="6904c-125"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="6904c-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6904c-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6904c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6904c-127">數學函數</span><span class="sxs-lookup"><span data-stu-id="6904c-127">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




