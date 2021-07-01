---
title: SV_TessFactor
description: 在修補程式的每個邊緣上定義鑲嵌量。
ms.assetid: 970ff744-da5b-4933-866c-dd38b85fb48d
keywords:
- SV_TessFactor HLSL
topic_type:
- apiref
api_name:
- SV_TessFactor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 308034fe607283ef9f1213cca1cabb4a7229765e
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118893"
---
# <a name="sv_tessfactor"></a><span data-ttu-id="84b14-104">SV \_ TessFactor</span><span class="sxs-lookup"><span data-stu-id="84b14-104">SV\_TessFactor</span></span>

<span data-ttu-id="84b14-105">在修補程式的每個邊緣上定義鑲嵌量。</span><span class="sxs-lookup"><span data-stu-id="84b14-105">Defines the tessellation amount on each edge of a patch.</span></span>

## <a name="type"></a><span data-ttu-id="84b14-106">類型</span><span class="sxs-lookup"><span data-stu-id="84b14-106">Type</span></span>



|  <span data-ttu-id="84b14-107">類型</span><span class="sxs-lookup"><span data-stu-id="84b14-107">Type</span></span>          |  <span data-ttu-id="84b14-108">輸入拓撲</span><span class="sxs-lookup"><span data-stu-id="84b14-108">Input topology</span></span>              |
|------------|----------------|
| <span data-ttu-id="84b14-109">float \[ 4\]</span><span class="sxs-lookup"><span data-stu-id="84b14-109">float\[4\]</span></span> | <span data-ttu-id="84b14-110">四個修補程式</span><span class="sxs-lookup"><span data-stu-id="84b14-110">quad patch</span></span>     |
| <span data-ttu-id="84b14-111">float \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="84b14-111">float\[3\]</span></span> | <span data-ttu-id="84b14-112">三個修補程式</span><span class="sxs-lookup"><span data-stu-id="84b14-112">tri patch</span></span>      |
| <span data-ttu-id="84b14-113">float \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="84b14-113">float\[2\]</span></span> | <span data-ttu-id="84b14-114">等值 線</span><span class="sxs-lookup"><span data-stu-id="84b14-114">isoline</span></span>        |



 

<span data-ttu-id="84b14-115">鑲嵌因數必須宣告為數組;它們無法封裝成單一向量。</span><span class="sxs-lookup"><span data-stu-id="84b14-115">Tessellation factors must be declared as an array; they cannot be packed into a single vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="84b14-116">備註</span><span class="sxs-lookup"><span data-stu-id="84b14-116">Remarks</span></span>

<span data-ttu-id="84b14-117">您必須在輪廓著色器的 patch 常數函式期間定義鑲嵌式因素的值。</span><span class="sxs-lookup"><span data-stu-id="84b14-117">The value for tessellation factor must be defined during the patch constant function of the hull shader.</span></span>

<span data-ttu-id="84b14-118">如果使用四或三個修補程式，則為輪廓著色器所需的輸出值。</span><span class="sxs-lookup"><span data-stu-id="84b14-118">Required output value for the hull shader if using quad or tri patches.</span></span> <span data-ttu-id="84b14-119">此值也是網域著色器的必要輸入值，可符合鑲嵌式階段之間的修補程式常數資料簽章。</span><span class="sxs-lookup"><span data-stu-id="84b14-119">This value is also a required input value for the domain shader to match the patch-constant data signatures between the tessellation stages.</span></span>

<span data-ttu-id="84b14-120">針對等值線，SV TessFactor 中的第一個值 \_ 是行密度鑲嵌因數，第二個值是行詳細資料鑲嵌因數。</span><span class="sxs-lookup"><span data-stu-id="84b14-120">For an isoline, the first value in SV\_TessFactor is the line-density tessellation factor, the second value is the line-detail tessellation factor.</span></span>

### <a name="tri-patch-tessellation-factors"></a><span data-ttu-id="84b14-121">三個修補程式鑲嵌因素</span><span class="sxs-lookup"><span data-stu-id="84b14-121">Tri Patch Tessellation Factors</span></span>

