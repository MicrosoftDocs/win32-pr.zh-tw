---
description: 傳回2D 向量的正規化版本。
ms.assetid: fac4f269-2778-4500-af9e-23a0112543b0
title: 'D3DXVec2Normalize 函式 (D3DX10Math) '
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: e2894a86c0aa0c2ef6b45a41664b2d0cca1427c1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103854051"
---
# <a name="d3dxvec2normalize-function-d3dx10mathh"></a><span data-ttu-id="ab137-103">D3DXVec2Normalize 函式 (D3DX10Math) </span><span class="sxs-lookup"><span data-stu-id="ab137-103">D3DXVec2Normalize function (D3DX10Math.h)</span></span>

<span data-ttu-id="ab137-104">傳回2D 向量的正規化版本。</span><span class="sxs-lookup"><span data-stu-id="ab137-104">Returns the normalized version of a 2D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab137-105">語法</span><span class="sxs-lookup"><span data-stu-id="ab137-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2Normalize(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV
);
```



## <a name="parameters"></a><span data-ttu-id="ab137-106">參數</span><span class="sxs-lookup"><span data-stu-id="ab137-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab137-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="ab137-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ab137-108">類型： **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="ab137-108">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="ab137-109">作業結果之 [**D3DXVECTOR2**](d3d10-d3dxvector2.md) 的指標。</span><span class="sxs-lookup"><span data-stu-id="ab137-109">Pointer to the [**D3DXVECTOR2**](d3d10-d3dxvector2.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="ab137-110">*pV* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ab137-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab137-111">Type： **Const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="ab137-111">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="ab137-112">來源 D3DXVECTOR2 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="ab137-112">Pointer to the source D3DXVECTOR2 structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab137-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="ab137-113">Return value</span></span>

<span data-ttu-id="ab137-114">類型： **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="ab137-114">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="ab137-115">D3DXVECTOR2 結構的指標，此結構是向量的正規化版本。</span><span class="sxs-lookup"><span data-stu-id="ab137-115">Pointer to a D3DXVECTOR2 structure that is the normalized version of the vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab137-116">備註</span><span class="sxs-lookup"><span data-stu-id="ab137-116">Remarks</span></span>

<span data-ttu-id="ab137-117">此函式的傳回值與不悅參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="ab137-117">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="ab137-118">如此一來，D3DXVec2Normalize 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="ab137-118">In this way, the D3DXVec2Normalize function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab137-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="ab137-119">Requirements</span></span>



| <span data-ttu-id="ab137-120">需求</span><span class="sxs-lookup"><span data-stu-id="ab137-120">Requirement</span></span> | <span data-ttu-id="ab137-121">值</span><span class="sxs-lookup"><span data-stu-id="ab137-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ab137-122">標頭</span><span class="sxs-lookup"><span data-stu-id="ab137-122">Header</span></span><br/>  | <dl> <span data-ttu-id="ab137-123"><dt>D3DX10Math。h</dt></span><span class="sxs-lookup"><span data-stu-id="ab137-123"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="ab137-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="ab137-124">Library</span></span><br/> | <dl> <span data-ttu-id="ab137-125"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="ab137-125"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ab137-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ab137-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab137-127">數學函數</span><span class="sxs-lookup"><span data-stu-id="ab137-127">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
