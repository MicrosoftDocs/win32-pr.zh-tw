---
description: 使用線性插補來建立色彩值。
ms.assetid: bf7bf2f4-5fb5-44d3-a7e5-7998640d7d49
title: 'D3DXColorLerp 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorLerp
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3521ee9e76aecd486093f903d336c08553e0e4ef
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103854011"
---
# <a name="d3dxcolorlerp-function"></a><span data-ttu-id="13454-103">D3DXColorLerp 函式</span><span class="sxs-lookup"><span data-stu-id="13454-103">D3DXColorLerp function</span></span>

<span data-ttu-id="13454-104">使用線性插補來建立色彩值。</span><span class="sxs-lookup"><span data-stu-id="13454-104">Uses linear interpolation to create a color value.</span></span>

## <a name="syntax"></a><span data-ttu-id="13454-105">語法</span><span class="sxs-lookup"><span data-stu-id="13454-105">Syntax</span></span>


```C++
D3DXCOLOR* D3DXColorLerp(
  _Inout_       D3DXCOLOR *pOut,
  _In_    const D3DXCOLOR *pC1,
  _In_    const D3DXCOLOR *pC2,
  _In_          FLOAT     s
);
```



## <a name="parameters"></a><span data-ttu-id="13454-106">參數</span><span class="sxs-lookup"><span data-stu-id="13454-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13454-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="13454-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="13454-108">類型： **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="13454-108">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="13454-109">[**D3DXCOLOR**](d3dxcolor.md)結構的指標，該結構為運算的結果。</span><span class="sxs-lookup"><span data-stu-id="13454-109">Pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="13454-110">*test-pc1* \[在\]</span><span class="sxs-lookup"><span data-stu-id="13454-110">*pC1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13454-111">Type： **Const [**D3DXCOLOR**](d3dxcolor.md) \***</span><span class="sxs-lookup"><span data-stu-id="13454-111">Type: **const [**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="13454-112">來源 [**D3DXCOLOR**](d3dxcolor.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="13454-112">Pointer to a source [**D3DXCOLOR**](d3dxcolor.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="13454-113">*pC2* \[在\]</span><span class="sxs-lookup"><span data-stu-id="13454-113">*pC2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13454-114">Type： **Const [**D3DXCOLOR**](d3dxcolor.md) \***</span><span class="sxs-lookup"><span data-stu-id="13454-114">Type: **const [**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="13454-115">來源 [**D3DXCOLOR**](d3dxcolor.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="13454-115">Pointer to a source [**D3DXCOLOR**](d3dxcolor.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="13454-116"> \[ 中的 s\]</span><span class="sxs-lookup"><span data-stu-id="13454-116">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13454-117">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="13454-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="13454-118">以線性方式在色彩（Test-pc1 和 pC2）之間插補的參數，會將它們視為4D 向量。</span><span class="sxs-lookup"><span data-stu-id="13454-118">Parameter that linearly interpolates between the colors, pC1 and pC2, treating them both as 4D vectors.</span></span> <span data-ttu-id="13454-119">的值沒有限制。</span><span class="sxs-lookup"><span data-stu-id="13454-119">There are no limits on the value of s.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13454-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="13454-120">Return value</span></span>

<span data-ttu-id="13454-121">類型： **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="13454-121">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="13454-122">此函式會傳回 [**D3DXCOLOR**](d3dxcolor.md) 結構的指標，此結構是線性插補的結果。</span><span class="sxs-lookup"><span data-stu-id="13454-122">This function returns a pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the result of the linear interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="13454-123">備註</span><span class="sxs-lookup"><span data-stu-id="13454-123">Remarks</span></span>

<span data-ttu-id="13454-124">此函式的傳回值與不悅參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="13454-124">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="13454-125">如此一來， **D3DXColorLerp** 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="13454-125">In this way, the **D3DXColorLerp** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="13454-126">此函式會將 [**D3DXCOLOR**](d3dxcolor.md) 結構的紅色、綠色、藍色和 Alpha 元件，插補兩個色彩，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="13454-126">This function interpolates the red, green, blue, and alpha components of a [**D3DXCOLOR**](d3dxcolor.md) structure between two colors, as shown in the following example.</span></span>


```
   
pOut->r = pC1->r + s * (pC2->r - pC1->r);
```



<span data-ttu-id="13454-127">如果您在色彩 A 和 B 之間以線性方式插即插，而 s 為0，則產生的色彩為。如果 s 是1，則產生的色彩為色彩 B。</span><span class="sxs-lookup"><span data-stu-id="13454-127">If you are linearly interpolating between the colors A and B, and s is 0, the resulting color is A. If s is 1, the resulting color is color B.</span></span>

## <a name="requirements"></a><span data-ttu-id="13454-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="13454-128">Requirements</span></span>



| <span data-ttu-id="13454-129">需求</span><span class="sxs-lookup"><span data-stu-id="13454-129">Requirement</span></span> | <span data-ttu-id="13454-130">值</span><span class="sxs-lookup"><span data-stu-id="13454-130">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="13454-131">標頭</span><span class="sxs-lookup"><span data-stu-id="13454-131">Header</span></span><br/>  | <dl> <span data-ttu-id="13454-132"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="13454-132"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="13454-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="13454-133">Library</span></span><br/> | <dl> <span data-ttu-id="13454-134"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="13454-134"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="13454-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="13454-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13454-136">數學函數</span><span class="sxs-lookup"><span data-stu-id="13454-136">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="13454-137">**D3DXColorModulate**</span><span class="sxs-lookup"><span data-stu-id="13454-137">**D3DXColorModulate**</span></span>](d3dxcolormodulate.md)
</dt> <dt>

[<span data-ttu-id="13454-138">**D3DXColorNegative**</span><span class="sxs-lookup"><span data-stu-id="13454-138">**D3DXColorNegative**</span></span>](d3dxcolornegative.md)
</dt> <dt>

[<span data-ttu-id="13454-139">**D3DXColorScale**</span><span class="sxs-lookup"><span data-stu-id="13454-139">**D3DXColorScale**</span></span>](d3dxcolorscale.md)
</dt> </dl>

 

 
