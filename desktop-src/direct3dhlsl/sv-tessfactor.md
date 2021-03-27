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
ms.openlocfilehash: 8fa49b19109985b590747098826199b33a32dd2d
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104971480"
---
# <a name="sv_tessfactor"></a><span data-ttu-id="4a151-104">SV \_ TessFactor</span><span class="sxs-lookup"><span data-stu-id="4a151-104">SV\_TessFactor</span></span>

<span data-ttu-id="4a151-105">在修補程式的每個邊緣上定義鑲嵌量。</span><span class="sxs-lookup"><span data-stu-id="4a151-105">Defines the tessellation amount on each edge of a patch.</span></span>

## <a name="type"></a><span data-ttu-id="4a151-106">類型</span><span class="sxs-lookup"><span data-stu-id="4a151-106">Type</span></span>



|            |                |
|------------|----------------|
| <span data-ttu-id="4a151-107">類型</span><span class="sxs-lookup"><span data-stu-id="4a151-107">Type</span></span>       | <span data-ttu-id="4a151-108">輸入拓撲</span><span class="sxs-lookup"><span data-stu-id="4a151-108">Input Topology</span></span> |
| <span data-ttu-id="4a151-109">float \[ 4\]</span><span class="sxs-lookup"><span data-stu-id="4a151-109">float\[4\]</span></span> | <span data-ttu-id="4a151-110">四個修補程式</span><span class="sxs-lookup"><span data-stu-id="4a151-110">quad patch</span></span>     |
| <span data-ttu-id="4a151-111">float \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="4a151-111">float\[3\]</span></span> | <span data-ttu-id="4a151-112">三個修補程式</span><span class="sxs-lookup"><span data-stu-id="4a151-112">tri patch</span></span>      |
| <span data-ttu-id="4a151-113">float \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="4a151-113">float\[2\]</span></span> | <span data-ttu-id="4a151-114">等值 線</span><span class="sxs-lookup"><span data-stu-id="4a151-114">isoline</span></span>        |



 

<span data-ttu-id="4a151-115">鑲嵌因數必須宣告為數組;它們無法封裝成單一向量。</span><span class="sxs-lookup"><span data-stu-id="4a151-115">Tessellation factors must be declared as an array; they cannot be packed into a single vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a151-116">備註</span><span class="sxs-lookup"><span data-stu-id="4a151-116">Remarks</span></span>

<span data-ttu-id="4a151-117">您必須在輪廓著色器的 patch 常數函式期間定義鑲嵌式因素的值。</span><span class="sxs-lookup"><span data-stu-id="4a151-117">The value for tessellation factor must be defined during the patch constant function of the hull shader.</span></span>

<span data-ttu-id="4a151-118">如果使用四或三個修補程式，則為輪廓著色器所需的輸出值。</span><span class="sxs-lookup"><span data-stu-id="4a151-118">Required output value for the hull shader if using quad or tri patches.</span></span> <span data-ttu-id="4a151-119">此值也是網域著色器的必要輸入值，可符合鑲嵌式階段之間的修補程式常數資料簽章。</span><span class="sxs-lookup"><span data-stu-id="4a151-119">This value is also a required input value for the domain shader to match the patch-constant data signatures between the tessellation stages.</span></span>

<span data-ttu-id="4a151-120">針對等值線，SV TessFactor 中的第一個值 \_ 是行密度鑲嵌因數，第二個值是行詳細資料鑲嵌因數。</span><span class="sxs-lookup"><span data-stu-id="4a151-120">For an isoline, the first value in SV\_TessFactor is the line-density tessellation factor, the second value is the line-detail tessellation factor.</span></span>

### <a name="tri-patch-tessellation-factors"></a><span data-ttu-id="4a151-121">三個修補程式鑲嵌因素</span><span class="sxs-lookup"><span data-stu-id="4a151-121">Tri Patch Tessellation Factors</span></span>

