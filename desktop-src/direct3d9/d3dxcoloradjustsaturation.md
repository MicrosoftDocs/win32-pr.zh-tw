---
description: D3DXColorAdjustSaturation 函式 (D3dx9math) -調整色彩的飽和度值。
ms.assetid: 1f66c3b4-2f02-4993-80c6-c484180c2459
title: 'D3DXColorAdjustSaturation 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorAdjustSaturation
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 878cdd83a04f594da3133eda314486af96ac3d56
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115866"
---
# <a name="d3dxcoloradjustsaturation-function-d3dx9mathh"></a><span data-ttu-id="28944-103">D3DXColorAdjustSaturation 函式 (D3dx9math) </span><span class="sxs-lookup"><span data-stu-id="28944-103">D3DXColorAdjustSaturation function (D3dx9math.h)</span></span>

<span data-ttu-id="28944-104">調整色彩的飽和度值。</span><span class="sxs-lookup"><span data-stu-id="28944-104">Adjusts the saturation value of a color.</span></span>

## <a name="syntax"></a><span data-ttu-id="28944-105">語法</span><span class="sxs-lookup"><span data-stu-id="28944-105">Syntax</span></span>


```C++
D3DXCOLOR* D3DXColorAdjustSaturation(
  _Inout_       D3DXCOLOR *pOut,
  _In_    const D3DXCOLOR *pC,
  _In_          FLOAT     s
);
```



## <a name="parameters"></a><span data-ttu-id="28944-106">參數</span><span class="sxs-lookup"><span data-stu-id="28944-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28944-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="28944-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="28944-108">類型： **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="28944-108">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="28944-109">[**D3DXCOLOR**](d3dxcolor.md)結構的指標，該結構為運算的結果。</span><span class="sxs-lookup"><span data-stu-id="28944-109">Pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="28944-110">*電腦* \[在\]</span><span class="sxs-lookup"><span data-stu-id="28944-110">*pC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28944-111">Type： **Const [**D3DXCOLOR**](d3dxcolor.md) \***</span><span class="sxs-lookup"><span data-stu-id="28944-111">Type: **const [**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="28944-112">來源 [**D3DXCOLOR**](d3dxcolor.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="28944-112">Pointer to a source [**D3DXCOLOR**](d3dxcolor.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="28944-113"> \[ 中的 s\]</span><span class="sxs-lookup"><span data-stu-id="28944-113">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28944-114">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="28944-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="28944-115">飽和度值。</span><span class="sxs-lookup"><span data-stu-id="28944-115">Saturation value.</span></span> <span data-ttu-id="28944-116">此參數會在轉換成灰階的色彩和原始色彩（pC）之間以線性方式進行插補。</span><span class="sxs-lookup"><span data-stu-id="28944-116">This parameter linearly interpolates between the color converted to grayscale and the original color, pC.</span></span> <span data-ttu-id="28944-117">的值沒有限制。</span><span class="sxs-lookup"><span data-stu-id="28944-117">There are no limits on the value of s.</span></span> <span data-ttu-id="28944-118">如果 s 為0，則傳回的色彩為灰階色彩。</span><span class="sxs-lookup"><span data-stu-id="28944-118">If s is 0, the returned color is the grayscale color.</span></span> <span data-ttu-id="28944-119">如果 s 是1，則傳回的色彩會是原始色彩。</span><span class="sxs-lookup"><span data-stu-id="28944-119">If s is 1, the returned color is the original color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28944-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="28944-120">Return value</span></span>

<span data-ttu-id="28944-121">類型： **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="28944-121">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="28944-122">此函式會傳回 [**D3DXCOLOR**](d3dxcolor.md) 結構的指標，此結構是飽和度調整的結果。</span><span class="sxs-lookup"><span data-stu-id="28944-122">This function returns a pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the result of the saturation adjustment.</span></span>

## <a name="remarks"></a><span data-ttu-id="28944-123">備註</span><span class="sxs-lookup"><span data-stu-id="28944-123">Remarks</span></span>

<span data-ttu-id="28944-124">輸入 Alpha 通道會複製（未經修改）至輸出 Alpha 通道。</span><span class="sxs-lookup"><span data-stu-id="28944-124">The input alpha channel is copied, unmodified, to the output alpha channel.</span></span>

<span data-ttu-id="28944-125">此函式的傳回值與不悅參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="28944-125">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="28944-126">如此一來，此函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="28944-126">In this way, this function can be used as a parameter for another function.</span></span>

<span data-ttu-id="28944-127">此函式會在 unsaturated 色彩和色彩之間，插入 [**D3DXCOLOR**](d3dxcolor.md) 結構的紅色、綠色和藍色色彩元件，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="28944-127">This function interpolates the red, green, and blue color components of a [**D3DXCOLOR**](d3dxcolor.md) structure between an unsaturated color and a color, as shown in the following example.</span></span>


```
    // Approximate values for each component's contribution to luminance.
    // Based upon the NTSC standard described in ITU-R Recommendation BT.709.
    FLOAT grey = pC->r * 0.2125f + pC->g * 0.7154f + pC->b * 0.0721f;
    
    pOut->r = grey + s * (pC->r - grey);
```



<span data-ttu-id="28944-128">如果 s 大於0且小於1，則會減少飽和度。</span><span class="sxs-lookup"><span data-stu-id="28944-128">If s is greater than 0 and less than 1, the saturation is decreased.</span></span> <span data-ttu-id="28944-129">如果 s 大於1，則會增加飽和度。</span><span class="sxs-lookup"><span data-stu-id="28944-129">If s is greater than 1, the saturation is increased.</span></span>

<span data-ttu-id="28944-130">灰階色彩的計算方式如下：</span><span class="sxs-lookup"><span data-stu-id="28944-130">The grayscale color is computed as:</span></span>


```
r = g = b = 0.2125*r + 0.7154*g + 0.0721*b
```



## <a name="requirements"></a><span data-ttu-id="28944-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="28944-131">Requirements</span></span>



| <span data-ttu-id="28944-132">需求</span><span class="sxs-lookup"><span data-stu-id="28944-132">Requirement</span></span> | <span data-ttu-id="28944-133">值</span><span class="sxs-lookup"><span data-stu-id="28944-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="28944-134">標頭</span><span class="sxs-lookup"><span data-stu-id="28944-134">Header</span></span><br/>  | <dl> <span data-ttu-id="28944-135"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="28944-135"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="28944-136">程式庫</span><span class="sxs-lookup"><span data-stu-id="28944-136">Library</span></span><br/> | <dl> <span data-ttu-id="28944-137"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="28944-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="28944-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="28944-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28944-139">數學函數</span><span class="sxs-lookup"><span data-stu-id="28944-139">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="28944-140">**D3DXColorAdjustContrast**</span><span class="sxs-lookup"><span data-stu-id="28944-140">**D3DXColorAdjustContrast**</span></span>](d3dxcoloradjustcontrast.md)
</dt> </dl>

 

 
