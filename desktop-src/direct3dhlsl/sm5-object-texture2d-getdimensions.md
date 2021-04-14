---
title: Texture2D：： GetDimensions 函數
description: 傳回資源的維度。 |Texture2D：： GetDimensions 函數
ms.assetid: 921e425d-c0dd-4b8d-b590-0599fabfe606
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
ms.openlocfilehash: ba1fa832b51e86b5df3193895caa293bb006d82a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104992038"
---
# <a name="texture2dgetdimensions-function"></a><span data-ttu-id="eb973-105">Texture2D：： GetDimensions 函數</span><span class="sxs-lookup"><span data-stu-id="eb973-105">Texture2D::GetDimensions function</span></span>

<span data-ttu-id="eb973-106">傳回資源的維度。</span><span class="sxs-lookup"><span data-stu-id="eb973-106">Returns the dimensions of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb973-107">語法</span><span class="sxs-lookup"><span data-stu-id="eb973-107">Syntax</span></span>

``` syntax
void GetDimensions(
  in  
            uint MipLevel,
  out 
            uint Width,
  out uint Height,
  out 
            uint NumberOfLevels
);
```

## <a name="parameters"></a><span data-ttu-id="eb973-108">參數</span><span class="sxs-lookup"><span data-stu-id="eb973-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb973-109">*MipLevel* \[在\]</span><span class="sxs-lookup"><span data-stu-id="eb973-109">*MipLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb973-110">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="eb973-110">Type: **uint**</span></span>

<span data-ttu-id="eb973-111">選擇性。</span><span class="sxs-lookup"><span data-stu-id="eb973-111">Optional.</span></span> <span data-ttu-id="eb973-112">如果) 使用 *NumberOfLevels* ，則必須指定 mipmap 層級 (。</span><span class="sxs-lookup"><span data-stu-id="eb973-112">The mipmap level (must be specified if *NumberOfLevels* is used).</span></span>

</dd> <dt>

<span data-ttu-id="eb973-113">*寬度* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="eb973-113">*Width* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="eb973-114">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="eb973-114">Type: **uint**</span></span>

<span data-ttu-id="eb973-115">資源寬度，以材質。</span><span class="sxs-lookup"><span data-stu-id="eb973-115">The resource width, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="eb973-116">*高度* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="eb973-116">*Height* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="eb973-117">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="eb973-117">Type: **uint**</span></span>

<span data-ttu-id="eb973-118">資源高度，以材質。</span><span class="sxs-lookup"><span data-stu-id="eb973-118">The resource height, in texels.</span></span>

</dd> <dt>

<span data-ttu-id="eb973-119">*NumberOfLevels* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="eb973-119">*NumberOfLevels* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="eb973-120">類型： **uint**</span><span class="sxs-lookup"><span data-stu-id="eb973-120">Type: **uint**</span></span>

<span data-ttu-id="eb973-121"> (的 mipmap 層級數目需要 *MipLevel* 也) 。</span><span class="sxs-lookup"><span data-stu-id="eb973-121">The number of mipmap levels (requires *MipLevel* also).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb973-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="eb973-122">Return value</span></span>

<span data-ttu-id="eb973-123">Nothing</span><span class="sxs-lookup"><span data-stu-id="eb973-123">Nothing</span></span>

## <a name="remarks"></a><span data-ttu-id="eb973-124">備註</span><span class="sxs-lookup"><span data-stu-id="eb973-124">Remarks</span></span>

<span data-ttu-id="eb973-125">這是此方法的多載版本清單。</span><span class="sxs-lookup"><span data-stu-id="eb973-125">This is a list of the overloaded versions of this method.</span></span>


```
void GetDimensions(uint MipLevel, 
  out uint Width,
  out uint Height,
  out uint NumberOfLevels);

void GetDimensions (out uint Width,
  out uint Height);

void GetDimensions(uint MipLevel,
  out float Width,
  out float Height,
  out float NumberOfLevels);

void GetDimensions(out float Width,
  out float Height);
```



<span data-ttu-id="eb973-126">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="eb973-126">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="eb973-127">頂點</span><span class="sxs-lookup"><span data-stu-id="eb973-127">Vertex</span></span> | <span data-ttu-id="eb973-128">船體</span><span class="sxs-lookup"><span data-stu-id="eb973-128">Hull</span></span> | <span data-ttu-id="eb973-129">網域</span><span class="sxs-lookup"><span data-stu-id="eb973-129">Domain</span></span> | <span data-ttu-id="eb973-130">幾何</span><span class="sxs-lookup"><span data-stu-id="eb973-130">Geometry</span></span> | <span data-ttu-id="eb973-131">像素</span><span class="sxs-lookup"><span data-stu-id="eb973-131">Pixel</span></span> | <span data-ttu-id="eb973-132">計算</span><span class="sxs-lookup"><span data-stu-id="eb973-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="eb973-133">x</span><span class="sxs-lookup"><span data-stu-id="eb973-133">x</span></span>     | <span data-ttu-id="eb973-134">x</span><span class="sxs-lookup"><span data-stu-id="eb973-134">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="eb973-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="eb973-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb973-136">Texture2D</span><span class="sxs-lookup"><span data-stu-id="eb973-136">Texture2D</span></span>](sm5-object-texture2d.md)
</dt> <dt>

[<span data-ttu-id="eb973-137">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="eb973-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




