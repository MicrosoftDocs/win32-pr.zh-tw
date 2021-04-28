---
description: D3DXColorAdjustContrast 函式 (D3DX10Math) -調整色彩的對比值。
ms.assetid: c111d3c7-19c6-4a6b-af0d-a9e1bc0bb7d9
title: 'D3DXColorAdjustContrast 函式 (D3DX10Math) '
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 09781c5c11560c3497a5af57528cf478f6259816
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113326"
---
# <a name="d3dxcoloradjustcontrast-function-d3dx10mathh"></a><span data-ttu-id="dba07-103">D3DXColorAdjustContrast 函式 (D3DX10Math) </span><span class="sxs-lookup"><span data-stu-id="dba07-103">D3DXColorAdjustContrast function (D3DX10Math.h)</span></span>

<span data-ttu-id="dba07-104">調整色彩的對比值。</span><span class="sxs-lookup"><span data-stu-id="dba07-104">Adjusts the contrast value of a color.</span></span>

## <a name="syntax"></a><span data-ttu-id="dba07-105">語法</span><span class="sxs-lookup"><span data-stu-id="dba07-105">Syntax</span></span>


```C++
D3DXCOLOR* D3DXColorAdjustContrast(
  _In_       D3DXCOLOR *pOut,
  _In_ const D3DXCOLOR *pC,
  _In_       FLOAT     c
);
```



## <a name="parameters"></a><span data-ttu-id="dba07-106">參數</span><span class="sxs-lookup"><span data-stu-id="dba07-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dba07-107">*不悅* \[在\]</span><span class="sxs-lookup"><span data-stu-id="dba07-107">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dba07-108">類型： **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="dba07-108">Type: **[**D3DXCOLOR**](../direct3d9/d3dxcolor.md)\***</span></span>

<span data-ttu-id="dba07-109">\[在中， \] 是指作業結果之 [**D3DXCOLOR**](d3d10-d3dxcolor.md) 的指標。</span><span class="sxs-lookup"><span data-stu-id="dba07-109">\[in, out\] Pointer to a [**D3DXCOLOR**](d3d10-d3dxcolor.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="dba07-110">*電腦* \[在\]</span><span class="sxs-lookup"><span data-stu-id="dba07-110">*pC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dba07-111">Type： **Const [**D3DXCOLOR**](../direct3d9/d3dxcolor.md) \***</span><span class="sxs-lookup"><span data-stu-id="dba07-111">Type: **const [**D3DXCOLOR**](../direct3d9/d3dxcolor.md)\***</span></span>

<span data-ttu-id="dba07-112">來源 D3DXCOLOR 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="dba07-112">Pointer to a source D3DXCOLOR structure.</span></span>

</dd> <dt>

<span data-ttu-id="dba07-113">*c* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dba07-113">*c* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dba07-114">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dba07-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dba07-115">對比值。</span><span class="sxs-lookup"><span data-stu-id="dba07-115">Contrast value.</span></span> <span data-ttu-id="dba07-116">此參數會以線性方式在50% 的灰色與彩色電腦之間進行插補。</span><span class="sxs-lookup"><span data-stu-id="dba07-116">This parameter linearly interpolates between fifty percent gray and the color, pC.</span></span> <span data-ttu-id="dba07-117">C 的值沒有限制。</span><span class="sxs-lookup"><span data-stu-id="dba07-117">There are no limits on the value of c.</span></span> <span data-ttu-id="dba07-118">如果此參數為零，則傳回的色彩會是50% 灰色。</span><span class="sxs-lookup"><span data-stu-id="dba07-118">If this parameter is zero, then the returned color is fifty percent gray.</span></span> <span data-ttu-id="dba07-119">如果這個參數是1，則傳回的色彩會是原始色彩。</span><span class="sxs-lookup"><span data-stu-id="dba07-119">If this parameter is 1, then the returned color is the original color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dba07-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="dba07-120">Return value</span></span>

<span data-ttu-id="dba07-121">類型： **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="dba07-121">Type: **[**D3DXCOLOR**](../direct3d9/d3dxcolor.md)\***</span></span>

<span data-ttu-id="dba07-122">此函式會傳回 D3DXCOLOR 結構的指標，此結構是對比調整的結果。</span><span class="sxs-lookup"><span data-stu-id="dba07-122">This function returns a pointer to a D3DXCOLOR structure that is the result of the contrast adjustment.</span></span>

## <a name="remarks"></a><span data-ttu-id="dba07-123">備註</span><span class="sxs-lookup"><span data-stu-id="dba07-123">Remarks</span></span>

<span data-ttu-id="dba07-124">輸入 Alpha 通道會複製（未經修改）至輸出 Alpha 通道。</span><span class="sxs-lookup"><span data-stu-id="dba07-124">The input alpha channel is copied, unmodified, to the output alpha channel.</span></span>

<span data-ttu-id="dba07-125">此函式的傳回值與不悅參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="dba07-125">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="dba07-126">如此一來，此函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="dba07-126">In this way, this function can be used as a parameter for another function.</span></span>

<span data-ttu-id="dba07-127">此函式會將 D3DXCOLOR 結構的紅色、綠色和藍色色彩元件，插入50% 的灰色和指定的對比值之間，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="dba07-127">This function interpolates the red, green, and blue color components of a D3DXCOLOR structure between fifty percent gray and a specified contrast value, as shown in the following example.</span></span>


```
pOut->r = 0.5f + c * (pC->r - 0.5f);
```



<span data-ttu-id="dba07-128">如果 c 大於0且小於1，則會減少對比。</span><span class="sxs-lookup"><span data-stu-id="dba07-128">If c is greater than 0 and less than 1, the contrast is decreased.</span></span> <span data-ttu-id="dba07-129">如果 c 大於1，則會增加對比。</span><span class="sxs-lookup"><span data-stu-id="dba07-129">If c is greater than 1, the contrast is increased.</span></span>

## <a name="requirements"></a><span data-ttu-id="dba07-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="dba07-130">Requirements</span></span>



| <span data-ttu-id="dba07-131">需求</span><span class="sxs-lookup"><span data-stu-id="dba07-131">Requirement</span></span> | <span data-ttu-id="dba07-132">值</span><span class="sxs-lookup"><span data-stu-id="dba07-132">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dba07-133">標頭</span><span class="sxs-lookup"><span data-stu-id="dba07-133">Header</span></span><br/>  | <dl> <span data-ttu-id="dba07-134"><dt>D3DX10Math。h</dt></span><span class="sxs-lookup"><span data-stu-id="dba07-134"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="dba07-135">程式庫</span><span class="sxs-lookup"><span data-stu-id="dba07-135">Library</span></span><br/> | <dl> <span data-ttu-id="dba07-136"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="dba07-136"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="dba07-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dba07-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dba07-138">數學函數</span><span class="sxs-lookup"><span data-stu-id="dba07-138">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