<span data-ttu-id="4a151-122">第一個元件針對 patch 的 u = = 0 邊緣提供 tesselation 因素。</span><span class="sxs-lookup"><span data-stu-id="4a151-122">The first component provides the tesselation factor for the u==0 edge of the patch.</span></span> <span data-ttu-id="4a151-123">第二個元件提供 patch 的 v = = 0 邊緣的 tesselation 因素。</span><span class="sxs-lookup"><span data-stu-id="4a151-123">The second component provides the tesselation factor for the v==0 edge of the patch.</span></span> <span data-ttu-id="4a151-124">第三個元件針對 patch 的 w = = 0 邊緣提供 tesselation 因素。</span><span class="sxs-lookup"><span data-stu-id="4a151-124">The third component provides the tesselation factor for the w==0 edge of the patch.</span></span>

### <a name="quad-patch-tessellation-factors"></a><span data-ttu-id="4a151-125">四個修補程式鑲嵌因素</span><span class="sxs-lookup"><span data-stu-id="4a151-125">Quad Patch Tessellation Factors</span></span>

<span data-ttu-id="4a151-126">第一個元件針對 patch 的 u = = 0 邊緣提供 tesselation 因素。</span><span class="sxs-lookup"><span data-stu-id="4a151-126">The first component provides the tesselation factor for the u==0 edge of the patch.</span></span> <span data-ttu-id="4a151-127">第二個元件提供 patch 的 v = = 0 邊緣的 tesselation 因素。</span><span class="sxs-lookup"><span data-stu-id="4a151-127">The second component provides the tesselation factor for the v==0 edge of the patch.</span></span> <span data-ttu-id="4a151-128">第三個元件針對 patch 的 u = = 1 邊緣提供 tesselation 因素。</span><span class="sxs-lookup"><span data-stu-id="4a151-128">The third component provides the tesselation factor for the u==1 edge of the patch.</span></span> <span data-ttu-id="4a151-129">第四個元件提供 patch 的 v = = 1 邊緣的 tesselation 因數。</span><span class="sxs-lookup"><span data-stu-id="4a151-129">The fourth component provides the tesselation factor for the v==1 edge of the patch.</span></span> <span data-ttu-id="4a151-130">邊緣的順序會以順時針的方式從 u = = 0 邊緣（即修補程式左邊）開始，並從 v = = 0 邊緣（即修補程式頂端）開始。</span><span class="sxs-lookup"><span data-stu-id="4a151-130">The ordering of the edges is clockwise, starting from the u==0 edge, which is the left side of the patch, and from the v==0 edge, which is the top of the patch.</span></span>

<span data-ttu-id="4a151-131">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="4a151-131">This function is supported in the following types of shaders:</span></span>



|        |      |        |          |       |         |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="4a151-132">頂點</span><span class="sxs-lookup"><span data-stu-id="4a151-132">Vertex</span></span> | <span data-ttu-id="4a151-133">船體</span><span class="sxs-lookup"><span data-stu-id="4a151-133">Hull</span></span> | <span data-ttu-id="4a151-134">網域</span><span class="sxs-lookup"><span data-stu-id="4a151-134">Domain</span></span> | <span data-ttu-id="4a151-135">幾何</span><span class="sxs-lookup"><span data-stu-id="4a151-135">Geometry</span></span> | <span data-ttu-id="4a151-136">像素</span><span class="sxs-lookup"><span data-stu-id="4a151-136">Pixel</span></span> | <span data-ttu-id="4a151-137">計算</span><span class="sxs-lookup"><span data-stu-id="4a151-137">Compute</span></span> |
|        | <span data-ttu-id="4a151-138">x</span><span class="sxs-lookup"><span data-stu-id="4a151-138">x</span></span>    | <span data-ttu-id="4a151-139">x</span><span class="sxs-lookup"><span data-stu-id="4a151-139">x</span></span>      |          |       |         |



 

## <a name="see-also"></a><span data-ttu-id="4a151-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4a151-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a151-141">語意</span><span class="sxs-lookup"><span data-stu-id="4a151-141">Semantics</span></span>](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[<span data-ttu-id="4a151-142">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="4a151-142">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




