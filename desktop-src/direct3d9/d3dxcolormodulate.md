---
description: 混合兩種色彩。
ms.assetid: deff70c7-2359-48b2-ab40-8c418acf5a07
title: 'D3DXColorModulate 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorModulate
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: cf9b202da786f6ec87ceca9816c2a4fc86776577
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196330"
---
# <a name="d3dxcolormodulate-function"></a><span data-ttu-id="edb0a-103">D3DXColorModulate 函式</span><span class="sxs-lookup"><span data-stu-id="edb0a-103">D3DXColorModulate function</span></span>

<span data-ttu-id="edb0a-104">混合兩種色彩。</span><span class="sxs-lookup"><span data-stu-id="edb0a-104">Blends two colors.</span></span>

## <a name="syntax"></a><span data-ttu-id="edb0a-105">語法</span><span class="sxs-lookup"><span data-stu-id="edb0a-105">Syntax</span></span>


```C++
D3DXCOLOR* D3DXColorModulate(
  _Inout_       D3DXCOLOR *pOut,
  _In_    const D3DXCOLOR *pC1,
  _In_    const D3DXCOLOR *pC2
);
```



## <a name="parameters"></a><span data-ttu-id="edb0a-106">參數</span><span class="sxs-lookup"><span data-stu-id="edb0a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="edb0a-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="edb0a-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="edb0a-108">類型： **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="edb0a-108">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="edb0a-109">[**D3DXCOLOR**](d3dxcolor.md)結構的指標，該結構為運算的結果。</span><span class="sxs-lookup"><span data-stu-id="edb0a-109">Pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="edb0a-110">*test-pc1* \[在\]</span><span class="sxs-lookup"><span data-stu-id="edb0a-110">*pC1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edb0a-111">Type： **Const [**D3DXCOLOR**](d3dxcolor.md) \***</span><span class="sxs-lookup"><span data-stu-id="edb0a-111">Type: **const [**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="edb0a-112">來源 [**D3DXCOLOR**](d3dxcolor.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="edb0a-112">Pointer to a source [**D3DXCOLOR**](d3dxcolor.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="edb0a-113">*pC2* \[在\]</span><span class="sxs-lookup"><span data-stu-id="edb0a-113">*pC2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edb0a-114">Type： **Const [**D3DXCOLOR**](d3dxcolor.md) \***</span><span class="sxs-lookup"><span data-stu-id="edb0a-114">Type: **const [**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="edb0a-115">來源 [**D3DXCOLOR**](d3dxcolor.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="edb0a-115">Pointer to a source [**D3DXCOLOR**](d3dxcolor.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="edb0a-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="edb0a-116">Return value</span></span>

<span data-ttu-id="edb0a-117">類型： **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="edb0a-117">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="edb0a-118">此函式會傳回 [**D3DXCOLOR**](d3dxcolor.md) 結構的指標，此結構是混合作業的結果。</span><span class="sxs-lookup"><span data-stu-id="edb0a-118">This function returns a pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the result of the blending operation.</span></span>

## <a name="remarks"></a><span data-ttu-id="edb0a-119">備註</span><span class="sxs-lookup"><span data-stu-id="edb0a-119">Remarks</span></span>

<span data-ttu-id="edb0a-120">此函式的傳回值與不悅參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="edb0a-120">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="edb0a-121">如此一來， **D3DXColorModulate** 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="edb0a-121">In this way, the **D3DXColorModulate** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="edb0a-122">此函式會藉由將相符的色彩元件相乘來將兩個色彩混合在一起，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="edb0a-122">This function blends together two colors by multiplying matching color components, as shown in the following example.</span></span>


```
pOut->r = pC1->r * pC2->r;
```



## <a name="requirements"></a><span data-ttu-id="edb0a-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="edb0a-123">Requirements</span></span>



| <span data-ttu-id="edb0a-124">需求</span><span class="sxs-lookup"><span data-stu-id="edb0a-124">Requirement</span></span> | <span data-ttu-id="edb0a-125">值</span><span class="sxs-lookup"><span data-stu-id="edb0a-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="edb0a-126">標頭</span><span class="sxs-lookup"><span data-stu-id="edb0a-126">Header</span></span><br/>  | <dl> <span data-ttu-id="edb0a-127"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="edb0a-127"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="edb0a-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="edb0a-128">Library</span></span><br/> | <dl> <span data-ttu-id="edb0a-129"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="edb0a-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="edb0a-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="edb0a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edb0a-131">數學函數</span><span class="sxs-lookup"><span data-stu-id="edb0a-131">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="edb0a-132">**D3DXColorLerp**</span><span class="sxs-lookup"><span data-stu-id="edb0a-132">**D3DXColorLerp**</span></span>](d3dxcolorlerp.md)
</dt> <dt>

[<span data-ttu-id="edb0a-133">**D3DXColorNegative**</span><span class="sxs-lookup"><span data-stu-id="edb0a-133">**D3DXColorNegative**</span></span>](d3dxcolornegative.md)
</dt> <dt>

[<span data-ttu-id="edb0a-134">**D3DXColorScale**</span><span class="sxs-lookup"><span data-stu-id="edb0a-134">**D3DXColorScale**</span></span>](d3dxcolorscale.md)
</dt> </dl>

 

 




