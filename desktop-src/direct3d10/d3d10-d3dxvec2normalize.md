---
description: D3DXVec2Normalize 函式 (D3DX10Math) -傳回2D 向量的正規化版本。
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
ms.openlocfilehash: aaa7bde759b9023b69204d6cb39259f0905b9928
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108386"
---
# <a name="d3dxvec2normalize-function-d3dx10mathh"></a><span data-ttu-id="9a9dd-103">D3DXVec2Normalize 函式 (D3DX10Math) </span><span class="sxs-lookup"><span data-stu-id="9a9dd-103">D3DXVec2Normalize function (D3DX10Math.h)</span></span>

<span data-ttu-id="9a9dd-104">傳回2D 向量的正規化版本。</span><span class="sxs-lookup"><span data-stu-id="9a9dd-104">Returns the normalized version of a 2D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a9dd-105">語法</span><span class="sxs-lookup"><span data-stu-id="9a9dd-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2Normalize(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV
);
```



## <a name="parameters"></a><span data-ttu-id="9a9dd-106">參數</span><span class="sxs-lookup"><span data-stu-id="9a9dd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a9dd-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="9a9dd-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="9a9dd-108">類型： **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="9a9dd-108">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="9a9dd-109">作業結果之 [**D3DXVECTOR2**](d3d10-d3dxvector2.md) 的指標。</span><span class="sxs-lookup"><span data-stu-id="9a9dd-109">Pointer to the [**D3DXVECTOR2**](d3d10-d3dxvector2.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="9a9dd-110">*pV* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9a9dd-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a9dd-111">Type： **Const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="9a9dd-111">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="9a9dd-112">來源 D3DXVECTOR2 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="9a9dd-112">Pointer to the source D3DXVECTOR2 structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a9dd-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="9a9dd-113">Return value</span></span>

<span data-ttu-id="9a9dd-114">類型： **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="9a9dd-114">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="9a9dd-115">D3DXVECTOR2 結構的指標，此結構是向量的正規化版本。</span><span class="sxs-lookup"><span data-stu-id="9a9dd-115">Pointer to a D3DXVECTOR2 structure that is the normalized version of the vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a9dd-116">備註</span><span class="sxs-lookup"><span data-stu-id="9a9dd-116">Remarks</span></span>

<span data-ttu-id="9a9dd-117">此函式的傳回值與不悅參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="9a9dd-117">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="9a9dd-118">如此一來，D3DXVec2Normalize 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="9a9dd-118">In this way, the D3DXVec2Normalize function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a9dd-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="9a9dd-119">Requirements</span></span>



| <span data-ttu-id="9a9dd-120">需求</span><span class="sxs-lookup"><span data-stu-id="9a9dd-120">Requirement</span></span> | <span data-ttu-id="9a9dd-121">值</span><span class="sxs-lookup"><span data-stu-id="9a9dd-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9a9dd-122">標頭</span><span class="sxs-lookup"><span data-stu-id="9a9dd-122">Header</span></span><br/>  | <dl> <span data-ttu-id="9a9dd-123"><dt>D3DX10Math。h</dt></span><span class="sxs-lookup"><span data-stu-id="9a9dd-123"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="9a9dd-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="9a9dd-124">Library</span></span><br/> | <dl> <span data-ttu-id="9a9dd-125"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="9a9dd-125"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9a9dd-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9a9dd-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a9dd-127">數學函數</span><span class="sxs-lookup"><span data-stu-id="9a9dd-127">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