<span data-ttu-id="84b14-122">第一個元件針對 patch 的 u = = 0 邊緣提供 tesselation 因素。</span><span class="sxs-lookup"><span data-stu-id="84b14-122">The first component provides the tesselation factor for the u==0 edge of the patch.</span></span> <span data-ttu-id="84b14-123">第二個元件提供 patch 的 v = = 0 邊緣的 tesselation 因素。</span><span class="sxs-lookup"><span data-stu-id="84b14-123">The second component provides the tesselation factor for the v==0 edge of the patch.</span></span> <span data-ttu-id="84b14-124">第三個元件針對 patch 的 w = = 0 邊緣提供 tesselation 因素。</span><span class="sxs-lookup"><span data-stu-id="84b14-124">The third component provides the tesselation factor for the w==0 edge of the patch.</span></span>

### <a name="quad-patch-tessellation-factors"></a><span data-ttu-id="84b14-125">四個修補程式鑲嵌因素</span><span class="sxs-lookup"><span data-stu-id="84b14-125">Quad Patch Tessellation Factors</span></span>

<span data-ttu-id="84b14-126">第一個元件針對 patch 的 u = = 0 邊緣提供 tesselation 因素。</span><span class="sxs-lookup"><span data-stu-id="84b14-126">The first component provides the tesselation factor for the u==0 edge of the patch.</span></span> <span data-ttu-id="84b14-127">第二個元件提供 patch 的 v = = 0 邊緣的 tesselation 因素。</span><span class="sxs-lookup"><span data-stu-id="84b14-127">The second component provides the tesselation factor for the v==0 edge of the patch.</span></span> <span data-ttu-id="84b14-128">第三個元件針對 patch 的 u = = 1 邊緣提供 tesselation 因素。</span><span class="sxs-lookup"><span data-stu-id="84b14-128">The third component provides the tesselation factor for the u==1 edge of the patch.</span></span> <span data-ttu-id="84b14-129">第四個元件提供 patch 的 v = = 1 邊緣的 tesselation 因數。</span><span class="sxs-lookup"><span data-stu-id="84b14-129">The fourth component provides the tesselation factor for the v==1 edge of the patch.</span></span> <span data-ttu-id="84b14-130">邊緣的順序會以順時針的方式從 u = = 0 邊緣（即修補程式左邊）開始，並從 v = = 0 邊緣（即修補程式頂端）開始。</span><span class="sxs-lookup"><span data-stu-id="84b14-130">The ordering of the edges is clockwise, starting from the u==0 edge, which is the left side of the patch, and from the v==0 edge, which is the top of the patch.</span></span>

<span data-ttu-id="84b14-131">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="84b14-131">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="84b14-132">頂點</span><span class="sxs-lookup"><span data-stu-id="84b14-132">Vertex</span></span> | <span data-ttu-id="84b14-133">船體</span><span class="sxs-lookup"><span data-stu-id="84b14-133">Hull</span></span> | <span data-ttu-id="84b14-134">網域</span><span class="sxs-lookup"><span data-stu-id="84b14-134">Domain</span></span> | <span data-ttu-id="84b14-135">幾何</span><span class="sxs-lookup"><span data-stu-id="84b14-135">Geometry</span></span> | <span data-ttu-id="84b14-136">像素</span><span class="sxs-lookup"><span data-stu-id="84b14-136">Pixel</span></span> | <span data-ttu-id="84b14-137">計算</span><span class="sxs-lookup"><span data-stu-id="84b14-137">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="84b14-138">x</span><span class="sxs-lookup"><span data-stu-id="84b14-138">x</span></span>    | <span data-ttu-id="84b14-139">x</span><span class="sxs-lookup"><span data-stu-id="84b14-139">x</span></span>      |          |       |         |



 

## <a name="see-also"></a><span data-ttu-id="84b14-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="84b14-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84b14-141">語意</span><span class="sxs-lookup"><span data-stu-id="84b14-141">Semantics</span></span>](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[<span data-ttu-id="84b14-142">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="84b14-142">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




