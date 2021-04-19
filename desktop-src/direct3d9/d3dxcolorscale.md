---
description: 調整色彩值。
ms.assetid: 35e8adee-7ce5-4db5-8276-f0e408748e78
title: 'D3DXColorScale 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorScale
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 74020f302a26162df1e42cb4c9f020af3f64e59c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106989206"
---
# <a name="d3dxcolorscale-function"></a><span data-ttu-id="a8a75-103">D3DXColorScale 函式</span><span class="sxs-lookup"><span data-stu-id="a8a75-103">D3DXColorScale function</span></span>

<span data-ttu-id="a8a75-104">調整色彩值。</span><span class="sxs-lookup"><span data-stu-id="a8a75-104">Scales a color value.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8a75-105">語法</span><span class="sxs-lookup"><span data-stu-id="a8a75-105">Syntax</span></span>


```C++
D3DXCOLOR* D3DXColorScale(
  _Inout_       D3DXCOLOR *pOut,
  _In_    const D3DXCOLOR *pC,
  _In_          FLOAT     s
);
```



## <a name="parameters"></a><span data-ttu-id="a8a75-106">參數</span><span class="sxs-lookup"><span data-stu-id="a8a75-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8a75-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="a8a75-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a8a75-108">類型： **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="a8a75-108">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="a8a75-109">[**D3DXCOLOR**](d3dxcolor.md)結構的指標，該結構為運算的結果。</span><span class="sxs-lookup"><span data-stu-id="a8a75-109">Pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="a8a75-110">*電腦* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a8a75-110">*pC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8a75-111">Type： **Const [**D3DXCOLOR**](d3dxcolor.md) \***</span><span class="sxs-lookup"><span data-stu-id="a8a75-111">Type: **const [**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="a8a75-112">來源 [**D3DXCOLOR**](d3dxcolor.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="a8a75-112">Pointer to a source [**D3DXCOLOR**](d3dxcolor.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="a8a75-113"> \[ 中的 s\]</span><span class="sxs-lookup"><span data-stu-id="a8a75-113">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8a75-114">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a8a75-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a8a75-115">比例因數。</span><span class="sxs-lookup"><span data-stu-id="a8a75-115">Scale factor.</span></span> <span data-ttu-id="a8a75-116">它會調整色彩，例如，將它視為4D 向量。</span><span class="sxs-lookup"><span data-stu-id="a8a75-116">It scales the color, treating it like a 4D vector.</span></span> <span data-ttu-id="a8a75-117">的值沒有限制。</span><span class="sxs-lookup"><span data-stu-id="a8a75-117">There are no limits on the value of s.</span></span> <span data-ttu-id="a8a75-118">如果 s 是1，則產生的色彩會是原始色彩。</span><span class="sxs-lookup"><span data-stu-id="a8a75-118">If s is 1, the resulting color is the original color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8a75-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="a8a75-119">Return value</span></span>

<span data-ttu-id="a8a75-120">類型： **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="a8a75-120">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="a8a75-121">此函式會傳回 [**D3DXCOLOR**](d3dxcolor.md) 結構的指標，此結構是縮放的色彩值。</span><span class="sxs-lookup"><span data-stu-id="a8a75-121">This function returns a pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the scaled color value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8a75-122">備註</span><span class="sxs-lookup"><span data-stu-id="a8a75-122">Remarks</span></span>

<span data-ttu-id="a8a75-123">此函式的傳回值與不悅參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="a8a75-123">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="a8a75-124">如此一來， **D3DXColorScale** 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="a8a75-124">In this way, the **D3DXColorScale** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="a8a75-125">此函式會將 [**D3DXCOLOR**](d3dxcolor.md) 結構的色彩元件乘以指定的縮放比例，以計算縮放的色彩值，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="a8a75-125">This function computes the scaled color value by multiplying the color components of the [**D3DXCOLOR**](d3dxcolor.md) structure by the specified scale factor, as shown in the following example.</span></span>


```
pOut->r = pC->r * s;
```



## <a name="requirements"></a><span data-ttu-id="a8a75-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="a8a75-126">Requirements</span></span>



| <span data-ttu-id="a8a75-127">需求</span><span class="sxs-lookup"><span data-stu-id="a8a75-127">Requirement</span></span> | <span data-ttu-id="a8a75-128">值</span><span class="sxs-lookup"><span data-stu-id="a8a75-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a8a75-129">標頭</span><span class="sxs-lookup"><span data-stu-id="a8a75-129">Header</span></span><br/>  | <dl> <span data-ttu-id="a8a75-130"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="a8a75-130"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="a8a75-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="a8a75-131">Library</span></span><br/> | <dl> <span data-ttu-id="a8a75-132"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="a8a75-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a8a75-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a8a75-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8a75-134">數學函數</span><span class="sxs-lookup"><span data-stu-id="a8a75-134">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="a8a75-135">**D3DXColorLerp**</span><span class="sxs-lookup"><span data-stu-id="a8a75-135">**D3DXColorLerp**</span></span>](d3dxcolorlerp.md)
</dt> <dt>

[<span data-ttu-id="a8a75-136">**D3DXColorModulate**</span><span class="sxs-lookup"><span data-stu-id="a8a75-136">**D3DXColorModulate**</span></span>](d3dxcolormodulate.md)
</dt> <dt>

[<span data-ttu-id="a8a75-137">**D3DXColorNegative**</span><span class="sxs-lookup"><span data-stu-id="a8a75-137">**D3DXColorNegative**</span></span>](d3dxcolornegative.md)
</dt> </dl>

 

 
