---
description: 減去兩個色彩值以建立新的色彩值。
ms.assetid: c21f8402-c1c2-4909-896f-2872ef518537
title: 'D3DXColorSubtract 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorSubtract
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 47f28ea3a3fb6d1556e699fed3820e228faf6604
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106988191"
---
# <a name="d3dxcolorsubtract-function"></a><span data-ttu-id="2df97-103">D3DXColorSubtract 函式</span><span class="sxs-lookup"><span data-stu-id="2df97-103">D3DXColorSubtract function</span></span>

<span data-ttu-id="2df97-104">減去兩個色彩值以建立新的色彩值。</span><span class="sxs-lookup"><span data-stu-id="2df97-104">Subtracts two color values to create a new color value.</span></span>

## <a name="syntax"></a><span data-ttu-id="2df97-105">語法</span><span class="sxs-lookup"><span data-stu-id="2df97-105">Syntax</span></span>


```C++
D3DXCOLOR* D3DXColorSubtract(
  _Inout_       D3DXCOLOR *pOut,
  _In_    const D3DXCOLOR *pC1,
  _In_    const D3DXCOLOR *pC2
);
```



## <a name="parameters"></a><span data-ttu-id="2df97-106">參數</span><span class="sxs-lookup"><span data-stu-id="2df97-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2df97-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="2df97-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2df97-108">類型： **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="2df97-108">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="2df97-109">[**D3DXCOLOR**](d3dxcolor.md)結構的指標，該結構為運算的結果。</span><span class="sxs-lookup"><span data-stu-id="2df97-109">Pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="2df97-110">*test-pc1* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2df97-110">*pC1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2df97-111">Type： **Const [**D3DXCOLOR**](d3dxcolor.md) \***</span><span class="sxs-lookup"><span data-stu-id="2df97-111">Type: **const [**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="2df97-112">來源 [**D3DXCOLOR**](d3dxcolor.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="2df97-112">Pointer to a source [**D3DXCOLOR**](d3dxcolor.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="2df97-113">*pC2* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2df97-113">*pC2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2df97-114">Type： **Const [**D3DXCOLOR**](d3dxcolor.md) \***</span><span class="sxs-lookup"><span data-stu-id="2df97-114">Type: **const [**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="2df97-115">來源 [**D3DXCOLOR**](d3dxcolor.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="2df97-115">Pointer to a source [**D3DXCOLOR**](d3dxcolor.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2df97-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="2df97-116">Return value</span></span>

<span data-ttu-id="2df97-117">類型： **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="2df97-117">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="2df97-118">此函式會傳回 [**D3DXCOLOR**](d3dxcolor.md) 結構的指標，這是兩個色彩值之間的差異。</span><span class="sxs-lookup"><span data-stu-id="2df97-118">This function returns a pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the difference between two color values.</span></span>

## <a name="remarks"></a><span data-ttu-id="2df97-119">備註</span><span class="sxs-lookup"><span data-stu-id="2df97-119">Remarks</span></span>

<span data-ttu-id="2df97-120">此函式的傳回值與不悅參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="2df97-120">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="2df97-121">如此一來， **D3DXColorSubtract** 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="2df97-121">In this way, the **D3DXColorSubtract** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="2df97-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="2df97-122">Requirements</span></span>



| <span data-ttu-id="2df97-123">需求</span><span class="sxs-lookup"><span data-stu-id="2df97-123">Requirement</span></span> | <span data-ttu-id="2df97-124">值</span><span class="sxs-lookup"><span data-stu-id="2df97-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2df97-125">標頭</span><span class="sxs-lookup"><span data-stu-id="2df97-125">Header</span></span><br/>  | <dl> <span data-ttu-id="2df97-126"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="2df97-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="2df97-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="2df97-127">Library</span></span><br/> | <dl> <span data-ttu-id="2df97-128"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="2df97-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2df97-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2df97-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2df97-130">數學函數</span><span class="sxs-lookup"><span data-stu-id="2df97-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="2df97-131">**D3DXColorAdd**</span><span class="sxs-lookup"><span data-stu-id="2df97-131">**D3DXColorAdd**</span></span>](d3dxcoloradd.md)
</dt> </dl>

 

 




