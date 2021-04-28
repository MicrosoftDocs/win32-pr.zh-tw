---
description: D3DXFresnelTerm 函式 (D3dx9math) -計算 Fresnel 字詞。
ms.assetid: d3d281db-91a1-4100-8a82-028554b5a91d
title: 'D3DXFresnelTerm 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFresnelTerm
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5472f9839928fd3b4c1830bc309c7f610d487864
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114476"
---
# <a name="d3dxfresnelterm-function-d3dx9mathh"></a><span data-ttu-id="e68f9-103">D3DXFresnelTerm 函式 (D3dx9math) </span><span class="sxs-lookup"><span data-stu-id="e68f9-103">D3DXFresnelTerm function (D3dx9math.h)</span></span>

<span data-ttu-id="e68f9-104">計算 Fresnel 字詞。</span><span class="sxs-lookup"><span data-stu-id="e68f9-104">Calculate the Fresnel term.</span></span>

## <a name="syntax"></a><span data-ttu-id="e68f9-105">語法</span><span class="sxs-lookup"><span data-stu-id="e68f9-105">Syntax</span></span>


```C++
FLOAT D3DXFresnelTerm(
  _In_ FLOAT CosTheta,
  _In_ FLOAT RefractionIndex
);
```



## <a name="parameters"></a><span data-ttu-id="e68f9-106">參數</span><span class="sxs-lookup"><span data-stu-id="e68f9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e68f9-107">*CosTheta* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e68f9-107">*CosTheta* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e68f9-108">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e68f9-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e68f9-109">值長度必須介於 0 到 1 之間。</span><span class="sxs-lookup"><span data-stu-id="e68f9-109">The value must be between 0 and 1.</span></span>

</dd> <dt>

<span data-ttu-id="e68f9-110">*RefractionIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e68f9-110">*RefractionIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e68f9-111">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e68f9-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e68f9-112">材質的折射索引。</span><span class="sxs-lookup"><span data-stu-id="e68f9-112">The refraction index of a material.</span></span> <span data-ttu-id="e68f9-113">值必須大於1。</span><span class="sxs-lookup"><span data-stu-id="e68f9-113">The value must be greater than 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e68f9-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="e68f9-114">Return value</span></span>

<span data-ttu-id="e68f9-115">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e68f9-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e68f9-116">此函數會傳回 unpolarized light 的 Fresnel 字詞。</span><span class="sxs-lookup"><span data-stu-id="e68f9-116">This function returns the Fresnel term for unpolarized light.</span></span> <span data-ttu-id="e68f9-117">CosTheta 是事件角度的余弦值。</span><span class="sxs-lookup"><span data-stu-id="e68f9-117">CosTheta is the cosine of the incident angle.</span></span>

## <a name="remarks"></a><span data-ttu-id="e68f9-118">備註</span><span class="sxs-lookup"><span data-stu-id="e68f9-118">Remarks</span></span>

<span data-ttu-id="e68f9-119">若要尋找 Fresnel 字詞 (F) ：</span><span class="sxs-lookup"><span data-stu-id="e68f9-119">To find the Fresnel term (F):</span></span>

<span data-ttu-id="e68f9-120">如果是發生的角度，B 是折射的角度，則</span><span class="sxs-lookup"><span data-stu-id="e68f9-120">If A is angle of incidence and B is the angle of refraction, then</span></span>


```
F = 0.5 * [tan2(A - B) / tan2(A + B) + sin2(A - B) / sin2(A + B)]
  = 0.5 * sin2(A - B) / sin2(A + B) * [cos2(A + B) / cos2(A - B) + 1]
    
Let r   = sina(A) / sin(B)      (the relative refractive index)
Let c   = cos(A)
Let g   = (r2 + c2 - 1)1/2
```



<span data-ttu-id="e68f9-121">然後，使用三角函數和簡化進行擴充，您會得到：</span><span class="sxs-lookup"><span data-stu-id="e68f9-121">Then, expanding using the trig identities and simplifying, you get:</span></span>


```
F = 0.5 * (g + c)2 / (g - c)2 * ([c(g + c) - 1]2 / [c(g - c) + 1]2 + 1)
```



## <a name="requirements"></a><span data-ttu-id="e68f9-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="e68f9-122">Requirements</span></span>



| <span data-ttu-id="e68f9-123">需求</span><span class="sxs-lookup"><span data-stu-id="e68f9-123">Requirement</span></span> | <span data-ttu-id="e68f9-124">值</span><span class="sxs-lookup"><span data-stu-id="e68f9-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e68f9-125">標頭</span><span class="sxs-lookup"><span data-stu-id="e68f9-125">Header</span></span><br/>  | <dl> <span data-ttu-id="e68f9-126"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="e68f9-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="e68f9-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="e68f9-127">Library</span></span><br/> | <dl> <span data-ttu-id="e68f9-128"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="e68f9-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e68f9-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e68f9-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e68f9-130">數學函數</span><span class="sxs-lookup"><span data-stu-id="e68f9-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
