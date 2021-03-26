---
title: RWTexture1D：： GetDimensions 函數
description: 傳回資源的維度。 |RWTexture1D：： GetDimensions 函數
ms.assetid: 1bbd53ed-9396-4e8e-b2f3-3bd85f6e1a90
keywords:
- GetDimensions 函式 HLSL
topic_type:
- apiref
api_name:
- GetDimensions
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b65f0113ecf2c91786e45c35f5e8e832744bc952
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104973912"
---
# <a name="rwtexture1dgetdimensions-function"></a><span data-ttu-id="fecb4-105">RWTexture1D：： GetDimensions 函數</span><span class="sxs-lookup"><span data-stu-id="fecb4-105">RWTexture1D::GetDimensions function</span></span>

<span data-ttu-id="fecb4-106">傳回資源的維度。</span><span class="sxs-lookup"><span data-stu-id="fecb4-106">Returns the dimensions of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="fecb4-107">語法</span><span class="sxs-lookup"><span data-stu-id="fecb4-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out UINT Width
);
```

## <a name="parameters"></a><span data-ttu-id="fecb4-108">參數</span><span class="sxs-lookup"><span data-stu-id="fecb4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fecb4-109">*寬度* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="fecb4-109">*Width* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fecb4-110">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="fecb4-110">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="fecb4-111">資源寬度，以材質。</span><span class="sxs-lookup"><span data-stu-id="fecb4-111">The resource width, in texels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fecb4-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="fecb4-112">Return value</span></span>

<span data-ttu-id="fecb4-113">Nothing</span><span class="sxs-lookup"><span data-stu-id="fecb4-113">Nothing</span></span>

## <a name="remarks"></a><span data-ttu-id="fecb4-114">備註</span><span class="sxs-lookup"><span data-stu-id="fecb4-114">Remarks</span></span>

<span data-ttu-id="fecb4-115">這是此方法的多載版本清單。</span><span class="sxs-lookup"><span data-stu-id="fecb4-115">This is a list of the overloaded versions of this method.</span></span>


```
void GetDimensions (out UINT Width);

void GetDimensions(out float Width);
```



<span data-ttu-id="fecb4-116">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="fecb4-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="fecb4-117">頂點</span><span class="sxs-lookup"><span data-stu-id="fecb4-117">Vertex</span></span> | <span data-ttu-id="fecb4-118">船體</span><span class="sxs-lookup"><span data-stu-id="fecb4-118">Hull</span></span> | <span data-ttu-id="fecb4-119">網域</span><span class="sxs-lookup"><span data-stu-id="fecb4-119">Domain</span></span> | <span data-ttu-id="fecb4-120">幾何</span><span class="sxs-lookup"><span data-stu-id="fecb4-120">Geometry</span></span> | <span data-ttu-id="fecb4-121">像素</span><span class="sxs-lookup"><span data-stu-id="fecb4-121">Pixel</span></span> | <span data-ttu-id="fecb4-122">計算</span><span class="sxs-lookup"><span data-stu-id="fecb4-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="fecb4-123">x</span><span class="sxs-lookup"><span data-stu-id="fecb4-123">x</span></span>     | <span data-ttu-id="fecb4-124">x</span><span class="sxs-lookup"><span data-stu-id="fecb4-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="fecb4-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fecb4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fecb4-126">RWTexture1D</span><span class="sxs-lookup"><span data-stu-id="fecb4-126">RWTexture1D</span></span>](sm5-object-rwtexture1d.md)
</dt> <dt>

[<span data-ttu-id="fecb4-127">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="fecb4-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
