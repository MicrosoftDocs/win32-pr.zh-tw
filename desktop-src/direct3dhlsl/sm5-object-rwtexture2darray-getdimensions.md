---
title: RWTexture2DArray：： GetDimensions 函數
description: 傳回資源的維度。 |RWTexture2DArray：： GetDimensions 函數
ms.assetid: 473b3f41-854d-4881-a80b-2d2dd7e5d479
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
ms.openlocfilehash: 6d95148cb6dc51c739ee4546bd64ce22666d5fd7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104195862"
---
# <a name="rwtexture2darraygetdimensions-function"></a><span data-ttu-id="d9750-105">RWTexture2DArray：： GetDimensions 函數</span><span class="sxs-lookup"><span data-stu-id="d9750-105">RWTexture2DArray::GetDimensions function</span></span>

<span data-ttu-id="d9750-106">傳回資源的維度。</span><span class="sxs-lookup"><span data-stu-id="d9750-106">Returns the dimensions of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9750-107">語法</span><span class="sxs-lookup"><span data-stu-id="d9750-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out UINT Width,
  out UINT Height,
  out UINT Elements
);
```

## <a name="parameters"></a><span data-ttu-id="d9750-108">參數</span><span class="sxs-lookup"><span data-stu-id="d9750-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9750-109">*寬度* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d9750-109">*Width* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d9750-110">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d9750-110">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="d9750-111">資源寬度，以材質。</span><span class="sxs-lookup"><span data-stu-id="d9750-111">The resource width, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="d9750-112">*高度* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d9750-112">*Height* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d9750-113">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d9750-113">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="d9750-114">資源高度，以材質。</span><span class="sxs-lookup"><span data-stu-id="d9750-114">The resource height, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="d9750-115">*元素* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d9750-115">*Elements* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d9750-116">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d9750-116">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="d9750-117">陣列中的項目數。</span><span class="sxs-lookup"><span data-stu-id="d9750-117">The number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9750-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="d9750-118">Return value</span></span>

<span data-ttu-id="d9750-119">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="d9750-119">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9750-120">備註</span><span class="sxs-lookup"><span data-stu-id="d9750-120">Remarks</span></span>

<span data-ttu-id="d9750-121">這是此方法的多載版本清單。</span><span class="sxs-lookup"><span data-stu-id="d9750-121">This is a list of the overloaded versions of this method.</span></span>


```
void GetDimensions (out UINT Width,
  out UINT Height,
  out UINT Elements);

void GetDimensions(out float Width,
  out float Height,
  out float Elements);
```



<span data-ttu-id="d9750-122">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="d9750-122">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="d9750-123">頂點</span><span class="sxs-lookup"><span data-stu-id="d9750-123">Vertex</span></span> | <span data-ttu-id="d9750-124">船體</span><span class="sxs-lookup"><span data-stu-id="d9750-124">Hull</span></span> | <span data-ttu-id="d9750-125">網域</span><span class="sxs-lookup"><span data-stu-id="d9750-125">Domain</span></span> | <span data-ttu-id="d9750-126">幾何</span><span class="sxs-lookup"><span data-stu-id="d9750-126">Geometry</span></span> | <span data-ttu-id="d9750-127">像素</span><span class="sxs-lookup"><span data-stu-id="d9750-127">Pixel</span></span> | <span data-ttu-id="d9750-128">計算</span><span class="sxs-lookup"><span data-stu-id="d9750-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="d9750-129">x</span><span class="sxs-lookup"><span data-stu-id="d9750-129">x</span></span>     | <span data-ttu-id="d9750-130">x</span><span class="sxs-lookup"><span data-stu-id="d9750-130">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="d9750-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d9750-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9750-132">RWTexture2DArray</span><span class="sxs-lookup"><span data-stu-id="d9750-132">RWTexture2DArray</span></span>](sm5-object-rwtexture2darray.md)
</dt> <dt>

[<span data-ttu-id="d9750-133">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="d9750-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
