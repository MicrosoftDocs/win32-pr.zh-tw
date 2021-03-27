---
title: ProcessIsolineTessFactors 函式
description: 產生等值線的圓角鑲嵌因數。
ms.assetid: 0816b3e0-cb03-4a7a-9732-e84c637b3d48
keywords:
- ProcessIsolineTessFactors 函式 HLSL
topic_type:
- apiref
api_name:
- ProcessIsolineTessFactors
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 10da0e5bf0f2138c57da3fcfe962bc6a88800068
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103678747"
---
# <a name="processisolinetessfactors-function"></a><span data-ttu-id="63740-104">ProcessIsolineTessFactors 函式</span><span class="sxs-lookup"><span data-stu-id="63740-104">ProcessIsolineTessFactors function</span></span>

<span data-ttu-id="63740-105">產生等值線的圓角鑲嵌因數。</span><span class="sxs-lookup"><span data-stu-id="63740-105">Generates the rounded tessellation factors for an isoline.</span></span>

## <a name="syntax"></a><span data-ttu-id="63740-106">語法</span><span class="sxs-lookup"><span data-stu-id="63740-106">Syntax</span></span>

``` syntax
void ProcessIsolineTessFactors(
  in  float RawDetailFactor,
  in  float RawDensityFactor,
  out float RoundedDetailFactor,
  out float RoundedDensityFactor
);
```

## <a name="parameters"></a><span data-ttu-id="63740-107">參數</span><span class="sxs-lookup"><span data-stu-id="63740-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63740-108">*RawDetailFactor* \[在\]</span><span class="sxs-lookup"><span data-stu-id="63740-108">*RawDetailFactor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63740-109">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="63740-109">Type: **float**</span></span>

<span data-ttu-id="63740-110">所需的詳細因素。</span><span class="sxs-lookup"><span data-stu-id="63740-110">The desired detail factor.</span></span>

</dd> <dt>

<span data-ttu-id="63740-111">*RawDensityFactor* \[在\]</span><span class="sxs-lookup"><span data-stu-id="63740-111">*RawDensityFactor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63740-112">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="63740-112">Type: **float**</span></span>

<span data-ttu-id="63740-113">所需的密度因數。</span><span class="sxs-lookup"><span data-stu-id="63740-113">The desired density factor.</span></span>

</dd> <dt>

<span data-ttu-id="63740-114">*RoundedDetailFactor* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="63740-114">*RoundedDetailFactor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="63740-115">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="63740-115">Type: **float**</span></span>

<span data-ttu-id="63740-116">圓角詳細因數壓制至可供鑲嵌使用的範圍。</span><span class="sxs-lookup"><span data-stu-id="63740-116">The rounded detail factor clamped to a range that can be used by the tessellator.</span></span>

</dd> <dt>

<span data-ttu-id="63740-117">*RoundedDensityFactor* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="63740-117">*RoundedDensityFactor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="63740-118">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="63740-118">Type: **float**</span></span>

<span data-ttu-id="63740-119">鑲嵌會使用壓制至 rangethat 的舍入密度因數。</span><span class="sxs-lookup"><span data-stu-id="63740-119">The rounded density factor clamped to a rangethat can be used by the tessellator.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63740-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="63740-120">Return value</span></span>

<span data-ttu-id="63740-121">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="63740-121">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="63740-122">備註</span><span class="sxs-lookup"><span data-stu-id="63740-122">Remarks</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="63740-123">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="63740-123">Minimum Shader Model</span></span>

<span data-ttu-id="63740-124">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="63740-124">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="63740-125">著色器模型</span><span class="sxs-lookup"><span data-stu-id="63740-125">Shader Model</span></span>                                                                | <span data-ttu-id="63740-126">支援</span><span class="sxs-lookup"><span data-stu-id="63740-126">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="63740-127">[著色器模型 5](d3d11-graphics-reference-sm5.md) 和更新版本的著色器模型</span><span class="sxs-lookup"><span data-stu-id="63740-127">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="63740-128">是</span><span class="sxs-lookup"><span data-stu-id="63740-128">yes</span></span>       |



 

<span data-ttu-id="63740-129">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="63740-129">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="63740-130">頂點</span><span class="sxs-lookup"><span data-stu-id="63740-130">Vertex</span></span> | <span data-ttu-id="63740-131">船體</span><span class="sxs-lookup"><span data-stu-id="63740-131">Hull</span></span> | <span data-ttu-id="63740-132">網域</span><span class="sxs-lookup"><span data-stu-id="63740-132">Domain</span></span> | <span data-ttu-id="63740-133">幾何</span><span class="sxs-lookup"><span data-stu-id="63740-133">Geometry</span></span> | <span data-ttu-id="63740-134">像素</span><span class="sxs-lookup"><span data-stu-id="63740-134">Pixel</span></span> | <span data-ttu-id="63740-135">計算</span><span class="sxs-lookup"><span data-stu-id="63740-135">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="63740-136">x</span><span class="sxs-lookup"><span data-stu-id="63740-136">x</span></span>    |        |          |       |         |



 

## <a name="see-also"></a><span data-ttu-id="63740-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="63740-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63740-138">內建函式</span><span class="sxs-lookup"><span data-stu-id="63740-138">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="63740-139">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="63740-139">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




