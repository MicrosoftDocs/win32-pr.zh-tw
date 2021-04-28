---
description: D3DXColorAdjustContrast 函式 (D3dx9math) -調整色彩的對比值。
ms.assetid: be49c9c7-b625-4cbc-bd63-1d5766ae2dbb
title: 'D3DXColorAdjustContrast 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorAdjustContrast
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9dc9bb79d1ebbe536661347d76d13846dead6aa8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115876"
---
# <a name="d3dxcoloradjustcontrast-function-d3dx9mathh"></a><span data-ttu-id="2410e-103">D3DXColorAdjustContrast 函式 (D3dx9math) </span><span class="sxs-lookup"><span data-stu-id="2410e-103">D3DXColorAdjustContrast function (D3dx9math.h)</span></span>

<span data-ttu-id="2410e-104">調整色彩的對比值。</span><span class="sxs-lookup"><span data-stu-id="2410e-104">Adjusts the contrast value of a color.</span></span>

## <a name="syntax"></a><span data-ttu-id="2410e-105">語法</span><span class="sxs-lookup"><span data-stu-id="2410e-105">Syntax</span></span>


```C++
D3DXCOLOR* D3DXColorAdjustContrast(
  _Inout_       D3DXCOLOR *pOut,
  _In_    const D3DXCOLOR *pC,
  _In_          FLOAT     c
);
```



## <a name="parameters"></a><span data-ttu-id="2410e-106">參數</span><span class="sxs-lookup"><span data-stu-id="2410e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2410e-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="2410e-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2410e-108">類型： **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="2410e-108">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="2410e-109">[**D3DXCOLOR**](d3dxcolor.md)結構的指標，該結構為運算的結果。</span><span class="sxs-lookup"><span data-stu-id="2410e-109">Pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="2410e-110">*電腦* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2410e-110">*pC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2410e-111">Type： **Const [**D3DXCOLOR**](d3dxcolor.md) \***</span><span class="sxs-lookup"><span data-stu-id="2410e-111">Type: **const [**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="2410e-112">來源 [**D3DXCOLOR**](d3dxcolor.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="2410e-112">Pointer to a source [**D3DXCOLOR**](d3dxcolor.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="2410e-113">*c* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2410e-113">*c* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2410e-114">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2410e-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2410e-115">對比值。</span><span class="sxs-lookup"><span data-stu-id="2410e-115">Contrast value.</span></span> <span data-ttu-id="2410e-116">此參數會以線性方式在50% 的灰色與彩色電腦之間進行插補。</span><span class="sxs-lookup"><span data-stu-id="2410e-116">This parameter linearly interpolates between fifty percent gray and the color, pC.</span></span> <span data-ttu-id="2410e-117">C 的值沒有限制。</span><span class="sxs-lookup"><span data-stu-id="2410e-117">There are not limits on the value of c.</span></span> <span data-ttu-id="2410e-118">如果此參數為零，則傳回的色彩會是50% 灰色。</span><span class="sxs-lookup"><span data-stu-id="2410e-118">If this parameter is zero, then the returned color is fifty percent gray.</span></span> <span data-ttu-id="2410e-119">如果這個參數是1，則傳回的色彩會是原始色彩。</span><span class="sxs-lookup"><span data-stu-id="2410e-119">If this parameter is 1, then the returned color is the original color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2410e-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="2410e-120">Return value</span></span>

<span data-ttu-id="2410e-121">類型： **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="2410e-121">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="2410e-122">此函式會傳回 [**D3DXCOLOR**](d3dxcolor.md) 結構的指標，此結構是對比調整的結果。</span><span class="sxs-lookup"><span data-stu-id="2410e-122">This function returns a pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the result of the contrast adjustment.</span></span>

## <a name="remarks"></a><span data-ttu-id="2410e-123">備註</span><span class="sxs-lookup"><span data-stu-id="2410e-123">Remarks</span></span>

<span data-ttu-id="2410e-124">輸入 Alpha 通道會複製（未經修改）至輸出 Alpha 通道。</span><span class="sxs-lookup"><span data-stu-id="2410e-124">The input alpha channel is copied, unmodified, to the output alpha channel.</span></span>

<span data-ttu-id="2410e-125">此函式的傳回值與不悅參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="2410e-125">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="2410e-126">如此一來，此函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="2410e-126">In this way, this function can be used as a parameter for another function.</span></span>

<span data-ttu-id="2410e-127">此函式會將 [**D3DXCOLOR**](d3dxcolor.md) 結構的紅色、綠色和藍色色彩元件，插入50% 的灰色和指定的對比值之間，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="2410e-127">This function interpolates the red, green, and blue color components of a [**D3DXCOLOR**](d3dxcolor.md) structure between fifty percent gray and a specified contrast value, as shown in the following example.</span></span>


```
pOut->r = 0.5f + c * (pC->r - 0.5f);
```



<span data-ttu-id="2410e-128">如果 c 大於0且小於1，則會減少對比。</span><span class="sxs-lookup"><span data-stu-id="2410e-128">If c is greater than 0 and less than 1, the contrast is decreased.</span></span> <span data-ttu-id="2410e-129">如果 c 大於1，則會增加對比。</span><span class="sxs-lookup"><span data-stu-id="2410e-129">If c is greater than 1, the contrast is increased.</span></span>

## <a name="requirements"></a><span data-ttu-id="2410e-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="2410e-130">Requirements</span></span>



| <span data-ttu-id="2410e-131">需求</span><span class="sxs-lookup"><span data-stu-id="2410e-131">Requirement</span></span> | <span data-ttu-id="2410e-132">值</span><span class="sxs-lookup"><span data-stu-id="2410e-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2410e-133">標頭</span><span class="sxs-lookup"><span data-stu-id="2410e-133">Header</span></span><br/>  | <dl> <span data-ttu-id="2410e-134"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="2410e-134"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="2410e-135">程式庫</span><span class="sxs-lookup"><span data-stu-id="2410e-135">Library</span></span><br/> | <dl> <span data-ttu-id="2410e-136"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="2410e-136"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2410e-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2410e-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2410e-138">數學函數</span><span class="sxs-lookup"><span data-stu-id="2410e-138">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="2410e-139">**D3DXColorAdjustSaturation**</span><span class="sxs-lookup"><span data-stu-id="2410e-139">**D3DXColorAdjustSaturation**</span></span>](d3dxcoloradjustsaturation.md)
</dt> </dl>

 

 
