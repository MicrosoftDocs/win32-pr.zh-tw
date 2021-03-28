---
title: Texture2DMS：： GetDimensions 函數
description: 傳回資源的維度。 |Texture2DMS：： GetDimensions 函數
ms.assetid: badf4127-2498-4c2e-acc7-20507488fc6b
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
ms.openlocfilehash: f720a10ac73f48ce1f27c5676d706a75178aa8ee
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "103945879"
---
# <a name="texture2dmsgetdimensions-function"></a><span data-ttu-id="10ed5-105">Texture2DMS：： GetDimensions 函數</span><span class="sxs-lookup"><span data-stu-id="10ed5-105">Texture2DMS::GetDimensions function</span></span>

<span data-ttu-id="10ed5-106">傳回資源的維度。</span><span class="sxs-lookup"><span data-stu-id="10ed5-106">Returns the dimensions of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="10ed5-107">語法</span><span class="sxs-lookup"><span data-stu-id="10ed5-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out UINT Width,
  out UINT Height,
  out UINT NumberOfSamples
);
```

## <a name="parameters"></a><span data-ttu-id="10ed5-108">參數</span><span class="sxs-lookup"><span data-stu-id="10ed5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10ed5-109">*寬度* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="10ed5-109">*Width* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="10ed5-110">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="10ed5-110">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="10ed5-111">資源寬度，以材質。</span><span class="sxs-lookup"><span data-stu-id="10ed5-111">The resource width, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="10ed5-112">*高度* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="10ed5-112">*Height* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="10ed5-113">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="10ed5-113">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="10ed5-114">資源高度，以材質。</span><span class="sxs-lookup"><span data-stu-id="10ed5-114">The resource height, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="10ed5-115">*NumberOfSamples* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="10ed5-115">*NumberOfSamples* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="10ed5-116">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="10ed5-116">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="10ed5-117">範例位置的數目。</span><span class="sxs-lookup"><span data-stu-id="10ed5-117">The number of sample locations.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10ed5-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="10ed5-118">Return value</span></span>

<span data-ttu-id="10ed5-119">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="10ed5-119">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="10ed5-120">備註</span><span class="sxs-lookup"><span data-stu-id="10ed5-120">Remarks</span></span>

<span data-ttu-id="10ed5-121">這是此方法的多載版本清單。</span><span class="sxs-lookup"><span data-stu-id="10ed5-121">This is a list of the overloaded versions of this method.</span></span>


```
void GetDimensions(out float Width,
  out float Height,
  out float NumberOfSamples);
```



<span data-ttu-id="10ed5-122">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="10ed5-122">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="10ed5-123">頂點</span><span class="sxs-lookup"><span data-stu-id="10ed5-123">Vertex</span></span> | <span data-ttu-id="10ed5-124">船體</span><span class="sxs-lookup"><span data-stu-id="10ed5-124">Hull</span></span> | <span data-ttu-id="10ed5-125">網域</span><span class="sxs-lookup"><span data-stu-id="10ed5-125">Domain</span></span> | <span data-ttu-id="10ed5-126">幾何</span><span class="sxs-lookup"><span data-stu-id="10ed5-126">Geometry</span></span> | <span data-ttu-id="10ed5-127">像素</span><span class="sxs-lookup"><span data-stu-id="10ed5-127">Pixel</span></span> | <span data-ttu-id="10ed5-128">計算</span><span class="sxs-lookup"><span data-stu-id="10ed5-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="10ed5-129">x</span><span class="sxs-lookup"><span data-stu-id="10ed5-129">x</span></span>     | <span data-ttu-id="10ed5-130">x</span><span class="sxs-lookup"><span data-stu-id="10ed5-130">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="10ed5-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="10ed5-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10ed5-132">Texture2DMS</span><span class="sxs-lookup"><span data-stu-id="10ed5-132">Texture2DMS</span></span>](sm5-object-texture2dms.md)
</dt> <dt>

[<span data-ttu-id="10ed5-133">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="10ed5-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
