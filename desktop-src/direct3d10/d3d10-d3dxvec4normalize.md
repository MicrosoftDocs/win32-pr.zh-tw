---
description: 傳回4D 向量的正規化版本。
ms.assetid: ed3c48cf-4985-4ef3-b733-f8532e3ff6b5
title: 'D3DXVec4Normalize 函式 (D3DX10Math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Normalize
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: ebedbdddbe558bfad71520b64aa0cf2ff4c2f451
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323095"
---
# <a name="d3dxvec4normalize-function-d3dx10mathh"></a><span data-ttu-id="aaf87-103">D3DXVec4Normalize 函式 (D3DX10Math) </span><span class="sxs-lookup"><span data-stu-id="aaf87-103">D3DXVec4Normalize function (D3DX10Math.h)</span></span>

<span data-ttu-id="aaf87-104">傳回4D 向量的正規化版本。</span><span class="sxs-lookup"><span data-stu-id="aaf87-104">Returns the normalized version of a 4D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="aaf87-105">語法</span><span class="sxs-lookup"><span data-stu-id="aaf87-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4Normalize(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV
);
```



## <a name="parameters"></a><span data-ttu-id="aaf87-106">參數</span><span class="sxs-lookup"><span data-stu-id="aaf87-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aaf87-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="aaf87-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="aaf87-108">類型： **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="aaf87-108">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="aaf87-109">作業結果之 [**D3DXVECTOR4**](d3d10-d3dxvector4.md) 的指標。</span><span class="sxs-lookup"><span data-stu-id="aaf87-109">Pointer to the [**D3DXVECTOR4**](d3d10-d3dxvector4.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="aaf87-110">*pV* \[在\]</span><span class="sxs-lookup"><span data-stu-id="aaf87-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aaf87-111">Type： **Const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="aaf87-111">Type: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="aaf87-112">來源 D3DXVECTOR4 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="aaf87-112">Pointer to the source D3DXVECTOR4 structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aaf87-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="aaf87-113">Return value</span></span>

<span data-ttu-id="aaf87-114">類型： **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="aaf87-114">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="aaf87-115">D3DXVECTOR4 結構的指標，此結構是向量的正規化版本。</span><span class="sxs-lookup"><span data-stu-id="aaf87-115">Pointer to a D3DXVECTOR4 structure that is the normalized version of the vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="aaf87-116">備註</span><span class="sxs-lookup"><span data-stu-id="aaf87-116">Remarks</span></span>

<span data-ttu-id="aaf87-117">此函式的傳回值與不悅參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="aaf87-117">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="aaf87-118">如此一來，D3DXVec4Normalize 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="aaf87-118">In this way, the D3DXVec4Normalize function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="aaf87-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="aaf87-119">Requirements</span></span>



| <span data-ttu-id="aaf87-120">需求</span><span class="sxs-lookup"><span data-stu-id="aaf87-120">Requirement</span></span> | <span data-ttu-id="aaf87-121">值</span><span class="sxs-lookup"><span data-stu-id="aaf87-121">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aaf87-122">標頭</span><span class="sxs-lookup"><span data-stu-id="aaf87-122">Header</span></span><br/> | <dl> <span data-ttu-id="aaf87-123"><dt>D3DX10Math。h</dt></span><span class="sxs-lookup"><span data-stu-id="aaf87-123"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aaf87-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="aaf87-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aaf87-125">數學函數</span><span class="sxs-lookup"><span data-stu-id="aaf87-125">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
