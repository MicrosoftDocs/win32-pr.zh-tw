---
description: 建立色彩值的負值色彩值。
ms.assetid: 74143126-93f8-49fa-abe3-fd730b644d87
title: 'D3DXColorNegative 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorNegative
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a6d4d8559e64580897aec5261c450dc739496e75
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106992535"
---
# <a name="d3dxcolornegative-function"></a><span data-ttu-id="85565-103">D3DXColorNegative 函式</span><span class="sxs-lookup"><span data-stu-id="85565-103">D3DXColorNegative function</span></span>

<span data-ttu-id="85565-104">建立色彩值的負值色彩值。</span><span class="sxs-lookup"><span data-stu-id="85565-104">Creates the negative color value of a color value.</span></span>

## <a name="syntax"></a><span data-ttu-id="85565-105">語法</span><span class="sxs-lookup"><span data-stu-id="85565-105">Syntax</span></span>


```C++
D3DXCOLOR* D3DXColorNegative(
  _Inout_       D3DXCOLOR *pOut,
  _In_    const D3DXCOLOR *pC
);
```



## <a name="parameters"></a><span data-ttu-id="85565-106">參數</span><span class="sxs-lookup"><span data-stu-id="85565-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85565-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="85565-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="85565-108">類型： **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="85565-108">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="85565-109">[**D3DXCOLOR**](d3dxcolor.md)結構的指標，該結構為運算的結果。</span><span class="sxs-lookup"><span data-stu-id="85565-109">Pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="85565-110">*電腦* \[在\]</span><span class="sxs-lookup"><span data-stu-id="85565-110">*pC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85565-111">Type： **Const [**D3DXCOLOR**](d3dxcolor.md) \***</span><span class="sxs-lookup"><span data-stu-id="85565-111">Type: **const [**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="85565-112">來源 [**D3DXCOLOR**](d3dxcolor.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="85565-112">Pointer to a source [**D3DXCOLOR**](d3dxcolor.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85565-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="85565-113">Return value</span></span>

<span data-ttu-id="85565-114">類型： **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="85565-114">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="85565-115">此函式會傳回 [**D3DXCOLOR**](d3dxcolor.md) 結構的指標，此結構是色彩值的負色彩值。</span><span class="sxs-lookup"><span data-stu-id="85565-115">This function returns a pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the negative color value of the color value.</span></span>

## <a name="remarks"></a><span data-ttu-id="85565-116">備註</span><span class="sxs-lookup"><span data-stu-id="85565-116">Remarks</span></span>

<span data-ttu-id="85565-117">輸入 Alpha 通道會複製（未經修改）至輸出 Alpha 通道。</span><span class="sxs-lookup"><span data-stu-id="85565-117">The input alpha channel is copied, unmodified, to the output alpha channel.</span></span>

<span data-ttu-id="85565-118">此函式的傳回值與不悅參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="85565-118">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="85565-119">如此一來， **D3DXColorNegative** 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="85565-119">In this way, the **D3DXColorNegative** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="85565-120">此函式會藉由從 [**D3DXCOLOR**](d3dxcolor.md) 結構的色彩元件減去1.0 來傳回負的色彩值，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="85565-120">This function returns the negative color value by subtracting 1.0 from the color components of the [**D3DXCOLOR**](d3dxcolor.md) structure, as shown in the following example.</span></span>


```
pOut->r = 1.0f - pC->r;
```



## <a name="requirements"></a><span data-ttu-id="85565-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="85565-121">Requirements</span></span>



| <span data-ttu-id="85565-122">需求</span><span class="sxs-lookup"><span data-stu-id="85565-122">Requirement</span></span> | <span data-ttu-id="85565-123">值</span><span class="sxs-lookup"><span data-stu-id="85565-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="85565-124">標頭</span><span class="sxs-lookup"><span data-stu-id="85565-124">Header</span></span><br/>  | <dl> <span data-ttu-id="85565-125"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="85565-125"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="85565-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="85565-126">Library</span></span><br/> | <dl> <span data-ttu-id="85565-127"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="85565-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="85565-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="85565-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85565-129">數學函數</span><span class="sxs-lookup"><span data-stu-id="85565-129">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="85565-130">**D3DXColorLerp**</span><span class="sxs-lookup"><span data-stu-id="85565-130">**D3DXColorLerp**</span></span>](d3dxcolorlerp.md)
</dt> <dt>

[<span data-ttu-id="85565-131">**D3DXColorModulate**</span><span class="sxs-lookup"><span data-stu-id="85565-131">**D3DXColorModulate**</span></span>](d3dxcolormodulate.md)
</dt> <dt>

[<span data-ttu-id="85565-132">**D3DXColorScale**</span><span class="sxs-lookup"><span data-stu-id="85565-132">**D3DXColorScale**</span></span>](d3dxcolorscale.md)
</dt> </dl>

 

 




