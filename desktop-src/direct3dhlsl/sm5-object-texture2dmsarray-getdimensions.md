---
title: Texture2DMSArray：： GetDimensions 函數
description: 傳回資源的維度。 |Texture2DMSArray：： GetDimensions 函數
ms.assetid: 86d54e0d-f168-479f-b2af-f021b8994741
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
ms.openlocfilehash: e22a225178c2fa965ea842b8c86692d09b87168f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322464"
---
# <a name="texture2dmsarraygetdimensions-function"></a><span data-ttu-id="198e6-105">Texture2DMSArray：： GetDimensions 函數</span><span class="sxs-lookup"><span data-stu-id="198e6-105">Texture2DMSArray::GetDimensions function</span></span>

<span data-ttu-id="198e6-106">傳回資源的維度。</span><span class="sxs-lookup"><span data-stu-id="198e6-106">Returns the dimensions of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="198e6-107">語法</span><span class="sxs-lookup"><span data-stu-id="198e6-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out UINT Width,
  out UINT Height,
  out UINT Elements,
  out UINT NumberOfSamples
);
```

## <a name="parameters"></a><span data-ttu-id="198e6-108">參數</span><span class="sxs-lookup"><span data-stu-id="198e6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="198e6-109">*寬度* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="198e6-109">*Width* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="198e6-110">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="198e6-110">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="198e6-111">資源寬度，以材質。</span><span class="sxs-lookup"><span data-stu-id="198e6-111">The resource width, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="198e6-112">*高度* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="198e6-112">*Height* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="198e6-113">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="198e6-113">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="198e6-114">資源高度，以材質。</span><span class="sxs-lookup"><span data-stu-id="198e6-114">The resource height, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="198e6-115">*元素* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="198e6-115">*Elements* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="198e6-116">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="198e6-116">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="198e6-117">陣列中的項目數。</span><span class="sxs-lookup"><span data-stu-id="198e6-117">The number of elements in the array.</span></span>

</dd> <dt>

<span data-ttu-id="198e6-118">*NumberOfSamples* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="198e6-118">*NumberOfSamples* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="198e6-119">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="198e6-119">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="198e6-120">範例位置的數目。</span><span class="sxs-lookup"><span data-stu-id="198e6-120">The number of sample locations.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="198e6-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="198e6-121">Return value</span></span>

<span data-ttu-id="198e6-122">Nothing</span><span class="sxs-lookup"><span data-stu-id="198e6-122">Nothing</span></span>

## <a name="remarks"></a><span data-ttu-id="198e6-123">備註</span><span class="sxs-lookup"><span data-stu-id="198e6-123">Remarks</span></span>

<span data-ttu-id="198e6-124">這是此方法的多載版本清單。</span><span class="sxs-lookup"><span data-stu-id="198e6-124">This is a list of the overloaded versions of this method.</span></span>


```
void GetDimensions(out float Width,
  out float Height,
  out float Elements,
  out float NumberOfSamples);
```



<span data-ttu-id="198e6-125">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="198e6-125">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="198e6-126">頂點</span><span class="sxs-lookup"><span data-stu-id="198e6-126">Vertex</span></span> | <span data-ttu-id="198e6-127">船體</span><span class="sxs-lookup"><span data-stu-id="198e6-127">Hull</span></span> | <span data-ttu-id="198e6-128">網域</span><span class="sxs-lookup"><span data-stu-id="198e6-128">Domain</span></span> | <span data-ttu-id="198e6-129">幾何</span><span class="sxs-lookup"><span data-stu-id="198e6-129">Geometry</span></span> | <span data-ttu-id="198e6-130">像素</span><span class="sxs-lookup"><span data-stu-id="198e6-130">Pixel</span></span> | <span data-ttu-id="198e6-131">計算</span><span class="sxs-lookup"><span data-stu-id="198e6-131">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="198e6-132">x</span><span class="sxs-lookup"><span data-stu-id="198e6-132">x</span></span>     | <span data-ttu-id="198e6-133">x</span><span class="sxs-lookup"><span data-stu-id="198e6-133">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="198e6-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="198e6-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="198e6-135">Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="198e6-135">Texture2DMSArray</span></span>](sm5-object-texture2dmsarray.md)
</dt> <dt>

[<span data-ttu-id="198e6-136">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="198e6-136">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
